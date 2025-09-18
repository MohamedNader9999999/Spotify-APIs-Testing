# Spotify API Testing Project

## Overview

This project focuses on **testing the Spotify Web API**, specifically the endpoints responsible for fetching and managing **Albums**. The goal is to validate API behavior and ensure that a new application can seamlessly integrate with Spotify’s services.

## Objective

* Verify that Spotify Album APIs return correct data for valid requests
* Identify and document defects or inconsistencies in API responses
* Ensure smooth integration by testing **token regeneration** and **dependent API workflows**

## Scope of Testing

**Primary Endpoint Tested:**
[Spotify Web API – User Read Private & Album Scopes](https://developer.spotify.com/documentation/web-api/concepts/scopes#user-read-private)

### Covered Scenarios

* Get Album by Valid ID
* Get Multiple Albums (Batch Request)
* Handle Invalid/Incorrect Album IDs
* Verify Response Structure, Data Types, and Status Codes
* Validate Authorization Scenarios (Valid Token, Expired Token, Missing Token)
* Test API dependencies (where one API call’s response is used in subsequent requests)

## Tools & Environment

* **Postman** – For API execution and test automation
* **Spotify Developer Console** – For token generation and authentication setup
* **Environment Variables** – Used to store dynamically regenerated tokens and album IDs for dependent tests

## Testing Approach

1. **Test Case Design & Documentation**

   * Designed detailed test cases covering both **positive** and **negative** flows
   * Documented preconditions, steps, expected results, and dependencies between APIs

2. **Authorization Handling**

   * Implemented timely regeneration of tokens to avoid authorization failures
   * Automated usage of updated tokens within Postman environment variables

3. **Execution & Validation**

   * Ran test cases in Postman collections
   * Validated response payloads, headers, and status codes
   * Chained dependent APIs (e.g., using Album IDs from one response in another request)

4. **Bug Reporting**

   * Prepared a detailed bug report for all failed cases
   * Included step-by-step reproduction, expected vs. actual results, screenshots, severity, and priority

## Deliverables

* **Comprehensive Test Case Document**
* **Postman Collection with Environment Variables**
* **Detailed Bug Report** with actionable insights for developers

## Outcome

The testing process validates that **token management** and **dependent workflows** work correctly.Unfortunately, testing shows that the **Not All Spotify Album APIs** are reliable some of them do not work properly.

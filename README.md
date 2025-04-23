# PRODIGY_ST_03
This project automates the login functionality testing of SauceDemo using Selenium. It covers valid, invalid, and empty input cases with detailed assertions and browser automation.

# 🧪 Automated Login Testing Report - SauceDemo

![Test Status](https://img.shields.io/badge/tests-passed-brightgreen)
![Automation](https://img.shields.io/badge/automation-Selenium-blue)
![Language](https://img.shields.io/badge/language-Python-yellow)

> **Internship Task 3 - Prodigy InfoTech**  
> Author: *Praful Gawane*  
> Date: 2025-04-23

---

## 📋 Overview

This document presents the results of automated login testing on [SauceDemo](https://www.saucedemo.com/) using Selenium and Python. The purpose is to verify the correctness and robustness of the login feature under valid, invalid, and empty input conditions.

---

## ✅ Valid Login Test Cases

| TC ID | Description | Username | Password | Expected Result | Actual Result | Status |
|-------|-------------|----------|----------|------------------|----------------|--------|
| TC_V1 | Standard user login | `standard_user` | `secret_sauce` | Inventory page loads | As expected | ✅ Pass |
| TC_V2 | Problem user login (UI bug user) | `problem_user` | `secret_sauce` | Login successful | As expected | ✅ Pass |
| TC_V3 | Performance glitch user | `performance_glitch_user` | `secret_sauce` | Login successful | As expected | ✅ Pass |
| TC_V4 | Visual user login | `visual_user` | `secret_sauce` | Login successful | As expected | ✅ Pass |
| TC_V5 | Error user login | `error_user` | `secret_sauce` | Login successful | As expected | ✅ Pass |
| TC_V6 | Locked out user login | `locked_out_user` | `secret_sauce` | Login should fail | As expected | ✅ Pass |

---

## ❌ Invalid Login Test Cases

| TC ID | Description | Username | Password | Expected Result | Actual Result | Status |
|-------|-------------|----------|----------|------------------|----------------|--------|
| TC_I1 | Invalid password | `standard_user` | `wrongpass` | Login fails | As expected | ✅ Pass |
| TC_I2 | Non-existent user | `admin` | `admin123` | Login fails | As expected | ✅ Pass |
| TC_I3 | Valid user, wrong password | `visual_user` | `wrong` | Login fails | As expected | ✅ Pass |
| TC_I4 | Invalid user, valid password | `wrong_user` | `secret_sauce` | Login fails | As expected | ✅ Pass |
| TC_I5 | Guest credentials | `guest` | `guest123` | Login fails | As expected | ✅ Pass |
| TC_I6 | Root login | `root` | `root` | Login fails | As expected | ✅ Pass |
| TC_I7 | Numeric password | `user` | `123456` | Login fails | As expected | ✅ Pass |
| TC_I8 | Test login | `test` | `test123` | Login fails | As expected | ✅ Pass |
| TC_I9 | Space-only password | `problem_user` | `" "` | Login fails | As expected | ✅ Pass |
| TC_I10 | Space as username | `" "` | `secret_sauce` | Login fails | As expected | ✅ Pass |

---

## ⚠️ Empty & Whitespace Test Cases

| TC ID | Description | Username | Password | Expected Result | Actual Result | Status |
|-------|-------------|----------|----------|------------------|----------------|--------|
| TC_E1 | Empty username | `""` | `secret_sauce` | Login fails | As expected | ✅ Pass |
| TC_E2 | Empty password | `standard_user` | `""` | Login fails | As expected | ✅ Pass |
| TC_E3 | Both fields empty | `""` | `""` | Login fails | As expected | ✅ Pass |
| TC_E4 | Both fields whitespace | `"   "` | `"   "` | Login fails | As expected | ✅ Pass |

---

## 📌 Summary

- 🔍 Total Test Cases: **20**
- ✅ Passed: **20**
- ❌ Failed: **0**
- ✔️ Coverage: Valid, Invalid, Edge Cases
- 🔧 Framework: Selenium WebDriver + Python

# jenkins-qa-portfolioLK
My Jenkins Environment test automation portfolio using API fixtures and UI validations and based on Jenkins UI and API testing
# Jenkins Environment UI Automation with API Optimization

**Author**: Liliana Koretska  
**Role**: Test Automaation Engineer  
**Project**: Jenkins QA Automation (RedRoverSchool GitHub)

---

## Overview

This project showcases my contribution to a team-based automation initiative, where we enhanced Jenkins UI tests by replacing slow UI preconditions with efficient API setups. The automation specifically targets the *Environment* section of multi-configuration (matrix) projects in Jenkins.

---

## Problem Solved

Originally, tests relied on manual or UI-based Jenkins configuration. This caused:

- Long test execution times
- CI instability
- Unrepeatable test states

**My solution:**

- Created **API fixtures** to set up projects automatically.
- Made tests faster, atomic, and reliable.

---

## My Responsibilities

- Wrote both **API** and **UI** automated tests using `pytest`, `selenium`, and `httpx`
- Created reusable API fixtures for Jenkins project setup using XML configs
- Validated checkboxes in the Environment section:
  - Delete workspace before build
  - Use secret text(s) or file(s)
  - Add timestamps to Console Output
  - Inspect build log for scans
  - Terminate a build if it’s stuck
- Maintained Allure reports and GitHub PRs

---

## Links & Resources

- 🔗 [User Story: US_22.001](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/issues/719)  
- 🔗 [Test Case + AC: TC_22.001.01](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/issues/898)  
- 🔗 [Pull Request](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/pull/916)  
- 📊 [Allure Report](https://redroverschool.github.io/JenkinsQA_Python_2025_spring/1362/index.html#)  
- 🏆 [Top 6 Contributors](https://github.com/orgs/RedRoverSchool/projects/8/views/1)  
- 🎥 [Demo Video (YouTube)](https://youtube.com) *(link placeholder)*

---

## Sample Test Snippet

```python
@allure.title("UI: Verify 'Add timestamps to Console Output' checkbox is selected")
def test_timestamps_checkbox_selected(create_multiconfig_project_with_env_options_api, main_page):
    page = main_page.go_to_multiconfig_project_page(project_name).go_to_configure_page()
    assert page.is_elements_selected(page.Locators.TIMESTAMPS_CHECKBOX)

Result
Tests now run faster and pass reliably on CI

Each test is atomic, traceable, and uses reusable fixtures

My contributions improved the overall automation framework stability and speed

About Me
I'm a Software QA Engineer who bridges technical precision with collaborative spirit. I speak the same language as developers and stakeholders, and I focus on building test systems that are fast, scalable, and maintainable.


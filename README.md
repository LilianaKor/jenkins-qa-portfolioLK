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
  This was a team-based initiative focused on improving test automation for Jenkins' multiconfiguration, or matrix, projects — specifically the Environment section.
  The main challenge we faced was that our UI-based preconditions were too slow and fragile for continuous integration pipelines.
  I solved that by replacing them with fast, stable API-based fixtures.
Originally, Jenkins projects had to be created manually or through UI steps during test runs. That process was slow, flaky, and not scalable. To fix it, I implemented API fixtures that programmatically create the required Jenkins projects with XML configuration before the UI tests begin. This improved execution speed and reliability across the board.

My role in this project included writing atomic UI tests using pytest, Selenium, and Allure reporting. I also created API fixtures with httpx to prepare consistent, repeatable test environments. The tests I wrote verified the state of several checkboxes in the Environment configuration section, such as Delete workspace, Use secret text(s) or file(s), Add timestamps to the console output, Terminate a build if it’s stuck, and Inspect build logs.

Each test was mapped to a user story, acceptance criteria, and a GitHub issue, and I submitted clean, well-documented pull requests. The results were significant. 
I reduced test runtime, stabilized our continuous integration, and wrote modular, scalable test cases. 
As a result, I was recognized as one of the top six contributors in a team of over 140 engineers.

I’m excited to bring this same level of clarity, structure, and impact to your QA team.

---

## Links & Resources

- 🔗 [User Story: US_22.001](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/issues/719)  
- 🔗 [Test Case + AC: TC_22.001.01](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/issues/898)  
- 🔗 [Pull Request](https://github.com/RedRoverSchool/JenkinsQA_Python_2025_spring/pull/916)  
- 📊 [Allure Report](https://redroverschool.github.io/JenkinsQA_Python_2025_spring/1362/index.html#)  
- 🏆 [Top 6 Contributors](https://www.youtube.com/watch?v=LCbZNG4T5P0)  

## Demo Videos

### Jenkins Environment UI Automation with API Optimization 
by Test Authomation Engineer, active contributor Liliana Koretska
  
[![Watch the main demo](https://img.youtube.com/vi/LCbZNG4T5P0/0.jpg)](https://www.youtube.com/watch?v=LCbZNG4T5P0)

---

### Short Demo — Parametrize Checkboxes
[![Watch Short Demo](https://img.shields.io/badge/Watch-Short%20Demo-blue?style=for-the-badge)](https://www.youtube.com/watch?v=oBtOIODY-bM)
[YouTube link](https://www.youtube.com/watch?v=LCbZNG4T5P0)

---
## Result
Tests now run faster and pass reliably on CI

Each test is atomic, traceable, and uses reusable fixtures

My contributions improved the overall automation framework stability and speed

---
## About Me
I'm a QA Engineer who bridges technical precision with collaborative spirit. I speak the same language as developers and stakeholders, 
and I focus on building test systems that are fast, scalable, and maintainable.

## My Engagement 
- I am as one of the top six contributors in a team of over 140 engineers
- Top Contributor Screenshot: 
<img width="1648" height="1548" alt="image" src="https://github.com/user-attachments/assets/ed4775be-ae85-4bc6-aba6-997021d072c7" />


## Sample Test Snippet

```python
@allure.title("UI: Verify 'Add timestamps to Console Output' checkbox is selected")
def test_timestamps_checkbox_selected(create_multiconfig_project_with_env_options_api, main_page):
    page = main_page.go_to_multiconfig_project_page(project_name).go_to_configure_page()
    assert page.is_elements_selected(page.Locators.TIMESTAMPS_CHECKBOX)


<img width="808" height="638" alt="My Engagement" src="https://github.com/user-attachments/assets/72d6c68d-4d6a-4581-826a-0694a743ce33" />
---

## Parametrization of checkboxes Demo
 

# GitHub Actions and ansible-lint
## rzfeeser/github_actions_ansible-lint

### Purpose
The purpose of this repository is to provide an working example and template for using GitHub Actions in conjunction with `ansible-lint` and `ansible-playbook` for the purpose of automating the linting and running of Ansible code.

### Materials and Methods
- GitHub Actions
- Exploration of `ansible-lint`
- Linting on Pull Requests (PR)
  - Only lints what is in playbooks/ by following `.ansible-lint`
- Execution on WorkFlow Dispatch to run `ansible-playbook`

## Resources
- [GitHub - ansible-lint](https://github.com/ansible/ansible-lint)
- [GitHub Actions - ansible-lint](https://github.com/marketplace/actions/run-ansible-lint)
- [Documentation - ansible-lint](https://ansible.readthedocs.io/projects/lint/)

### Summary
**Ansible Lint** is a command-line tool for linting playbooks, roles and collections. Linting is to check code for syntax errors and bad practices. 

Ansible Lint works by parsing your Ansible code and running a series of checks against it. These checks are based on a set of rules that are defined in the Ansible Lint community. The rules are designed to help you to write Ansible code that is more reliable, secure, and maintainable. Controlling how `ansible-lint` behaves is possible via `.ansible-lint` file.

When Ansible Lint finds a potential problem in your code, it will emit a warning or error message. The message will include information about the problem, such as the rule that was violated and the line of code where the problem was found. Ansible Lint can also be configured to automatically fix some of the most common problems. For example, it can fix missing semicolons and indentation errors.

With GitHub Actions it is possible to run `ansible-lint` "automatically". Although this could be configured in a number of ways, this project uses a "Pull Request" as the oppertunity to run `ansible-lint`. The pass / fail nature of the tool makes it possible to determine if the proposed code is following best practices and therefore help make a determination if the code is suitable for acceptance.

A second action makes it possible to run playbooks with `ansible-playbook`. To trigger the playbook `playbooks/playbook.yml`
- Click on **Actions**
- Along the left click on **Github runs ansible-playbook**
- Finally near the right click on **run workflow**

### Repository Author
Russell Zachary Feeser || @RZFeeser  
https://rzfeeser.com  
https://iris7.com

**ChangeLog since 0.4.2**

#### **Changed**
- **Avoid shell-command for vault operations**
  - Replace `shell-command` with `call-process` to eliminate shell injection risk through the vault password file path ([3901c06](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/3901c06b5c06af371d91225b29b4f6fb1c54346f))
  - Mark `ansible-vault-password-file` as `:risky` to alert users that the file-local variable can be dangerous
  - Refactor `ansible-vault-get-password` to return a list of arguments instead of a formatted string, enabling direct process invocation

**ChangeLog since 0.4.1**

#### **Added**
-  **Use environment variables for vault password**
  - Provide the option to read the password from the environment ([#11](https://gitlab.com/emacs-ansible/emacs-ansible/-/issues/11) [09677789](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/09677789acc4039726723f24efb0f1ad30ad6fa7))

**ChangeLog since 0.4.0**

#### **Changed**
- **Snippet creation**
  - Update lib/generate.rb so that it checks out the ansible subdirectory to create and generate the snippets ([commit 68877788](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/68877788)).

#### **Fixed**
- **Submodule removal**
  - The lib/ansible submodule has been removed ([#6](https://gitlab.com/emacs-ansible/emacs-ansible/-/issues/6)).

**Changelog Since Version 0.3.2**

#### **Added**
- **Vault Management Improvements**:
  - Do not recreate vault file if there is no change ([#5](https://gitlab.com/emacs-ansible/emacs-ansible/-/issues/5)).
    - Thanks to Uwe Koloska! ([Merge Request #4](https://gitlab.com/emacs-ansible/emacs-ansible/-/merge_requests/4)).
- **New Features**:
  - Add an alias `ansible` to `ansible-mode` for improved functionality ([Merge Request #2](https://gitlab.com/emacs-ansible/emacs-ansible/-/merge_requests/2)).
  - Ability to prompt for passwords interactively for convenience ([commit 814ea508](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/814ea508dba6d30f4e8e8f82193e97eb4544268d)).

#### **Changed**
- **Documentation Enhancements**:
  - Added links to docstrings for better API usability ([Merge Request #1](https://gitlab.com/emacs-ansible/emacs-ansible/-/merge_requests/1)).
  - Updated README for renaming from `ansible` to `ansible-mode` ([commit 057df87](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/057df87c556a5f1ccaf98078aec5c9f413df17e1)).
	- Corrected default location for password file in the documentation ([commit b056f75](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/b056f75ff65cf6a7325274ec7a326bcacb9a751f)).

#### **Fixed**
- **Output Parsing**:
  - Fixed PromQL output parsing to prevent matching non-`.yml` files ([commit 4042e3d3](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/4042e3d3d115f442a007448c54d3dd9b21bbd0ec)).
  - Fixed parsing issues for other languages ([Merge Request #3](https://gitlab.com/emacs-ansible/emacs-ansible/-/merge_requests/3)).
- **Code Improvements**:
  - Deduplication of identifiers for snippets ([#4](https://gitlab.com/emacs-ansible/emacs-ansible/-/issues/4)).
  - Handle `ansible-lint` command formatting ([commit 223a387](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/223a387f7a61f6f557e85fc7dfef0999f81523d)).
  - Fix syntax highlighting for comments ([PR #43](https://gitlab.com/emacs-ansible/emacs-ansible/-/pull_requests/43)).
  - Addressed compilation warnings by alphabetizing keyword lists ([commit eebb2fb](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/eebb2fb49d3c0a0586d1e4ead9ba618c7d003cae)).
- **Bugfixes**:
  - Warn instead of failing silently if incorrect parameters are provided ([commit 079c993](https://gitlab.com/emacs-ansible/emacs-ansible/-/commit/079c993b0825eef7c527f1e9083c3f0a0fefc01d)).

---

### **Acknowledgments**
Special thanks to contributors:
- **Uwe Koloska**
- **Peter Oliver**
- **Célestin Matte**
- **Ken’ichiro Oyama**
- **Frédéric Giquel**
- **Brian O'Reilly**

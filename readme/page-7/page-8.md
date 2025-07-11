# Page 8

## Ignoring Specific Rules Per Line

Add comments to your code using language-specific syntax to ignore specific rules per line:

{% code title="Comment Template" %}
```
nokodemcode: rule-id
```
{% endcode %}

**Ignore Specific Rules**

For issues like **Improper Neutralization of Input During Web Page Generation**, you can ignore specific rule IDs for this line of code:

* javascript\_rule-InsecureInnerHtml
* javascript\_rule-InsecureDocumentMethod

{% code title="JavaScript Syntax Example" %}
```javascript
// nokodemcode: javascript_rule-InsecureInnerHtml, javascript_rule-InsecureDocumentMethod
```
{% endcode %}

{% stepper %}
{% step %}
#### Find the Rule ID

1. Locate and retrieve the Rule ID in one of two ways, through either the Kodem platform or [VS Code](https://docs.kodemsecurity.com/integrations/ignoring-code-issues#example-in-vs-code).

{% hint style="info" %}
Multiple rules can be ignored by separating IDs with commas.
{% endhint %}

**Kodem Platform**:

1. Navigate to the [Kodem platform](https://app.kodemsecurity.com/).
2. Select your region from the dropdown menu in the upper right corner.
3. Log in by entering your organization's slug provided by Kodem.
4. Select **Issues** under **Triage** in the sidebar menu.
5. Select and issue and scroll to the bottom of the Triage drawer.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-18 at 19.17.51.png" alt=""><figcaption><p>Rule ID in Triage Drawer</p></figcaption></figure>
{% endstep %}

{% step %}
#### Add the Comment

1. Place the comment directly above or next to the line of code with issues.
{% endstep %}

{% step %}
#### Issue Exclusion

Once the scanning completes:

* Only the specified rule(s) that generate the issues are excluded.
* Other rule(s) that generate issues on the same line of code will still be generated and appear.
{% endstep %}
{% endstepper %}

<details>

<summary>Example in VS Code</summary>

### Ignore Specific Rules

Multiple issues can be ignored by separating rule IDs with commas.

#### Find the Rule ID

1. Open VS Code.

1) Click on the Kodem extension from the Activity Bar (sidebar).
2) In your project, you can retrieve the Rule ID(s) from either:
   * The Overview panel (left sidebar). Excluding issue type in parenthesis.
   * Bottom of the Kodem Issue dedicated panel (right sidebar).&#x20;
   * Inline annotations in the editor panel. Rule ID is in the parenthesis.
   * Quick Fix actions menu shortcut.
   * Problems panel. Rule ID is in the parenthesis.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-19 at 14.25.31.png" alt=""><figcaption><p>Retrieve Rule ID</p></figcaption></figure>

3. Place the comment directly above or next to  the line of code with issues. The file is automatically scanned.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-19 at 14.45.36.png" alt=""><figcaption><p>Ignore Specific Rules in VS Code</p></figcaption></figure>

4. Once the file completes scanning:
   * Only the specified rule(s) that generate the issues are excluded.
   * Other rule(s) that generate issues on the same line of code will still be generated and appear.

<figure><img src="https://docs.kodemsecurity.com/~gitbook/image?url=https%3A%2F%2F3136411388-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FZY4dsfekGohX1DwoEMB8%252Fuploads%252FZ8MxpbS9XpnRJRQLS4YF%252FScreenshot%25202025-06-15%2520at%252013.05.32.png%3Falt%3Dmedia%26token%3Db2304192-2870-4c30-9821-7cc06a1c19fa&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=dea0d210&#x26;sv=2" alt=""><figcaption><p>Issue Exclusion in VS Code</p></figcaption></figure>

#### Copy Issue Details

Copy issue details to share with team.

1. Select the shortcut from the Quick Fix action menu in the editor panel and problems panel.
2. Past, store and share issue details.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-19 at 14.49.28.png" alt=""><figcaption><p>Copy Issue Details</p></figcaption></figure>

</details>

## Ignoring All Rules Per Line <a href="#validate-fixes" id="validate-fixes"></a>

Add comments to your code to ignore all rules for a specific line:

{% code title="Comment Template" %}
```
nokodemcode
```
{% endcode %}

**Ignore All Rules**

For issues like **Improper Neutralization of Input During Web Page Generation**, you can ignore all rule IDs for this line of code:

* javascript\_rule-InsecureInnerHtml
* javascript\_rule-InsecureDocumentMethod

{% code title="JavaScript Syntax Example" %}
```javascript
// nokodemcode
```
{% endcode %}

1. Add the comment to ignore all rules by manually entering the comment using language-specific syntax above or next to the line of code with issues.
2. All rules generating issues on that line will be excluded regardless of type.

<details>

<summary>Example in VS Code </summary>

### Ignore All Rules

1. Open VS Code.
2. Click on the Kodem extension from the Activity Bar (sidebar).
3. Place the comment directly above or next to  the line of code with issues. The file is automatically scanned.&#x20;

<figure><img src="../../.gitbook/assets/333.webp" alt=""><figcaption><p>Ignore All Rules in VS Code</p></figcaption></figure>

4. Once the file completes scanning, all the rules that generate the issue(s) on the line of code are excluded.

<figure><img src="../../.gitbook/assets/4444.webp" alt=""><figcaption><p>Issues Exclusion in VS Code</p></figcaption></figure>

</details>

## Ignoring Files & Folders

Create a `.kodemcodeignore` file in your project root to specify files and directories to exclude from scanning using patterns similar to `.gitignore`:

```bash
# Common directories to exclude
node_modules/
vendor/
dist/
build/

# Ignore specific file types
*.min.js
*.test.js
*.log

# Specific files to ignore
example.txt
config.dev.json

# Include a specific file that would otherwise be ignored
!important.log

# Directory patterns
directory/        # Ignores the directory named "directory" and all its contents
directory/*       # Ignores all files and directories inside "directory", but not the directory itself
**/directory      # Ignores a directory named "directory" at any level
**/directory/     # Ignores all files and directories inside "directory" at any level
```

#### Syntax Rules

* Each line specifies a pattern
* Blank lines are ignored and can be used for readability
* Lines starting with `#` are treated as comments

#### Pattern Types

**Exact File Names**

```python
example.txt    # Ignores a file named exactly "example.txt"
```

**Wildcards**

```bash
/*.log          # Ignores all files ending with .log
file?.txt      # Matches file1.txt, file2.txt, etc.
file[123].txt  # Matches file1.txt, file2.txt, file3.txt
file[a-z].txt  # Matches filea.txt, fileb.txt, etc.
```

**Directory Exclusions**

```bash
directory/     # Ignores the directory named "directory" and all its contents
directory/*    # Ignores all files and directories inside "directory", but not the directory itself
**/directory   # Ignores a directory named "directory" at any level
```

**Negation**

```c
*.log          # Ignores all .log files
!important.log # But keeps important.log
```

<details>

<summary></summary>

<div><figure><img src="../../.gitbook/assets/plantlovershopcard.webp" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/teapotnewA6.webp" alt=""><figcaption></figcaption></figure></div>

<figure><img src="../../.gitbook/assets/1.jpeg" alt=""><figcaption></figcaption></figure>

</details>

<figure><img src="../../.gitbook/assets/plantlovershopcard.webp" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-19 at 14.45.36.png" alt="fdvced"><figcaption><p>dceds</p></figcaption></figure>


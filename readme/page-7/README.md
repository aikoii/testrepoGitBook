# Page 7

This article describes recommended steps in Machinify Audit to efficiently and accurately perform clinical or coding DRG reviews.

## Introduction

A DRG audit, or Diagnosis Related Group audit, is a review of a patient's hospital stay to ensure that the DRG assignment and payment are accurate. DRG audits can help hospitals avoid costly billing issues and penalties. Machinify Audit supports audit angles MS-DRG (Medicare Severity Diagnosis Related Groups) and APR-DRG (All Patient Refined Diagnosis Related Groups).

This article describes DRG audits and covers steps applicable for clinical and coding reviews for both MS-DRG and APR-DRG. Clinical and coding reviews are quite similar, but if your team does not perform all of the steps listed, then focus on the steps that apply to your company’s audit process.

## Step 1: Get case context from the Overview tab

{% hint style="success" %}
**Goal**: Get oriented with the case context in the first 15 seconds.
{% endhint %}

Your first stop to orient yourself with case details is the **Overview** tab in the middle panel.

The top of the **Overview** tab is a high-level overview with the case’s basic info.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

Use its fields to orient yourself to the case:

| Field                 | Description                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Claim Number**      | Claim number associated with this case.                                                                                                                                                                                                                                                                                                                                                                  |
| **Audit Angle**       | Type of review, such as _Clinical_ or _Coding_.                                                                                                                                                                                                                                                                                                                                                          |
| **Paid on**           | Date of payment only if this is a postpay review. For prepay reviews, this field shows the adjudication date.                                                                                                                                                                                                                                                                                            |
| **LOB**               | Line of business the claim is in, such as Medicare, Medicaid, Commercial, ASO, and FI.                                                                                                                                                                                                                                                                                                                   |
| **DRG**               | Diagnosis-Related Group code. For MS-DRG, also the number of CCs and MCCs. For APR-DRG, also the number of SOIs.                                                                                                                                                                                                                                                                                         |
| **Adjudicated on:**   | Date of adjudication.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Admission Date:**   | Date of admission.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Discharge Date:**   | Date of discharge.                                                                                                                                                                                                                                                                                                                                                                                       |
| **LOS**               | The length of stay.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Discharge Status**  | Discharge status code, such as `01` for home care, or `02` for transfer to short term acute care. See [this list](https://med.noridianmedicare.com/web/jea/topics/claim-submission/patient-discharge-status-codes) for a reference.                                                                                                                                                                      |
| **Patient Age / Sex** | Important patient demographics info.                                                                                                                                                                                                                                                                                                                                                                     |
| **Expires on:**       | After the expiration date, you can no longer submit it to recover money. The duration for claim expiration is based on multiple requirements: (1) Federal requirements such as CMS (2) state audit requirements (3) Payer policies, which can’t be longer than federal or state limits (4) payer/provider contract rules, which similarly can’t be longer than the limits in previous items 1 through 3. |

Below this section is a series of expandable/collapsible panels with more information.

### Summary

The first section, **Summary,** is a human-readable clinical summary based on the medical records. This is the first of the collapsible sections. It contains a concise overview of the case. It provides you with meaningful context and details before you start your review.

<div align="left"><figure><img src="broken-reference" alt="" width="563"><figcaption></figcaption></figure></div>

To validate the information, hover your mouse over the text. Machinify Audit displays a popup that shows actual text from the medical record.

<div align="left"><figure><img src="broken-reference" alt="" width="563"><figcaption></figcaption></figure></div>

To compare against the medical record raw image, click the page number (such as **Page 5** in the example) to leave the overview tab and instead directly view that section of the medical record.

### Charges

Details of the charges associated with this case.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

### Provider

Details of the medical provider.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

### Member

Details about the patient, which is also known as the _member_.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

### Codes

Scroll to the **Codes** section for details of the DRG, codes, and diagnosis descriptions.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

## Step 2: Review points of interest (POIs)

{% hint style="success" %}
**Goal**: Spend no more than one to two minutes learning information here. You’ll revisit this information in a deeper way later in the review.
{% endhint %}

{% include "https://app.gitbook.com/s/sRQUHvVPiGFWk0VjnTm5/~/reusable/qoIXR4UjwTJBRJKmquVU/" %}

## Step 3: Evaluate diagnoses & procedures

{% hint style="success" %}
**Goal:** The time for Step 3 completion is approximately five minutes. Not all questions need answering. You only need to answer enough questions to arrive at a decision. See below for discussion about which codes drive the DRG or severity of illness (SOI).
{% endhint %}

### Check which diagnosis codes you need to review

Find the first tab in the left panel, **Validate Billed Codes**. Each diagnosis or procedure deemed worthy of review due to its relevance for accurate DRG payment is listed in the review items in the first tab of the left panel. Each code associated with a specific policy guide lists the criteria to evaluate the item for validity. Diagnoses or procedures with a generic policy have a single-line audit statement.

Sometimes _not all codes_ shown in the left panel affect the DRG (MS-DRG) or SOI (APR-DRG). You can confirm each code’s status in the **Overview** tab in the middle panel. Under **Diagnoses**, check the rightmost column. For APR-DRG audits, instead look for the column **Affects SOI**. For MS-DRG audits, look for **Affects DRG.**

<div align="left"><figure><img src="broken-reference" alt="" width="165"><figcaption></figcaption></figure></div>

### **Criteria evidence reference links**

Diagnosis codes with policy criteria and supporting evidence in the medical records show reference links that are shown with a summary and a link to the location in the medical record. Click on a reference link to navigate to the medical record content that supports the finding.

<div align="left"><figure><img src="../../.gitbook/assets/driedbunches.png" alt=""><figcaption></figcaption></figure></div>

To avoid missing critical context, many links might be provided. The links are sorted by relevance, similar to a Google search. Usually, one of the first few results answer the clinical question. Step through the links using the up and down arrows next to the link.

*   **Review AI-assisted evidence highlights.** Machinify Audit uses AI to highlight the most important parts of the record for a criterion. _If you confirm the reference in the medical record_, click the star to the right of the highlight to convert it to auditor-confirmed evidence. The star becomes yellow and _your initials_ replace the AI icon on the left.\


    <figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>
* **Search for evidence to add as new highlights.** If no reference links exist or you strongly suspect that reference links are incorrect, search the medical records for more evidence.
  * Click the search box in the tab for **Search Documents** in the right panel. Search for any medical term or word (such as `SPO2` or `pna`). Machinify Audit shows all relevant results, including related terms, across all documents for the case. Scroll the preview hits of the searched term or word in the right pane, or click a search result to jump directly to the medical record.
  * Use the **Points of Interest** section to jump to specific sections in medical records.
  * To add highlights from the medical record, first use your mouse to highlight text in the medical record. Click the **+ Highlight** button that appears. Finally, click on the criterion in the left pane to associate with this reference link.

### Criteria notes

You can add a text note on any criteria by clicking the tiny document icon next to each criterion. Criteria text fields help future human reviewers understand your decisions. It also helps the AI assistant summarize your case findings.

<div align="left"><figure><img src="../../.gitbook/assets/morningtinypawws_det1+copy.jpeg" alt=""><figcaption></figcaption></figure></div>

### **Criteria and criteria group icons**

As you review criteria, mark if the criteria is met (click the checkmark, which turns green), or not met (click the X, which turns red), or fill in a numerical value. If the numerical value is pre-filled, verify its answer by marking the check or X.

Some criteria are grouped hierarchically under one label:

<div align="left"><figure><img src="../../.gitbook/assets/1.jpeg" alt=""><figcaption></figcaption></figure></div>

Grouped criteria have an icon to the left of the group label to indicate its status. A green round checkmark means that these grouped criteria are already satisfied. A red X means criteria are not met. A yellow circle with horizontal line indicates undetermined.

{% hint style="warning" %}
**IMPORTANT:** If the icon for a criteria group becomes a round green checkmark <img src="broken-reference" alt="" data-size="line">, don’t spend more time answering questions in that group. Skip to the following group.
{% endhint %}

Not all sub-criteria in a group need to be evaluated or marked green or red. For example, it’s common that only one of the grouped sub-criteria might need to be satisfied. Narrow your focus to any unfinished evaluation criteria using data in the summary and POIs.

### If a diagnosis audit is done, you see its green round checkmark

When you begin an audit of a diagnosis code, look to the right of the diagnosis name for an icon. Often, it’s initially yellow with a horizontal line to indicate that it’s undetermined. When required guidelines are met for this diagnosis, its icon becomes a green round checkmark.

<figure><img src="../../.gitbook/assets/CleanShot 2023-01-10 at 12.42.50@2x.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**IMPORTANT:** If the diagnosis icon becomes a round green checkmark <img src="broken-reference" alt="" data-size="line">, don’t spend more time answering questions for it. Skip ahead to the following diagnosis code.
{% endhint %}

### **Delete a diagnosis or procedure for disqualified codes**

If a code is disqualified, delete the diagnosis or procedure.

1. Click the code in the left panel to open it.
2. Click **ACTIONS** next to the code.
3. Click **Delete From Claim**.

If applicable, Machinify Audit automatically tries to re-group the claim and identify the new DRG with its corresponding price. You’ll see the new DRG value at the top of the overview tab (in the middle pane) and the **DRG calculator** tab (the third tab in the middle pane).

### Check for impact if you re-sequence, delete, or add codes

If a code re-sequencing, deletion, or addition results in a DRG or SOI level change, a code that’s unlisted may need to be added for further validation of the new DRG or SOI level. Click the **More** button at the top of the left panel in this tab to add other codes submitted on the Uniform Bill 2004 (UB-04) that need further review.

For APR-DRG audits, it’s especially important that after a code is deleted, you must go to the DRG calculator to see if there are any new codes driving the SOI level or DRG:

1. Go to the **DRG calculator** tab in the middle panel.
2. Click **Current review**.
3. Click **Calculate** to refresh or register recent changes.
4.  Even if a code is deleted and the DRG (and SOI) remains the same, it does not mean your audit is complete. Review the **Current review** tab contents for whether there are additional codes in the overview summary with a “Y” (for “yes”) in the **Affects SOI** column to review.\


    <div align="left"><figure><img src="broken-reference" alt="" width="164"><figcaption></figcaption></figure></div>
5. If there are additional codes to review, you can add these codes by clicking **More** in the left panel drop down menu. You can compare the **Current Review** to the **Original Claim** to see any differences.
6. To add new codes that aren’t on the UB, go to the second tab on the left panel called **Add Diagnoses/Procedures**. Note that you _cannot_ add new codes to the first tab in the left panel Validate Billed Codes. Newly added added codes can be reviewed in detail only under the second tab on the left panel. If you deleted codes and you need to add new codes to replace deleted ones, add them now.\
   ![](broken-reference)

## Step 4: Edit claim fields only if there’s a change to principal diagnosis or discharge status

{% hint style="success" %}
**Goal:** The time varies on this step depending on what might need to be modified. If changes are needed, this takes approximately two minutes.
{% endhint %}

If you invalidate or delete the principal diagnosis, you must select a new one, or the system defaults to the following code in the list as the principal diagnosis. You must select the appropriate principal diagnosis if the billed one is incorrect.

If there was a change in the discharge status, change it from what was billed to something else supported by the documentation.

To edit these fields, go to the third tab on the left panel, **Edit Claim Fields**.

## Step 5: Review the revised DRG and write a final case summary

{% hint style="success" %}
**Goal:** The time for this step’s completion is approximately three minutes.
{% endhint %}

Review the revised DRG and write a case summary:

1. Go to the left panel’s fourth tab, **Final Review**.
2. Verify the revised DRG and coding changes.
3. Use the text box to type your findings. The AI Summary writer attempts to automatically write up the findings based on what you documented previously. The UI for the DRG final case summary varies by payer:
   * You may see a selector with choices **Manual** and **Automatic**. To use the default AI-generated summary, set the selector in the upper-right to **Automatic**. For example, use this if there are no coding changes and no additional context is needed. To edit the summary, set the selector in the upper right to **Manual.** You can add, delete, or revise text as appropriate. For example, ensure it has all code changes, the cited location in the record and any coding references, and any revised DRG.
   * You may see a **+Regenerate** button instead of the **Manual/Automatic** selector. There is a default AI summary, but you can edit it to add, delete, or revise the text as appropriate. If you want to ignore your changes and revert to the original AI-generated summary, click **+Regenerate**.

{% hint style="info" %}
**Tip:** Avoid unnecessary duplication in the final case summary text box: other reviewers can see your clinical criteria answers, they can follow links to the medical records, and they see the same POIs. Only add any non-obvious insights that emerge from your unique knowledge as a clinical subject matter expert.
{% endhint %}

Here’s an example of an APR-DRG final summary in **Manual** mode:

<figure><img src="../../.gitbook/assets/CleanShot 2023-01-25 at 19.27.15@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/plantlovershopcard.webp" alt=""><figcaption></figcaption></figure>

<div align="left"><figure><img src="../../.gitbook/assets/teapotnewA6.webp" alt=""><figcaption></figcaption></figure></div>

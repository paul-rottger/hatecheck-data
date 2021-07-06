In this repo, you can find the data from our ACL 2021 paper "HateCheck: Functional Tests for Hate Speech Detection Models".
- "test_suite_cases.csv" contains the full test suite (3,728 cases in 29 functional tests).
- "test_suite_annotations.csv" provides detailed annotation outcomes for each case in the test suite.
- The corresponding "all_" files cover all 3,901 cases that were initially generated, from which 173 were excluded from the test suite due to fewer than four out five annotators agreeing with our gold standard label.
- "template_placeholders.csv" contains the tokens that the placeholders in the case templates are replaced with for generating the test cases.

<br/>

## "test_suite_cases.csv" and "all_cases.csv"

**functionality**
The shorthand for the functionality tested by the test case.

**case_id**
The unique ID of the test case (assigned to each of the 3,901 cases we initially generated)

**test_case**
The text of the test case.

**label_gold**
The gold standard label (hateful/non-hateful) of the test case. All test cases within a given functionality have the same gold standard label.

**target_ident**
Where applicable, the protected group targeted or referenced by the test case. We cover seven protected groups in the test suite: women, trans people, gay people, black people, disabled people, Muslims and immigrants.

**direction**
For hateful cases, the binary secondary label indicating whether they are *directed* at an individual as part of a protected group or aimed at the group in *general*.

**focus_words**
Where applicable, the key word or phrase in a given test case (e.g. "cut their throats").

**focus_lemma**
Where applicable, the corresponding lemma (e.g. "cut sb. throat").

**ref_case_id**
For hateful cases, where applicable, the ID of the simpler hateful case which was perturbed to generate them.
For non-hateful cases, where applicable, the ID of the hateful case which is contrasted.

**ref_templ_id**
The equivalent, but for template IDs.

**templ_id**
The unique ID of the template from which the test case was generated (assigned to each of the 866 cases and templates from which we generated the 3,901 initial cases).

<br/>

## "test_suite_annotations.csv" and "all_annotations.csv"

**functionality**, **case_id**, **templ_id**, **test_case**, **label_gold** See above.

**label_[1:10]**
The label provided for the test case by a given annotator. We recruited and trained a team of ten annotators. Each test case was annotated by exactly five annotators.

**count_label_h**
The number of annotators who labeled a given test case as hateful.

**count_label_nh**
The number of annotators who labeled a given test case as non-hateful.

**label_annot_maj**
The majority label.







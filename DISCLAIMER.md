# Medical and Legal Disclaimer

**Project:** Snip EMR Assistant – WinRT OCR + Linguistic Cleanup + Local LLM + Deep Disease Scanner  
**License:** MIT

---

## 1. Not a Medical Device

This software is provided **for research, education, and documentation assistance only**.

It is **not**:

- A medical device.
- A diagnostic system.
- A decision support tool.
- Cleared, approved, or certified by the **FDA**, **EMA**, or any other regulatory authority.

Any use of this software in clinical workflows is at the sole risk and responsibility of the user and/or deploying organization.

---

## 2. No Diagnosis, Treatment, or Clinical Advice

The Snip EMR Assistant, including the **“Deep Disease Scanner”** and all LLM-based features:

- **Does not** diagnose disease.
- **Does not** recommend treatment or management.
- **Does not** replace independent clinical judgment by a licensed healthcare professional.

Outputs (e.g., disease flags, comorbidity “hits,” timelines, summaries, MDM text) are **suggestions and drafts only** and must be independently reviewed, edited, and validated by a clinician before being used in any clinical context.

---

## 3. Deep Disease Scanner – Current Limitations

The **Deep Disease Scanner** is an **experimental prototype** that combines:

- Compiled regular expressions (regex) over OCR’d text.
- Optional local LLM analysis on small context windows.

By design and by limitation:

1. It may produce **false positives** (e.g., flagging a disease that is not actually present).
2. It may produce **false negatives** (e.g., failing to detect a documented disease).
3. It may misinterpret:
   - Negations (e.g., “no CAD”, “denies diabetes”).
   - Historical vs active problems.
   - Family history vs personal history.
4. It may be sensitive to:
   - OCR errors and layout artifacts.
   - Abbreviations and local documentation styles.
   - Incomplete or truncated context.

Therefore:

> **The Deep Disease Scanner must never be relied upon as the sole source of truth for medical conditions, risk assessment, or clinical decisions.**

The intended use of the scanner **in its current state** is to help **highlight parts of the text for human review**, not to provide automated medical conclusions.

---

## 4. No Warranty

This project is distributed under the **MIT License**:

> THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,  
> INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A  
> PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT  
> HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION  
> OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE  
> SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

You should read the full license text in `LICENSE`.

---

## 5. Responsibility of Deployers and Integrators

Anyone who:

- Integrates this software into a clinical product, EMR, or platform.
- Modifies it and deploys it as a service.
- Distributes it as part of a commercial or institutional solution.

is responsible for:

1. Assessing regulatory impact (e.g., **FDA 510(k)**, **De Novo**, or other regional requirements).
2. Implementing appropriate quality management and risk controls (e.g., **ISO 14971**, **IEC 62304**, **ISO 13485**) as applicable.
3. Ensuring that end-users understand the **experimental** nature and limitations of the software.

The maintainers of this repository do **not** assume any responsibility for how third parties deploy or represent this software.

---

## 6. Protected Health Information (PHI)

This repository and its issue tracker are **not** appropriate places to store or share Protected Health Information (PHI) or other identifiable patient data.

- Do **not** upload real patient notes or images.
- Do **not** paste PHI into GitHub issues, discussions, or pull requests.
- Use **synthetic, anonymized, or heavily redacted** examples only.

---

## 7. Future Regulated Versions

A future, regulated version of this codebase may be developed under:

- Formal Risk Management (**ISO 14971**),
- Software Lifecycle Processes (**IEC 62304**),
- Quality Management Systems (**ISO 13485**),
- And potentially subject to **FDA** or other regulatory submissions.

Such a regulated version would be developed, validated, and maintained separately from this open-source repository.

This open-source project should be considered **pre-regulatory**, research-grade software only.

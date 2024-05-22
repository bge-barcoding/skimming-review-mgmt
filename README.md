# skimming-review-mgmt

This repository is for tracking, reviewing and aggregating genome skimming pipeline runs.
The general idea is that Ollie's skimming [pipeline](https://github.com/o-william-white/skim2mt)
might be able to produce a report that includes:

- visualizations, such as multiqc plots
- summary stats, such as yield for the current run (e.g. x/95 COI sequences recovered)
- results for checks against reference DB (e.g. nodal distance b/w obs and exp species)
- results for nonsense mutation checks (e.g. AA translation of HMM alignment)

Such a report might be generated, for example, by populating a (R)Markdown template and
transforming it to PDF (e.g. with pandoc or by knitting). The submitter then commits and
pushes this PDF to a standard location in a local fork of this repo and produces a pull
request for it. Other reviewers are tagged in the PR, who then review the report. If OK,
the PR is merged. In this way, we gradually accumulate standard reports in one location
so that we keep track of what's done and how we assessed it. The approach is also what 
ERGA does for genomes and is similar to the review process for Journal of Open Source 
Software (JOSS) and for BioConda contributions.

# Data, code and records

## The rule behind all the others

Raw data are never edited. Everything else, from cleaned tables to figures, can be regenerated from the raw data plus the code. If it cannot, the project is not in good order.

## Where data live

Store project data on storage approved by your institution or the lab head. A laptop or a personal cloud account is never the only copy. Keep three copies on two kinds of storage, with one off site. Check that restoring from backup works, once a year.

Use a password manager and two-factor authentication on every account that touches lab data. Do not share accounts. Do not email sensitive data.

## How projects are organised

Every project has a folder with the same layout:

```
project_name/
  README.md
  data_raw/
  data_processed/
  code/
  results/
  docs/
```

Name files in lower case with no spaces, put dates in the form 2026-10-05 at the start, and describe the content. Do not write "final" or "final2" in a file name. Use version control, or the version history of the storage, to keep versions.

Every project folder has a [README](../templates/project-readme.md) saying what the project is, who is involved, where the raw data came from, how to rerun the analysis, and what each column in each data table means.

## Code

Analysis code lives in a Git repository, one per project. Commit often, with messages that say what changed and why. Record software versions, using an environment file or container. Keep passwords, keys and tokens out of repositories. Anyone in the lab should be able to clone the repository, follow the README, and reproduce your figures.

When a paper is submitted, the repository gets a tagged release and a licence, and it is archived on a service that issues a DOI.

## Sequencing and imaging data

Raw sequencing files and raw images are stored unchanged and read-only. For every analysis, record the reference genome and annotation versions, the software versions and the random seeds, so that a colleague gets the same result. Set quality-control thresholds before you look at the outcome, and write them down.

## Sharing data

We aim for FAIR data: findable, accessible, interoperable and reusable. At submission, deposit the data behind each paper in an appropriate repository, with the metadata another researcher would need. Datasets from public funding should be open unless there is a legal or ethical reason, or a documented intellectual property reason approved by the lab head. Data from human donors are the usual exception, as described below.

Protocols go on protocols.io with a version number once they are stable, and the project README links to them.

## Personal and sensitive data

If a project uses data about people, including patient data, genetic data and sample metadata, then the legal basis, the ethics approval and the data protection assessment come before the first file is touched. Collect the minimum you need. Pseudonymise as early as you can, and keep the key separate from the data. Give access only to people who need it, and remove it when they stop needing it. Follow the institution's rules and its data protection officer's advice.

Sequencing, genotype and other molecular data from donor cells can identify the donor, so they count as personal data even when no name is attached. Check the donor consent and the approval before you plan to share them. Raw sequence data from human lines normally go to a controlled-access repository, such as the European Genome-phenome Archive, and not to an open one, unless the consent clearly allows open release. Processed data without genotype information can often be shared openly. Ask the data protection officer when you are unsure.

If you think personal data have been lost, exposed or sent to the wrong person, tell the lab head and your institution's data protection officer the same day. Under GDPR a reportable breach must reach the supervisory authority within 72 hours of the institution becoming aware of it, so hours count.

## How long we keep things

Keep raw data, notebooks, code and approvals for at least ten years after publication, unless an approval, contract or funder requires a different period. Your institution's policy overrides this where it differs.

## Handover

When you leave or change projects, hand over your data, notebooks, code and sample inventories before your last day. The [offboarding checklist](../templates/offboarding-checklist.md) lists what has to be done. The lab head signs off on it.

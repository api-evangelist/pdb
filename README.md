# RCSB PDB (pdb)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

RCSB Protein Data Bank (RCSB PDB) is a scientific data resource providing free, open access to the 3D structural data of biological macromolecules including proteins, nucleic acids, and complex assemblies. It serves researchers worldwide through a suite of programmatic APIs covering data retrieval, full-text and attribute search, sequence and structure similarity search, molecular model data access, volumetric electron density maps, sequence coordinate alignments, and structure alignment calculations.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pdb/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pdb/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producer
- **Access:** Open

## Tags

- Structural Biology
- Proteomics
- Bioinformatics
- Genomics
- Life Sciences
- Open Data
- Research
- Macromolecules
- Crystallography
- NMR

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### RCSB PDB Data API

Provides structured access to the complete RCSB PDB holdings via REST and GraphQL interfaces. Given a known PDB identifier, callers can retrieve rich JSON metadata about entries, polymer entities, non-polymer entities (ligands), polymer entity instances (chains), assemblies, branched entities, and chemical components.

- **Human URL:** [https://data.rcsb.org](https://data.rcsb.org)
- **Base URL:** `https://data.rcsb.org/rest/v1/core`

#### Properties

- [Documentation](https://data.rcsb.org/redoc/index.html)
- [GraphQL Endpoint](https://data.rcsb.org/graphql)
- [GraphQL Explorer](https://data.rcsb.org/graphiql/index.html)
- [Python SDK](https://github.com/rcsb/py-rcsb-api)
- [JavaScript SDK](https://github.com/rcsb/rcsb-api-tools)

### RCSB PDB Search API

Full-featured search API for locating PDB identifiers that match complex query conditions. Supports text attribute searches, BLAST-like sequence similarity (protein, DNA, RNA), chemical small-molecule queries (formula, SMILES, InChI), 3D structure embedding searches, sequence motif searches, structural motif searches, and unstructured full-text searches.

- **Human URL:** [https://search.rcsb.org](https://search.rcsb.org)
- **Base URL:** `https://search.rcsb.org/rcsbsearch/v2/query`

#### Properties

- [Documentation](https://search.rcsb.org/redoc/index.html)
- [Getting Started](https://www.rcsb.org/docs/programmatic-access/web-apis-overview)

### RCSB PDB ModelServer API

Provides on-demand access to subsets of macromolecular model data stored in PDBx/mmCIF format. Callers can request individual chains, residue ranges, ligand environments, or symmetry-expanded assemblies without downloading full structure files.

- **Human URL:** [https://models.rcsb.org](https://models.rcsb.org)
- **Base URL:** `https://models.rcsb.org`

#### Properties

- [Documentation](https://models.rcsb.org)

### RCSB PDB VolumeServer API

Delivers subsets of volumetric electron density and cryo-EM map data associated with PDB entries. Researchers can query a specific region around a ligand or residue and retrieve only the relevant density slice, accelerating interactive visualization.

- **Human URL:** [https://maps.rcsb.org](https://maps.rcsb.org)
- **Base URL:** `https://maps.rcsb.org`

#### Properties

- [Documentation](https://maps.rcsb.org)

### RCSB PDB Sequence Coordinates API

GraphQL service providing sequence-level alignments between structural databases and external sequence resources. Exposes alignment and annotations queries enabling mapping of PDB chain positions to UniProt, NCBI RefSeq, CATH, SCOPe, and Computed Structure Models (CSMs).

- **Human URL:** [https://sequence-coordinates.rcsb.org](https://sequence-coordinates.rcsb.org)
- **Base URL:** `https://sequence-coordinates.rcsb.org/graphql`

#### Properties

- [Documentation](https://sequence-coordinates.rcsb.org)
- [GraphQL Explorer](https://sequence-coordinates.rcsb.org/graphiql/index.html)

### RCSB PDB Structure Alignment API

Asynchronous REST API that performs programmatic structure alignment calculations between PDB entries or user-supplied coordinate files. Callers submit a job via POST /submit and poll GET /results with a UUID ticket for status and output.

- **Human URL:** [https://alignment.rcsb.org](https://alignment.rcsb.org)
- **Base URL:** `https://alignment.rcsb.org`

#### Properties

- [Documentation](https://alignment.rcsb.org/api-reference.html)
- [Query Editor](https://alignment.rcsb.org/query-editor.html)

## Common Properties

- [Website](https://www.rcsb.org)
- [Documentation](https://www.rcsb.org/docs/programmatic-access/web-apis-overview)
- [Getting Started](https://www.rcsb.org/docs/programmatic-access)
- [File Downloads](https://files.wwpdb.org)
- [GitHub](https://github.com/rcsb)
- [Python SDK](https://github.com/rcsb/py-rcsb-api)
- [JavaScript SDK](https://github.com/rcsb/rcsb-api-tools)
- [Plans](plans/pdb-plans-pricing.yml) - API Commons Plans 0.1
- [Rate Limits](rate-limits/pdb-rate-limits.yml) - API Commons Rate Limits 0.1
- [FinOps](finops/pdb-finops.yml) - FOCUS-aligned FinOps Framework 1.0
- [Contact](mailto:info@rcsb.org)
- [Mailing List](https://groups.google.com/g/rcsb-pdb-api-announcements)

## Plans

RCSB PDB APIs are freely available to all researchers and developers with no subscription fee, API key, or registration required. All API endpoints are rate-limited to ensure fair access across the global research community.

- **Open Access (Free)** - All six API services plus bulk file downloads at no cost. Recommended starting rate of a few requests per second. HTTP 429 returned when limits are exceeded. Static file downloads via HTTPS and rsync are unrestricted.

## Rate Limits

- No published numeric ceiling; a sustained rate of a few requests per second is recommended across all API endpoints.
- HTTP 429 is returned when the limit is exceeded; clients should implement exponential backoff and honor Retry-After.
- Static file downloads (https://files.wwpdb.org, rsync://rsync.rcsb.org) are not rate-limited.
- Bulk workloads should prefer rsync for full archive replication and off-peak scheduling.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com

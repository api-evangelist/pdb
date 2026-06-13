# RCSB PDB (pdb)

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

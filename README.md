# LOF-ODP-002: Legal Role Conferral

| | |
|---|---|
| **Status** | Draft 0.2.0, for review by the LOF founding coordinators |
| **IRI** | https://w3id.org/lof/odp-002.owl |
| **Specification** | https://legal-ontologies-foundry.github.io/odp/odp-002/ |
| **License** | [CC BY 4.0](LICENSE) |
| **Contact** | David R. Koepsell (drkoepsell@tamu.edu) |

## Scope

Covers legal roles and the legal acts that confer, modify, and terminate them. Excludes the specific duties, claims, and powers attached to a role, which are covered by LOF-ODP-003, and non-legal social roles.

**Depends on:** [LOF-ODP-001](https://w3id.org/lof/odp-001.owl), imported from its base release.

## Competency questions

1. Which legal roles does this person or organization currently bear?
2. Which legal act conferred this role, and under what legal content?
3. Which legal act terminated this role?
4. Which legal content specifies what this role consists in?
5. Which of a person's legal roles arose by operation of law rather than by a conferring act?
6. Which legal act changed what this role consists in, without ending it?
7. When was this role conferred, and when was it terminated? (BFO *occupies temporal region* on the acts.)
8. Which organization bears this role, and which of its members acted in conferring it?

## BFO grounding (LOF-P-004)

| Term | BFO category | Rationale |
|---|---|---|
| legal role | role (BFO:0000023) | Borne because of external circumstances (appointment, contract, statute); the bearer need not change physically to acquire or lose it. Exactly one bearer, as ISO/IEC 21838-2 requires of every specifically dependent continuant: when an office changes hands, one role ends and another begins. |

## Alignment (LOF-P-015)

Legal role is a kind of D-Acts *deontic role*, and role conferral and termination acts are kinds of D-Acts *deontic declaration*; a conferral or termination performed by means of a legal document is a *deontic document act*. These alignments, proposed by W. Mandrick, are stated in the LOF to D-Acts bridge. Organizations and their members come from the Common Core Ontologies through the LOF to CCO bridge. The pattern itself stays grounded directly in BFO role, and is compatible with the agent-role modeling in LKIF-Core. Akoma Ntoso's TLCRole and TLCPerson references can be mapped to legal role and its bearer.

## Files

| Path | Contents |
|---|---|
| `lof-odp-002.owl` | Full release: merged with imports and reasoned |
| `lof-odp-002-base.owl` | Base release: this pattern's own axioms only (import this) |
| `src/ontology/lof-odp-002-edit.owl` | Editors' file (OWL functional syntax; edit in Protégé) |
| `src/ontology/lof-odp-002-idranges.owl` | Term ID ranges (ODP002_0001000 to 0001999: first editor) |
| `src/sparql/` | QC checks run by `make test` |

## Building and testing

```
cd src/ontology
make test                    # HermiT consistency + seven SPARQL QC checks + ROBOT report
make release VERSION=0.2.0   # writes the two release files to the repo root
```

Requires Java 11 or later; ROBOT is downloaded on first use. The same checks
run on every pull request (`.github/workflows/qc.yml`).

## Citation

Koepsell, D. R. (2026). *LOF-ODP-002: Legal Role Conferral*, version 0.2.0 (draft). Legal Ontologies
Foundry. https://w3id.org/lof/odp-002/releases/0.2.0/lof-odp-002.owl

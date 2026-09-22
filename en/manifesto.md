---
title: "The MaiML Manifesto"
version: "1.0.0"
status: "Draft"
language: "en"
source: "MaiML_Manifesto_Paper_English_v1.0.0.docx"
source_sha256: "898a2f3194505703176e89d4640a29ceea8d406d046d7a56410466e1162f7f53"
---

# The MaiML Manifesto

**Design Principles for Research as a Knowledge-Generation Process**  
MaiML Core Team (authorship to be finalized upon approval)  
Draft Version 1.0.0 (paper form) | 2026-09-04

> This Markdown edition is derived from the saved English Word edition v1.0.0. Its content version is the same 1.0.0 as the Word edition, and the text is unchanged.

> **Status of this document**
>
> This paper presents the design principles (design rationale) behind MaiML. It is a non-normative, stand-alone document and a pre-approval draft. The specification of MaiML and its requirements are defined by JIS K 0200 and the MaiML schema. The content of this paper is not included in the normative documents (JIS, the ISO working draft, or the technical report).

## Contents

- [Abstract](#sec-abstract)
- [1  Introduction: why state the design principles](#sec-1)
- [2  The central thesis: the essence of research is the workflow](#sec-2)
- [3  The MaiML Manifesto (ten articles)](#sec-3)
- [4  Rationale for the principles](#sec-4)
- [5  From principles to implementation: mapping to the structure of MaiML](#sec-5)
- [6  Sharing and learning by humans and AI](#sec-6)
- [7  Positioning and limitations](#sec-7)
- [8  Conclusion](#sec-8)
- [References](#references)

<a id="sec-abstract"></a>
## Abstract

While the standardization of data formats for measurement and analysis has advanced steadily, no established method exists for sharing and inheriting, in machine-readable form, how the data were produced — the research workflow itself. This paper presents the design principles behind MaiML (Measurement Analysis Instrument Markup Language) as a ten-article manifesto, explains the rationale for each principle, and shows how the principles are realized in the structure of MaiML. The central thesis is a view of research: the essence of research is the workflow, and research is the practice of designing, executing, improving, and passing on knowledge-generation processes. From this thesis follow the principles of separating structure from semantics, separating design from execution, preserving the purity of abstraction, guaranteeing independent availability, and keeping the specification minimal and loosely coupled — opening the way to treating workflows as Knowledge Assets that humans and AI can share and learn.

Keywords: workflow; knowledge-generation process; design principles; Petri net; XES; Knowledge Asset; Workflow Engineering; MaiML

<a id="sec-1"></a>
## 1  Introduction: why state the design principles

Science has long been believed to advance by accumulating data. In measurement and analysis, the standardization of storage and exchange formats has made steady progress. Yet when instruments are replaced, personnel change, and dedicated software is lost, data alone do not make research reproducible. What must be passed on is the way the research was carried out — the process by which knowledge is generated.

MaiML is a data format for measurement and analysis designed from this problem awareness, and its specification has been standardized as JIS K 0200. A standard specifies what to record and how; explaining why the format is structured as it is lies outside the role of a standard. If the design principles are not articulated, decisions about extension, implementation, and operation lose their axis, and ad hoc interpretations erode the coherence of the specification.

This paper declares the design principles of MaiML as a ten-article manifesto (Section 3), explains their rationale (Section 4), and maps the principles to the structures of the specification (Section 5). This paper contains no requirements: conformance is defined solely by JIS K 0200 and the MaiML schema.

<a id="sec-2"></a>
## 2  The central thesis: the essence of research is the workflow

The value of research lies not only in the numbers obtained but in how those numbers were produced. Data are traces of research; the essence lies in the workflow — how research proceeds and how knowledge is generated. Seen this way, researchers are designers of knowledge-generation processes before they are producers of data.

This view bridges the experimental researcher's perspective (Protocol → Experiment → Data) and the software-engineering perspective (Class → Instance): designing a reusable procedure (Protocol), defining abstract models (Template), and obtaining concrete entities (Data) through execution corresponds to the relation between classes and instances in object orientation. If science is the discipline of understanding the structure of the world and engineering is the discipline of using understood structure for design, MaiML stands at their meeting point: turning understood research structure into designable knowledge assets. We call the general form of this methodology Workflow Engineering — the methodology of designing, representing, managing, and improving research workflows as reusable knowledge assets — and MaiML is its implementation.

<a id="sec-3"></a>
## 3  The MaiML Manifesto (ten articles)

The following preamble, ten articles, and creed constitute the declaration of MaiML's design principles.

Science has long been believed to advance through the accumulation of data. Yet the true value of research lies not only in the numerical results obtained, but in how those results were produced—that is, in the knowledge-generation process itself.

Even when instruments are replaced, personnel change, or dedicated software is lost, what should be passed on is the way the research was carried out. Data also form part of knowledge, but the source from which knowledge is generated lies in the workflow.

We hereby set out these design principles for MaiML as a language for designing, sharing, and passing on the knowledge-generation process of research as a machine-readable knowledge asset.

#### Article 1. The essence of research is the workflow.

Data are traces of research. The essence lies in the workflow: how research proceeds and how knowledge is generated.

#### Article 2. Research is the practice of designing, executing, improving, and passing on knowledge-generation processes.

Researchers do not merely produce data; we design the processes that produce them.

#### Article 3. A workflow is an asset.

A reusable workflow becomes a Knowledge Asset. If a paper is a description for people, MaiML is a workflow description for machines.

#### Article 4. Separate structure from semantics.

Petri Net represents structure, while Template represents semantics. By separating the two, a workflow becomes reusable both mathematically and scientifically.

#### Article 5. Separate design from execution.

Record design (Petri Net) and execution (XES) separately. Research becomes reproducible only when both the blueprint and the execution history are available.

#### Article 6. Preserve the purity of abstraction.

A workflow retains only reusable concepts, while specific instruments, people, and dates and times are kept separate. Purity is what creates reusability and prevents data destruction.

#### Article 7. Guarantee independent availability.

Research must be understandable and reproducible from its description itself, without strong dependence on the particular instrument originally used or on particular dedicated software.

#### Article 8. Generalization is the means of inheritance.

Extract structure from individual phenomena, generalize it, and pass it on to the next generation. Structuring is not the goal; it is a means of generalization.

#### Article 9. Humans and AI share and learn workflows.

AI can learn not only from digitized data, but also from digitized knowledge-generation processes themselves. Workflows become a common language through which humans and machines learn together.

#### Article 10. Design the specification to be minimal and loosely coupled to operations.

MaiML defines only structure, identification, and relationships. Search, access control, and semantic interpretation are delegated to external systems that interoperate as an ecosystem. MaiML defines the framework and relationships of data, while leaving the content itself to external resources.

#### Creed

We believe that the world has structures that can be understood.

The use of measurement instruments, programming, and MaiML can all be regarded as part of the endeavor to discover, generalize, and pass on structure.

We position MaiML as a language that translates the knowledge-generation process of research into a form that humans and AI can share and pass on.

These are the MaiML Design Principles.

<a id="sec-4"></a>
## 4  Rationale for the principles

### 4.1  Separating structure from semantics (Article 4)

A research process can be decomposed into operations (transitions) and states (places), and their ordering, branching, and dependency can be described purely mathematically as a Petri net. The Petri net says nothing about meaning; meaning is given by Templates, which attach scientific semantics such as "SEM observation" or "measurement condition" to each structural node. Separating structure from semantics lets the same structure be reused across procedures in different fields, and the same semantic system be applied to different structures. That a workflow becomes reusable both mathematically and scientifically is a consequence of this separation.

### 4.2  Separating design from execution (Article 5)

The Petri net represents the design (plan) of research, not its execution. Execution is recorded as an event log based on the concepts of XES, the international standard for process mining: state transitions such as start, complete, and suspend, with their times and performers. Only when both the blueprint and the execution history are available can research be reproduced by a third party. Keeping results (Data) and execution evidence (EventLog) separate prevents the static structure of results from mixing with the dynamic history of execution.

### 4.3  The purity of abstraction (Article 6)

A workflow describes the concept "observation by SEM" but not a specific model name, person, or date; such concrete information is separated into the identification and provenance layer. This purity is not an aesthetic preference but a condition of reusability: a workflow contaminated with a model name loses its value the moment that model disappears. Preserving purity keeps the workflow open to future changes of subject and instrument.

### 4.4  Independent availability (Article 7)

When the three elements — design (Protocol), results (Data), and execution (EventLog) — are present, research can be understood and reproduced from the description itself, without strong dependence on the original instrument or dedicated software. This is independent availability, the goal of the design. If any of the three is missing, reproduction regresses into dependence on instruments or memory.

### 4.5  Minimal specification, loose coupling (Article 10)

MaiML defines the frame of data — structure, identification, relationships, and generic containers — and does not define the scientific meaning of the data or their physical representation. Meaning is delegated to external vocabularies and ontologies; raw data remain in existing formats such as TIFF and CSV, referenced and connected through three aspects: location (URI), identity (hash), and interpretation (format). Search, access control, key management, and retention governance are the responsibility of external systems and operation. As a consequence of this loose coupling, MaiML functions as a data catalog that binds heterogeneous data around workflows — but the binding subject is always the workflow, and the catalog function is its by-product.

<a id="sec-5"></a>
## 5  From principles to implementation: mapping to the structure of MaiML

A MaiML document consists of four layers: document, which consolidates identification, integrity, and responsibility; protocol, which represents the design; data, which represents the measured results; and eventLog, which represents the execution history. Table 1 maps the ten articles to the structures that realize them, providing traceability from the design principles to the specification.

**Table 1  Mapping between the design principles and the structure of MaiML**

| Principle | Design consequence | Realization in MaiML |
| --- | --- | --- |
| Articles 1–3 (workflow-centric; assetization) | The design target is the research workflow, not the data | The protocol layer is the core; workflows are described machine-readably |
| Article 4 (structure vs. semantics) | Mathematical structure and scientific meaning are carried by different elements | The Petri net (place, transition, arc) carries structure; Templates (materialTemplate, conditionTemplate, resultTemplate, instruction) carry semantics |
| Article 5 (design vs. execution) | Blueprint and execution history are recorded in separate layers | protocol (design) and eventLog (log, trace, event based on XES concepts) are separated; results reside in data |
| Article 6 (purity of abstraction) | Concrete instruments, people, and dates are excluded from the workflow | Models, people, organizations, and dates go to the document layer (creator, vendor, owner, date); execution times go to the eventLog layer |
| Article 7 (independent availability) | Understanding and reproduction from the description itself | protocol, data, and eventLog can be held in a single XML document |
| Article 8 (generalization as inheritance) | Two tiers: templates and instances | Template/Instance separation and references (ref attributes, templateRef, instanceRef) |
| Article 9 (humans and AI share and learn) | Contextualized, typed, machine-readable data | The type system (xsi:type), units, and structured execution histories make the description learnable |
| Article 10 (minimal specification, loose coupling) | Define only the frame of data; delegate the content | External references via insertion (uri, hash, format); identification and provenance via UUID, chain, and parent; search and access control delegated externally |

NOTE  The normative content of each realization (multiplicities, types, conformance conditions) is defined by JIS K 0200 and the MaiML schema. This table shows the correspondence only.

<a id="sec-6"></a>
## 6  Sharing and learning by humans and AI

Descriptions that follow these principles have a strong affinity with data science and AI. First, because samples, conditions, operations, and provenance are recorded in structured form alongside result values, the data are contextualized, typed, and machine-readable — training data with high comparability, reproducibility, and explainability. Second, because structure and semantics, and design and execution, are recorded separately, AI can learn not only from data but from the knowledge-generation process itself — the Workflow Pattern. This becomes a foundation for autonomous measurement, automated experimentation, and AI-proposed workflows.

By extracting common structure from individual workflows, abstracting it into Workflow Patterns, and accumulating these in a Workflow Library, research methods are reused across organizations and generations. Just as Design Patterns in software engineering turned design knowledge into assets, Workflow Patterns turn research methods into assets. The workflow becomes a common language through which humans and machines learn together.

<a id="sec-7"></a>
## 7  Positioning and limitations

This paper states design principles; it is not a normative document. Where a principle and the specification conflict, the specification (JIS K 0200 and the MaiML schema) always prevails. This paper also does not address operational design — search, authentication, authorization, key management, or retention governance — which belongs to operational guidelines and external systems (Article 10). The principles may apply beyond measurement and analysis, but their generalization — the systematization of Workflow Engineering — remains future work.

<a id="sec-8"></a>
## 8  Conclusion

Research cannot be inherited through data alone. Only by abstracting the workflow and structuring it while preserving its purity does research become inheritable as a knowledge asset. The structures of MaiML — the four-layer composition, the Petri net and Templates, the execution history based on XES concepts, and external references via insertion — are all consequences of the ten articles presented here. We believe that the world has structures that can be understood. MaiML is a language for finding such structure, generalizing it, and passing it on.

<a id="references"></a>
## References

[1] JIS K 0200:2024, Measurement analysis data format (MaiML). Japanese Standards Association.

[2] Murata, T. (1989). Petri Nets: Properties, Analysis and Applications. Proceedings of the IEEE, 77(4), 541-580.

[3] IEEE Std 1849-2023, IEEE Standard for eXtensible Event Stream (XES) for Achieving Interoperability in Event Logs and Event Streams.

[4] Wilkinson, M. D., et al. (2016). The FAIR Guiding Principles for scientific data management and stewardship. Scientific Data, 3, 160018.

[5] Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). Design Patterns: Elements of Reusable Object-Oriented Software. Addison-Wesley.

[6] W3C, Extensible Markup Language (XML) 1.0 (Fifth Edition), 2008.

---

Generation information: source `MaiML_Manifesto_Paper_English_v1.0.0.docx`, SHA-256 `898a2f3194505703176e89d4640a29ceea8d406d046d7a56410466e1162f7f53`.

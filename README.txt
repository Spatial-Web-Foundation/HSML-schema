HSML Schema - Hyperspace Modeling Language
==========================================

Version: 0.2
Date: September 1, 2025
Creator: Stephane Fellah (Spatial Web Foundation)

OVERVIEW
--------
The Hyperspace Modeling Language (HSML) is a semantic framework for modeling 
spatial web concepts, activities, agents, governance, and communication within 
distributed systems. This repository contains the complete HSML ontology 
specification in OWL/RDF format with SHACL validation shapes.

PROJECT STRUCTURE
-----------------
This directory contains the complete HSML schema specification:

Core Files:
- hsml.ttl                    # Master ontology that imports all modules
- hsml-context.jsonld         # JSON-LD context for short name mapping

Core Module:
- core.ttl                    # Foundational concepts (Entity, Domain, etc.)
- core-shapes.ttl             # SHACL validation shapes for core module

Activity Module:
- activity.ttl                # Activity and workflow definitions
- activity-shapes.ttl         # SHACL validation shapes for activities

Agent Module:
- agent.ttl                   # Agent, Person, Organization, Goal definitions
- agent-shapes.ttl            # SHACL validation shapes for agents

Communication Module:
- comm.ttl                    # Channel and Message definitions
- comm-shapes.ttl             # SHACL validation shapes for communication

Governance Module:
- governance.ttl              # Contract, Credential, Policy, Norm definitions
- governance-shapes.ttl       # SHACL validation shapes for governance

Hyperspace Module:
- hyperspace.ttl              # Core hyperspace concepts
- hyperspace-shapes.ttl       # SHACL validation shapes for hyperspaces
- hyperspace/metric.ttl       # Metric space submodule
- hyperspace/metric-shapes.ttl # SHACL validation shapes for metrics

Documentation:
- hsml-implementation.pdf     # Complete HSML implementation specification

ONTOLOGY MODULES
----------------

1. CORE MODULE (core.ttl)
   - Entity: Abstract root class for all HSML entities
   - Domain: Foundational entity representing spheres of knowledge/influence
   - SpatialFeature: Location-bound or geometry-bearing elements
   - Thing: Bounded, passive items without agency
   - Concept: Abstract ideas or categories
   - Condition: Logical conditions for validation
   - Participation: Entity involvement in specific roles
   - Role: Function or position within participation

2. ACTIVITY MODULE (activity.ttl)
   - Activity: Concrete instances of work being performed
   - ActivitySchema: Reusable templates for activities
   - ActivityStep: Individual steps within composite activities
   - Variable: Data containers for activity inputs/outputs
   - VariableBinding: Concrete values for variables
   - DataLink: Data flow connections between steps

3. AGENT MODULE (agent.ttl)
   - Agent: Autonomous entities capable of activities
   - Person: Human agents with self-sovereign identity
   - Organization: Collective groups under common governance
   - Goal: States or objectives agents aim to achieve

4. COMMUNICATION MODULE (comm.ttl)
   - Channel: Contextual groupings for transient communications
   - Message: Semantic records of communicative artifacts
   - Properties for message routing, correlation, and content

5. GOVERNANCE MODULE (governance.ttl)
   - Contract: Formal agreements between parties
   - Credential: Verifiable claims about entities
   - Policy: Declarative rules and constraints
   - Norm: Atomic deontic rules (obligations, permissions, prohibitions)

6. HYPERSPACE MODULE (hyperspace.ttl)
   - Hyperspace: Domain-attached spatial structures
   - Path: First-class composed paths
   - Operation: Declarative operations over hyperspaces
   - Metric submodule for quantitative reasoning

USAGE
-----

1. Loading the Complete Schema:
   Load hsml.ttl to get the complete HSML model with all modules.

2. JSON-LD Context:
   Use hsml-context.jsonld for JSON-LD serialization with short names:
   {
     "@context": "hsml-context.jsonld",
     "@type": "Activity",
     "name": "Sample Activity",
     "performedBy": { "@id": "agent:123" }
   }

3. SHACL Validation:
   Each module includes SHACL shapes for validation:
   - NodeShapes define constraints for classes
   - PropertyShapes define constraints for properties
   - Cardinality, datatypes, and value constraints are enforced

4. Module-Specific Loading:
   Load individual modules for specific use cases:
   - core.ttl for foundational concepts
   - activity.ttl for workflow modeling
   - agent.ttl for agent-based systems
   - comm.ttl for communication modeling
   - governance.ttl for policy and credential management
   - hyperspace.ttl for spatial reasoning

NAMESPACES
----------
- core: https://www.spatialwebfoundation.org/ns/hsml/core#
- act: https://www.spatialwebfoundation.org/ns/hsml/activity#
- agt: https://www.spatialwebfoundation.org/ns/hsml/agent#
- comm: https://www.spatialwebfoundation.org/ns/hsml/comm#
- gov: https://www.spatialwebfoundation.org/ns/hsml/governance#
- hspace: https://www.spatialwebfoundation.org/ns/hsml/hyperspace#
- metric: https://www.spatialwebfoundation.org/ns/hsml/hyperspace/metric#

VERSION INFORMATION
-------------------
- Version: 0.2
- Version IRI: https://www.spatialwebfoundation.org/ns/hsml/0.2/
- Created: 2025-09-01
- Creator: Stephane Fellah
- Publisher: Spatial Web Foundation

DEPENDENCIES
------------
- OWL 2 (Web Ontology Language)
- RDF (Resource Description Framework)
- SHACL (Shapes Constraint Language)
- Dublin Core Terms (dct:)
- Schema.org (schema:)
- Verifiable Credentials (vc:)
- PROV-O (prov:)
- SKOS (skos:)

VALIDATION
----------
All ontology files include SHACL shapes for validation:
- Cardinality constraints (minCount, maxCount)
- Datatype validation
- Class membership validation
- Property value constraints
- Custom validation rules

EXAMPLES
--------
See the hsml-implementation.pdf for detailed examples and use cases.

CONTACT
-------
For questions or contributions:
- Creator: Stephane Fellah
- Organization: Spatial Web Foundation
- Website: https://www.spatialwebfoundation.org/
- Email: info@spatialwebfoundation.org

LICENSE
-------
This work is provided by the Spatial Web Foundation under appropriate licensing terms.
Please refer to the organization for licensing details.

CHANGELOG
---------
Version 0.2 (2025-09-01):
- Complete ontology specification with all modules
- SHACL validation shapes for all classes and properties
- JSON-LD context for short name mapping
- Comprehensive governance and credential support
- Metric space submodule for quantitative reasoning
- Updated metadata and version information

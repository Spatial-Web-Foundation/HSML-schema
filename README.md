# HSML (Hyperspace Modeling Language)

This repository contains the formal schema definitions for the Hyperspace Modeling Language (HSML), a comprehensive ontology for modeling spatial entities,relationships and interactions in the Spatial Web.

## Overview

HSML provides a structured way to model and represent spatial relationships, activities, and interactions between entities in a spatial context. It combines concepts from hypergraph theory, spatial modeling, and semantic web technologies to create a rich framework for spatial data representation.

## Repository Structure

The repository is organized into several key directories and files:

### Core Schema Files

- `hsml-combined.shacl.jsonld` - Combined SHACL shapes in JSON-LD format
- `hsml-combined.shacl.ttl` - Combined SHACL shapes in Turtle format
- `hsml-combined.owl.ttl` - Combined OWL ontology in Turtle format
- `hsml.context.jsonld` - JSON-LD context definitions
- `hsml.owl.ttl` - Base OWL ontology
- `hsml.shacl.ttl` - Base SHACL shapes

### Domain-Specific Directories (for modular development)

- `activity/` - Activity-related schema definitions
- `agent/` - Agent-related schema definitions
- `channel/` - Channel-related schema definitions
- `contract/` - Contract-related schema definitions
- `core/` - Core schema definitions
- `credential/` - Credential-related schema definitions
- `domain/` - Domain-related schema definitions
- `hyperspace/` - Hyperspace-related schema definitions
- `thing/` - Thing-related schema definitions

## Key Concepts

The schema defines several important concepts:

1. **Entity** - Base class for all spatial entities
2. **Domain** - Represents a spatial domain with identity and credentials
3. **Activity** - Represents actions or processes that occur in space
4. **Agent** - Represents entities that can perform activities
5. **Channel** - Represents communication channels between entities
6. **Contract** - Represents agreements between entities
7. **Hyperspace** - Represents generalized spatial concepts

## Usage

The schema can be used in various formats:

- JSON-LD for web applications
- Turtle (TTL) for RDF applications
- SHACL shapes for data validation

### Example Usage

```json
{
  "@context": "https://www.spatialwebfoundation.org/ns/hsml#",
  "@type": "Thing",
  "name": "Light Bulb 1",
  "swid": "did:swid:hotel123:smartroom1:lightbulb1"
}
```

## Dependencies

The schema uses several standard ontologies:

- SHACL (Shapes Constraint Language)
- RDFS (Resource Description Framework Schema)
- OWL (Web Ontology Language)
- JSON-LD format



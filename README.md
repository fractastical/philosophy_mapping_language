# Philosophical Mapping Language (PML)

A structured format for mapping relationships between philosophical texts, translations, and concepts across cultural and intellectual traditions.

## Overview

PML enables systematic exploration of how philosophical ideas resonate across different traditions, with support for both single-source mappings and multi-AI consensus building. Originally developed for mapping Dao De Jing translations to Western philosophers, it's designed to be extensible to any cross-cultural philosophical analysis.

## Features

### Core Capabilities
- **Structured Mappings**: YAML-based format linking texts, translations, and philosophical concepts
- **Quantified Relationships**: Numerical alignment scores with confidence intervals
- **Evidence Linking**: Direct citations connecting source and target concepts
- **Thematic Bridging**: Identification of conceptual connections across traditions

### Multi-AI Support (MA-PML)
- **Consensus Building**: Aggregate insights from multiple AI systems
- **Disagreement Analysis**: Systematic identification of interpretive differences  
- **Confidence Weighting**: Bayesian averaging with uncertainty quantification
- **Bias Detection**: Meta-analysis of systematic preferences across AI models

## Quick Start

### Basic Mapping Format

```yaml
relationships:
  - translation:
      translator: "Arthur Waley"
      year: 1934
    resonance:
      philosopher: "Henri Bergson"
      alignment_strength: 0.85
      key_concepts: ["élan vital", "creative evolution", "durée"]
      textual_evidence:
        - source: "DDJ Ch.1 - 'Dao flows everywhere'"
        - target: "Creative Evolution - 'the universe endures'"
```

### Multi-AI Consensus

```yaml
ai_consensus:
  claude:
    alignment_strength: 0.85
    confidence: 0.90
    reasoning: "Waley's flowing translation captures Bergson's temporal dynamics"
  gpt4:
    alignment_strength: 0.78
    confidence: 0.85
    reasoning: "Both emphasize process over static being"
  
consensus_metrics:
  mean_alignment: 0.8125
  agreement_level: "high"
```

## Use Cases

### Academic Research
- **Cross-Cultural Philosophy**: Map concepts between Eastern and Western traditions
- **Translation Studies**: Compare how different translations emphasize different philosophical aspects
- **Comparative Analysis**: Quantify conceptual similarities across philosophical schools

### Educational Applications
- **Teaching Tools**: Interactive exploration of philosophical connections
- **Curriculum Development**: Structured approach to comparative philosophy courses
- **Student Research**: Framework for systematic philosophical comparison

### AI Research
- **Model Comparison**: Evaluate how different AI systems interpret philosophical relationships
- **Bias Analysis**: Detect systematic preferences in AI philosophical reasoning
- **Consensus Building**: Aggregate multiple AI perspectives for robust analysis

## Schema Structure

### Primary Elements

| Element | Description | Required |
|---------|-------------|----------|
| `translation` | Source text translator and metadata | Yes |
| `resonance` | Target philosopher and alignment data | Yes |
| `alignment_strength` | Numerical similarity score (0.0-1.0) | Yes |
| `textual_evidence` | Supporting citations | For strength > 0.7 |
| `thematic_bridges` | Conceptual connection types | Minimum 2 |

### Advanced Features

- **Conceptual Clusters**: Group related concepts across multiple texts
- **Cross-Mappings**: Many-to-many philosopher relationships  
- **Validation Rules**: Quality assurance and consistency checking
- **Export Formats**: LaTeX, JSON, SQL, Markdown outputs

## Installation & Usage

### Prerequisites
- YAML parser (PyYAML for Python, js-yaml for JavaScript)
- Optional: Visualization libraries (D3.js, matplotlib, etc.)

### Basic Usage

```python
import yaml
from pml_validator import validate_mapping

# Load PML file
with open('ddj_mappings.pml', 'r') as f:
    mapping = yaml.safe_load(f)

# Validate structure
validation_result = validate_mapping(mapping)

# Query mappings
high_confidence = [r for r in mapping['relationships'] 
                  if r['resonance']['alignment_strength'] > 0.8]
```

### Multi-AI Processing

```python
from pml_consensus import merge_ai_mappings, calculate_consensus

# Merge multiple AI-generated mappings
consensus_mapping = merge_ai_mappings([
    'claude_mapping.pml',
    'gpt4_mapping.pml', 
    'gemini_mapping.pml'
])

# Analyze agreement patterns
agreement_analysis = calculate_consensus(consensus_mapping)
```

## Examples

### Current Mappings
- **Dao De Jing → Western Philosophy**: 7 major translations mapped to corresponding philosophical traditions
- **Alignment Range**: 0.75-0.90 across all mappings
- **High Consensus**: Waley-Bergson, Lau-Whitehead connections
- **Areas of Debate**: Mitchell-Heidegger existential interpretations

### Query Examples
```yaml
# Find strong consensus mappings
query: "alignment_strength > 0.8 AND agreement_level = 'high'"

# Compare AI interpretations  
query: "philosopher = 'Heidegger' GROUP BY ai_source"

# Explore concept clusters
query: "concept_cluster = 'emptiness_void' EXPAND western_concepts"
```

## Visualization

### Display Modes
- **Consensus View**: Weighted averages with confidence intervals
- **Comparative Matrix**: Side-by-side AI analysis
- **Network Graph**: Philosopher-concept relationship mapping
- **Uncertainty Heatmap**: Confidence visualization across mappings

### Export Formats
- **Academic**: LaTeX tables with citations
- **Interactive**: JSON for web applications  
- **Educational**: Simplified markdown for teaching
- **Research**: Normalized SQL for analysis

## Contributing

### Adding New Mappings
1. Follow the PML schema structure
2. Include textual evidence for alignment_strength > 0.7
3. Validate using provided tools
4. Submit with reasoning documentation

### Extending to New Domains
- Buddhist-Analytic Philosophy
- Islamic-Continental Philosophy  
- African-Pragmatist Philosophy
- Indigenous-Phenomenological Philosophy

### Quality Guidelines
- **Minimum 3 AI sources** for consensus mappings
- **Primary source citations** required for high-strength alignments
- **Peer review** for systematic extensions
- **Bias testing** across cultural perspectives

## Technical Specifications

### Validation Rules
```yaml
validation_rules:
  - alignment_strength: "0.0-1.0 scale"
  - textual_evidence: "required for strength > 0.7"  
  - thematic_bridges: "minimum 2 required"
  - ai_consensus: "minimum 3 sources for MA-PML"
```

### Confidence Calibration
- **Bayesian Averaging**: Weight by AI confidence scores
- **Cross-Validation**: Monthly recalibration against expert judgments
- **Uncertainty Quantification**: Standard deviation thresholds for agreement levels

## License

MIT License - see LICENSE file for details.

## Citation

```bibtex
@software{philosophical_mapping_language,
  title={Philosophical Mapping Language: A Structured Format for Cross-Cultural Philosophical Analysis},
  author={Claude and Human Collaborator},
  year={2025},
  url={https://github.com/philosophy/pml}
}
```

## Support

- **Documentation**: Full specification at `/docs`
- **Examples**: Sample mappings in `/examples`
- **Tools**: Validation and visualization utilities in `/tools`
- **Community**: Discussion forum at [philosophy-mapping.org](https://philosophy-mapping.org)

---

*PML enables systematic exploration of how wisdom traditions speak to each other across cultures and centuries.*

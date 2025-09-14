# Scientific Knowledge Contribution (SKC) Dataset

## 📖 Overview

The exponential growth of scientific literature has reshaped the contemporary research landscape, creating an urgent need for novel computational methods to enable knowledge navigation and theory construction. With annual academic output exceeding 2.5 million papers, traditional bibliometric analyses struggle to capture the multidimensional knowledge contributions that emerging research makes to scientific progress.

This dataset proposes a methodological shift from subjective citation intent analysis to objective knowledge contribution identification—moving from exploring "why authors cite" to identifying "what knowledge the cited work contributes." We have curated a high-quality knowledge contribution classification dataset containing 2,000 annotated samples from 802,202 citation instances collected from the ACL Anthology.

## 🎯 Research Motivation

Traditional function-oriented citation classification faces fundamental limitations:
- **Subjectivity Issues**: Focus on authors' subjective motivations rather than objective contributions of cited works
- **Decontextualization Problems**: Disconnect from real citation contexts
- **Scale Limitations**: Mainstream datasets (e.g., ACL-ARC, SciCite) are too small
- **Insufficient Granularity**: Lack of fine-grained contribution type categorization

## 📊 SKC Classification Framework

Our proposed Scientific Knowledge Contribution (SKC) classification framework systematically divides citation contributions into five major categories:

| Category | Description | Example |
|----------|-------------|---------|
| **Method Technology** | Citation where the citing paper directly uses, implements, improves, or extends methods, techniques, algorithms, models, systems, parsers, or evaluation metrics from the cited paper. Must be used by "we" (the authors). | "We adopt the BERT model [CITATION] as our encoder" |
| **Resource Tool** | Citation where the citing paper uses datasets, corpora, or explicitly labeled toolkits/toolboxes created by the cited paper. Must be directly used by "we" (the authors). | "We first extracted texts from DeReKo corpus [CITATION]" |
| **Theory** | Citation where the citing paper adopts theoretical concepts, definitions, frameworks, or paradigms from the cited paper to build their theoretical foundation. Focuses on "what is" or "how to understand". | "We use the theoretical rules proposed by [CITATION] to help us better establish each category" |
| **Evidential Finding** | Citation providing specific, verifiable empirical findings (experimental results, performance data, observed phenomena) used for: 1) direct comparison, 2) justifying decisions, or 3) stating empirical facts. | "[CITATION] showed RNNs fail on long sequences, so we use Transformers" |
| **Background** | Citation providing necessary understanding foundation or positioning research within the field through: 1) developmental course (vertical timeline) or 2) research landscape (horizontal snapshot). | "Multimodal sentiment analysis has become a research hotspot [CITATION1] [CITATION2][CITATION3]" |

## 🔧 Dataset Construction

### Data Source
- **Corpus**: ACL Anthology (1979-2021)
- **Raw Citations**: 802,202 instances
- **Annotated Samples**: 2,000 high-quality instances
- **Languages**: Primarily English academic papers

### Annotation Process
1. **Expert Annotation**: Domain experts with NLP background
2. **Quality Control**: Multi-round validation and consistency checks
3. **Inter-annotator Agreement**: Cohen's κ > 0.75
4. **Guideline Development**: Comprehensive annotation guidelines


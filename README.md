# BMAD Business Planning Module

Professional business planning and process mapping agents for strategic documentation and organizational clarity.

## 🎯 Overview

This BMAD module provides two specialized agents designed to help businesses and agencies create comprehensive strategic documentation:

- **Business Plan Architect** - Creates structured business plans using proven frameworks
- **Process Mapper** - Documents and optimizes business processes systematically

## ✨ Features

### Business Plan Architect
- 10-tier business planning methodology
- Pulls scattered ideas into structured documentation
- Uses frameworks like Business Model Canvas, Blue Ocean Strategy, Jobs-to-be-Done
- Living document approach - start somewhere, refine as you go
- Prioritizes based on current business stage
- Integrates existing materials and identifies gaps

### Process Mapper
- Systematic process documentation
- Visual and written process mapping
- Bottleneck identification
- Optimization recommendations
- Multiple process categories (operational, customer, financial, etc.)

## 📦 Installation

### Prerequisites
- BMAD Method already installed in your project
- Node.js 16+ and npm

### Quick Install (Once Published)
```bash
npx bmad-method@alpha install bmad-business-planning
```

### Manual Installation (Current)

1. Clone this repository:
```bash
cd ~/workspace
git clone https://github.com/MatthewKerns/bmad-business-planning-module.git
```

2. Copy the module files to your BMAD installation:
```bash
# Navigate to your project with BMAD installed
cd /path/to/your/project

# Create the business-planning directory in _bmad
mkdir -p _bmad/business-planning

# Copy the module files
cp -r ~/workspace/agency-operations/bmad-business-planning-module/src/* _bmad/business-planning/
```

3. Update your BMAD manifests:

Add to `_bmad/_config/agent-manifest.csv`:
```csv
business-planning,business-plan-architect,Business Plan Architect,Creates comprehensive business plans
business-planning,process-mapper,Process Mapper,Maps business processes systematically
```

Add to `_bmad/_config/workflow-manifest.csv`:
```csv
business-planning,business-plan,Business Plan Creation,10-tier strategic planning
business-planning,process-mapping,Process Mapping,Systematic process documentation
```

4. Copy the configuration files:
```bash
cp _bmad/business-planning/config/*.yaml _bmad/_config/agents/
```

## 🚀 Usage

### Using the Business Plan Architect

1. **Via Skill command:**
```
/bmad:business-planning:agents:business-plan-architect
```

2. **Via Party Mode:**
Include in your party configuration to have the architect participate in strategic discussions.

3. **Direct workflow invocation:**
```
/bmad:business-planning:workflows:business-plan
```

### Using the Process Mapper

1. **Via Skill command:**
```
/bmad:business-planning:agents:process-mapper
```

2. **Via workflow:**
```
/bmad:business-planning:workflows:process-mapping
```

## 📖 Example Use Cases

### Creating a Business Plan
Perfect for:
- New ventures needing comprehensive planning
- Existing businesses seeking strategic focus
- Teams needing alignment documentation
- Businesses preparing for investment

The architect will guide you through:
1. Business context and existing materials assessment
2. Mission and Vision (Messaging Foundation)
3. Core Values and Operating Principles
4. Business Model and Revenue Strategy
5. Target Market and Customer Definition
6. Competitive Analysis
7. Product/Service Portfolio
8. Go-to-Market Strategy
9. Operations Plan
10. Financial Projections

### Mapping Business Processes
Ideal for:
- Documenting standard operating procedures
- Identifying workflow bottlenecks
- Onboarding new team members
- Process optimization projects
- Quality management systems

The mapper will help you document:
- Process inputs and outputs
- Step-by-step workflows
- Decision points and branches
- Roles and responsibilities
- Tools and resources needed
- Performance metrics

## 🏗️ Module Structure

```
bmad-business-planning-module/
├── src/
│   ├── module.yaml                    # Module configuration
│   ├── agents/
│   │   ├── business-plan-architect.md # Agent definition
│   │   └── process-mapper.md          # Agent definition
│   ├── workflows/
│   │   ├── business-plan/
│   │   │   ├── instructions.md        # Workflow instructions
│   │   │   ├── template.md            # Output template
│   │   │   ├── workflow.yaml          # Workflow config
│   │   │   └── business-plan-frameworks.csv
│   │   └── process-mapping/
│   │       ├── instructions.md
│   │       ├── template.md
│   │       ├── workflow.yaml
│   │       └── process-categories.csv
│   └── config/
│       ├── cis-business-plan-architect.customize.yaml
│       └── cis-process-mapper.customize.yaml
├── package.json
└── README.md
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Additional business frameworks
- New process mapping methodologies
- Bug fixes and improvements
- Documentation enhancements

## 📄 License

MIT License - See LICENSE file for details

## 🆘 Support

For issues or questions:
- Open an issue in this repository
- Contact the AI Agency Development OS Team

## 🔄 Version History

### v1.0.0 (2024-02-05)
- Initial release
- Business Plan Architect agent
- Process Mapper agent
- Complete workflow implementations
- Framework CSV files for guided planning

---

Built with ❤️ for the BMAD community by the AI Agency Development OS Team
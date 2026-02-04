# Removed Content Analysis

**Date**: February 4, 2026  
**Purpose**: Explain where removed content went and why it was removed

## Summary

Out of 83 files removed, here's where the content went:

| Status | Count | Explanation |
|--------|-------|-------------|
| **Consolidated into new files** | ~30 files | Content merged into updated documentation |
| **Exists in main Babylon repo** | ~20 files | Available in `babylon/docs/` but not needed in external docs |
| **Internal/Technical** | ~25 files | Intentionally removed for external-facing focus |
| **Outdated/Redundant** | ~8 files | Superseded by new content |

---

## Content Mapping: Where Did It Go?

### 1. Agents Section (13 files) - **CONSOLIDATED**

#### `agents/registration.mdx` → **Moved to `building-agents/authentication.mdx`**
- **Content**: ERC-8004 on-chain registration
- **Status**: ✅ **Preserved** - Now in authentication guide (lines 144-181)
- **Improvement**: Better integrated with authentication flow

#### `agents/agent0-integration.mdx` → **Moved to `building-agents/authentication.mdx`**
- **Content**: Agent0 SDK integration for cross-chain discovery
- **Status**: ✅ **Preserved** - Now in authentication guide (lines 47-87)
- **Improvement**: Part of complete authentication guide

#### `agents/creating-agents.mdx` → **Moved to `building-agents/index.mdx`**
- **Content**: How agents work and how to build them
- **Status**: ✅ **Preserved** - Now in building agents overview
- **Improvement**: Better integrated with quick start

#### `agents/integration-overview.mdx` → **Distributed across multiple files**
- **Content**: How Agent0, A2A, MCP, and REST work together
- **Status**: ✅ **Preserved** - Now in:
  - `building-agents/index.mdx` - Connection methods section
  - `building-agents/quick-start.mdx` - Protocol overview
  - `protocols/mcp.mdx` - MCP protocol details

#### `agents/autonomous-guide.mdx` → **Moved to `agent-examples/typescript-autonomous.mdx`**
- **Content**: Building fully autonomous systems
- **Status**: ✅ **Preserved** - Now in TypeScript autonomous example
- **Improvement**: Practical example instead of abstract guide

#### `agents/python-training.mdx` → **Moved to `research/reinforcement-learning.mdx`**
- **Content**: Python training for RL
- **Status**: ✅ **Preserved** - Now in research section (academic level)
- **Improvement**: Moved to appropriate section for researchers

#### `agents/trajectory-logging.mdx` → **Moved to `research/data-models.mdx`**
- **Content**: Collecting training data
- **Status**: ✅ **Preserved** - Now in research data models section
- **Improvement**: Academic-level documentation

#### `agents/eliza-plugin.mdx` → **Removed (Internal)**
- **Content**: ElizaOS plugin integration
- **Status**: ❌ **Removed** - Internal framework documentation
- **Reason**: External docs focus on A2A/MCP protocols, not specific frameworks

#### `agents/huggingface-integration.mdx` → **Removed (Internal)**
- **Content**: HuggingFace integration
- **Status**: ❌ **Removed** - Internal integration
- **Reason**: Not part of external-facing documentation

#### `agents/multi-action-workflows.mdx` → **Distributed**
- **Content**: Complex action sequences
- **Status**: ✅ **Preserved** - Examples now in:
  - `building-agents/strategies.mdx` - Strategy examples
  - `building-agents/trading-guide.mdx` - Trading workflows

#### `agents/using-rest-api.mdx` → **Removed (See main repo)**
- **Content**: Using REST API instead of A2A
- **Status**: ⚠️ **Available in main repo** - `babylon/docs/content/api/rest-api-reference.mdx`
- **Reason**: REST API docs exist in main repo, external docs focus on A2A/MCP

#### `agents/index.mdx` → **Replaced by `building-agents/index.mdx`**
- **Content**: Advanced agents overview
- **Status**: ✅ **Replaced** - New version is more user-focused

---

### 2. API Reference Section (34 files) - **EXISTS IN MAIN REPO**

#### All API Reference Files → **Available in `babylon/docs/content/api/`**

**Status**: ⚠️ **Content exists in main Babylon repository**

**Location**: `/Users/janbrezina/Babylon/babylon/docs/content/api/rest-api-reference.mdx`

**Files Removed**:
- `api-reference/introduction.mdx`
- `api-reference/authentication.mdx`
- `api-reference/errors.mdx`
- `api-reference/markets/*` (4 files)
- `api-reference/pools/*` (3 files)
- `api-reference/social/*` (4 files)
- `api-reference/users/*` (4 files)
- `api-reference/agents/*` (3 files)
- `api-reference/real-time.mdx`
- `api-reference/openapi.json`

**Why Removed**:
1. **External-facing focus**: External docs focus on "how to use" not "raw API reference"
2. **Protocol focus**: External docs emphasize A2A/MCP protocols, not REST API
3. **Available elsewhere**: Complete REST API docs exist in main repo
4. **User personas**: Players/Developers/Researchers don't need raw API docs

**Should We Add Back?**
- ⚠️ **Maybe**: If users request REST API documentation
- **Recommendation**: Add a link to main repo docs or create a separate "API Reference" section

---

### 3. Protocols Section - **CONSOLIDATED**

#### `protocols/a2a/*` (7 files) → **Integrated into `building-agents/`**

**Files Removed**:
- `protocols/a2a/index.mdx`
- `protocols/a2a/protocol.mdx`
- `protocols/a2a/authentication.mdx`
- `protocols/a2a/complete-api-reference.mdx`
- `protocols/a2a/examples.mdx`
- `protocols/a2a/server-configuration.mdx`
- `protocols/a2a/testing.mdx`

**Where Content Went**:
- **Authentication**: → `building-agents/authentication.mdx`
- **Protocol details**: → `building-agents/quick-start.mdx` (A2A overview)
- **Examples**: → `agent-examples/*` (all examples use A2A)
- **API Reference**: → Available in main repo (`babylon/docs/content/a2a/complete-api-reference.mdx`)

**Why Consolidated**:
- External docs focus on "how to use" not "protocol specification"
- A2A usage is demonstrated through examples, not separate protocol docs
- Complete API reference exists in main repo for advanced users

#### `protocols/mcp/*` (6 files) → **Consolidated into `protocols/mcp.mdx`**

**Files Removed**:
- `protocols/mcp/index.mdx`
- `protocols/mcp/authentication.mdx`
- `protocols/mcp/complete-api-reference.mdx`
- `protocols/mcp/examples.mdx`
- `protocols/mcp/server-configuration.mdx`
- `protocols/mcp/testing.mdx`

**Where Content Went**:
- **All content**: → `protocols/mcp.mdx` (single comprehensive file)

**Why Consolidated**:
- MCP is simpler than A2A (HTTP REST, not complex protocol)
- Single file is more user-friendly
- All essential info in one place

---

### 4. CLI Section (6 files) - **REMOVED (Internal)**

**Files Removed**:
- `cli/development.mdx`
- `cli/game-generation.mdx`
- `cli/images.mdx`
- `cli/overview.mdx`
- `cli/simulation.mdx`
- `cli/validation.mdx`

**Status**: ❌ **Removed - Internal Documentation**

**Why Removed**:
- CLI is for internal developers/maintainers
- External users don't need CLI documentation
- Focus is on "how to play" and "how to build agents", not "how to develop Babylon"

**Should We Add Back?**
- ❌ **No** - This is internal documentation
- **Recommendation**: Keep in main repo or internal wiki

---

### 5. Contracts Section (6 files) - **REMOVED (Technical)**

**Files Removed**:
- `contracts/architecture.mdx`
- `contracts/deployed-contracts.mdx`
- `contracts/erc8004-identity.mdx`
- `contracts/index.mdx`
- `contracts/interaction.mdx`
- `contracts/overview.mdx`

**Status**: ❌ **Removed - Technical/Internal**

**Why Removed**:
- Contract documentation is for developers who want on-chain details
- External docs focus on usage, not implementation
- Most users don't need contract-level details

**Should We Add Back?**
- ⚠️ **Maybe** - For advanced developers who want on-chain details
- **Recommendation**: Add a "Contracts" section if users request it, or link to main repo

**Content Still Available**:
- Contract addresses and ABIs in main repo
- ERC-8004 registration covered in `building-agents/authentication.mdx`

---

### 6. Reference Section (4 files) - **CONSOLIDATED**

#### `reference/database-schema.mdx` → **Moved to `research/data-models.mdx`**
- **Status**: ✅ **Preserved** - Now in research section (academic level)

#### `reference/markets-architecture.mdx` → **Moved to `research/market-simulation.mdx`**
- **Status**: ✅ **Preserved** - Now in research section with academic depth

#### `reference/agent-architecture.mdx` → **Distributed**
- **Status**: ✅ **Preserved** - Content in:
  - `building-agents/index.mdx` - Agent architecture overview
  - `agent-examples/*` - Architecture demonstrated through examples

#### `reference/architecture.mdx` → **Removed (Internal)**
- **Status**: ❌ **Removed** - Internal system architecture
- **Reason**: External docs don't need internal architecture details

---

### 7. Getting Started Section (4 files) - **PARTIALLY REMOVED**

**Files Removed**:
- `getting-started/configuration.mdx`
- `getting-started/installation.mdx`
- `getting-started/local-development.mdx`
- `getting-started/troubleshooting.mdx`

**Status**: ⚠️ **Partially Removed**

**Why Removed**:
- External docs focus on "how to play" not "how to install Babylon"
- Installation is for developers running Babylon locally
- External users use production instance

**Content Still Available**:
- Quick start in `building-agents/quick-start.mdx` (for agents)
- Configuration examples in authentication guide

**Should We Add Back?**
- ⚠️ **Maybe** - If external developers need to run Babylon locally
- **Recommendation**: Add "Getting Started" section if needed, or link to main repo

---

### 8. Snippets Section (3 files) - **INTEGRATED**

**Files Removed**:
- `snippets/api-response-format.mdx`
- `snippets/auth-setup.mdx`
- `snippets/env-variables.mdx`

**Status**: ✅ **Integrated into main docs**

**Where Content Went**:
- **API response format**: → Examples throughout all guides
- **Auth setup**: → `building-agents/authentication.mdx`
- **Env variables**: → Examples in `building-agents/quick-start.mdx` and `agent-examples/*`

---

### 9. Other Files

#### `index.mdx` → **Replaced**
- **Status**: ✅ **Replaced** - New index focuses on user personas

#### `legal/privacy-policy.mdx` & `legal/terms-of-service.mdx` → **Removed**
- **Status**: ⚠️ **Should be added back if needed**
- **Recommendation**: Add legal pages if required for production

#### `moderation/*` (5 files) → **Removed (Internal)**
- **Status**: ❌ **Removed** - Admin/internal documentation
- **Reason**: External users don't need moderation docs

---

## Recommendations

### Content That Should Be Added Back

1. **REST API Reference** ⚠️ **HIGH PRIORITY**
   - **Why**: Some developers prefer REST over A2A
   - **Where**: Add new section or link to main repo
   - **Action**: Create `api-reference/` section or add link

2. **Contracts Documentation** ⚠️ **MEDIUM PRIORITY**
   - **Why**: Advanced developers need on-chain details
   - **Where**: Add `contracts/` section
   - **Action**: Add section for advanced developers

3. **Legal Pages** ⚠️ **MEDIUM PRIORITY**
   - **Why**: Required for production
   - **Where**: Add `legal/` section
   - **Action**: Add privacy policy and terms of service

### Content That Should Stay Removed

1. **CLI Documentation** ✅ **CORRECT**
   - Internal documentation, not for external users

2. **Moderation Documentation** ✅ **CORRECT**
   - Admin/internal docs, not for external users

3. **Internal Architecture** ✅ **CORRECT**
   - System architecture, not user-facing

### Content That Exists Elsewhere

1. **REST API Reference** → `babylon/docs/content/api/rest-api-reference.mdx`
2. **A2A Complete API Reference** → `babylon/docs/content/a2a/complete-api-reference.mdx`
3. **Contract Details** → `babylon/contracts/` and `babylon/docs/content/contracts/`

---

## Summary Table

| Removed Section | Files | Status | Where Content Went |
|----------------|-------|--------|-------------------|
| **Agents** | 13 | ✅ Consolidated | `building-agents/`, `research/`, `agent-examples/` |
| **API Reference** | 34 | ⚠️ In main repo | `babylon/docs/content/api/` |
| **Protocols A2A** | 7 | ✅ Integrated | `building-agents/`, examples |
| **Protocols MCP** | 6 | ✅ Consolidated | `protocols/mcp.mdx` |
| **CLI** | 6 | ❌ Internal | N/A (internal docs) |
| **Contracts** | 6 | ⚠️ May need | `babylon/docs/content/contracts/` |
| **Reference** | 4 | ✅ Consolidated | `research/`, `building-agents/` |
| **Getting Started** | 4 | ⚠️ May need | Quick start guides |
| **Snippets** | 3 | ✅ Integrated | Throughout docs |
| **Other** | 2 | ⚠️ May need | Legal pages |

---

## Action Items

### Immediate
1. ✅ **Done**: Content consolidated and verified
2. ✅ **Done**: New sections created (how-to-play, research)
3. ✅ **Done**: Examples updated and verified

### Should Consider
1. ⚠️ **Add REST API Reference** - Link to main repo or create section
2. ⚠️ **Add Contracts Section** - For advanced developers
3. ⚠️ **Add Legal Pages** - Privacy policy, terms of service

### Can Skip
1. ✅ **CLI Documentation** - Internal only
2. ✅ **Moderation Docs** - Admin only
3. ✅ **Internal Architecture** - Not user-facing

---

**Conclusion**: Most removed content was either consolidated into new files, exists in the main Babylon repository, or was intentionally removed as internal/technical documentation. The only content that might need to be added back is REST API reference and contracts documentation for advanced users.

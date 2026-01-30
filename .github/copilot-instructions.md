# Copilot Instructions for EmbyIconThemes

## Project Overview

**EmbyIconThemes** is a curated collection of PNG icon/theme images for Emby, a media server platform. The repository stores category and genre-specific images used in the Emby UI to represent different content types (movies, TV shows, music, podcasts, etc.).

### Key Characteristics

- **Type**: Asset/Theme repository (image collection)
- **Primary Content**: ~60 PNG image files representing Emby content categories
- **Categories**: Range from standard genres (Drama, Comedy, Action) to specific themes (LGBTQ+ content, politics, nature, sports)
- **Git Workflow**: Simple commit history - files added via uploads, minimal branching
- **Scale**: Binary files (~2-4MB per PNG), no source code

## Repository Structure

```
/
├── *.png                 # Individual theme/icon images (60+ files)
├── .git/                 # Git repository metadata
└── .github/              # GitHub-specific files (workflows, docs)
```

### Image Naming Convention

- Filenames match content categories: `action and adventure.png`, `music.png`, `gay bb.png`
- Spaces in filenames are preserved as-is
- No file extension variations (all `.png`)
- Sorting appears categorical rather than alphabetical

## Development Workflows

### Managing Images

1. **Adding New Icons**: Use GitHub's upload interface or git commits
   - Add PNG files to repository root
   - Keep filenames descriptive and consistent with existing naming
   - Ensure images are optimized PNGs (2-4MB typical size)

2. **Updating Existing Icons**: Replace files with new versions
   - Maintain identical filenames to prevent breakage in Emby
   - Commit message: "Add files via upload" (current convention)

3. **Organizing Assets**: Currently all files in root directory
   - Consider subdirectories if repository grows (e.g., `/icons/`, `/themes/`)
   - Document any reorganization in a README for Emby integration points

## Integration with Emby

**Important**: These images are consumed by Emby Server. When making changes:

- **Filename changes** are breaking changes - Emby likely references them by exact filename
- **Visual consistency**: Maintain consistent art style and composition across the theme set
- **Format requirement**: All files must be PNG format
- **Resolution/Size**: Maintain consistent dimensions across related icon sets (typically what Emby expects)

## Development Best Practices

1. **Git Discipline**
   - Use clear, descriptive commit messages (avoid generic "Add files via upload")
   - Keep binary files tracked efficiently (consider `.gitattributes` if LFS is needed)
   - Document the theme purpose or version in commit messages if adding multiple related icons

2. **Quality Standards**
   - Verify PNG compression to minimize file size
   - Test images display correctly in Emby UI before committing
   - Maintain artistic consistency within theme sets

3. **Documentation**
   - Consider adding a `README.md` explaining:
     - Theme philosophy/purpose
     - How to use icons in Emby
     - Contribution guidelines for new categories
     - Category descriptions and use cases

## Common Tasks

| Task | Approach |
|------|----------|
| Add single icon | Commit to main, use descriptive filename |
| Add theme category | Create 1+ PNG(s), commit with category name |
| Check file history | `git log --follow <filename>` for icon version history |
| View differences | `git show <commit>` to inspect image changes in commits |

## External Dependencies

- **Emby Server**: Primary consumer of these icon files
- **GitHub**: Repository hosting and upload interface
- No build tools, dependencies, or compilation required

---

**Note**: This is a minimal documentation for a binary asset repository. If becoming a collaborative theme project, consider adding a `README.md` with theme guidelines and a `CONTRIBUTING.md` for community submissions.

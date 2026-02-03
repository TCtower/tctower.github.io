# Setup Instructions for Local Jekyll Development

This guide provides commands to set up a conda environment for running this Jekyll site locally.

## Prerequisites

- Conda (Miniconda or Anaconda) installed
- Basic terminal knowledge

## Step-by-Step Setup

### 1. Create a new conda environment with Ruby

```bash
# Create conda environment with Ruby (using conda-forge channel)
conda create -n jekyll-env -c conda-forge ruby=3.1 nodejs -y
```

### 2. Activate the conda environment and fix PATH

**Important:** After activating the conda environment, you need to ensure the conda Ruby is used instead of the system Ruby.

```bash
conda activate jekyll-env
export PATH="/opt/anaconda3/envs/jekyll-env/bin:$PATH"
```

**Note:** Replace `/opt/anaconda3` with your conda installation path if different. You can find it with `conda info --base`.

### 3. Verify Ruby version

Make sure you're using the conda Ruby (should be 3.3.x or 3.1.x):

```bash
which ruby
ruby --version
```

You should see something like `/opt/anaconda3/envs/jekyll-env/bin/ruby` and `ruby 3.3.x` or `ruby 3.1.x`.

### 4. Update RubyGems

```bash
gem update --system
```

### 5. Install Bundler (Ruby package manager)

```bash
gem install bundler
```

### 6. Navigate to the project directory

```bash
cd /Users/shiqihe/Desktop/3_Project/tctower.github.io
```

### 7. Create/Update Gemfile

If the Gemfile doesn't exist or is incorrect, create one with the following content:

```bash
cat > Gemfile << 'EOF'
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
end
EOF
```

### 8. Install Jekyll and dependencies

```bash
bundle install
```

### 9. (Optional) Install Node.js dependencies (for JavaScript minification)

```bash
npm install
```

### 10. Run the Jekyll development server

```bash
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`

### 11. (Optional) Run with live reload and watch for changes

```bash
bundle exec jekyll serve --livereload
```

## Quick Reference Commands

### Activate environment (for future sessions)
```bash
conda activate jekyll-env
export PATH="/opt/anaconda3/envs/jekyll-env/bin:$PATH"
cd /Users/shiqihe/Desktop/3_Project/tctower.github.io
```

**Note:** The `export PATH` command is crucial to ensure you're using the conda Ruby, not the system Ruby.

### Start the server
```bash
bundle exec jekyll serve
```

### Build the site (without serving)
```bash
bundle exec jekyll build
```

### Update gems
```bash
bundle update
```

### Deactivate conda environment
```bash
conda deactivate
```

## Troubleshooting

### If you encounter permission errors with gem install:
```bash
# Use --user-install flag
gem install bundler --user-install
```

### If bundle install fails with Ruby version errors:

This usually means you're using the system Ruby instead of conda Ruby. Fix it with:

```bash
# Make sure you're in the conda environment
conda activate jekyll-env

# Fix PATH to use conda Ruby
export PATH="/opt/anaconda3/envs/jekyll-env/bin:$PATH"

# Verify you're using the right Ruby
which ruby
ruby --version

# Update RubyGems
gem update --system

# Then try bundle install again
bundle install
```

### If Jekyll serve fails:
```bash
# Check Jekyll version
bundle exec jekyll --version

# Try with verbose output
bundle exec jekyll serve --verbose

conda activate jekyll-env
export PATH="/opt/anaconda3/envs/jekyll-env/bin:$PATH"
cd /Users/shiqihe/Desktop/3_Project/tctower.github.io
bundle exec jekyll serve
```

## Notes

- The site will automatically regenerate when you make changes to source files
- Press `Ctrl+C` to stop the server
- The compiled site is output to `_site/` directory (this is ignored by git)
- Make sure to use `bundle exec` prefix when running Jekyll commands to ensure you're using the correct gem versions

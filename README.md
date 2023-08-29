# watsonx chatbot course

This is the watsonx chatbot course hosted on GitHub Pages using Material for MkDocs. To view it online, go to:

<https://ibm.github.io/watsonx-chatbot-course>

Create a new repo based off this template, and use the following folders as a guide:

```ini

- data (any data (CSV, JSON, etc files) to be used)
- docs (this is where the workshop is documented)
|_ <folder-n> (these are exercises for the workshop)
  |_README.md (the steps for the exercise, in Markdown)
|_ README.md (this will appear on the gitbook home page)
- notebooks (any Jupyter notebooks can go here)
- src (any application source code can go here)
.mkdocs.yaml (configuration for mkdocs)
.travis.yaml (runs markdownlint by default)
README.md (only used for GitHub.com)
```

## Tips and conventions

### Screenshots

Screenshots look better if they are full page.
Use [ImageMagick](https://imagemagick.org) to create a nice border around images with this command:

```bash
magick mogrify -bordercolor gray -border 2
```

## License & Authors

If you would like to see the detailed LICENSE click [here](./LICENSE).

- Author: JJ Asghar <awesome@ibm.com>

```text
Copyright:: 2023- IBM, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

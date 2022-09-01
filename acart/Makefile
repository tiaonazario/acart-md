BUILDDIR="build"
FILENAME="acart"
FILESTYLE="assets/citation-style.csl"
FILELAYOUT="layouts/pattern.tex"

pdf:
	@echo "Creating build folder"
	@mkdir "${BUILDDIR}" -p
	@echo "Creating pdf file"
	@pandoc "${FILENAME}.md" \
		--resource-path="./" \
		--citeproc \
		--csl="${FILESTYLE}" \
		--from="markdown+tex_math_single_backslash+tex_math_dollars+raw_tex" \
		--to="latex" \
		--output="${BUILDDIR}/${FILENAME}.pdf" \
		--pdf-engine="xelatex" \
		--include-in-header="${FILELAYOUT}"
	@echo "Done, created pdf file"

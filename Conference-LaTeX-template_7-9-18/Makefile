FILE_NAME := conference_041818

TEMP_FILES := \
	$(FILE_NAME).aux \
	$(FILE_NAME).bbl \
	$(FILE_NAME).log \
	$(FILE_NAME).blg \
	$(FILE_NAME).brf \
	$(FILE_NAME).dvi \
	$(FILE_NAME).out

SECTION_FILES = \
	$(FILE_NAME).tex \
	body.tex

BIBTEX_FILES = mining.bib

GEN_FIGURES = \

STATIC_FIGURES = #./img/* \

TABLES = #./table/* \

DEBUG=yes
ifneq '$(DEBUG)' 'yes'
LATEX_FLAGS="-interaction=batchmode --file-line-error --synctex=1"
endif
LATEX_FLAG_ENC="-kanji=utf8"

.DELETE_ON_ERROR:

################################################################################
# Main paper building
################################################################################

$(FILE_NAME).pdf: $(SECTION_FILES) $(GEN_FIGURES) $(STATIC_FIGURES) $(TABLES) $(BIBTEX_FILES)
	platex $(LATEX_FLAGS) $(FILE_NAME)
	pbibtex $(FILE_NAME)
	platex $(LATEX_FLAGS) $(FILE_NAME)
	platex $(LATEX_FLAGS) $(FILE_NAME)
	dvipdfmx $(FILE_NAME)
	rm -f $(TEMP_FILES)
	open $(FILE_NAME).pdf
.PHONY: clean
clean:
	rm -f $(TEMP_FILES) $(GEN_FIGURES) $(FILE_NAME).pdf

CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(report)

SET(LATEX_COMPILER_FLAGS "-interaction=nonstopmode --enable-write18" CACHE STRING "Flags passed to latex.")
INCLUDE(UseLATEX.cmake)

SET(SOURCE_INPUTS
  produit.tex
  decoupage.tex
  design.tex
  mesure.tex
  conclusion.tex
  )

SET(IMAGES_PATH "images")

ADD_LATEX_DOCUMENT(report.tex INPUTS ${SOURCE_INPUTS} IMAGE_DIRS ${IMAGES_PATH} DEFAULT_PDF MANGLE_TARGET_NAMES)

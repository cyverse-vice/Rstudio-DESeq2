FROM cyversevice/rstudio-verse:3.6.0

RUN apt-get update && apt-get install -y zlib1g-dev libxml2-dev
RUN if (!requireNamespace("BiocManager", quietly = TRUE))
       install.packages("BiocManager")
RUN BiocManager::install(version = "3.10")
RUN Rscript -e 'source("http://bioconductor.org/biocLite.R"); biocLite("devtools"); biocLite("pachterlab/sleuth");'
RUN Rscript -e 'source("http://bioconductor.org/biocLite.R"); biocLite("edgeR");'
RUN Rscript -e 'source("http://bioconductor.org/biocLite.R"); biocLite("annotate"); biocLite("genefilter");'
RUN Rscript -e 'source("http://bioconductor.org/biocLite.R"); biocLite("DESeq2");'
RUN Rscript -e 'source("http://bioconductor.org/biocLite.R"); biocLite("ballgown");'

# gene_fusion_normalizer

#install 

unzip gene_fusion_normalizer_0.2.1 \
cd gene_fusion_normalizer \
pip install -e . \



#run --col 입력 없으면 자동으로 fusion col 인식

  gene-fusion-normalizer "/path/gene_fusion_normalizer/gene_split_test.xlsx" \
  --col "fusion" \
  --gtf "/path/Homo_sapiens.GRCh38.110.gtf.gz" \
  --hgnc "/path/hgnc_complete_set.txt" \
  --explode \
  -o "/out_path/fusion_mapped.xlsx"

  
# 기능 요약
- 여러 방식으로 쓰여진 fusion gene 이름(geneA-geneB)을 표준화 하여 분리
- 기본적으로 "-" 를 기준으로 fusion gene을 나누지만 "-"이 여러 가지인 경우 \
  => 모든 경우의 수를 split 시키고 해당 유전자 이름이 알려진 바가 있는지 여부 검색 \
  => intergenic 또는 RNA name인 경우는 그대로 입력
 


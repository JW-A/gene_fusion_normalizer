# gene_fusion_normalizer

#install 
unzip gene_fusion_normalizer_0.2.1
cd gene_fusion_normalizer
pip install -e .

#run 
  gene-fusion-normalizer "/path/gene_fusion_normalizer/gene_split_test.xlsx" \
  #--col "fusion" \
  --gtf "/path/Homo_sapiens.GRCh38.110.gtf.gz" \
  --hgnc "/path/hgnc_complete_set.txt" \
  --explode \
  -o "/out_path/fusion_mapped.xlsx"
 
 #--col 입력 없으면 자동으로 fusion col 인식
  

# MIP
#Fix general usage cog_bioinf fasta, snp vcf, BWA etc etc
#No snps in current exons????

-project_name /hpc/cog_bioinf/data/flip/mipgen/test_runs/ecarbo_160614_log_8bp_tag/Erare_MIP_140616_log_8bp_tag
-bwa_genome_index /hpc/cog_bioinf/data/flip/Sets/Reference/1kgenome/human_g1k_v37.fasta
-regions_to_scan /hpc/cog_bioinf/data/flip/mipgen/test_runs/Erare_MIP_140616.bed
-min_capture_size 152
-max_capture_size 152
-bwa_threads 4
-arm_lengths 16:24,17:23,18:22,19:21,20:20
-lig_min_length 20
#-score_method svr
#svr score should be at least 1.4
#-svr_priority_score 1.5
-score_method logistic
#logistic score should be at least 0.7
-logistic_priority_score 0.7
-logistic_optimal_score 0.9
-tag_sizes 8,0
-tabix tabix -f
-snp_file /hpc/cog_bioinf/data/flip/Sets/Reference/00-common_all.vcf.gz
-max_mip_overlap 25
-double_tile_strands_separately off
-starting_mip_overlap 4
-feature_flank 25

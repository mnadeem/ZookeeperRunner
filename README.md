dropIndexByName MN_10703_CHGBK_IDX; 
DELETE mn_partitions where table_name = 'MN_CF_SPREADSHEET'
truncate table mn_cf_eligible_item 
ALTER INDEX MN_10299_CP_VIDX NOPARALLEL; 
CREATE INDEX temp_spreadsheet_type_idx ON mn_cf_spreadsheet(spreadsheet_type) NOLOGGING PARALLEL (DEGREE 8)
DROP INDEX temp_spreadsheet_name_idx 
CALL alter_indirect_sale_table('MN_INDIR_SALE_OPEN')
DROP_UNUSED_COLUMNS('MN_RBTPMT_SALE_CLOSED','REPORT_PROJ_AMOUNT_DUE,REPORT_PROJ_BENEFIT_APPLIED,REPORT_PROJ_TIER_ATTAINED')
rdt
===
1) ST:

FE:					Classic:
rdt_21240_hlrfe
rdt_21250_hlrfe		rdt_21250_hlr
rdt_21260_hlrfe		rdt_21260_hlr

					Classic on BSP:
					rdt_21260_bsp_hlr

BS:
rdt_21260_spx_is_hlrfe		rdt_21403_is_hlrfe

BSP:
rdt_21260_spx_bsp_hlrfe		rdt_21403_bsp_hlrfe


2) FT:

rdt_ft_21260_hlr
rdt_ft_21260_hlrfe

rdt_ft_21260_hlr_ansi
rdt_ft_21260_hlrfe_ansi

rdt_ft_21260_hlr_ttc

3) Current Redundancy environments:
 a) N+1 (renaming of files pending: HLRA->HLR1, HLRB->HLR2, HLRR->HLRStandby)
 
	(I) Standby as Classic:

                     /-----------------------\
                     |         HLR MONO      |
                     | rdt_21260_hlr_standby |
                     \-----------------------/
                      /         |          \
                     /          |           \
    /-----------------\         |          /-----------------\
    |       HLR1      |         |          |       HLR2      |
    | rdt_21260_hlr_1 |         |          | rdt_21260_hlr_2 |
    \-----------------/         |          \-----------------/
                                |
                      /-------------------\
                      |        STP        |
                      | rdt_21260_hlr_stp |
                      \-------------------/


		
	(II) Standby as FE (for FT):

                     /----------------------------\
                     |        HLR FE Standby      |
                     | rdt_21260_hlrfe_standby_ft |
                     \----------------------------/
                      /             |            \
                     /              |             \
    /--------------------\          |          /--------------------\
    |        HLR1        |          |          |        HLR2        |
    | rdt_21260_hlr_1_ft |          |          | rdt_21260_hlr_2_ft |
    \--------------------/          |          \--------------------/
                                    |
                        /----------------------\
                        |          STP         |
                        | rdt_21260_hlr_stp_ft |
                        \----------------------/

		
	(III) Standby as BS (EBS, SPX in QUASI ACCOC MODE) (for FT):

    /-------------------------------\
    |        BC0, BC1, BC2...       |
    | rdt_21403_is_hlrfe_standby_ft |
    \-------------------------------/
                          \
                    /----------------------------------\
                    |        CP1 (HLRStandby)           |
                    | rdt_21260_spx_is_hlrfe_standby_ft |
                    \----------------------------------/
                      /             |            \
                     /              |             \
    /--------------------\          |          /--------------------\
    |        HLR1        |          |          |        HLR2        |
    | rdt_21260_hlr_1_ft |          |          | rdt_21260_hlr_2_ft |
    \--------------------/          |          \--------------------/
                                    |
                        /----------------------\
                        |          STP         |
                        | rdt_21260_hlr_stp_ft |
                        \----------------------/



 b) 1+1 (naming convention: HLRA, HLRB)
	-to be updated


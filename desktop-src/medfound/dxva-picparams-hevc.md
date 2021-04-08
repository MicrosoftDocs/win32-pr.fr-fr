---
description: Fournit les paramètres au niveau de l’image d’une image compressée pour le décodage vidéo HEVC.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: Structure DXVA_PicParams_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111782"
---
# <a name="dxva_picparams_hevc-structure"></a>DXVA \_ PicParams \_ HEVC, structure

Fournit les paramètres au niveau de l’image d’une image compressée pour le décodage vidéo HEVC.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a>Membres

<dl> <dt>

**PicWidthInMinCbsY**
</dt> <dd></dd> <dt>

**PicHeightInMinCbsY**
</dt> <dd></dd> <dt>

**\_format Chroma \_ IDC**
</dt> <dd></dd> <dt>

**\_indicateur de \_ plan de couleur distinct \_** 
</dt> <dd></dd> <dt>

**luminance de profondeur de bit \_ \_ \_ minus8** 
</dt> <dd></dd> <dt>

**Chroma de profondeur de bits \_ \_ \_ minus8**
</dt> <dd></dd> <dt>

**Log2 \_ Max \_ PIC \_ Order \_ CNT \_ LSB \_ minus4**
</dt> <dd></dd> <dt>

**NoPicReorderingFlag** 
</dt> <dd></dd> <dt>

 **NoBiPredFlag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wFormatAndSequenceInfoFlags**
</dt> <dd></dd> <dt>

**CurrPic**
</dt> <dd></dd> <dt>

**SPS \_ Max \_ Dec \_ PIC \_ Buffering \_ minus1**
</dt> <dd></dd> <dt>

**Log2 \_ taille de bloc de codage de luminance min. \_ \_ \_ \_ \_ minus3**
</dt> <dd></dd> <dt>

**\_taille du \_ \_ bloc de \_ codage de luminance min \_ \_ . log2 diff Max \_ .**
</dt> <dd></dd> <dt>

**Log2 \_ \_ taille du bloc de transformation min \_ \_ \_ minus2**
</dt> <dd></dd> <dt>

**taille du bloc de la \_ \_ \_ transformation min diff Max \_ \_ log2 \_**
</dt> <dd></dd> <dt>

**profondeur maximale de la \_ hiérarchie de transformation \_ \_ \_**
</dt> <dd></dd> <dt>

**\_profondeur de hiérarchie de transformation Max \_ \_ \_ intra**
</dt> <dd></dd> <dt>

**num \_ short \_ term \_ Ref \_ PIC \_**
</dt> <dd></dd> <dt>

**nombre \_ d' \_ \_ \_ alimentations pics de Ref long term \_**
</dt> <dd></dd> <dt>

**nombre \_ Réf. \_ idx \_ L0 \_ par défaut \_ actif \_ minus1**
</dt> <dd></dd> <dt>

**nombre \_ Ref \_ idx \_ L1 \_ par défaut \_ actif \_ minus1**
</dt> <dd></dd> <dt>

**init \_ QP \_ minus26**
</dt> <dd></dd> <dt>

**ucNumDeltaPocsOfRefRpsIdx**
</dt> <dd></dd> <dt>

**wNumBitsForShortTermRPSInSlice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**indicateur d’activation de la liste de mise à l’échelle \_ \_ \_**
</dt> <dd></dd> <dt>

**\_indicateur amp activé \_**
</dt> <dd></dd> <dt>

**exemple d' \_ indicateur d’activation de \_ décalage adaptatif \_ \_**
</dt> <dd></dd> <dt>

**\_indicateur PCM activé \_** 
</dt> <dd></dd> <dt>

**\_exemple de \_ luminance de profondeur de bit \_ \_ \_ minus1** 
</dt> <dd></dd> <dt>

**exemple PCM- \_ \_ profondeur de bit de \_ \_ \_ minus1 Chroma** 
</dt> <dd></dd> <dt>

**\_taille du bloc de codage de luminance log2 min \_ PCM \_ \_ \_ \_ \_ minus3** 
</dt> <dd></dd> <dt>

**\_taille du \_ \_ bloc de \_ \_ codage de luminance PCM \_ \_ Min \_ . log2 diff max.**
</dt> <dd></dd> <dt>

**\_indicateur de filtre de boucle PCM \_ \_ désactivé \_**
</dt> <dd></dd> <dt>

**\_indicateur de \_ \_ présence pics \_ de Ref long term \_** 
</dt> <dd></dd> <dt>

**indicateur de la \_ MVP temporelle SPS \_ \_ activée \_**
</dt> <dd></dd> <dt>

**\_indicateur d’activation d’intra- \_ lissage fort \_ \_** 
</dt> <dd></dd> <dt>

**indicateur de segment dépendants \_ \_ \_ activés \_** 
</dt> <dd></dd> <dt>

**indicateur de sortie indicateur \_ \_ présent \_** 
</dt> <dd></dd> <dt>

**nombre \_ de \_ \_ bits d’en-tête de tranche extra \_** 
</dt> <dd></dd> <dt>

**\_indicateur de \_ désactivation du masquage des données \_ \_**
</dt> <dd></dd> <dt>

**\_indicateur CABAC init \_ présent \_**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwCodingParamToolFlags**
</dt> <dd></dd> <dt>

**\_drapeau intra-imposé \_ restreint \_**
</dt> <dd></dd> <dt>

**indicateur de transformation \_ \_ avec omission activée \_**
</dt> <dd></dd> <dt>

**\_indicateur d' \_ activation du Delta QP \_ cu \_**
</dt> <dd></dd> <dt>

**\_indicateur de \_ décalage de Chroma QP de la tranche PPS \_ \_ \_ présent \_**
</dt> <dd></dd> <dt>

**\_indicateur prédit pondéré \_**
</dt> <dd></dd> <dt>

**\_indicateur bipred pondéré \_**
</dt> <dd></dd> <dt>

**indicateur de contournement de la transchargement \_ \_ activé \_**
</dt> <dd></dd> <dt>

**\_indicateur d’activation des vignettes \_** 
</dt> <dd></dd> <dt>

**indicateur d’activation de la \_ synchronisation du codage entropie \_ \_ \_** 
</dt> <dd></dd> <dt>

**\_indicateur d’espacement uniforme \_** 
</dt> <dd></dd> <dt>

**filtre de boucle \_ sur l’indicateur d' \_ \_ activation des vignettes \_ \_** 
</dt> <dd></dd> <dt>

**\_filtre de boucle PPS sur l' \_ \_ \_ indicateur des tranches \_ activées \_**
</dt> <dd></dd> <dt>

**indicateur de déblocage de \_ \_ remplacement \_ activé \_**
</dt> <dd></dd> <dt>

**\_indicateur de déblocage PPS \_ \_ désactivé \_**
</dt> <dd></dd> <dt>

**\_indicateur de modification des listes \_ \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ indicateur présent d’extension d’en-tête de segment \_ de secteur \_**
</dt> <dd></dd> <dt>

**IrapPicFlag**
</dt> <dd></dd> <dt>

**IdrPicFlag** 
</dt> <dd></dd> <dt>

**IntraPicFlag** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwCodingSettingPicturePropertyFlags**
</dt> <dd></dd> <dt>

**décalage de PPS \_ CB \_ QP \_**
</dt> <dd></dd> <dt>

**\_décalage PPS CR \_ QP \_**
</dt> <dd></dd> <dt>

**nombre \_ de \_ colonnes de vignette \_ minus1**
</dt> <dd></dd> <dt>

**nombre \_ de \_ lignes de mosaïque \_ minus1**
</dt> <dd></dd> <dt>

**largeur de colonne \_ \_ minus1**
</dt> <dd></dd> <dt>

**hauteur de ligne \_ \_ minus1**
</dt> <dd></dd> <dt>

**profondeur Delta de comparaison de \_ cu \_ QP \_ \_**
</dt> <dd></dd> <dt>

**\_div2 de \_ décalage \_ bêta PPS**
</dt> <dd></dd> <dt>

**PPS \_ TC \_ offset \_ div2**
</dt> <dd></dd> <dt>

**Log2 \_ \_ niveau de fusion parallèle \_ \_ minus2**
</dt> <dd></dd> <dt>

**CurrPicOrderCntVal**
</dt> <dd></dd> <dt>

**RefPicList**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**PicOrderCntValList**
</dt> <dd></dd> <dt>

**RefPicSetStCurrBefore**
</dt> <dd></dd> <dt>

**RefPicSetStCurrAfter**
</dt> <dd></dd> <dt>

**RefPicSetLtCurr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**StatusReportFeedbackNumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 





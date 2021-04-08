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
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="28d4d-103">DXVA \_ PicParams \_ HEVC, structure</span><span class="sxs-lookup"><span data-stu-id="28d4d-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="28d4d-104">Fournit les paramètres au niveau de l’image d’une image compressée pour le décodage vidéo HEVC.</span><span class="sxs-lookup"><span data-stu-id="28d4d-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28d4d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="28d4d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="28d4d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28d4d-107">**PicWidthInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="28d4d-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-108">**PicHeightInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="28d4d-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-109">**\_format Chroma \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="28d4d-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-110">**\_indicateur de \_ plan de couleur distinct \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-111">**luminance de profondeur de bit \_ \_ \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="28d4d-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-112">**Chroma de profondeur de bits \_ \_ \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="28d4d-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-113">**Log2 \_ Max \_ PIC \_ Order \_ CNT \_ LSB \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="28d4d-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-114">**NoPicReorderingFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4d-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="28d4d-115">**NoBiPredFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4d-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-117">**wFormatAndSequenceInfoFlags**</span><span class="sxs-lookup"><span data-stu-id="28d4d-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-118">**CurrPic**</span><span class="sxs-lookup"><span data-stu-id="28d4d-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-119">**SPS \_ Max \_ Dec \_ PIC \_ Buffering \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-120">**Log2 \_ taille de bloc de codage de luminance min. \_ \_ \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="28d4d-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-121">**\_taille du \_ \_ bloc de \_ codage de luminance min \_ \_ . log2 diff Max \_ .**</span><span class="sxs-lookup"><span data-stu-id="28d4d-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-122">**Log2 \_ \_ taille du bloc de transformation min \_ \_ \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="28d4d-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-123">**taille du bloc de la \_ \_ \_ transformation min diff Max \_ \_ log2 \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-124">**profondeur maximale de la \_ hiérarchie de transformation \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-125">**\_profondeur de hiérarchie de transformation Max \_ \_ \_ intra**</span><span class="sxs-lookup"><span data-stu-id="28d4d-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-126">**num \_ short \_ term \_ Ref \_ PIC \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-127">**nombre \_ d' \_ \_ \_ alimentations pics de Ref long term \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-128">**nombre \_ Réf. \_ idx \_ L0 \_ par défaut \_ actif \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-129">**nombre \_ Ref \_ idx \_ L1 \_ par défaut \_ actif \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-130">**init \_ QP \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="28d4d-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-131">**ucNumDeltaPocsOfRefRpsIdx**</span><span class="sxs-lookup"><span data-stu-id="28d4d-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-132">**wNumBitsForShortTermRPSInSlice**</span><span class="sxs-lookup"><span data-stu-id="28d4d-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="28d4d-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-134">**indicateur d’activation de la liste de mise à l’échelle \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-135">**\_indicateur amp activé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-136">**exemple d' \_ indicateur d’activation de \_ décalage adaptatif \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-137">**\_indicateur PCM activé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-138">**\_exemple de \_ luminance de profondeur de bit \_ \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-139">**exemple PCM- \_ \_ profondeur de bit de \_ \_ \_ minus1 Chroma**</span><span class="sxs-lookup"><span data-stu-id="28d4d-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-140">**\_taille du bloc de codage de luminance log2 min \_ PCM \_ \_ \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="28d4d-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-141">**\_taille du \_ \_ bloc de \_ \_ codage de luminance PCM \_ \_ Min \_ . log2 diff max.**</span><span class="sxs-lookup"><span data-stu-id="28d4d-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-142">**\_indicateur de filtre de boucle PCM \_ \_ désactivé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-143">**\_indicateur de \_ \_ présence pics \_ de Ref long term \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-144">**indicateur de la \_ MVP temporelle SPS \_ \_ activée \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-145">**\_indicateur d’activation d’intra- \_ lissage fort \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-146">**indicateur de segment dépendants \_ \_ \_ activés \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-147">**indicateur de sortie indicateur \_ \_ présent \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-148">**nombre \_ de \_ \_ bits d’en-tête de tranche extra \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-149">**\_indicateur de \_ désactivation du masquage des données \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-150">**\_indicateur CABAC init \_ présent \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="28d4d-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-152">**dwCodingParamToolFlags**</span><span class="sxs-lookup"><span data-stu-id="28d4d-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-153">**\_drapeau intra-imposé \_ restreint \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-154">**indicateur de transformation \_ \_ avec omission activée \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-155">**\_indicateur d' \_ activation du Delta QP \_ cu \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-156">**\_indicateur de \_ décalage de Chroma QP de la tranche PPS \_ \_ \_ présent \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-157">**\_indicateur prédit pondéré \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-158">**\_indicateur bipred pondéré \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-159">**indicateur de contournement de la transchargement \_ \_ activé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-160">**\_indicateur d’activation des vignettes \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-161">**indicateur d’activation de la \_ synchronisation du codage entropie \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-162">**\_indicateur d’espacement uniforme \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-163">**filtre de boucle \_ sur l’indicateur d' \_ \_ activation des vignettes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-164">**\_filtre de boucle PPS sur l' \_ \_ \_ indicateur des tranches \_ activées \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-165">**indicateur de déblocage de \_ \_ remplacement \_ activé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-166">**\_indicateur de déblocage PPS \_ \_ désactivé \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-167">**\_indicateur de modification des listes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-168">**\_ \_ \_ indicateur présent d’extension d’en-tête de segment \_ de secteur \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-169">**IrapPicFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4d-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-170">**IdrPicFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4d-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-171">**IntraPicFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4d-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="28d4d-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-173">**dwCodingSettingPicturePropertyFlags**</span><span class="sxs-lookup"><span data-stu-id="28d4d-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-174">**décalage de PPS \_ CB \_ QP \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-175">**\_décalage PPS CR \_ QP \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-176">**nombre \_ de \_ colonnes de vignette \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-177">**nombre \_ de \_ lignes de mosaïque \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-178">**largeur de colonne \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-179">**hauteur de ligne \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="28d4d-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-180">**profondeur Delta de comparaison de \_ cu \_ QP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28d4d-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-181">**\_div2 de \_ décalage \_ bêta PPS**</span><span class="sxs-lookup"><span data-stu-id="28d4d-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-182">**PPS \_ TC \_ offset \_ div2**</span><span class="sxs-lookup"><span data-stu-id="28d4d-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-183">**Log2 \_ \_ niveau de fusion parallèle \_ \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="28d4d-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-184">**CurrPicOrderCntVal**</span><span class="sxs-lookup"><span data-stu-id="28d4d-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-185">**RefPicList**</span><span class="sxs-lookup"><span data-stu-id="28d4d-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="28d4d-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-187">**PicOrderCntValList**</span><span class="sxs-lookup"><span data-stu-id="28d4d-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-188">**RefPicSetStCurrBefore**</span><span class="sxs-lookup"><span data-stu-id="28d4d-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-189">**RefPicSetStCurrAfter**</span><span class="sxs-lookup"><span data-stu-id="28d4d-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-190">**RefPicSetLtCurr**</span><span class="sxs-lookup"><span data-stu-id="28d4d-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="28d4d-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="28d4d-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="28d4d-193">**StatusReportFeedbackNumber**</span><span class="sxs-lookup"><span data-stu-id="28d4d-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="28d4d-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="28d4d-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="28d4d-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28d4d-195">Requirements</span></span>



| <span data-ttu-id="28d4d-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28d4d-196">Requirement</span></span> | <span data-ttu-id="28d4d-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="28d4d-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="28d4d-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28d4d-198">Minimum supported client</span></span><br/> | <span data-ttu-id="28d4d-199">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28d4d-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="28d4d-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28d4d-200">Minimum supported server</span></span><br/> | <span data-ttu-id="28d4d-201">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28d4d-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="28d4d-202">En-tête</span><span class="sxs-lookup"><span data-stu-id="28d4d-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d4d-203"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d4d-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d4d-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28d4d-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d4d-205">Structures de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28d4d-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 





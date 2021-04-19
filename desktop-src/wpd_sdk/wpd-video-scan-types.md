---
description: Le \_ \_ \_ type d’énumération types d’analyses vidéo wpd décrit la façon dont les champs d’un fichier vidéo sont encodés.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Énumération WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545355"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="b4fa3-103">\_ \_ Énumération des types d’analyses vidéo wpd \_</span><span class="sxs-lookup"><span data-stu-id="b4fa3-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="b4fa3-104">Le type d’énumération **\_ \_ \_ types d’analyses vidéo wpd** décrit la façon dont les champs d’un fichier vidéo sont encodés.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fa3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4fa3-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="b4fa3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b4fa3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4fa3-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_type d' \_ analyse vidéo wpd \_ \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-108">Le type d’analyse n’a pas été défini pour ce fichier vidéo ou n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_type d' \_ analyse vidéo wpd \_ \_ progressif**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-110">Fichier vidéo d’analyse progressive.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_champ de \_ type d’analyse vidéo wpd entrelacé en \_ \_ \_ \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-112">Fichier vidéo entrelacé dans lequel les champs alternatifs et le champ supérieur (avec la ligne 1) sont dessinés en premier.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="b4fa3-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_champ de \_ type d’analyse vidéo wpd entrelacé en \_ \_ \_ \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-115">Fichier vidéo entrelacé dans lequel les champs alternatifs et le champ inférieur (avec la ligne 2) sont dessinés en premier.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="b4fa3-116">Pour plus d’informations, consultez la section Notes, à la suite de cette section.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**\_champ de \_ type d’analyse vidéo wpd unique en \_ \_ \_ \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-118">Fichier vidéo entrelacé dans lequel les champs sont envoyés en tant qu’échantillons contigus et le champ supérieur (avec la ligne 1) est dessiné en premier.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="b4fa3-119">Pour plus d’informations, consultez la section Notes, à la suite de cette section.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**\_champ de \_ type d’analyse vidéo wpd simple en \_ \_ \_ \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-121">Fichier vidéo entrelacé dans lequel les champs sont envoyés en tant qu’échantillons contigus et le champ inférieur (avec la ligne 2) est envoyé en premier.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_balayage vidéo \_ de \_ type \_ wpd \_ entrelacé mixte**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-123">Fichier vidéo avec un mélange de modes d’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="b4fa3-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_balayage vidéo wpd- \_ \_ type \_ mixte \_ entrelacé \_ et \_ progressif**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="b4fa3-125">Fichier vidéo avec un mélange de modes entrelacés et progressifs.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4fa3-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b4fa3-126">Remarks</span></span>

<span data-ttu-id="b4fa3-127">Cette énumération est utilisée par la propriété de [ \_ \_ \_ type d’analyse vidéo wpd](properties-and-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="b4fa3-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="b4fa3-128">Il existe deux types de formats de fichier entrelacés qui sont spécifiés par cette énumération.</span><span class="sxs-lookup"><span data-stu-id="b4fa3-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="b4fa3-129">**Wpd \_ \_Champ de type d’analyse vidéo \_ \_ \_ entrelacée** fait référence à un format de fichier dans lequel les trames sont remises au fur et à mesure qu’elles ont été analysées. les champs alternatifs et les données sont placés ligne par ligne, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="b4fa3-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="b4fa3-130">**Trame 1**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-130">**Frame 1**</span></span>

<span data-ttu-id="b4fa3-131">Champ 1 : ligne 1</span><span class="sxs-lookup"><span data-stu-id="b4fa3-131">Field 1: Line 1</span></span>

<span data-ttu-id="b4fa3-132">Champ 2 : ligne 1</span><span class="sxs-lookup"><span data-stu-id="b4fa3-132">Field 2: Line 1</span></span>

<span data-ttu-id="b4fa3-133">Champ 1 : ligne 2</span><span class="sxs-lookup"><span data-stu-id="b4fa3-133">Field 1: Line 2</span></span>

<span data-ttu-id="b4fa3-134">Champ 2 : ligne 2</span><span class="sxs-lookup"><span data-stu-id="b4fa3-134">Field 2: Line 2</span></span>

<span data-ttu-id="b4fa3-135">Champ 1 : ligne 3</span><span class="sxs-lookup"><span data-stu-id="b4fa3-135">Field 1: Line 3</span></span>

<span data-ttu-id="b4fa3-136">Champ 2 : ligne 3</span><span class="sxs-lookup"><span data-stu-id="b4fa3-136">Field 2: Line 3</span></span>

<span data-ttu-id="b4fa3-137">...</span><span class="sxs-lookup"><span data-stu-id="b4fa3-137">...</span></span>

<span data-ttu-id="b4fa3-138">**Wpd \_ Le \_ champ de type d’analyse vidéo \_ \_ \_ unique** fait référence à un format de fichier où chaque champ est stocké dans un bloc unique de lignes de numérisation, et les champs sont stockés de manière séquentielle, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="b4fa3-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="b4fa3-139">**Trame 1**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-139">**Frame 1**</span></span>

<span data-ttu-id="b4fa3-140">Champ 1 : ligne 1</span><span class="sxs-lookup"><span data-stu-id="b4fa3-140">Field 1: Line 1</span></span>

<span data-ttu-id="b4fa3-141">Champ 1 : ligne 2</span><span class="sxs-lookup"><span data-stu-id="b4fa3-141">Field 1: Line 2</span></span>

<span data-ttu-id="b4fa3-142">Champ 1 : ligne 3</span><span class="sxs-lookup"><span data-stu-id="b4fa3-142">Field 1: Line 3</span></span>

<span data-ttu-id="b4fa3-143">...</span><span class="sxs-lookup"><span data-stu-id="b4fa3-143">...</span></span>

<span data-ttu-id="b4fa3-144">Suivi de</span><span class="sxs-lookup"><span data-stu-id="b4fa3-144">Followed by</span></span>

<span data-ttu-id="b4fa3-145">Champ 2 : ligne 1</span><span class="sxs-lookup"><span data-stu-id="b4fa3-145">Field 2: Line 1</span></span>

<span data-ttu-id="b4fa3-146">Champ 2 : ligne 2</span><span class="sxs-lookup"><span data-stu-id="b4fa3-146">Field 2: Line 2</span></span>

<span data-ttu-id="b4fa3-147">Champ 2 : ligne 3</span><span class="sxs-lookup"><span data-stu-id="b4fa3-147">Field 2: Line 3</span></span>

<span data-ttu-id="b4fa3-148">...</span><span class="sxs-lookup"><span data-stu-id="b4fa3-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="b4fa3-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4fa3-149">Requirements</span></span>



| <span data-ttu-id="b4fa3-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4fa3-150">Requirement</span></span> | <span data-ttu-id="b4fa3-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4fa3-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fa3-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4fa3-152">Header</span></span><br/> | <dl> <span data-ttu-id="b4fa3-153"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fa3-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4fa3-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4fa3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fa3-155">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="b4fa3-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





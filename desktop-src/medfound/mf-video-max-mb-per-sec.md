---
description: Spécifie, sur IMFTransform, la vitesse de traitement maximale bloc macro, en blocs macros par seconde, qui est prise en charge par l’encodeur matériel.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Attribut MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542908"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="dd77a-103">\_ \_ Attribut nombre maximal de \_ Mo \_ par \_ seconde de la vidéo MF</span><span class="sxs-lookup"><span data-stu-id="dd77a-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="dd77a-104">Spécifie, sur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la vitesse de traitement maximale bloc macro, en blocs macros par seconde, qui est prise en charge par l’encodeur matériel.</span><span class="sxs-lookup"><span data-stu-id="dd77a-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="dd77a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dd77a-105">Data type</span></span>

<span data-ttu-id="dd77a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dd77a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dd77a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dd77a-107">Remarks</span></span>

<span data-ttu-id="dd77a-108">Ceci est un attribut de lecture seule.</span><span class="sxs-lookup"><span data-stu-id="dd77a-108">This is a read-only attribute.</span></span>

<span data-ttu-id="dd77a-109">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="dd77a-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="dd77a-110">Cet attribut est affecté par les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="dd77a-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="dd77a-111">[MF \_ \_ \_ Niveau vidéo MT](mf-mt-video-level.md) (qui est un alias du [ \_ niveau de \_ MPEG2 \_ MT MPEG2](mf-mt-mpeg2-level-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="dd77a-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="dd77a-112">CODECAPI \_ AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="dd77a-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="dd77a-113">CODECAPI \_ AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="dd77a-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="dd77a-114">Si l’attribut de [ \_ \_ \_ niveau vidéo MF MT](mf-mt-video-level.md) est présent, l’encodeur doit retourner la vitesse de traitement pour le débit binaire et la résolution les plus élevés pris en charge au niveau spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd77a-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="dd77a-115">Si l' \_ \_ \_ attribut de niveau vidéo MF MT n’est pas présent, il doit utiliser un niveau par défaut de 4.</span><span class="sxs-lookup"><span data-stu-id="dd77a-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="dd77a-116">Si la propriété [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI a été définie, l’encodeur doit retourner la vitesse de traitement correspondant à la valeur définie pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dd77a-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="dd77a-117">Si l' \_ attribut CODECAPI AVEncCommonQualityVsSpeed n’est pas présent, il doit utiliser la valeur par défaut 0, qui doit être le mode de traitement le plus rapide.</span><span class="sxs-lookup"><span data-stu-id="dd77a-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="dd77a-118">Si la propriété [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI a été définie sur une valeur valide et prise en charge, l’encodeur doit retourner la vitesse de traitement correspondant à la valeur définie pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dd77a-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="dd77a-119">Si l' \_ attribut CODECAPI AVEncMPVDefaultBPictureCount n’est pas une avance, t, il doit utiliser une valeur par défaut de 0 B frames.</span><span class="sxs-lookup"><span data-stu-id="dd77a-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="dd77a-120">Seuls les 28 bits inférieurs doivent être utilisés par une application.</span><span class="sxs-lookup"><span data-stu-id="dd77a-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="dd77a-121">Le 4bits supérieur est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dd77a-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="dd77a-122">Les applications doivent ignorer les 4 bits supérieurs et MFTs doit définir les 4 bits supérieurs à 0.</span><span class="sxs-lookup"><span data-stu-id="dd77a-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd77a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd77a-123">Requirements</span></span>



| <span data-ttu-id="dd77a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd77a-124">Requirement</span></span> | <span data-ttu-id="dd77a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd77a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd77a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd77a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dd77a-127">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd77a-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="dd77a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd77a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dd77a-129">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd77a-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dd77a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd77a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd77a-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd77a-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd77a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd77a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd77a-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd77a-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

---
description: Active le traitement vidéo par le lecteur source.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Attribut MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484808"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="8fe97-103">\_Lecteur source MF-activer l’attribut de \_ \_ \_ \_ traitement vidéo</span><span class="sxs-lookup"><span data-stu-id="8fe97-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="8fe97-104">Active le traitement vidéo par le [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="8fe97-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="8fe97-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8fe97-105">Data type</span></span>

<span data-ttu-id="8fe97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8fe97-106">**UINT32**</span></span>



| <span data-ttu-id="8fe97-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe97-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="8fe97-108">Signification</span><span class="sxs-lookup"><span data-stu-id="8fe97-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="8fe97-109"><dt>**Différente**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe97-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="8fe97-110">Activez le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="8fe97-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="8fe97-111"><dt>**Nuls**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe97-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="8fe97-112">Désactivez le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="8fe97-112">Disable video processing.</span></span> <span data-ttu-id="8fe97-113">(Par défaut)</span><span class="sxs-lookup"><span data-stu-id="8fe97-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="8fe97-114">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8fe97-114">Get/set</span></span>

<span data-ttu-id="8fe97-115">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8fe97-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8fe97-116">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8fe97-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe97-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8fe97-117">Remarks</span></span>

<span data-ttu-id="8fe97-118">Si cet attribut a la **valeur true** (différent de zéro), le lecteur source peut effectuer le traitement vidéo limité suivant sur des images vidéo non compressées :</span><span class="sxs-lookup"><span data-stu-id="8fe97-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="8fe97-119">Conversion de YUV en RGB-32.</span><span class="sxs-lookup"><span data-stu-id="8fe97-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="8fe97-120">Entrelac.</span><span class="sxs-lookup"><span data-stu-id="8fe97-120">Deinterlacing.</span></span>

<span data-ttu-id="8fe97-121">Ces opérations sont effectuées dans le logiciel et ne sont pas optimisées pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="8fe97-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="8fe97-122">Cette fonctionnalité est destinée aux applications qui traitent un petit nombre de frames, par exemple pour créer une miniature de vidéo, ou des applications qui ne décodent pas les trames en temps réel.</span><span class="sxs-lookup"><span data-stu-id="8fe97-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="8fe97-123">L’opération de désentrelacement interpole les données d’un champ unique, de sorte qu’elles sont perdues.</span><span class="sxs-lookup"><span data-stu-id="8fe97-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="8fe97-124">Évitez ce paramètre si vous utilisez Direct3D pour afficher les images vidéo, car le GPU offre généralement de meilleures capacités de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="8fe97-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="8fe97-125">Si cet attribut a la **valeur true**, les attributs suivants doivent avoir la **valeur false**:</span><span class="sxs-lookup"><span data-stu-id="8fe97-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="8fe97-126">\_ \_ Gestionnaire D3D du lecteur source \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="8fe97-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="8fe97-127">\_ \_ convertisseurs de désactivation MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="8fe97-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="8fe97-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe97-128">Requirements</span></span>



| <span data-ttu-id="8fe97-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe97-129">Requirement</span></span> | <span data-ttu-id="8fe97-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe97-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe97-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe97-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe97-132">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8fe97-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8fe97-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe97-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe97-134">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8fe97-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8fe97-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fe97-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe97-136"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe97-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe97-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe97-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe97-138">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fe97-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8fe97-139">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="8fe97-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="8fe97-140">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="8fe97-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 





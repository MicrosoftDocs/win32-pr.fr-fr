---
description: Spécifie une classe de service Planificateur de classes multimédias (MMCSS) pour les threads de traitement audio dans le lecteur source ou le writer de récepteur.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Attribut MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531811"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="b0e67-103">MF \_ ReadWrite de la \_ classe MMCSS, \_ \_ attribut audio</span><span class="sxs-lookup"><span data-stu-id="b0e67-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="b0e67-104">Spécifie une classe de [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour les threads de traitement audio dans le lecteur source ou le writer de récepteur.</span><span class="sxs-lookup"><span data-stu-id="b0e67-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0e67-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b0e67-105">Data type</span></span>

<span data-ttu-id="b0e67-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b0e67-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="b0e67-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="b0e67-107">Get/set</span></span>

<span data-ttu-id="b0e67-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b0e67-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b0e67-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b0e67-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e67-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e67-110">Remarks</span></span>

<span data-ttu-id="b0e67-111">Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="b0e67-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="b0e67-112">La valeur de l’attribut doit être un nom de classe MMCSS valide.</span><span class="sxs-lookup"><span data-stu-id="b0e67-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="b0e67-113">Si cet attribut est défini, le lecteur source ou l’enregistreur du récepteur enregistre ses threads de traitement audio avec la classe MMCSS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0e67-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="b0e67-114">MMCSS garantit que le traitement des données dans le lecteur source ou le writer du récepteur a priorité sur les autres tâches système.</span><span class="sxs-lookup"><span data-stu-id="b0e67-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="b0e67-115">Pour spécifier la priorité de base pour les threads audio, définissez l’attribut [ \_ audio MF ReadWrite \_ MMCSS \_ Priority \_ ](mf-readwrite-mmcss-priority-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e67-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="b0e67-116">Si cet attribut n’est pas défini, la priorité de base pour les threads audio est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b0e67-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="b0e67-117">Cet attribut remplace l’attribut de [classe de la \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class.md) pour les threads de traitement audio.</span><span class="sxs-lookup"><span data-stu-id="b0e67-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="b0e67-118">Si aucun attribut n’est défini, les threads audio ne sont pas inscrits auprès de MCSS.</span><span class="sxs-lookup"><span data-stu-id="b0e67-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="b0e67-119">Pour la plupart des applications, le problème audio est bien plus perceptible pour l’utilisateur que le problème de vidéo, et donc moins acceptable.</span><span class="sxs-lookup"><span data-stu-id="b0e67-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="b0e67-120">Pour cette raison, une application doit généralement définir l' \_ audio de la classe MF ReadWrite ReadWrite \_ \_ \_ sur une classe MMCSS de priorité supérieure à celle de la [ \_ classe MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md).</span><span class="sxs-lookup"><span data-stu-id="b0e67-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="b0e67-121">Cela garantit que le traitement audio reçoit une priorité plus élevée que d’autres tâches.</span><span class="sxs-lookup"><span data-stu-id="b0e67-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e67-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0e67-122">Requirements</span></span>



| <span data-ttu-id="b0e67-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0e67-123">Requirement</span></span> | <span data-ttu-id="b0e67-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0e67-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e67-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e67-126">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0e67-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b0e67-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e67-128">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0e67-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b0e67-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0e67-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e67-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e67-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0e67-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0e67-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e67-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e67-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

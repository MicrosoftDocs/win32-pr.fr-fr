---
description: Spécifie une classe de service Planificateur de classes multimédias (MMCSS) pour le lecteur source ou le writer de récepteur.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Attribut MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759076"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="cee42-103">MF \_ ReadWrite \_ - \_ attribut de classe mmcss</span><span class="sxs-lookup"><span data-stu-id="cee42-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="cee42-104">Spécifie une classe de [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour le lecteur source ou le writer de récepteur.</span><span class="sxs-lookup"><span data-stu-id="cee42-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="cee42-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cee42-105">Data type</span></span>

<span data-ttu-id="cee42-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cee42-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="cee42-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="cee42-107">Get/set</span></span>

<span data-ttu-id="cee42-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="cee42-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="cee42-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="cee42-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="cee42-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cee42-110">Remarks</span></span>

<span data-ttu-id="cee42-111">Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="cee42-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="cee42-112">La valeur de l’attribut doit être un nom de classe MMCSS valide.</span><span class="sxs-lookup"><span data-stu-id="cee42-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="cee42-113">Si cet attribut est défini, le lecteur source ou l’enregistreur du récepteur enregistre tous ses threads avec la classe MMCSS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cee42-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="cee42-114">MMCSS garantit que le traitement des données dans le lecteur source ou le writer du récepteur a priorité sur les autres tâches système.</span><span class="sxs-lookup"><span data-stu-id="cee42-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="cee42-115">Pour spécifier la priorité de base, définissez l’attribut de priorité de la [ \_ \_ \_ priorité MMCSS ReadWrite MF](mf-readwrite-mmcss-priority.md) .</span><span class="sxs-lookup"><span data-stu-id="cee42-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="cee42-116">Si cet attribut n’est pas défini, la priorité de base est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="cee42-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="cee42-117">Pour les threads de traitement audio, l’attribut audio de la [ \_ \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class-audio.md) (s’il est défini) remplace cet attribut.</span><span class="sxs-lookup"><span data-stu-id="cee42-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee42-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cee42-118">Requirements</span></span>



| <span data-ttu-id="cee42-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cee42-119">Requirement</span></span> | <span data-ttu-id="cee42-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cee42-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee42-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cee42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cee42-122">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cee42-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cee42-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cee42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cee42-124">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="cee42-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="cee42-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cee42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cee42-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="cee42-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee42-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cee42-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee42-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cee42-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

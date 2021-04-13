---
title: Informations de référence sur DirectShow QASF
description: Informations de référence sur DirectShow QASF
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, référence QASF
- Filtres QASF, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382275"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="d3339-107">Informations de référence sur DirectShow QASF</span><span class="sxs-lookup"><span data-stu-id="d3339-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="d3339-108">Cette section contient des références de programmation pour les filtres, interfaces et énumérations QASF DirectShow suivants.</span><span class="sxs-lookup"><span data-stu-id="d3339-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="d3339-109">La documentation du kit de développement logiciel (SDK) DirectShow contient des documents de guide de référence et de programmation pour les interfaces génériques supplémentaires exposées par ces filtres, tels que **IBaseFilter** et **IPIN**, ainsi que pour les versions antérieures des composants qasf.</span><span class="sxs-lookup"><span data-stu-id="d3339-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="d3339-110">Pour obtenir une explication du nom de QASF, consultez [à propos de DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d3339-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="d3339-111">Les filtres suivants sont inclus avec les composants DirectShow QASF.</span><span class="sxs-lookup"><span data-stu-id="d3339-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d3339-112">Filtrer</span><span class="sxs-lookup"><span data-stu-id="d3339-112">Filter</span></span>                                           | <span data-ttu-id="d3339-113">Description</span><span class="sxs-lookup"><span data-stu-id="d3339-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="d3339-114">Filtre de lecteur ASF WM</span><span class="sxs-lookup"><span data-stu-id="d3339-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="d3339-115">Lit et analyse les fichiers ASF locaux ou distants.</span><span class="sxs-lookup"><span data-stu-id="d3339-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="d3339-116">Filtre d’enregistreur ASF WM</span><span class="sxs-lookup"><span data-stu-id="d3339-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="d3339-117">Crée des fichiers ASF à partir de flux d’entrée compressés ou non compressés.</span><span class="sxs-lookup"><span data-stu-id="d3339-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="d3339-118">Les interfaces suivantes sont définies pour une utilisation avec les composants DirectShow QASF.</span><span class="sxs-lookup"><span data-stu-id="d3339-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d3339-119">Interface</span><span class="sxs-lookup"><span data-stu-id="d3339-119">Interface</span></span>                                                  | <span data-ttu-id="d3339-120">Description</span><span class="sxs-lookup"><span data-stu-id="d3339-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3339-121">**IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="d3339-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="d3339-122">Fournit une méthode qui permet aux applications de s’inscrire pour les rappels à partir des broches d’entrée de l' [enregistreur ASF WM](wm-asf-writer-filter.md) ou des broches de sortie du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d3339-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="d3339-123">Utilisé dans l’indexation et lors de l’ajout d’extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="d3339-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="d3339-124">**IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="d3339-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="d3339-125">Implémentée par les applications et appelée par les filtres.</span><span class="sxs-lookup"><span data-stu-id="d3339-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="d3339-126">Les applications utilisent la méthode une sur cette interface pour obtenir des informations sur des échantillons individuels dans le flux.</span><span class="sxs-lookup"><span data-stu-id="d3339-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="d3339-127">Utilisé dans l’indexation et lors de l’ajout d’extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="d3339-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="d3339-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3339-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="d3339-129">Implémenté sur le writer WM ASF.</span><span class="sxs-lookup"><span data-stu-id="d3339-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="d3339-130">Utilisé par les applications pour spécifier des profils et des paramètres d’indexation pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="d3339-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d3339-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3339-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="d3339-132">Fournit des fonctions de configuration supplémentaires sur le writer WM ASF.</span><span class="sxs-lookup"><span data-stu-id="d3339-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="d3339-133">L’énumération, la structure et les événements suivants sont définis pour être utilisés avec les composants DirectShow QASF.</span><span class="sxs-lookup"><span data-stu-id="d3339-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="d3339-134">Énumération</span><span class="sxs-lookup"><span data-stu-id="d3339-134">Enumeration</span></span>                                                               | <span data-ttu-id="d3339-135">Description</span><span class="sxs-lookup"><span data-stu-id="d3339-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3339-136">[\_\_paramètre am ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3339-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="d3339-137">Définit les paramètres de configuration de filtre utilisés dans les méthodes [**IConfigAsfWriter2 :: GetParam**](iconfigasfwriter2-getparam.md) et [**setParam**](iconfigasfwriter2-setparam.md) .</span><span class="sxs-lookup"><span data-stu-id="d3339-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="d3339-138">Structure</span><span class="sxs-lookup"><span data-stu-id="d3339-138">Structure</span></span>                                         | <span data-ttu-id="d3339-139">Description</span><span class="sxs-lookup"><span data-stu-id="d3339-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3339-140">**\_données d' \_ événement \_ WMT AM**</span><span class="sxs-lookup"><span data-stu-id="d3339-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="d3339-141">Contient des informations relatives à un événement d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) et au code d’état associé renvoyé par le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d3339-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="d3339-142">Événement</span><span class="sxs-lookup"><span data-stu-id="d3339-142">Event</span></span>                                           | <span data-ttu-id="d3339-143">Description</span><span class="sxs-lookup"><span data-stu-id="d3339-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3339-144">\_événement EC WMT \_</span><span class="sxs-lookup"><span data-stu-id="d3339-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="d3339-145">Événement transféré à partir du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d3339-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="d3339-146">événement d’index de l’WMT de la EC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d3339-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="d3339-147">Envoyé lorsqu’une application utilise le [writer ASF](wm-asf-writer-filter.md) pour indexer les fichiers Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="d3339-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 
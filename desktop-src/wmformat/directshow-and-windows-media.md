---
title: DirectShow et Windows Media
description: DirectShow et Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675677"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="fb47b-107">DirectShow et Windows Media</span><span class="sxs-lookup"><span data-stu-id="fb47b-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="fb47b-108">En guise d’alternative à l’utilisation du kit de développement logiciel (SDK) Windows Media format exclusivement, les applications peuvent également lire et écrire du contenu Windows Media à l’aide de l’architecture de diffusion en continu Microsoft® DirectShow®, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb47b-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="fb47b-109">Section</span><span class="sxs-lookup"><span data-stu-id="fb47b-109">Section</span></span>                                                                                   | <span data-ttu-id="fb47b-110">Description</span><span class="sxs-lookup"><span data-stu-id="fb47b-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb47b-111">À propos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb47b-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="fb47b-112">Décrit DirectShow en termes généraux et indique où obtenir plus d’informations à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="fb47b-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="fb47b-113">Pourquoi utiliser DirectShow ?</span><span class="sxs-lookup"><span data-stu-id="fb47b-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="fb47b-114">Décrit comment DirectShow simplifie certaines tâches dans la création et la lecture de contenu basé sur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fb47b-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="fb47b-115">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb47b-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="fb47b-116">Décrit comment lire des fichiers ASF à l’aide de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb47b-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="fb47b-117">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb47b-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="fb47b-118">Décrit comment créer des fichiers ASF à l’aide de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb47b-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="fb47b-119">\_Notification d’événement d’État WMT dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb47b-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="fb47b-120">Décrit les événements d' **\_ État WMT** qui sont gérés par le lecteur ASF et les filtres d’écriture ASF, ainsi que la façon dont les applications peuvent recevoir ces événements.</span><span class="sxs-lookup"><span data-stu-id="fb47b-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="fb47b-121">Prise en charge de DRM dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb47b-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="fb47b-122">Décrit comment lire et écrire des fichiers protégés par DRM par le biais de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb47b-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="fb47b-123">Informations de référence sur DirectShow QASF</span><span class="sxs-lookup"><span data-stu-id="fb47b-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="fb47b-124">Contient la documentation de référence pour les composants DirectShow qui prennent en charge Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fb47b-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="fb47b-125">Trois exemples d’applications dans le kit de développement logiciel (SDK) illustrent l’utilisation de DirectShow : DSCopy, DSPlay et DSSeekFM.</span><span class="sxs-lookup"><span data-stu-id="fb47b-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="fb47b-126">Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="fb47b-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="fb47b-127">Les applications qui utilisent les composants QASF inclus dans ce kit de développement logiciel requièrent l’installation du runtime SDK Microsoft DirectX® 8,1 ou version ultérieure sur les systèmes Windows® 2000, Windows 98 et Windows 95.</span><span class="sxs-lookup"><span data-stu-id="fb47b-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="fb47b-128">Plus précisément, ce Runtime est requis par le filtre de wrappers DMO qui héberge les codecs Windows Media dans un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb47b-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 





---
title: Hiérarchisation des flux
description: Hiérarchisation des flux
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, hiérarchisation des flux
- ASF (Advanced Systems Format), hiérarchisation des flux
- ASF (format des systèmes avancés), hiérarchisation des flux
- Windows Media Format SDK, ordre de priorité pour les flux
- ASF (Advanced Systems Format), ordre de priorité pour les flux
- ASF (format des systèmes avancés), ordre de priorité pour les flux
- flux, hiérarchisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030820"
---
# <a name="stream-prioritization"></a><span data-ttu-id="c386f-110">Hiérarchisation des flux</span><span class="sxs-lookup"><span data-stu-id="c386f-110">Stream Prioritization</span></span>

<span data-ttu-id="c386f-111">Lorsque vous créez un fichier ASF, vous pouvez spécifier un ordre de priorité pour ses flux constitutifs.</span><span class="sxs-lookup"><span data-stu-id="c386f-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="c386f-112">Si vous diffusez un fichier classé par ordre de priorité et que la bande passante disponible n’est pas suffisante pour remettre tous les flux, le lecteur supprimera les flux dans l’ordre de priorité inverse.</span><span class="sxs-lookup"><span data-stu-id="c386f-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="c386f-113">De cette façon, vous pouvez vous assurer que les flux les plus importants dans votre fichier ne seront pas supprimés en raison de problèmes réseau.</span><span class="sxs-lookup"><span data-stu-id="c386f-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="c386f-114">La hiérarchisation des flux est configurée avec un objet de priorité de flux et ajoutée au profil.</span><span class="sxs-lookup"><span data-stu-id="c386f-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="c386f-115">Un profil ne peut contenir qu’un seul objet de définition de priorités de flux.</span><span class="sxs-lookup"><span data-stu-id="c386f-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c386f-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c386f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c386f-117">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="c386f-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="c386f-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c386f-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c386f-119">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c386f-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c386f-120">**IWMProfile3::RemoveStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c386f-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="c386f-121">**IWMProfile3::SetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c386f-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c386f-122">**Interface IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c386f-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="c386f-123">**Utilisation de la hiérarchisation des flux**</span><span class="sxs-lookup"><span data-stu-id="c386f-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 





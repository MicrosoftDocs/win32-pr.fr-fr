---
title: Interfaces NDF
description: Les interfaces suivantes peuvent être utilisées pour étendre les fonctionnalités des classes d’assistance Microsoft qui sont identifiées comme extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028483"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="e5ded-103">Interfaces NDF</span><span class="sxs-lookup"><span data-stu-id="e5ded-103">NDF Interfaces</span></span>

<span data-ttu-id="e5ded-104">Les interfaces suivantes peuvent être utilisées pour étendre les fonctionnalités des classes d’assistance Microsoft qui sont identifiées comme extensibles.</span><span class="sxs-lookup"><span data-stu-id="e5ded-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="e5ded-105">Bien que cette fonctionnalité ne soit pas requise pour la plupart des applications, elle peut fournir des diagnostics et des résolutions plus spécifiques dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="e5ded-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="e5ded-106">Ces interfaces et leurs méthodes associées sont destinées aux développeurs qui implémentent leurs propres classes d’assistance tierces qui étendent les fonctionnalités NDF.</span><span class="sxs-lookup"><span data-stu-id="e5ded-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="e5ded-107">Nom de l'interface</span><span class="sxs-lookup"><span data-stu-id="e5ded-107">Interface Name</span></span>                                                 | <span data-ttu-id="e5ded-108">Description</span><span class="sxs-lookup"><span data-stu-id="e5ded-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5ded-109">**INetDiagHelper**</span><span class="sxs-lookup"><span data-stu-id="e5ded-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="e5ded-110">Appelée par l’NDF pour la plupart des activités qui se produisent pendant un diagnostic.</span><span class="sxs-lookup"><span data-stu-id="e5ded-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="e5ded-111">**INetDiagHelperEx**</span><span class="sxs-lookup"><span data-stu-id="e5ded-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="e5ded-112">Appelé par l’NDF pour capturer et fournir des informations associées aux diagnostics et à la résolution des problèmes liés au réseau.</span><span class="sxs-lookup"><span data-stu-id="e5ded-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="e5ded-113">**INetDiagHelperInfo**</span><span class="sxs-lookup"><span data-stu-id="e5ded-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="e5ded-114">Appelé par l’NDF pour confirmer qu’il contient des informations requises</span><span class="sxs-lookup"><span data-stu-id="e5ded-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="e5ded-115">**INetDiagHelperUtilFactory**</span><span class="sxs-lookup"><span data-stu-id="e5ded-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="e5ded-116">Réservé pour le système.</span><span class="sxs-lookup"><span data-stu-id="e5ded-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 





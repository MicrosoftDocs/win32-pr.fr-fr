---
description: L’interface IUpdateSearcher définit les propriétés suivantes.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propriétés IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "104322582"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="6a109-103">Propriétés IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="6a109-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="6a109-104">L’interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a109-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="6a109-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="6a109-105">Property</span></span>                                                                                           | <span data-ttu-id="6a109-106">Description</span><span class="sxs-lookup"><span data-stu-id="6a109-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a109-107">**CanAutomaticallyUpgradeService**</span><span class="sxs-lookup"><span data-stu-id="6a109-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="6a109-108">Obtient et définit une valeur booléenne qui indique si les appels futurs aux méthodes [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) et [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) entraînent une mise à niveau automatique vers Windows Update Agent (WUA).</span><span class="sxs-lookup"><span data-stu-id="6a109-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="6a109-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="6a109-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="6a109-110">Identifie l’application cliente actuelle.</span><span class="sxs-lookup"><span data-stu-id="6a109-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="6a109-111">**IncludePotentiallySupersededUpdates**</span><span class="sxs-lookup"><span data-stu-id="6a109-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="6a109-112">Obtient et définit une valeur booléenne qui indique si les résultats de la recherche incluent des mises à jour qui sont remplacées par d’autres mises à jour dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="6a109-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="6a109-113">**En ligne**</span><span class="sxs-lookup"><span data-stu-id="6a109-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="6a109-114">Obtient et définit une valeur booléenne qui indique si le [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se met en ligne pour rechercher des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="6a109-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="6a109-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="6a109-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="6a109-116">Obtient et définit un site à rechercher lorsque le site à rechercher n’est pas un site Windows Update.</span><span class="sxs-lookup"><span data-stu-id="6a109-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="6a109-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="6a109-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="6a109-118">Obtient et définit une valeur [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) qui indique le serveur dans lequel Rechercher des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="6a109-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 




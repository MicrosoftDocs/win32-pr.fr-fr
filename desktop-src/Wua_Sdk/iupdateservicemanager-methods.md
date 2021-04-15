---
description: L’interface IUpdateServiceManager définit les méthodes suivantes.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Méthodes IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525084"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="2dd3d-103">Méthodes IUpdateServiceManager</span><span class="sxs-lookup"><span data-stu-id="2dd3d-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="2dd3d-104">L’interface [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="2dd3d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="2dd3d-105">Method</span></span>                                                                           | <span data-ttu-id="2dd3d-106">Description</span><span class="sxs-lookup"><span data-stu-id="2dd3d-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dd3d-107">**AddScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="2dd3d-108">Inscrit un package d’analyse en tant que service avec Windows Update Agent (WUA), puis retourne une interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .</span><span class="sxs-lookup"><span data-stu-id="2dd3d-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="2dd3d-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="2dd3d-110">Inscrit un service auprès de WUA.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="2dd3d-111">**RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="2dd3d-112">Inscrit un service avec Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="2dd3d-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="2dd3d-114">Supprime une inscription de service de WUA.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="2dd3d-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="2dd3d-116">Définit des options pour l’objet qui spécifie l’ID de service, et indique s’il faut afficher un avertissement lors de la modification de l’inscription de Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="2dd3d-117">**UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="2dd3d-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="2dd3d-118">Annule l’inscription d’un service avec Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="2dd3d-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 




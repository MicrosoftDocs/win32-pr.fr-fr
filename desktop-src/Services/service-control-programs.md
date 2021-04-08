---
description: Un programme de contrôle de service démarre et contrôle les services.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programmes de contrôle de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862382"
---
# <a name="service-control-programs"></a><span data-ttu-id="eae86-103">Programmes de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="eae86-103">Service Control Programs</span></span>

<span data-ttu-id="eae86-104">Un programme de contrôle de service démarre et contrôle les services.</span><span class="sxs-lookup"><span data-stu-id="eae86-104">A service control program starts and controls services.</span></span> <span data-ttu-id="eae86-105">Il effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="eae86-105">It performs the following actions:</span></span>

-   <span data-ttu-id="eae86-106">Démarre un service ou un service de pilote, si le type de démarrage est \_ démarrage de la demande de service \_ .</span><span class="sxs-lookup"><span data-stu-id="eae86-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="eae86-107">Envoie des demandes de contrôle à un service en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eae86-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="eae86-108">Interroge l’état actuel d’un service en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eae86-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="eae86-109">Ces actions requièrent un handle ouvert pour l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="eae86-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="eae86-110">Pour obtenir le descripteur, le programme de contrôle des services doit :</span><span class="sxs-lookup"><span data-stu-id="eae86-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="eae86-111">Utilisez la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour obtenir un descripteur de la base de données SCM sur une machine spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eae86-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="eae86-112">Utilisez la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour obtenir un handle de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="eae86-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="eae86-113">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="eae86-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="eae86-114">Démarrage du service</span><span class="sxs-lookup"><span data-stu-id="eae86-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="eae86-115">Demandes de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="eae86-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="eae86-116">Contrôle d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="eae86-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 




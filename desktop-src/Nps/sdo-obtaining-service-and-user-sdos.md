---
title: Obtention des SDOs de service et d’utilisateur
description: Pour obtenir SDOs pour NPS (IAS) ou un utilisateur particulier, appelez les méthodes ISdoMachine GetServiceSDO ou ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315713"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="754f0-103">Obtention des SDOs de service et d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="754f0-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="754f0-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="754f0-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="754f0-105">Pour obtenir SDOs pour NPS (IAS) ou un utilisateur particulier, appelez les méthodes [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) .</span><span class="sxs-lookup"><span data-stu-id="754f0-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="754f0-106">Ces méthodes retournent des pointeurs vers des interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="754f0-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="754f0-107">Pour l’utilisateur SDO, utilisez la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="754f0-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="754f0-108">Pour le service SDO, utilisez **IUnknown :: QueryInterface** pour obtenir une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) ou une interface [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="754f0-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="754f0-109">Avant d’appeler [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), appelez [**ISdoMachine :: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) pour associer l’objet ordinateur à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="754f0-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="754f0-110">Consultez [récupération d’un SDO de service](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) et [récupération d’un utilisateur SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) pour obtenir un exemple de code qui montre comment obtenir ces SDOs.</span><span class="sxs-lookup"><span data-stu-id="754f0-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 
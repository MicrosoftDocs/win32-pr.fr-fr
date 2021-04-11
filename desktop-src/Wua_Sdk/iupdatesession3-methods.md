---
description: L’interface IUpdateSession3 définit les méthodes suivantes.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Méthodes IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112159"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="3d01a-103">Méthodes IUpdateSession3</span><span class="sxs-lookup"><span data-stu-id="3d01a-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="3d01a-104">L’interface [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d01a-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="3d01a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3d01a-105">Method</span></span>                                                                           | <span data-ttu-id="3d01a-106">Description</span><span class="sxs-lookup"><span data-stu-id="3d01a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d01a-107">**CreateUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="3d01a-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="3d01a-108">Retourne un pointeur vers une interface [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) pour la session.</span><span class="sxs-lookup"><span data-stu-id="3d01a-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="3d01a-109">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="3d01a-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="3d01a-110">Retourne un pointeur vers une interface [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) .</span><span class="sxs-lookup"><span data-stu-id="3d01a-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="3d01a-111">L’interface contient des enregistrements d’événements correspondants sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3d01a-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="3d01a-112">Cela amène la méthode [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) à interroger de manière synchrone l’ordinateur sur l’historique des événements de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3d01a-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="3d01a-113">Pour plus d’informations sur les membres hérités par cette interface, consultez les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d01a-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="3d01a-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="3d01a-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="3d01a-115">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="3d01a-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 




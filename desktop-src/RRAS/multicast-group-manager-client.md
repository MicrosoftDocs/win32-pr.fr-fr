---
title: Client du gestionnaire de groupe de multidiffusion
description: Un client est une entité qui appelle une fonction MGM, telle qu’un protocole de routage ou une application administrative.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675577"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="75155-103">Client du gestionnaire de groupe de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="75155-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="75155-104">Un client est une entité qui appelle une fonction MGM, telle qu’un protocole de routage ou une application administrative.</span><span class="sxs-lookup"><span data-stu-id="75155-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="75155-105">L’API MGM est principalement utilisée par les protocoles de routage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="75155-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="75155-106">Les développeurs de protocoles de routage de multidiffusion utilisent l’API MGM pour :</span><span class="sxs-lookup"><span data-stu-id="75155-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="75155-107">Tenir à jour l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="75155-107">Maintain group membership</span></span>
-   <span data-ttu-id="75155-108">Contrôle de la propriété de l’interface</span><span class="sxs-lookup"><span data-stu-id="75155-108">Control interface ownership</span></span>
-   <span data-ttu-id="75155-109">Recevoir des notifications du gestionnaire de groupe de multidiffusion concernant les demandes de données multidiffusion de protocoles de routage de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="75155-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="75155-110">Les applications d’administration spécifiques qui doivent surveiller les entrées de transfert de multidiffusion (MFEs) peuvent le faire sans ajouter ou supprimer l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="75155-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="75155-111">Les développeurs d’applications administratives utilisent des fonctions MGM spécifiques pour examiner les informations dans MFEs.</span><span class="sxs-lookup"><span data-stu-id="75155-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="75155-112">Les protocoles de routage de multidiffusion accèdent également à MFEs.</span><span class="sxs-lookup"><span data-stu-id="75155-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="75155-113">Un MFE transmet des informations que le gestionnaire de groupe de multidiffusion crée en fonction de l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="75155-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="75155-114">Les MFEs récupérés à partir du gestionnaire de groupe de multidiffusion peuvent fournir des informations statistiques.</span><span class="sxs-lookup"><span data-stu-id="75155-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="75155-115">Une application administrative peut ensuite utiliser ces informations pour déterminer les actions appropriées.</span><span class="sxs-lookup"><span data-stu-id="75155-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="75155-116">Par exemple, une application administrative peut effectuer des actions basées sur le volume de paquets sur une interface spécifique.</span><span class="sxs-lookup"><span data-stu-id="75155-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 





---
title: Comprendre les fonctions et les en-têtes d’informations MprInfo
description: Les fonctions suivantes requièrent que l’appelant passe une structure ou un en-tête d’informations comme l’un des paramètres.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940027"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="e0423-103">Comprendre les fonctions et les en-têtes d’informations MprInfo</span><span class="sxs-lookup"><span data-stu-id="e0423-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="e0423-104">Les fonctions suivantes requièrent que l’appelant passe une structure ou un *en-tête* d’informations comme l’un des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e0423-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="e0423-105">Fonction d’administration</span><span class="sxs-lookup"><span data-stu-id="e0423-105">Administration function</span></span>                                                        | <span data-ttu-id="e0423-106">Fonction de configuration</span><span class="sxs-lookup"><span data-stu-id="e0423-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0423-107">Aucune fonction d’administration</span><span class="sxs-lookup"><span data-stu-id="e0423-107">No administration function</span></span>                                                     | [<span data-ttu-id="e0423-108">**MprConfigTransportCreate**</span><span class="sxs-lookup"><span data-stu-id="e0423-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="e0423-109">**MprAdminTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="e0423-110">**MprConfigTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="e0423-111">**MprAdminInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="e0423-112">**MprConfigInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="e0423-113">**MprAdminInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="e0423-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="e0423-114">**MprConfigInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="e0423-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="e0423-115">De même, les fonctions suivantes retournent des en-têtes d’informations.</span><span class="sxs-lookup"><span data-stu-id="e0423-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="e0423-116">Fonction d’administration</span><span class="sxs-lookup"><span data-stu-id="e0423-116">Administration function</span></span>                                                        | <span data-ttu-id="e0423-117">Fonction de configuration</span><span class="sxs-lookup"><span data-stu-id="e0423-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="e0423-118">**MprAdminTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="e0423-119">**MprConfigTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="e0423-120">**MprAdminInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="e0423-121">**MprConfigInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0423-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="e0423-122">Pour les fonctions de transport, l’en-tête d’informations contient des informations globales pour le transport.</span><span class="sxs-lookup"><span data-stu-id="e0423-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="e0423-123">Pour les fonctions client (InterfaceTransport), l’en-tête contient des informations spécifiques au client (par exemple, OSPF) en cours de gestion.</span><span class="sxs-lookup"><span data-stu-id="e0423-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="e0423-124">Les en-têtes d’informations et leur contenu doivent être manipulés uniquement à l’aide des fonctions [MprInfo](router-information-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="e0423-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="e0423-125">Les développeurs ne doivent pas tenter de manipuler directement le contenu des en-têtes d’informations.</span><span class="sxs-lookup"><span data-stu-id="e0423-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="e0423-126">Les fonctions d’interface uniquement, telles que [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , ne nécessitent pas l’utilisation de fonctions MprInfo.</span><span class="sxs-lookup"><span data-stu-id="e0423-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="e0423-127">Les informations qui sont passées et retournées avec ces fonctions sont toujours sous la forme d’une structure d' [**\_ interface MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .</span><span class="sxs-lookup"><span data-stu-id="e0423-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 





---
description: Si votre fournisseur de réseau doit prendre en charge l’exploration de ses ressources réseau, il doit implémenter les fonctions suivantes. MPR appelle ces fonctions pour énumérer les ressources.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Fonctions d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033922"
---
# <a name="enumeration-functions"></a><span data-ttu-id="03e17-104">Fonctions d’énumération</span><span class="sxs-lookup"><span data-stu-id="03e17-104">Enumeration Functions</span></span>

<span data-ttu-id="03e17-105">Si votre fournisseur de réseau doit prendre en charge l’exploration de ses ressources réseau, il doit implémenter les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="03e17-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="03e17-106">MPR appelle ces fonctions pour énumérer les ressources.</span><span class="sxs-lookup"><span data-stu-id="03e17-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="03e17-107">Un fournisseur réseau n’est pas tenu d’implémenter les fonctions d’énumération.</span><span class="sxs-lookup"><span data-stu-id="03e17-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="03e17-108">Toutefois, si un fournisseur de réseau implémente [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)ou [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), il doit également implémenter les deux autres fonctions d’énumération.</span><span class="sxs-lookup"><span data-stu-id="03e17-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="03e17-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="03e17-109">Function</span></span>                                                     | <span data-ttu-id="03e17-110">Description</span><span class="sxs-lookup"><span data-stu-id="03e17-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03e17-111">**NPOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="03e17-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="03e17-112">Ouvre une énumération des ressources réseau ou des connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="03e17-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="03e17-113">**NPEnumResource**</span><span class="sxs-lookup"><span data-stu-id="03e17-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="03e17-114">Effectue une énumération sur un handle retourné par [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span><span class="sxs-lookup"><span data-stu-id="03e17-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="03e17-115">**NPCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="03e17-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="03e17-116">Ferme une énumération.</span><span class="sxs-lookup"><span data-stu-id="03e17-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="03e17-117">**NPGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="03e17-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="03e17-118">Détermine si le fournisseur est le fournisseur correct pour répondre à une demande pour une ressource réseau spécifiée et retourne des informations sur le type de la ressource.</span><span class="sxs-lookup"><span data-stu-id="03e17-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="03e17-119">**NPGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="03e17-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="03e17-120">Retourne le parent d’une ressource réseau spécifiée dans la hiérarchie de navigation.</span><span class="sxs-lookup"><span data-stu-id="03e17-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 




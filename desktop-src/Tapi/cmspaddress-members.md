---
description: La liste suivante contient les membres d’adresse CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membres CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869201"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="c1acc-103">Membres CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="c1acc-103">CMSPAddress Members</span></span>



| <span data-ttu-id="c1acc-104">Types de membres</span><span class="sxs-lookup"><span data-stu-id="c1acc-104">Member types</span></span>                    | <span data-ttu-id="c1acc-105">Nom</span><span class="sxs-lookup"><span data-stu-id="c1acc-105">Name</span></span>                    | <span data-ttu-id="c1acc-106">Description</span><span class="sxs-lookup"><span data-stu-id="c1acc-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1acc-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1acc-107">Iunknown</span></span>                        | <span data-ttu-id="c1acc-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="c1acc-108">\*m\_pFTM</span></span>               | <span data-ttu-id="c1acc-109">Pointeur vers le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="c1acc-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="c1acc-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="c1acc-110">HANDLE</span></span>                          | <span data-ttu-id="c1acc-111">m \_ htEvent</span><span class="sxs-lookup"><span data-stu-id="c1acc-111">m\_htEvent</span></span>              | <span data-ttu-id="c1acc-112">Handle de l’événement de Tapi3.dll, qui est utilisé pour notifier l’interface TAPI que le MSP souhaite lui envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="c1acc-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="c1acc-113">entrée de liste \_</span><span class="sxs-lookup"><span data-stu-id="c1acc-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="c1acc-114">m \_ EventList</span><span class="sxs-lookup"><span data-stu-id="c1acc-114">m\_EventList</span></span>            | <span data-ttu-id="c1acc-115">Liste des événements.</span><span class="sxs-lookup"><span data-stu-id="c1acc-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="c1acc-116">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="c1acc-116">CMSPCritSection</span></span>                 | <span data-ttu-id="c1acc-117">m \_ EventDataLock</span><span class="sxs-lookup"><span data-stu-id="c1acc-117">m\_EventDataLock</span></span>        | <span data-ttu-id="c1acc-118">Verrou qui protège les données relatives à la gestion des événements avec l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="c1acc-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="c1acc-119">ITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="c1acc-119">ITTerminalManager</span></span>               | <span data-ttu-id="c1acc-120">\*m \_ pITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="c1acc-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="c1acc-121">Pointeur vers l’objet du gestionnaire de terminal.</span><span class="sxs-lookup"><span data-stu-id="c1acc-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="c1acc-122">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="c1acc-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="c1acc-123">\_terminaux m</span><span class="sxs-lookup"><span data-stu-id="c1acc-123">m\_Terminals</span></span>            | <span data-ttu-id="c1acc-124">Liste des terminaux statiques qui peuvent être utilisés sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="c1acc-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="c1acc-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="c1acc-125">BOOL</span></span>                            | <span data-ttu-id="c1acc-126">m \_ fTerminalsUpToDate</span><span class="sxs-lookup"><span data-stu-id="c1acc-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="c1acc-127">Cet indicateur a la **valeur true** si la liste des terminaux est à jour.</span><span class="sxs-lookup"><span data-stu-id="c1acc-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="c1acc-128">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="c1acc-128">CMSPCritSection</span></span>                 | <span data-ttu-id="c1acc-129">m \_ TerminalDataLock</span><span class="sxs-lookup"><span data-stu-id="c1acc-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="c1acc-130">Verrou qui protège les membres de données liés aux terminaux.</span><span class="sxs-lookup"><span data-stu-id="c1acc-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 




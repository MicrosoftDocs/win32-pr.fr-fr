---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381876"
---
# <a name="iagentuserinput"></a><span data-ttu-id="fa461-103">IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="fa461-103">IAgentUserInput</span></span>

<span data-ttu-id="fa461-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa461-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fa461-105">Lorsque le serveur notifie le client d’entrée-actif avec [**IAgentNotifySink :: Command**](iagentnotifysink--command.md), il retourne des informations par le biais de l’objet [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="fa461-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="fa461-106">**IAgentUserInput** définit une interface qui permet aux applications d’interroger ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="fa461-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="fa461-107">**Méthodes dans l'ordre Vtable**</span><span class="sxs-lookup"><span data-stu-id="fa461-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="fa461-108">Méthodes IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="fa461-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="fa461-109">Description</span><span class="sxs-lookup"><span data-stu-id="fa461-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa461-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="fa461-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="fa461-111">Retourne le nombre d’autres commandes retournées dans un événement de [**commande**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="fa461-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="fa461-112">**GetItemID**</span><span class="sxs-lookup"><span data-stu-id="fa461-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="fa461-113">Retourne l’ID d’une autre [**commande**](command-event.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="fa461-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="fa461-114">**GetItemConfidence**</span><span class="sxs-lookup"><span data-stu-id="fa461-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="fa461-115">Retourne la valeur de la propriété [**confidence**](confidence-property.md) pour une alternative de [**commande**](command-event.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="fa461-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="fa461-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="fa461-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="fa461-117">Retourne la valeur du texte [**vocal**](voice-property.md) pour une autre [**commande**](command-event.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="fa461-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="fa461-118">**GetAllItemData**</span><span class="sxs-lookup"><span data-stu-id="fa461-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="fa461-119">Retourne les données pour toutes les autres [**commandes**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="fa461-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 
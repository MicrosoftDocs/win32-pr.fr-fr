---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031162"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="bc755-103">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="bc755-103">IAgentNotifySink</span></span>

<span data-ttu-id="bc755-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc755-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bc755-105">IAgentNotifySink notifie les clients lorsque certains changements d’État se produisent.</span><span class="sxs-lookup"><span data-stu-id="bc755-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="bc755-106">Ces fonctions sont également disponibles à partir de [IAgentNotifySinkEx](iagentnotifysinkex.md).</span><span class="sxs-lookup"><span data-stu-id="bc755-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="bc755-107">**Méthodes dans l'ordre Vtable**</span><span class="sxs-lookup"><span data-stu-id="bc755-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="bc755-108">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="bc755-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="bc755-109">Description</span><span class="sxs-lookup"><span data-stu-id="bc755-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc755-110">**Commande**</span><span class="sxs-lookup"><span data-stu-id="bc755-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="bc755-111">Se produit lorsque le serveur traite une commande définie par le client.</span><span class="sxs-lookup"><span data-stu-id="bc755-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="bc755-112">**ActivateInputState**</span><span class="sxs-lookup"><span data-stu-id="bc755-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="bc755-113">Se produit lorsqu’un caractère devient ou cesse d’être actif.</span><span class="sxs-lookup"><span data-stu-id="bc755-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="bc755-114">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="bc755-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="bc755-115">Se produit lorsque l’état **visible** du caractère change.</span><span class="sxs-lookup"><span data-stu-id="bc755-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="bc755-116">**Événement clic**</span><span class="sxs-lookup"><span data-stu-id="bc755-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="bc755-117">Se produit lors d’un clic sur un caractère.</span><span class="sxs-lookup"><span data-stu-id="bc755-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="bc755-118">**DblClick, événement**</span><span class="sxs-lookup"><span data-stu-id="bc755-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="bc755-119">Se produit lors d’un double-clic sur un caractère.</span><span class="sxs-lookup"><span data-stu-id="bc755-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="bc755-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="bc755-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="bc755-121">Se produit lorsqu’un utilisateur commence à faire glisser un caractère.</span><span class="sxs-lookup"><span data-stu-id="bc755-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="bc755-122">**DragComplete**</span><span class="sxs-lookup"><span data-stu-id="bc755-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="bc755-123">Se produit lorsqu’un utilisateur arrête de faire glisser un caractère.</span><span class="sxs-lookup"><span data-stu-id="bc755-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="bc755-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="bc755-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="bc755-125">Se produit lorsque le serveur commence à traiter un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="bc755-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="bc755-126">**RequestComplete**</span><span class="sxs-lookup"><span data-stu-id="bc755-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="bc755-127">Se produit lorsque le serveur termine le traitement d’un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="bc755-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="bc755-128">**Signet**</span><span class="sxs-lookup"><span data-stu-id="bc755-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="bc755-129">Se produit lorsque le serveur traite un signet.</span><span class="sxs-lookup"><span data-stu-id="bc755-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="bc755-130">**Périodes**</span><span class="sxs-lookup"><span data-stu-id="bc755-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="bc755-131">Se produit lorsque le serveur démarre ou termine le traitement de l’inactivité.</span><span class="sxs-lookup"><span data-stu-id="bc755-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="bc755-132">**Activer**</span><span class="sxs-lookup"><span data-stu-id="bc755-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="bc755-133">Se produit lorsqu’un caractère a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="bc755-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="bc755-134">**Taille**</span><span class="sxs-lookup"><span data-stu-id="bc755-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="bc755-135">Se produit lorsqu’un caractère a été redimensionné.</span><span class="sxs-lookup"><span data-stu-id="bc755-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="bc755-136">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="bc755-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="bc755-137">Se produit lorsque l’état de visibilité de la bulle de texte d’un caractère change.</span><span class="sxs-lookup"><span data-stu-id="bc755-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="bc755-138">Les événements IAgentNotifySink :: restart et IAgentNotifySink :: Shutdown, pris en charge dans les versions antérieures de Microsoft Agent, sont désormais obsolètes.</span><span class="sxs-lookup"><span data-stu-id="bc755-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="bc755-139">Bien qu’pris en charge pour la compatibilité descendante, le serveur n’envoie plus ces événements.</span><span class="sxs-lookup"><span data-stu-id="bc755-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 
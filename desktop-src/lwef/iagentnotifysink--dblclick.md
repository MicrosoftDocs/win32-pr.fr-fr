---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120922"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="e6cd7-103">IAgentNotifySink ::D blClick</span><span class="sxs-lookup"><span data-stu-id="e6cd7-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="e6cd7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6cd7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="e6cd7-105">Avertit une application cliente lorsque l’utilisateur double-clique sur un caractère.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="e6cd7-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="e6cd7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="e6cd7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="e6cd7-108">Identificateur du caractère double-cliqué.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="e6cd7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="e6cd7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="e6cd7-110">Paramètre qui indique le bouton de la souris et l’état de la touche de modification.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="e6cd7-111">Le paramètre peut retourner n’importe quelle combinaison des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e6cd7-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="e6cd7-112">Value</span><span class="sxs-lookup"><span data-stu-id="e6cd7-112">Value</span></span>  | <span data-ttu-id="e6cd7-113">Description</span><span class="sxs-lookup"><span data-stu-id="e6cd7-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="e6cd7-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="e6cd7-114">0x0001</span></span> | <span data-ttu-id="e6cd7-115">Bouton gauche</span><span class="sxs-lookup"><span data-stu-id="e6cd7-115">Left Button</span></span>                                    |
| <span data-ttu-id="e6cd7-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="e6cd7-116">0x0010</span></span> | <span data-ttu-id="e6cd7-117">Bouton central</span><span class="sxs-lookup"><span data-stu-id="e6cd7-117">Middle Button</span></span>                                  |
| <span data-ttu-id="e6cd7-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="e6cd7-118">0x0002</span></span> | <span data-ttu-id="e6cd7-119">Bouton droit</span><span class="sxs-lookup"><span data-stu-id="e6cd7-119">Right Button</span></span>                                   |
| <span data-ttu-id="e6cd7-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="e6cd7-120">0x0004</span></span> | <span data-ttu-id="e6cd7-121">Touche Maj enfoncée</span><span class="sxs-lookup"><span data-stu-id="e6cd7-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="e6cd7-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="e6cd7-122">0x0008</span></span> | <span data-ttu-id="e6cd7-123">Touche CTRL enfoncée</span><span class="sxs-lookup"><span data-stu-id="e6cd7-123">Control Key Down</span></span>                               |
| <span data-ttu-id="e6cd7-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="e6cd7-124">0x0020</span></span> | <span data-ttu-id="e6cd7-125">Touche Alt enfoncée</span><span class="sxs-lookup"><span data-stu-id="e6cd7-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="e6cd7-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="e6cd7-126">0x1000</span></span> | <span data-ttu-id="e6cd7-127">Un événement s’est produit sur l’icône de la barre des tâches du caractère</span><span class="sxs-lookup"><span data-stu-id="e6cd7-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="e6cd7-128"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e6cd7-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="e6cd7-129">Coordonnée x du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="e6cd7-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="e6cd7-130"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="e6cd7-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="e6cd7-131">Coordonnée y du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="e6cd7-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="e6cd7-132">Cet événement est envoyé au client d’entrée-actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="e6cd7-133">Si aucun des clients du caractère n’est en entrée-actif, le serveur notifie le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="e6cd7-134">Si le caractère est visible, le serveur rend également ce client en entrée-actif et envoie [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="e6cd7-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="e6cd7-135">Si le caractère est masqué, le caractère s’affiche également automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e6cd7-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 





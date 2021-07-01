---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120823"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="b15a2-103">IAgentNotifySink ::D ragStart</span><span class="sxs-lookup"><span data-stu-id="b15a2-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="b15a2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b15a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="b15a2-105">Avertit une application cliente lorsque l’utilisateur commence à faire glisser un caractère.</span><span class="sxs-lookup"><span data-stu-id="b15a2-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="b15a2-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b15a2-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b15a2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b15a2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b15a2-108">Identificateur du caractère déplacé.</span><span class="sxs-lookup"><span data-stu-id="b15a2-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="b15a2-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="b15a2-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="b15a2-110">Paramètre qui indique le bouton de la souris et l’état de la touche de modification.</span><span class="sxs-lookup"><span data-stu-id="b15a2-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="b15a2-111">Le paramètre peut retourner n’importe quelle combinaison des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b15a2-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="b15a2-112">Value</span><span class="sxs-lookup"><span data-stu-id="b15a2-112">Value</span></span>  | <span data-ttu-id="b15a2-113">Description</span><span class="sxs-lookup"><span data-stu-id="b15a2-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="b15a2-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="b15a2-114">0x0001</span></span> | <span data-ttu-id="b15a2-115">Bouton gauche</span><span class="sxs-lookup"><span data-stu-id="b15a2-115">Left Button</span></span>      |
| <span data-ttu-id="b15a2-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="b15a2-116">0x0010</span></span> | <span data-ttu-id="b15a2-117">Bouton central</span><span class="sxs-lookup"><span data-stu-id="b15a2-117">Middle Button</span></span>    |
| <span data-ttu-id="b15a2-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="b15a2-118">0x0002</span></span> | <span data-ttu-id="b15a2-119">Bouton droit</span><span class="sxs-lookup"><span data-stu-id="b15a2-119">Right Button</span></span>     |
| <span data-ttu-id="b15a2-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="b15a2-120">0x0004</span></span> | <span data-ttu-id="b15a2-121">Touche Maj enfoncée</span><span class="sxs-lookup"><span data-stu-id="b15a2-121">Shift Key Down</span></span>   |
| <span data-ttu-id="b15a2-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="b15a2-122">0x0008</span></span> | <span data-ttu-id="b15a2-123">Touche CTRL enfoncée</span><span class="sxs-lookup"><span data-stu-id="b15a2-123">Control Key Down</span></span> |
| <span data-ttu-id="b15a2-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="b15a2-124">0x0020</span></span> | <span data-ttu-id="b15a2-125">Touche Alt enfoncée</span><span class="sxs-lookup"><span data-stu-id="b15a2-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="b15a2-126"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b15a2-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b15a2-127">Coordonnée x du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="b15a2-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b15a2-128"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b15a2-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b15a2-129">Coordonnée y du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="b15a2-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 





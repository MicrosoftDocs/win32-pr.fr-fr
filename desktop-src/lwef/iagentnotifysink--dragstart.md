---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310078"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="77598-103">IAgentNotifySink ::D ragStart</span><span class="sxs-lookup"><span data-stu-id="77598-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="77598-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77598-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="77598-105">Avertit une application cliente lorsque l’utilisateur commence à faire glisser un caractère.</span><span class="sxs-lookup"><span data-stu-id="77598-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="77598-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="77598-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="77598-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="77598-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="77598-108">Identificateur du caractère déplacé.</span><span class="sxs-lookup"><span data-stu-id="77598-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="77598-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="77598-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="77598-110">Paramètre qui indique le bouton de la souris et l’état de la touche de modification.</span><span class="sxs-lookup"><span data-stu-id="77598-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="77598-111">Le paramètre peut retourner n’importe quelle combinaison des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="77598-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="77598-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="77598-112">0x0001</span></span> | <span data-ttu-id="77598-113">Bouton gauche</span><span class="sxs-lookup"><span data-stu-id="77598-113">Left Button</span></span>      |
| <span data-ttu-id="77598-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="77598-114">0x0010</span></span> | <span data-ttu-id="77598-115">Bouton central</span><span class="sxs-lookup"><span data-stu-id="77598-115">Middle Button</span></span>    |
| <span data-ttu-id="77598-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="77598-116">0x0002</span></span> | <span data-ttu-id="77598-117">Bouton droit</span><span class="sxs-lookup"><span data-stu-id="77598-117">Right Button</span></span>     |
| <span data-ttu-id="77598-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="77598-118">0x0004</span></span> | <span data-ttu-id="77598-119">Touche Maj enfoncée</span><span class="sxs-lookup"><span data-stu-id="77598-119">Shift Key Down</span></span>   |
| <span data-ttu-id="77598-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="77598-120">0x0008</span></span> | <span data-ttu-id="77598-121">Touche CTRL enfoncée</span><span class="sxs-lookup"><span data-stu-id="77598-121">Control Key Down</span></span> |
| <span data-ttu-id="77598-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="77598-122">0x0020</span></span> | <span data-ttu-id="77598-123">Touche Alt enfoncée</span><span class="sxs-lookup"><span data-stu-id="77598-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="77598-124"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="77598-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="77598-125">Coordonnée x du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="77598-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="77598-126"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="77598-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="77598-127">Coordonnée y du pointeur de la souris en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="77598-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 





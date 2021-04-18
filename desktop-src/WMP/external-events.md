---
title: Événements externes
description: Événements externes
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Apparences du lecteur Windows Media, événements externes
- apparences, événements externes
- événements, externes
- écriture de code pour les apparences, événements externes
- événements externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512275"
---
# <a name="external-events"></a><span data-ttu-id="94a76-108">Événements externes</span><span class="sxs-lookup"><span data-stu-id="94a76-108">External Events</span></span>

<span data-ttu-id="94a76-109">Lorsque les utilisateurs cliquent sur un bouton ou appuient sur une touche, vous pouvez répondre à leur entrée à l’aide de gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="94a76-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="94a76-110">Un gestionnaire d’événements est une section de code qui s’exécute chaque fois que l’événement est déclenché.</span><span class="sxs-lookup"><span data-stu-id="94a76-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="94a76-111">Les événements suivants sont pris en charge par les éléments d’apparence :</span><span class="sxs-lookup"><span data-stu-id="94a76-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="94a76-112">**load**</span><span class="sxs-lookup"><span data-stu-id="94a76-112">**load**</span></span>
-   <span data-ttu-id="94a76-113">**close**</span><span class="sxs-lookup"><span data-stu-id="94a76-113">**close**</span></span>
-   <span data-ttu-id="94a76-114">**redimensionner**</span><span class="sxs-lookup"><span data-stu-id="94a76-114">**resize**</span></span>
-   <span data-ttu-id="94a76-115">**minute**</span><span class="sxs-lookup"><span data-stu-id="94a76-115">**timer**</span></span>
-   <span data-ttu-id="94a76-116">**Cliquez sur**</span><span class="sxs-lookup"><span data-stu-id="94a76-116">**click**</span></span>
-   <span data-ttu-id="94a76-117">**dblclick**</span><span class="sxs-lookup"><span data-stu-id="94a76-117">**dblclick**</span></span>
-   <span data-ttu-id="94a76-118">**error**</span><span class="sxs-lookup"><span data-stu-id="94a76-118">**error**</span></span>
-   <span data-ttu-id="94a76-119">**mousedown**</span><span class="sxs-lookup"><span data-stu-id="94a76-119">**mousedown**</span></span>
-   <span data-ttu-id="94a76-120">**mouseup**</span><span class="sxs-lookup"><span data-stu-id="94a76-120">**mouseup**</span></span>
-   <span data-ttu-id="94a76-121">**mousemove**</span><span class="sxs-lookup"><span data-stu-id="94a76-121">**mousemove**</span></span>
-   <span data-ttu-id="94a76-122">**mouseover**</span><span class="sxs-lookup"><span data-stu-id="94a76-122">**mouseover**</span></span>
-   <span data-ttu-id="94a76-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="94a76-123">**mouseout**</span></span>
-   <span data-ttu-id="94a76-124">**keypress**</span><span class="sxs-lookup"><span data-stu-id="94a76-124">**keypress**</span></span>
-   <span data-ttu-id="94a76-125">**keydown**</span><span class="sxs-lookup"><span data-stu-id="94a76-125">**keydown**</span></span>
-   <span data-ttu-id="94a76-126">**keyup**</span><span class="sxs-lookup"><span data-stu-id="94a76-126">**keyup**</span></span>

<span data-ttu-id="94a76-127">Pour plus d’informations sur les événements spécifiques, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="94a76-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="94a76-128">Un gestionnaire d’événements externes type nomme l’événement et définit le code qui s’exécute.</span><span class="sxs-lookup"><span data-stu-id="94a76-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="94a76-129">Par exemple, si vous souhaitez créer du code pour démarrer le lecteur Windows Media quand l’utilisateur clique sur un bouton, vous devez placer la ligne suivante dans votre code de bouton.</span><span class="sxs-lookup"><span data-stu-id="94a76-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="94a76-130">Cela permet de lire le fichier nommé Laure. WMA.</span><span class="sxs-lookup"><span data-stu-id="94a76-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="94a76-131">Notez que vous ajoutez le mot « on » à des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="94a76-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94a76-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94a76-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a76-133">**Gestion des événements**</span><span class="sxs-lookup"><span data-stu-id="94a76-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 





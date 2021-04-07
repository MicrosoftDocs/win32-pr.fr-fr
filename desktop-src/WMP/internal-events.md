---
title: Événements internes
description: Événements internes
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Apparences du lecteur Windows Media, événements internes
- apparences, événements internes
- événements, internes
- écriture de code pour les apparences, événements internes
- événements internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939748"
---
# <a name="internal-events"></a><span data-ttu-id="a8d30-108">Événements internes</span><span class="sxs-lookup"><span data-stu-id="a8d30-108">Internal Events</span></span>

<span data-ttu-id="a8d30-109">Vous pouvez détecter les modifications qui se produisent dans le lecteur Windows Media ou les modifications apportées à votre propre apparence.</span><span class="sxs-lookup"><span data-stu-id="a8d30-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="a8d30-110">Ces modifications peuvent être apportées aux propriétés ou méthodes de l’objet lecteur Windows Media, aux modifications apportées aux attributs d’apparence, etc.</span><span class="sxs-lookup"><span data-stu-id="a8d30-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="a8d30-111">Modifications des propriétés du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="a8d30-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="a8d30-112">Vous pouvez traiter les modifications dans le lecteur Windows Media à l’aide de l’écouteur wmpprop.</span><span class="sxs-lookup"><span data-stu-id="a8d30-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="a8d30-113">Vous devez configurer l’écouteur en tant que valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="a8d30-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="a8d30-114">Placez la valeur entre guillemets doubles et commencez par le mot « wmpprop » suivi d’un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="a8d30-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="a8d30-115">Vous incluez ensuite la propriété que vous souhaitez écouter.</span><span class="sxs-lookup"><span data-stu-id="a8d30-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="a8d30-116">Lorsque la propriété change, la valeur de l’attribut change également.</span><span class="sxs-lookup"><span data-stu-id="a8d30-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="a8d30-117">Par exemple, pour que la valeur d’un élément Slider change à chaque modification de la valeur de l’attribut **CurrentPosition** , tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a8d30-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="a8d30-118">**Important** N’utilisez pas wmpprop sur les méthodes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a8d30-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="a8d30-119">Des résultats inattendus peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="a8d30-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="a8d30-120">Modifications de la méthode du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="a8d30-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="a8d30-121">Vous pouvez faire en sorte que votre apparence réponde à la disponibilité des méthodes sur le lecteur Windows Media à l’aide de wmpenabled et wmpdisabled.</span><span class="sxs-lookup"><span data-stu-id="a8d30-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="a8d30-122">Celles-ci sont utilisées de la même façon que l’écouteur wmpprop, à ceci près que vous pouvez uniquement les utiliser sur les méthodes de l’objet de **contrôle** qui sont prises en charge par la méthode **isAvailable** .</span><span class="sxs-lookup"><span data-stu-id="a8d30-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="a8d30-123">Par exemple, vous pouvez activer un bouton uniquement lorsque la méthode **Play** est activée, à l’aide d’un code similaire à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="a8d30-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="a8d30-124">**Important** N’utilisez pas wmpenabled ou wmpdisabled sur les propriétés du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a8d30-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="a8d30-125">Des résultats inattendus peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="a8d30-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="a8d30-126">Modifications des attributs d’apparence</span><span class="sxs-lookup"><span data-stu-id="a8d30-126">Skin Attribute Changes</span></span>

<span data-ttu-id="a8d30-127">Vous pouvez répondre aux modifications apportées à vos attributs d’apparence de l’une des deux manières suivantes : à l’aide de wmpprop ou de l’événement **\_ OnChange** .</span><span class="sxs-lookup"><span data-stu-id="a8d30-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="a8d30-128">Vous pouvez utiliser wmpprop pour écouter les modifications apportées à votre propre apparence.</span><span class="sxs-lookup"><span data-stu-id="a8d30-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="a8d30-129">Par exemple, pour afficher la valeur de curseur dans une zone de texte, vous pouvez taper la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a8d30-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="a8d30-130">Vous pouvez utiliser l’événement **\_ OnChange** pour traiter les événements à l’intérieur d’un élément.</span><span class="sxs-lookup"><span data-stu-id="a8d30-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="a8d30-131">Vous devez joindre le nom de l’attribut que vous souhaitez suivre à **\_ OnChange**.</span><span class="sxs-lookup"><span data-stu-id="a8d30-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="a8d30-132">Par exemple, si vous souhaitez suivre la valeur d’une zone de texte, vous devez taper :</span><span class="sxs-lookup"><span data-stu-id="a8d30-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="a8d30-133">Vous assignerez ensuite une chaîne JScript que vous souhaitez exécuter lorsque la valeur change.</span><span class="sxs-lookup"><span data-stu-id="a8d30-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="a8d30-134">Par exemple, pour répondre à une modification de la valeur d’une zone de texte qui peut être utilisée pour ajuster le volume du lecteur Windows Media, tapez la commande suivante à l’intérieur de votre élément de **texte** en tant qu’attribut :</span><span class="sxs-lookup"><span data-stu-id="a8d30-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="a8d30-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8d30-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d30-136">**Gestion des événements**</span><span class="sxs-lookup"><span data-stu-id="a8d30-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 





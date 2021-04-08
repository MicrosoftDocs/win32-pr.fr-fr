---
title: Collection AnimationNames
description: Collection AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840053"
---
# <a name="the-animationnames-collection"></a><span data-ttu-id="4d1a1-103">Collection AnimationNames</span><span class="sxs-lookup"><span data-stu-id="4d1a1-103">The AnimationNames Collection</span></span>

<span data-ttu-id="4d1a1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d1a1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4d1a1-105">La collection [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) est une collection spéciale qui contient la liste des noms d’animation compilés pour un caractère.</span><span class="sxs-lookup"><span data-stu-id="4d1a1-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="4d1a1-106">Vous pouvez utiliser la collection pour énumérer les noms des animations d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="4d1a1-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="4d1a1-107">Par exemple, dans Visual Basic ou VBScript (2,0 ou version ultérieure), vous pouvez accéder à ces noms à l’aide de l’exemple **de code for each... Instructions suivantes** :</span><span class="sxs-lookup"><span data-stu-id="4d1a1-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="4d1a1-108">Les éléments de la collection n’ont pas de propriétés, donc les éléments individuels ne sont pas accessibles directement.</span><span class="sxs-lookup"><span data-stu-id="4d1a1-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="4d1a1-109">Pour. Les caractères ACF, la collection retourne toutes les animations qui ont été définies pour le caractère, pas seulement celles qui ont été récupérées avec la méthode d' [**extraction**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1a1-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 





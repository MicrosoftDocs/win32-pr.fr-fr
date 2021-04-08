---
title: À propos des objets cdrom et CdromCollection
description: À propos des objets cdrom et CdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Lecteur Windows Media, objet cdrom
- Windows Media Player Object Model, CDROM, objet
- modèle objet, objet cdrom
- Contrôle ActiveX du lecteur Windows Media, objet cdrom
- Contrôle ActiveX, objet cdrom
- Contrôle ActiveX mobile pour Windows Media Player, objet cdrom
- Windows Media Player Mobile, objet cdrom
- Objet cdrom
- Lecteur Windows Media, objet CdromCollection
- Modèle objet du lecteur Windows Media, objet CdromCollection
- modèle objet, objet CdromCollection
- Contrôle ActiveX du lecteur Windows Media, objet CdromCollection
- Contrôle ActiveX, objet CdromCollection
- Contrôle ActiveX Windows Media Player Mobile, objet CdromCollection
- Windows Media Player Mobile, objet CdromCollection
- Objet CdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673801"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="08646-119">À propos des objets cdrom et CdromCollection</span><span class="sxs-lookup"><span data-stu-id="08646-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="08646-120">Les objets **cdrom** et **CdromCollection** régissent l’interface des lecteurs de CD sur votre ordinateur pour la lecture et la lecture de CD.</span><span class="sxs-lookup"><span data-stu-id="08646-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="08646-121">L’objet **CdromCollection** est accessible uniquement par le biais de la propriété **CdromCollection** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="08646-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="08646-122">La propriété **cdromCollection** retourne l’objet **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="08646-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="08646-123">Vous pouvez uniquement accéder aux propriétés de l’objet **CdromCollection** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="08646-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="08646-124">Par exemple, pour utiliser la propriété **Count** , vous devez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="08646-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="08646-125">Vous pouvez accéder à l’objet **cdrom** uniquement par le biais de l’objet **CdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="08646-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="08646-126">Par exemple, pour éjecter le CD à l’aide de la méthode **EJECT** , vous devez d’abord créer l’objet collection, puis un élément dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="08646-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="08646-127">Pour éjecter le CD, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="08646-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="08646-128">Dans les deux cas, vous créez d’abord l’objet de collection (**CdromCollection**), puis vous obtenez un objet spécifique de cette collection.</span><span class="sxs-lookup"><span data-stu-id="08646-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="08646-129">L’objet est le premier élément de la collection, **Item**(0), qui correspond au premier lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="08646-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="08646-130">Vous appelez ensuite une méthode, **éjecter**, sur cet élément.</span><span class="sxs-lookup"><span data-stu-id="08646-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08646-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08646-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08646-132">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="08646-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="08646-133">**Objet CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="08646-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="08646-134">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="08646-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





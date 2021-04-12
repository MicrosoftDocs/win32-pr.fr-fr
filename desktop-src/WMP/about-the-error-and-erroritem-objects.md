---
title: À propos des objets Error et ErrorItem
description: À propos des objets Error et ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Lecteur Windows Media, objet d’erreur
- Modèle d’objet du lecteur Windows Media, objet d’erreur
- modèle objet, objet d’erreur
- Contrôle ActiveX du lecteur Windows Media, objet d’erreur
- Contrôle ActiveX, objet d’erreur
- Contrôle ActiveX Windows Media Player Mobile, objet d’erreur
- Windows Media Player Mobile, objet d’erreur
- Objet d’erreur
- Lecteur Windows Media, objet ErrorItem
- Modèle objet du lecteur Windows Media, objet ErrorItem
- modèle objet, objet ErrorItem
- Contrôle ActiveX du lecteur Windows Media, objet ErrorItem
- Contrôle ActiveX, objet ErrorItem
- Contrôle ActiveX Windows Media Player Mobile, objet ErrorItem
- Windows Media Player Mobile, objet ErrorItem
- Objet ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310261"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="30b0f-119">À propos des objets Error et ErrorItem</span><span class="sxs-lookup"><span data-stu-id="30b0f-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="30b0f-120">Les objets **Error** et **ErrorItem** régissent les fonctionnalités de gestion des erreurs du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="30b0f-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="30b0f-121">L’objet **Error** est obtenu à partir de l’objet **Player** via la propriété **Error** .</span><span class="sxs-lookup"><span data-stu-id="30b0f-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="30b0f-122">Vous pouvez obtenir un code spécifique à partir de l’objet d' **erreur** à l’aide de la propriété **Item** de l’objet **Error** pour créer l’objet **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="30b0f-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="30b0f-123">Par exemple, pour obtenir le code d’erreur du premier élément d’erreur, tapez :</span><span class="sxs-lookup"><span data-stu-id="30b0f-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="30b0f-124">Vous pouvez également appeler l’aide Web avec l’objet d' **erreur** à l’aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="30b0f-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="30b0f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30b0f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b0f-126">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="30b0f-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="30b0f-127">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="30b0f-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="30b0f-128">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="30b0f-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





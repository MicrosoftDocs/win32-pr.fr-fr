---
title: Modification des valeurs d’attribut
description: Modification des valeurs d’attribut
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, modification des valeurs
- modification des valeurs d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029361"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="964bb-114">Modification des valeurs d’attribut</span><span class="sxs-lookup"><span data-stu-id="964bb-114">Changing Attribute Values</span></span>

<span data-ttu-id="964bb-115">Vous pouvez modifier la valeur d’un attribut si votre page Web ou application dispose d’un accès en lecture/écriture à la bibliothèque et que l’attribut peut être à la fois lu et écrit.</span><span class="sxs-lookup"><span data-stu-id="964bb-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="964bb-116">Vous pouvez modifier un attribut de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="964bb-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="964bb-117">Pour modifier les attributs de plusieurs éléments multimédias, vous pouvez les affecter à leur tour au *lecteur*. propriété **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="964bb-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="964bb-118">Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="964bb-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="964bb-119">Pour modifier un attribut, appelez le *lecteur*. *currentMedia*. méthode **setItemInfo** comme indiqué dans l’exemple C# suivant.</span><span class="sxs-lookup"><span data-stu-id="964bb-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="964bb-120">Nous vous recommandons d’appeler le *support*. méthode **isReadOnlyItem** pour déterminer si vous pouvez modifier un attribut particulier.</span><span class="sxs-lookup"><span data-stu-id="964bb-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="964bb-121">Si vous incorporez le contrôle dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas exécuté le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="964bb-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="964bb-122">Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications.</span><span class="sxs-lookup"><span data-stu-id="964bb-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="964bb-123">Dans les deux cas, les modifications sont immédiatement disponibles dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="964bb-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="964bb-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="964bb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="964bb-125">**Attributs d’élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="964bb-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="964bb-126">**Accès à la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="964bb-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="964bb-127">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="964bb-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="964bb-128">**Lecture des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="964bb-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 





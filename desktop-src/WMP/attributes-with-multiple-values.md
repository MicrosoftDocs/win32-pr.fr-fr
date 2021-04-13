---
title: Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Player)
description: Attributs avec plusieurs valeurs
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
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
- attributs, valeurs multiples
- valeurs d’attribut multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383719"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="9cc1c-114">Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="9cc1c-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="9cc1c-115">Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="9cc1c-116">Par exemple, l' **auteur**, le **WM/compositeur** et les attributs **WM/genre** peuvent avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="9cc1c-117">Le type de données de tels attributs est **une chaîne à valeurs multiples**.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="9cc1c-118">Dans le lecteur Windows Media, la bibliothèque affiche plusieurs valeurs dans un champ unique, en les séparant par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="9cc1c-119">Toutefois, chaque valeur est en fait un attribut distinct de l’élément Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="9cc1c-120">Vous pouvez écrire du code qui détermine si un attribut donné a plusieurs valeurs, puis récupérer toutes ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="9cc1c-121">Vous devez utiliser le *média*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="9cc1c-122">Si vous utilisez le *média*. méthode **getItemInfo** pour récupérer un attribut à valeurs multiples, vous récupérez uniquement la première valeur.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="9cc1c-123">Le dernier exemple de la rubrique [lecture des valeurs d’attribut](reading-attribute-values.md) illustre l’utilisation du *média*. **getAttributeCountByType** et *Media*. méthodes **getItemInfoByType** pour récupérer plusieurs valeurs pour un attribut donné.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cc1c-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cc1c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc1c-125">**Attributs d’élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="9cc1c-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="9cc1c-126">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="9cc1c-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9cc1c-127">**Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD**</span><span class="sxs-lookup"><span data-stu-id="9cc1c-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 





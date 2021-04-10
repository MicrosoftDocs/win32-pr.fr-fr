---
description: Utilisez cette annotation pour définir le contenu d’un fichier externe comme valeur d’initialisation d’un paramètre d’effet.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotation d’initialisation de paramètre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200678"
---
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="69331-103">Annotation d’initialisation de paramètre</span><span class="sxs-lookup"><span data-stu-id="69331-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="69331-104">Utilisez cette annotation pour définir le contenu d’un fichier externe comme valeur d’initialisation d’un paramètre d’effet.</span><span class="sxs-lookup"><span data-stu-id="69331-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="69331-105">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="69331-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="69331-106">où la valeur est une chaîne de texte ASCII qui peut contenir un chemin d’accès absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="69331-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="69331-107">Un chemin d’accès relatif est relatif au répertoire qui contient le fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="69331-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="69331-108">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="69331-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="69331-109">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="69331-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69331-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69331-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69331-111">Informations de référence sur les annotations et sémantiques DirectX standard</span><span class="sxs-lookup"><span data-stu-id="69331-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 




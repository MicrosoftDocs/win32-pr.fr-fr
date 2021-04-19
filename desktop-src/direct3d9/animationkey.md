---
description: Définit un ensemble de clés d’animation. Une clé de matrice est utile pour les jeux de données d’animation qui doivent être représentés en tant que matrices de transformation.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513945"
---
# <a name="animationkey"></a><span data-ttu-id="6256d-104">AnimationKey</span><span class="sxs-lookup"><span data-stu-id="6256d-104">AnimationKey</span></span>

<span data-ttu-id="6256d-105">Définit un ensemble de clés d’animation.</span><span class="sxs-lookup"><span data-stu-id="6256d-105">Defines a set of animation keys.</span></span> <span data-ttu-id="6256d-106">Une clé de matrice est utile pour les jeux de données d’animation qui doivent être représentés en tant que matrices de transformation.</span><span class="sxs-lookup"><span data-stu-id="6256d-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="6256d-107">Où :</span><span class="sxs-lookup"><span data-stu-id="6256d-107">Where:</span></span>

-   <span data-ttu-id="6256d-108">KeyType : spécifie si les clés sont des clés de rotation, de mise à l’échelle, de position ou de matrice (à l’aide des entiers 0, 1, 2 ou 3, respectivement).</span><span class="sxs-lookup"><span data-stu-id="6256d-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="6256d-109">nKeys : nombre de clés.</span><span class="sxs-lookup"><span data-stu-id="6256d-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="6256d-110">Keys : un tableau de clés.</span><span class="sxs-lookup"><span data-stu-id="6256d-110">keys - An array of keys.</span></span> <span data-ttu-id="6256d-111">Consultez [**TimedFloatKeys**](timedfloatkeys.md).</span><span class="sxs-lookup"><span data-stu-id="6256d-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6256d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6256d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6256d-113">Modèles</span><span class="sxs-lookup"><span data-stu-id="6256d-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




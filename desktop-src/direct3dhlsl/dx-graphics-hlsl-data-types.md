---
title: Types de données (HLSL)
description: Le langage HLSL prend en charge de nombreux types de données intrinsèques différents. Ce tableau indique les types à utiliser pour définir des variables de nuanceur.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129646"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="404c3-104">Types de données (HLSL)</span><span class="sxs-lookup"><span data-stu-id="404c3-104">Data Types (HLSL)</span></span>

<span data-ttu-id="404c3-105">Le langage HLSL prend en charge de nombreux types de données intrinsèques différents.</span><span class="sxs-lookup"><span data-stu-id="404c3-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="404c3-106">Ce tableau indique les types à utiliser pour définir des variables de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="404c3-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="404c3-107">Utiliser ce type intrinsèque</span><span class="sxs-lookup"><span data-stu-id="404c3-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="404c3-108">Pour définir cette variable de nuanceur</span><span class="sxs-lookup"><span data-stu-id="404c3-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="404c3-109">Scalaire</span><span class="sxs-lookup"><span data-stu-id="404c3-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="404c3-110">Scalaire à un composant</span><span class="sxs-lookup"><span data-stu-id="404c3-110">One-component scalar</span></span>                       |
| <span data-ttu-id="404c3-111">[Vector](dx-graphics-hlsl-vector.md), [matrice](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="404c3-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="404c3-112">Vecteur ou matrice à composants multiples</span><span class="sxs-lookup"><span data-stu-id="404c3-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="404c3-113">[Échantillonneur](dx-graphics-hlsl-sampler.md), [texture](dx-graphics-hlsl-texture.md) ou [mémoire tampon](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="404c3-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="404c3-114">Échantillonneur, texture ou objet de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="404c3-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="404c3-115">[Struct](dx-graphics-hlsl-struct.md), [défini par l’utilisateur](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="404c3-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="404c3-116">Structure personnalisée ou typedef</span><span class="sxs-lookup"><span data-stu-id="404c3-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="404c3-117">Array</span><span class="sxs-lookup"><span data-stu-id="404c3-117">Array</span></span>                                                                                   | <span data-ttu-id="404c3-118">Expressions scalaires littérales déclarées contenant la plupart des autres types</span><span class="sxs-lookup"><span data-stu-id="404c3-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="404c3-119">Objet d’État</span><span class="sxs-lookup"><span data-stu-id="404c3-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="404c3-120">Représentations HLSL d’objets d’État</span><span class="sxs-lookup"><span data-stu-id="404c3-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="404c3-121">Pour vous aider à mieux comprendre comment utiliser des vecteurs et des matrices en HLSL, vous pouvez lire ces informations générales sur la façon dont le langage HLSL utilise la mathématique [par composant](dx-graphics-hlsl-per-component-math.md) .</span><span class="sxs-lookup"><span data-stu-id="404c3-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="404c3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="404c3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="404c3-123">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="404c3-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





---
title: instance
description: Utilisez cet attribut pour instancier un nuanceur Geometry.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030601"
---
# <a name="instance"></a><span data-ttu-id="21ebb-103">instance</span><span class="sxs-lookup"><span data-stu-id="21ebb-103">instance</span></span>

<span data-ttu-id="21ebb-104">Utilisez cet attribut pour instancier un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="21ebb-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="21ebb-105">Notes</span><span class="sxs-lookup"><span data-stu-id="21ebb-105">Remarks</span></span>

<span data-ttu-id="21ebb-106">X est un index d’entiers qui indique le nombre d’instances à exécuter pour chaque élément dessiné (par exemple, pour chaque triangle).</span><span class="sxs-lookup"><span data-stu-id="21ebb-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="21ebb-107">Lorsque vous utilisez cet attribut, utilisez [SV \_ GSInstanceID](sv-gsinstanceid.md) pour identifier l’instance d’un nuanceur Geometry qui est exécutée.</span><span class="sxs-lookup"><span data-stu-id="21ebb-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="21ebb-108">Cet attribut est pris en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="21ebb-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="21ebb-109">Sommet</span><span class="sxs-lookup"><span data-stu-id="21ebb-109">Vertex</span></span> | <span data-ttu-id="21ebb-110">Forme</span><span class="sxs-lookup"><span data-stu-id="21ebb-110">Hull</span></span> | <span data-ttu-id="21ebb-111">Domain</span><span class="sxs-lookup"><span data-stu-id="21ebb-111">Domain</span></span> | <span data-ttu-id="21ebb-112">Géométrie</span><span class="sxs-lookup"><span data-stu-id="21ebb-112">Geometry</span></span> | <span data-ttu-id="21ebb-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="21ebb-113">Pixel</span></span> | <span data-ttu-id="21ebb-114">Compute</span><span class="sxs-lookup"><span data-stu-id="21ebb-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="21ebb-115">x</span><span class="sxs-lookup"><span data-stu-id="21ebb-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="21ebb-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21ebb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ebb-117">Attributs du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="21ebb-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="21ebb-118">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="21ebb-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





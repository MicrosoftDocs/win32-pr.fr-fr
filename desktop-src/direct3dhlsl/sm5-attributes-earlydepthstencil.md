---
title: earlydepthstencil
description: Force le test des stencils de profondeur avant l’exécution d’un nuanceur.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990816"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="058a2-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="058a2-103">earlydepthstencil</span></span>

<span data-ttu-id="058a2-104">Force le test des stencils de profondeur avant l’exécution d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="058a2-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="058a2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="058a2-105">Remarks</span></span>

<span data-ttu-id="058a2-106">Le test des stencils de profondeur est normalement effectué lors du traitement des pixels par un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="058a2-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="058a2-107">En forçant le test des stencils à profondeur précoce, le test est effectué avant l’exécution du nuanceur. l’objectif est d’améliorer les performances par pixel en éliminant/réduisant/évitant le traitement des pixels inutiles.</span><span class="sxs-lookup"><span data-stu-id="058a2-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="058a2-108">Une application peut forcer le test des stencils de profondeur précoce en fournissant l’attribut ou le matériel peut exécuter des tests de stencil de profondeur à condition qu’aucune valeur de profondeur ne soit écrite et qu’aucune opération d’accès non triée ne soit exécutée dans un nuanceur en tant qu’optimisation.</span><span class="sxs-lookup"><span data-stu-id="058a2-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="058a2-109">Cet attribut est pris en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="058a2-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="058a2-110">Sommet</span><span class="sxs-lookup"><span data-stu-id="058a2-110">Vertex</span></span> | <span data-ttu-id="058a2-111">Forme</span><span class="sxs-lookup"><span data-stu-id="058a2-111">Hull</span></span> | <span data-ttu-id="058a2-112">Domain</span><span class="sxs-lookup"><span data-stu-id="058a2-112">Domain</span></span> | <span data-ttu-id="058a2-113">Géométrie</span><span class="sxs-lookup"><span data-stu-id="058a2-113">Geometry</span></span> | <span data-ttu-id="058a2-114">Pixel</span><span class="sxs-lookup"><span data-stu-id="058a2-114">Pixel</span></span> | <span data-ttu-id="058a2-115">Compute</span><span class="sxs-lookup"><span data-stu-id="058a2-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="058a2-116">x</span><span class="sxs-lookup"><span data-stu-id="058a2-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="058a2-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="058a2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="058a2-118">Attributs du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="058a2-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="058a2-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="058a2-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





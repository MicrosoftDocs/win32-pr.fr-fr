---
title: outputtopology
description: Définit le type de la primitive de sortie pour le du paveur.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940569"
---
# <a name="outputtopology"></a><span data-ttu-id="60650-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="60650-103">outputtopology</span></span>

<span data-ttu-id="60650-104">Définit le type de la primitive de sortie pour le du paveur.</span><span class="sxs-lookup"><span data-stu-id="60650-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="60650-105">Notes</span><span class="sxs-lookup"><span data-stu-id="60650-105">Remarks</span></span>

<span data-ttu-id="60650-106">X doit être un [**point**](dx-graphics-hlsl-geometry-shader.md), une **ligne**, un **triangle \_** ou un **rectangle \_ CCW** et doit être placé entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="60650-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="60650-107">Voici les options valides pour cet attribut :</span><span class="sxs-lookup"><span data-stu-id="60650-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="60650-108">Cet attribut est pris en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="60650-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="60650-109">Sommet</span><span class="sxs-lookup"><span data-stu-id="60650-109">Vertex</span></span> | <span data-ttu-id="60650-110">Forme</span><span class="sxs-lookup"><span data-stu-id="60650-110">Hull</span></span> | <span data-ttu-id="60650-111">Domain</span><span class="sxs-lookup"><span data-stu-id="60650-111">Domain</span></span> | <span data-ttu-id="60650-112">Géométrie</span><span class="sxs-lookup"><span data-stu-id="60650-112">Geometry</span></span> | <span data-ttu-id="60650-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="60650-113">Pixel</span></span> | <span data-ttu-id="60650-114">Compute</span><span class="sxs-lookup"><span data-stu-id="60650-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="60650-115">x</span><span class="sxs-lookup"><span data-stu-id="60650-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="60650-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60650-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60650-117">Attributs du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="60650-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="60650-118">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="60650-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





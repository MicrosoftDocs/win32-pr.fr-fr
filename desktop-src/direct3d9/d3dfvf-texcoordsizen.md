---
description: Construit des modèles binaires utilisés pour identifier les formats de coordonnée de texture dans une description de la Commission. Les résultats de ces macros peuvent être combinés dans une description de la Commission des prix finals à l’aide de l’opérateur OR.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522760"
---
# <a name="d3dfvf_texcoordsizen"></a><span data-ttu-id="6d33d-104">D3DFVF \_ TEXCOORDSIZEN</span><span class="sxs-lookup"><span data-stu-id="6d33d-104">D3DFVF\_TEXCOORDSIZEN</span></span>

<span data-ttu-id="6d33d-105">Construit des modèles binaires utilisés pour identifier les formats de coordonnée de texture dans une description de la Commission.</span><span class="sxs-lookup"><span data-stu-id="6d33d-105">Constructs bit patterns that are used to identify texture coordinate formats within a FVF description.</span></span> <span data-ttu-id="6d33d-106">Les résultats de ces macros peuvent être combinés dans une description de la Commission des prix finals à l’aide de l’opérateur OR.</span><span class="sxs-lookup"><span data-stu-id="6d33d-106">The results of these macros can be combined within a FVF description by using the OR operator.</span></span>

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a><span data-ttu-id="6d33d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d33d-107">Parameters</span></span>



| <span data-ttu-id="6d33d-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6d33d-108">Parameter</span></span>                                                                                                    | <span data-ttu-id="6d33d-109">Description</span><span class="sxs-lookup"><span data-stu-id="6d33d-109">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d33d-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span><span class="sxs-lookup"><span data-stu-id="6d33d-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span></span><br/> | <span data-ttu-id="6d33d-111">Valeur qui identifie le jeu de coordonnées de texture auquel la taille de coordonnée de texture (1-, 2-, 3-ou 4Dimensional) s’applique.</span><span class="sxs-lookup"><span data-stu-id="6d33d-111">Value that identifies the texture coordinate set at which the texture coordinate size (1-, 2-, 3-, or 4Dimensional) applies.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d33d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6d33d-112">Remarks</span></span>

<span data-ttu-id="6d33d-113">Les macros **\_ TEXCOORDSIZEN D3DFVF** utilisent les constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d33d-113">The **D3DFVF\_TEXCOORDSIZEN** macros use the following constants.</span></span>


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



<span data-ttu-id="6d33d-114">La description de la Commission de la Commission suivante identifie un format de vertex qui a une position. un normal ; couleurs diffuses et spéculaires ; et deux jeux de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="6d33d-114">The following FVF description identifies a vertex format that has a position; a normal; diffuse and specular colors; and two sets of texture coordinates.</span></span> <span data-ttu-id="6d33d-115">Le premier jeu de coordonnées de texture comprend un seul élément, et le deuxième jeu comprend deux éléments :</span><span class="sxs-lookup"><span data-stu-id="6d33d-115">The first set of texture coordinates includes a single element, and the second set includes two elements:</span></span>


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a><span data-ttu-id="6d33d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d33d-116">Requirements</span></span>



| <span data-ttu-id="6d33d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d33d-117">Requirement</span></span> | <span data-ttu-id="6d33d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d33d-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d33d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d33d-119">Header</span></span><br/> | <dl> <span data-ttu-id="6d33d-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d33d-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d33d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d33d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d33d-122">Macros</span><span class="sxs-lookup"><span data-stu-id="6d33d-122">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="6d33d-123">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="6d33d-123">D3DFVF</span></span>](d3dfvf.md)
</dt> </dl>

 

 





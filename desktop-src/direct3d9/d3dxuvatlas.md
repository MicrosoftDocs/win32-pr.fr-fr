---
description: Définit des options pour effectuer des calculs de distance géodésique, lors de l’ajustement d’une texture à une surface incurvée. Utilisez cet indicateur pour choisir entre la haute qualité et les calculs rapides lors du calcul d’un Atlas de textures.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Énumération D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537249"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="d1ed4-104">Énumération D3DXUVATLAS</span><span class="sxs-lookup"><span data-stu-id="d1ed4-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="d1ed4-105">Définit des options pour effectuer des calculs de distance géodésique, lors de l’ajustement d’une texture à une surface incurvée.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="d1ed4-106">Utilisez cet indicateur pour choisir entre la haute qualité et les calculs rapides lors du calcul d’un Atlas de textures.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ed4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1ed4-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="d1ed4-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1ed4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1ed4-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="d1ed4-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="d1ed4-110">Les mailles avec plus de 25 000 visages auront la méthode de distance geodasic rapide appliquée, tandis que la méthode de distance géodésique de qualité supérieure sera appliquée aux mailles avec moins de 25 000 visages.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="d1ed4-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ géodésique \_ rapidement**</span><span class="sxs-lookup"><span data-stu-id="d1ed4-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="d1ed4-112">Utilise des approximations pour améliorer la vitesse de représentation graphique au détriment d’une augmentation ou de plusieurs graphiques en sortie de la maille.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d1ed4-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**Qualité de la \_ géodésique D3DXUVATLAS \_**</span><span class="sxs-lookup"><span data-stu-id="d1ed4-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="d1ed4-114">Fournit de meilleurs graphiques de qualité, mais nécessite plus de temps et de mémoire que rapide.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1ed4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1ed4-115">Requirements</span></span>



| <span data-ttu-id="d1ed4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1ed4-116">Requirement</span></span> | <span data-ttu-id="d1ed4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1ed4-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ed4-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1ed4-118">Header</span></span><br/> | <dl> <span data-ttu-id="d1ed4-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ed4-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ed4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1ed4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ed4-121">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="d1ed4-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





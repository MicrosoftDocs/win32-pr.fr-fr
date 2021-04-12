---
description: Options de soudure conjointe des sommets.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Énumération D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322993"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="a30a1-103">Énumération D3DXWELDEPSILONSFLAGS</span><span class="sxs-lookup"><span data-stu-id="a30a1-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="a30a1-104">Options de soudure conjointe des sommets.</span><span class="sxs-lookup"><span data-stu-id="a30a1-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a30a1-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="a30a1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a30a1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a30a1-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**</span><span class="sxs-lookup"><span data-stu-id="a30a1-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="a30a1-108">Soudure ensemble tous les vertex qui se trouvent au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="a30a1-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="a30a1-109">L’utilisation de cet indicateur évite une comparaison Epsilon entre les composants de vertex.</span><span class="sxs-lookup"><span data-stu-id="a30a1-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="a30a1-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**</span><span class="sxs-lookup"><span data-stu-id="a30a1-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="a30a1-111">Si un composant de vertex donné se trouve dans Epsilon, modifiez les vertex partiellement correspondants afin que les deux composants soient identiques.</span><span class="sxs-lookup"><span data-stu-id="a30a1-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="a30a1-112">Si tous les composants sont identiques, supprimez l’un des sommets.</span><span class="sxs-lookup"><span data-stu-id="a30a1-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a30a1-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**</span><span class="sxs-lookup"><span data-stu-id="a30a1-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="a30a1-114">Indique à la soudure d’autoriser uniquement les modifications apportées aux vertex et non la suppression.</span><span class="sxs-lookup"><span data-stu-id="a30a1-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="a30a1-115">Cet indicateur n’est valide que si D3DXWELDEPSILONS \_ WELDPARTIALMATCHES est défini.</span><span class="sxs-lookup"><span data-stu-id="a30a1-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="a30a1-116">Il est utile de modifier les vertex pour qu’ils soient égaux, mais pas pour permettre la suppression des vertex.</span><span class="sxs-lookup"><span data-stu-id="a30a1-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="a30a1-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="a30a1-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="a30a1-118">Indique à la soudure de ne pas fractionner les vertex qui se trouvent dans des groupes d’attributs distincts.</span><span class="sxs-lookup"><span data-stu-id="a30a1-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="a30a1-119">Lorsque la méthode [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) est appelée avec l' \_ indicateur D3DXMESHOPT ATTRSORT, l’indicateur D3DXMESHOPT \_ DONOTSPLIT est également défini.</span><span class="sxs-lookup"><span data-stu-id="a30a1-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="a30a1-120">La définition de cet indicateur peut ralentir le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="a30a1-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a30a1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a30a1-121">Requirements</span></span>



| <span data-ttu-id="a30a1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a30a1-122">Requirement</span></span> | <span data-ttu-id="a30a1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a30a1-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a30a1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a30a1-124">Header</span></span><br/> | <dl> <span data-ttu-id="a30a1-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a30a1-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30a1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a30a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30a1-127">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="a30a1-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="a30a1-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="a30a1-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 





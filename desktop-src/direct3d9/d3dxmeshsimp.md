---
description: Spécifie les options de simplification d’une maille.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Énumération D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116218"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="b4b90-103">Énumération D3DXMESHSIMP</span><span class="sxs-lookup"><span data-stu-id="b4b90-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="b4b90-104">Spécifie les options de simplification d’une maille.</span><span class="sxs-lookup"><span data-stu-id="b4b90-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4b90-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="b4b90-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b4b90-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4b90-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP \_ vertex**</span><span class="sxs-lookup"><span data-stu-id="b4b90-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="b4b90-108">Le maillage sera simplifié par le nombre de vertex spécifié dans le paramètre MinValue.</span><span class="sxs-lookup"><span data-stu-id="b4b90-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b4b90-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**\_Visage D3DXMESHSIMP**</span><span class="sxs-lookup"><span data-stu-id="b4b90-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="b4b90-110">Le maillage sera simplifié par le nombre de visages spécifié dans le paramètre MinValue.</span><span class="sxs-lookup"><span data-stu-id="b4b90-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4b90-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4b90-111">Requirements</span></span>



| <span data-ttu-id="b4b90-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4b90-112">Requirement</span></span> | <span data-ttu-id="b4b90-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4b90-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b90-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4b90-114">Header</span></span><br/> | <dl> <span data-ttu-id="b4b90-115"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b90-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b90-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4b90-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b90-117">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="b4b90-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="b4b90-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="b4b90-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 





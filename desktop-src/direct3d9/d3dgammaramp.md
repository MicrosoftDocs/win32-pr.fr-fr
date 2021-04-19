---
description: Contient des données de rampe rouge, verte et bleue.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: D3DGAMMARAMP, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538521"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="e1cb0-103">D3DGAMMARAMP, structure</span><span class="sxs-lookup"><span data-stu-id="e1cb0-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="e1cb0-104">Contient des données de rampe rouge, verte et bleue.</span><span class="sxs-lookup"><span data-stu-id="e1cb0-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cb0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1cb0-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="e1cb0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e1cb0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1cb0-107">**rouge**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="e1cb0-108">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1cb0-109">Tableau de l’élément de mot 256 qui décrit la rampe gamma rouge.</span><span class="sxs-lookup"><span data-stu-id="e1cb0-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="e1cb0-110">**écologie**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="e1cb0-111">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1cb0-112">Tableau de l’élément de mot 256 qui décrit la rampe gamma vert.</span><span class="sxs-lookup"><span data-stu-id="e1cb0-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="e1cb0-113">**bleu**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="e1cb0-114">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1cb0-115">Tableau de l’élément de mot 256 qui décrit la rampe gamma bleue.</span><span class="sxs-lookup"><span data-stu-id="e1cb0-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1cb0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1cb0-116">Requirements</span></span>



| <span data-ttu-id="e1cb0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1cb0-117">Requirement</span></span> | <span data-ttu-id="e1cb0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cb0-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cb0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1cb0-119">Header</span></span><br/> | <dl> <span data-ttu-id="e1cb0-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cb0-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1cb0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1cb0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cb0-122">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1cb0-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e1cb0-123">**GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="e1cb0-124">**SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="e1cb0-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 

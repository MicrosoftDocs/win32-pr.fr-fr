---
description: Décrit un volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Structure D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323053"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="86c13-103">D3DVOLUME \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="86c13-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="86c13-104">Décrit un volume.</span><span class="sxs-lookup"><span data-stu-id="86c13-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86c13-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="86c13-106">Membres</span><span class="sxs-lookup"><span data-stu-id="86c13-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="86c13-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="86c13-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-108">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-109">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface du volume.</span><span class="sxs-lookup"><span data-stu-id="86c13-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="86c13-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-111">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-112">Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource en tant que volume.</span><span class="sxs-lookup"><span data-stu-id="86c13-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="86c13-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-115">Pas utilisé pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="86c13-115">Currently not used.</span></span> <span data-ttu-id="86c13-116">Toujours retourné comme 0.</span><span class="sxs-lookup"><span data-stu-id="86c13-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="86c13-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-118">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-119">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour ce volume.</span><span class="sxs-lookup"><span data-stu-id="86c13-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-120">**Width**</span><span class="sxs-lookup"><span data-stu-id="86c13-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-122">Largeur du volume, en pixels.</span><span class="sxs-lookup"><span data-stu-id="86c13-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-123">**Height**</span><span class="sxs-lookup"><span data-stu-id="86c13-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-125">Hauteur du volume, en pixels.</span><span class="sxs-lookup"><span data-stu-id="86c13-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="86c13-126">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="86c13-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="86c13-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86c13-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="86c13-128">Profondeur du volume, en pixels.</span><span class="sxs-lookup"><span data-stu-id="86c13-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86c13-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c13-129">Requirements</span></span>



| <span data-ttu-id="86c13-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86c13-130">Requirement</span></span> | <span data-ttu-id="86c13-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="86c13-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86c13-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="86c13-132">Header</span></span><br/> | <dl> <span data-ttu-id="86c13-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c13-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c13-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c13-135">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="86c13-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="86c13-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="86c13-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="86c13-137">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="86c13-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 

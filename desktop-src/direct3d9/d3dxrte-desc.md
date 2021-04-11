---
description: Décrit une cible de rendu hors écran utilisée par une instance de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Structure D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211749"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="599b7-103">D3DXRTE \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="599b7-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="599b7-104">Décrit une cible de rendu hors écran utilisée par une instance de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span><span class="sxs-lookup"><span data-stu-id="599b7-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="599b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="599b7-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="599b7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="599b7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="599b7-107">**Taille**</span><span class="sxs-lookup"><span data-stu-id="599b7-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="599b7-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="599b7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="599b7-109">Largeur et hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="599b7-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="599b7-110">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="599b7-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="599b7-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="599b7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="599b7-112">Nombre maximal de détails (LOD).</span><span class="sxs-lookup"><span data-stu-id="599b7-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="599b7-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="599b7-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="599b7-114">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="599b7-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="599b7-115">Format de la mémoire tampon des couleurs.</span><span class="sxs-lookup"><span data-stu-id="599b7-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="599b7-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="599b7-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="599b7-117">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="599b7-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="599b7-118">Indique si la mémoire tampon z est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="599b7-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="599b7-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="599b7-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="599b7-120">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="599b7-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="599b7-121">Format de la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="599b7-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="599b7-122">Notes</span><span class="sxs-lookup"><span data-stu-id="599b7-122">Remarks</span></span>

<span data-ttu-id="599b7-123">Cette méthode est utilisée pour retourner les paramètres de création utilisés lors de la création d’un objet [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="599b7-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="599b7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="599b7-124">Requirements</span></span>



| <span data-ttu-id="599b7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="599b7-125">Requirement</span></span> | <span data-ttu-id="599b7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="599b7-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="599b7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="599b7-127">Header</span></span><br/> | <dl> <span data-ttu-id="599b7-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="599b7-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599b7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="599b7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599b7-130">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="599b7-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

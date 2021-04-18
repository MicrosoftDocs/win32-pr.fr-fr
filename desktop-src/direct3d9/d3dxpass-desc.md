---
description: Décrit une passe pour un objet Effect.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Structure D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322637"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="6f768-103">D3DXPASS \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="6f768-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="6f768-104">Décrit une passe pour un objet Effect.</span><span class="sxs-lookup"><span data-stu-id="6f768-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f768-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f768-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="6f768-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6f768-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f768-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6f768-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="6f768-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f768-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f768-109">Valeur de chaîne utilisée pour la passe.</span><span class="sxs-lookup"><span data-stu-id="6f768-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="6f768-110">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="6f768-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="6f768-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f768-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f768-112">Les annotations sont des données spécifiques à l’utilisateur qui peuvent être attachées à n’importe quelle technique, passe ou paramètre.</span><span class="sxs-lookup"><span data-stu-id="6f768-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="6f768-113">Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="6f768-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f768-114">**pVertexShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="6f768-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="6f768-115">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f768-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="6f768-116">Pointeur désignant la fonction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="6f768-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="6f768-117">Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette structure retourne un pointeur **null** lorsqu’il est appelé par [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="6f768-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f768-118">**pPixelShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="6f768-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="6f768-119">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f768-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="6f768-120">Pointeur vers la fonction de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6f768-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="6f768-121">Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette structure retourne un pointeur **null** lorsqu’il est appelé par [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="6f768-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f768-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f768-122">Requirements</span></span>



| <span data-ttu-id="6f768-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f768-123">Requirement</span></span> | <span data-ttu-id="6f768-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f768-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f768-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f768-125">Header</span></span><br/> | <dl> <span data-ttu-id="6f768-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f768-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f768-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f768-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f768-128">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="6f768-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="6f768-129">**GetPassDesc**</span><span class="sxs-lookup"><span data-stu-id="6f768-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 

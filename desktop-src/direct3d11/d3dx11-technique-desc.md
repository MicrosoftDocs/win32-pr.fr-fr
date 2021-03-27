---
title: Structure D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Décrit une technique d’effet.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Structure D3DX11_TECHNIQUE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762181"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="ff41d-104">Structure de la \_ technique D3DX11 \_ desc</span><span class="sxs-lookup"><span data-stu-id="ff41d-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="ff41d-105">Décrit une technique d’effet.</span><span class="sxs-lookup"><span data-stu-id="ff41d-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff41d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff41d-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="ff41d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ff41d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff41d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ff41d-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="ff41d-109">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff41d-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ff41d-110">Nom de cette technique (NULL si non anonyme).</span><span class="sxs-lookup"><span data-stu-id="ff41d-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="ff41d-111">**Mettent**</span><span class="sxs-lookup"><span data-stu-id="ff41d-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="ff41d-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff41d-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ff41d-113">Nombre de passes contenues dans la technique.</span><span class="sxs-lookup"><span data-stu-id="ff41d-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="ff41d-114">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="ff41d-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="ff41d-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff41d-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ff41d-116">Nombre d’annotations sur cette technique.</span><span class="sxs-lookup"><span data-stu-id="ff41d-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff41d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ff41d-117">Remarks</span></span>

<span data-ttu-id="ff41d-118">La \_ technique D3DX11 \_ desc est utilisée avec [**ID3DX11EffectTechnique :: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="ff41d-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff41d-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff41d-119">Requirements</span></span>



| <span data-ttu-id="ff41d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff41d-120">Requirement</span></span> | <span data-ttu-id="ff41d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff41d-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff41d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff41d-122">Header</span></span><br/> | <dl> <span data-ttu-id="ff41d-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff41d-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff41d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff41d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff41d-125">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="ff41d-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


---
title: Structure D3DX11_GROUP_DESC (D3dx11effect. h)
description: Décrit un groupe d’effets.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Structure D3DX11_GROUP_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043186"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="f7dd4-104">\_Structure DESC du groupe D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="f7dd4-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="f7dd4-105">Décrit un groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="f7dd4-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7dd4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7dd4-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="f7dd4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f7dd4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7dd4-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f7dd4-109">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f7dd4-110">Nom de ce groupe ( **null** uniquement si global).</span><span class="sxs-lookup"><span data-stu-id="f7dd4-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="f7dd4-111">**Technologie**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="f7dd4-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f7dd4-113">Nombre de techniques contenues dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="f7dd4-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="f7dd4-114">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="f7dd4-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7dd4-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f7dd4-116">Nombre d’annotations sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="f7dd4-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7dd4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f7dd4-117">Remarks</span></span>

<span data-ttu-id="f7dd4-118">Le \_ groupe D3DX11 \_ desc est utilisé avec [**ID3DX11EffectTechnique :: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="f7dd4-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7dd4-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f7dd4-119">Requirements</span></span>



| <span data-ttu-id="f7dd4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7dd4-120">Requirement</span></span> | <span data-ttu-id="f7dd4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7dd4-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7dd4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7dd4-122">Header</span></span><br/> | <dl> <span data-ttu-id="f7dd4-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7dd4-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7dd4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7dd4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7dd4-125">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="f7dd4-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


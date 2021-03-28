---
title: Structure D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Décrit un effet.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Structure D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982586"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="aad8d-104">\_ \_ Structure DESC de l’effet D3DX11</span><span class="sxs-lookup"><span data-stu-id="aad8d-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="aad8d-105">Décrit un effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad8d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aad8d-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="aad8d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="aad8d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aad8d-108">**ConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="aad8d-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="aad8d-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aad8d-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aad8d-110">Nombre de mémoires tampons constantes dans cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="aad8d-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="aad8d-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="aad8d-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aad8d-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aad8d-113">Nombre de variables globales dans cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="aad8d-114">**InterfaceVariables**</span><span class="sxs-lookup"><span data-stu-id="aad8d-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="aad8d-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aad8d-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aad8d-116">Nombre d’interfaces globales dans cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="aad8d-117">**Technologie**</span><span class="sxs-lookup"><span data-stu-id="aad8d-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="aad8d-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aad8d-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aad8d-119">Nombre de techniques dans cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="aad8d-120">**Groupes**</span><span class="sxs-lookup"><span data-stu-id="aad8d-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="aad8d-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aad8d-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aad8d-122">Nombre de groupes dans cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad8d-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aad8d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="aad8d-123">Remarks</span></span>

<span data-ttu-id="aad8d-124">L' \_ effet D3DX11 \_ desc est utilisé avec [**ID3DX11Effect :: GetDesc**](id3dx11effect-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="aad8d-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aad8d-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aad8d-125">Requirements</span></span>



| <span data-ttu-id="aad8d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aad8d-126">Requirement</span></span> | <span data-ttu-id="aad8d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="aad8d-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad8d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="aad8d-128">Header</span></span><br/> | <dl> <span data-ttu-id="aad8d-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aad8d-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad8d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aad8d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad8d-131">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="aad8d-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


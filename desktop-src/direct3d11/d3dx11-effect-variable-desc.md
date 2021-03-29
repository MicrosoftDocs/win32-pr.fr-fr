---
title: Structure D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Décrit une variable Effect.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Structure D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996205"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="b2b0d-104">Structure de la \_ variable d’effet D3DX11 \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2b0d-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="b2b0d-105">Décrit une variable Effect.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b0d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b0d-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="b2b0d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b2b0d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2b0d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-109">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-110">Nom de cette variable, annotation ou membre de structure.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="b2b0d-111">**Équivalent**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-113">Chaîne sémantique de ce membre de la variable ou de la structure (NULL pour les annotations ou s’il n’est pas présent).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="b2b0d-114">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-116">Indicateurs facultatifs pour les variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="b2b0d-117">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-119">Nombre d’annotations sur cette variable (toujours 0 pour les annotations).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="b2b0d-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-122">Offset dans qui contient CBuffer ou tbuffer (toujours 0 pour les annotations ou les variables qui ne sont pas dans des mémoires tampons constantes).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="b2b0d-123">**ExplicitBindPoint**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="b2b0d-124">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2b0d-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b2b0d-125">Utilisé si la variable a été explicitement liée à l’aide du mot clé Register.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="b2b0d-126">Vérifiez les indicateurs pour \_ le \_ \_ point de \_ liaison explicite \_ de la variable d’effet D3DX11.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2b0d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b2b0d-127">Remarks</span></span>

<span data-ttu-id="b2b0d-128">La \_ \_ variable d’effet D3DX11 \_ desc est utilisée avec [**ID3DX11EffectVariable :: GetDesc**](id3dx11effectvariable-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b0d-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b2b0d-129">Requirements</span></span>



| <span data-ttu-id="b2b0d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2b0d-130">Requirement</span></span> | <span data-ttu-id="b2b0d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2b0d-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b0d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2b0d-132">Header</span></span><br/> | <dl> <span data-ttu-id="b2b0d-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b0d-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b0d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2b0d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b0d-135">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="b2b0d-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


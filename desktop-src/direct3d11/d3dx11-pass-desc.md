---
title: Structure D3DX11_PASS_DESC (D3dx11effect. h)
description: Décrit une passe d’effet, qui contient l’état du pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Structure D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982551"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="35dd6-104">D3DX11, structure de la \_ passe \_ desc</span><span class="sxs-lookup"><span data-stu-id="35dd6-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="35dd6-105">Décrit une passe d’effet, qui contient l’état du pipeline.</span><span class="sxs-lookup"><span data-stu-id="35dd6-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dd6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35dd6-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="35dd6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="35dd6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="35dd6-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="35dd6-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-109">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-110">Nom de cette passe (**null** si non anonyme).</span><span class="sxs-lookup"><span data-stu-id="35dd6-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-111">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="35dd6-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-113">Nombre d’annotations sur cette passe.</span><span class="sxs-lookup"><span data-stu-id="35dd6-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-114">**pIAInputSignature**</span><span class="sxs-lookup"><span data-stu-id="35dd6-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-115">Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="35dd6-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-116">Signature du nuanceur de sommets ou du nuanceur de géométrie (s’il n’existe aucun nuanceur de vertex) ou **null** s’il n’en existe pas.</span><span class="sxs-lookup"><span data-stu-id="35dd6-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-117">**IAInputSignatureSize**</span><span class="sxs-lookup"><span data-stu-id="35dd6-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-118">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-119">Taille de singature en octets.</span><span class="sxs-lookup"><span data-stu-id="35dd6-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-120">**StencilRef**</span><span class="sxs-lookup"><span data-stu-id="35dd6-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-122">Valeur de référence de stencil utilisée dans l’état de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="35dd6-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-123">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="35dd6-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-124">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-125">Exemple de masque pour l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="35dd6-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="35dd6-126">**BlendFactor**</span><span class="sxs-lookup"><span data-stu-id="35dd6-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="35dd6-127">Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35dd6-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="35dd6-128">Facteurs de mélange par composant (RVBA) pour l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="35dd6-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35dd6-129">Notes</span><span class="sxs-lookup"><span data-stu-id="35dd6-129">Remarks</span></span>

<span data-ttu-id="35dd6-130">D3DX11 \_ Pass \_ desc est utilisé avec [**ID3DX11EffectPass :: GetDesc**](id3dx11effectpass-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="35dd6-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35dd6-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="35dd6-131">Requirements</span></span>



| <span data-ttu-id="35dd6-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35dd6-132">Requirement</span></span> | <span data-ttu-id="35dd6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="35dd6-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dd6-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="35dd6-134">Header</span></span><br/> | <dl> <span data-ttu-id="35dd6-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="35dd6-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dd6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35dd6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dd6-137">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="35dd6-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


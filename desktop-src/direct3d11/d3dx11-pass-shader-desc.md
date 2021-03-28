---
title: Structure D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Décrit une passe d’effet.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Structure D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982546"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="d2f86-104">\_ \_ Structure DESC du nuanceur de passe D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="d2f86-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="d2f86-105">Décrit une passe d’effet.</span><span class="sxs-lookup"><span data-stu-id="d2f86-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f86-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f86-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="d2f86-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d2f86-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2f86-108">**pShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="d2f86-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="d2f86-109">Type : **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2f86-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="d2f86-110">Variable dont provient ce nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d2f86-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="d2f86-111">**ShaderIndex**</span><span class="sxs-lookup"><span data-stu-id="d2f86-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="d2f86-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2f86-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f86-113">Élément de pShaderVariable (si un tableau) ou 0 s’il n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="d2f86-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2f86-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d2f86-114">Remarks</span></span>

<span data-ttu-id="d2f86-115">Le \_ \_ nuanceur \_ de passe D3DX11 DESC est utilisé avec les méthodes [**ID3DX11EffectPass**](id3dx11effectpass.md) \* ShaderDesc.</span><span class="sxs-lookup"><span data-stu-id="d2f86-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="d2f86-116">S’il s’agit d’une assignation de nuanceur Inline, l’interface retournée est une variable de nuanceur anonyme, qui ne peut pas être récupérée d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="d2f86-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="d2f86-117">Son nom dans la description de la variable est « $Anonymous ».</span><span class="sxs-lookup"><span data-stu-id="d2f86-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="d2f86-118">S’il n’y a aucune assignation de ce type dans le bloc de réussite, pShaderVariable ! = **null**, mais pShaderVariable->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="d2f86-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f86-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2f86-119">Requirements</span></span>



| <span data-ttu-id="d2f86-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f86-120">Requirement</span></span> | <span data-ttu-id="d2f86-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f86-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f86-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2f86-122">Header</span></span><br/> | <dl> <span data-ttu-id="d2f86-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f86-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f86-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f86-125">Effets 11 structures</span><span class="sxs-lookup"><span data-stu-id="d2f86-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


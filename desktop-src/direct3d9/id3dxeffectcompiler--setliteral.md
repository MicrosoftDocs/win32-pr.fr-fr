---
description: Active/désactive l’État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler :: SetLiteral, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322718"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="352c6-104">ID3DXEffectCompiler :: SetLiteral, méthode</span><span class="sxs-lookup"><span data-stu-id="352c6-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="352c6-105">Active/désactive l’État littéral d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="352c6-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="352c6-106">Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="352c6-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="352c6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="352c6-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="352c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="352c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352c6-109">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="352c6-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352c6-110">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="352c6-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="352c6-111">Identificateur unique d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="352c6-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="352c6-112">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="352c6-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="352c6-113">*Littéral* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="352c6-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352c6-114">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352c6-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352c6-115">Affectez la valeur **true** pour que le paramètre soit un littéral, et **false** si le paramètre peut modifier la valeur pendant la durée de vie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="352c6-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352c6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="352c6-116">Return value</span></span>

<span data-ttu-id="352c6-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="352c6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="352c6-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="352c6-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="352c6-119">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="352c6-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="352c6-120">Notes</span><span class="sxs-lookup"><span data-stu-id="352c6-120">Remarks</span></span>

<span data-ttu-id="352c6-121">Cette méthode change uniquement si le paramètre est un littéral ou non.</span><span class="sxs-lookup"><span data-stu-id="352c6-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="352c6-122">Pour modifier la valeur d’un paramètre, utilisez une méthode comme [**ID3DXBaseEffect :: SetBool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect :: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="352c6-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="352c6-123">Cette fonction doit être appelée avant la compilation de l’effet.</span><span class="sxs-lookup"><span data-stu-id="352c6-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="352c6-124">Voici un exemple d’utilisation de cette fonction :</span><span class="sxs-lookup"><span data-stu-id="352c6-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="352c6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="352c6-125">Requirements</span></span>



| <span data-ttu-id="352c6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="352c6-126">Requirement</span></span> | <span data-ttu-id="352c6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="352c6-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="352c6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="352c6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="352c6-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="352c6-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="352c6-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="352c6-130">Library</span></span><br/> | <dl> <span data-ttu-id="352c6-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="352c6-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="352c6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="352c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352c6-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="352c6-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="352c6-134">Utilisations et littéraux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="352c6-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="352c6-135">**ID3DXEffectCompiler::GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="352c6-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 

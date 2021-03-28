---
title: Méthode ID3DX11EffectSamplerVariable SetSampler (D3dx11effect. h)
description: Définissez l’état de l’échantillonneur.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Méthode SetSampler Direct3D 11
- Méthode SetSampler Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode SetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323057"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="6c4b5-106">ID3DX11EffectSamplerVariable :: SetSampler, méthode</span><span class="sxs-lookup"><span data-stu-id="6c4b5-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="6c4b5-107">Définissez l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c4b5-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="6c4b5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c4b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4b5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="6c4b5-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4b5-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6c4b5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6c4b5-112">Index dans un tableau d’interfaces d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="6c4b5-113">S’il n’existe qu’une seule interface d’échantillonnage, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="6c4b5-114">*pSampler*</span><span class="sxs-lookup"><span data-stu-id="6c4b5-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4b5-115">Type : **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="6c4b5-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="6c4b5-116">Pointeur vers une interface [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) contenant l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4b5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c4b5-117">Return value</span></span>

<span data-ttu-id="6c4b5-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c4b5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c4b5-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c4b5-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6c4b5-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c4b5-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6c4b5-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6c4b5-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6c4b5-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c4b5-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6c4b5-124">Requirements</span></span>



| <span data-ttu-id="6c4b5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c4b5-125">Requirement</span></span> | <span data-ttu-id="6c4b5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c4b5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4b5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c4b5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6c4b5-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c4b5-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6c4b5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c4b5-129">Library</span></span><br/> | <dl> <span data-ttu-id="6c4b5-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4b5-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4b5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c4b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4b5-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="6c4b5-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 


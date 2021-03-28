---
title: Méthode ID3DX11EffectSamplerVariable GetSampler (D3dx11effect. h)
description: Obtient un pointeur vers une interface d’échantillonneur.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Méthode GetSampler Direct3D 11
- Méthode GetSampler Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode GetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53260a07e544d5f69a9575851614f694b778619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953994"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a><span data-ttu-id="4253f-106">ID3DX11EffectSamplerVariable :: GetSampler, méthode</span><span class="sxs-lookup"><span data-stu-id="4253f-106">ID3DX11EffectSamplerVariable::GetSampler method</span></span>

<span data-ttu-id="4253f-107">Obtient un pointeur vers une interface d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="4253f-107">Get a pointer to a sampler interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4253f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4253f-108">Syntax</span></span>


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a><span data-ttu-id="4253f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4253f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4253f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="4253f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4253f-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4253f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4253f-112">Index dans un tableau d’interfaces d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="4253f-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="4253f-113">S’il n’existe qu’une seule interface d’échantillonnage, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="4253f-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="4253f-114">*ppSampler*</span><span class="sxs-lookup"><span data-stu-id="4253f-114">*ppSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="4253f-115">Type : **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="4253f-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span></span>

<span data-ttu-id="4253f-116">Adresse d’un pointeur vers une interface d’échantillonneur (consultez [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span><span class="sxs-lookup"><span data-stu-id="4253f-116">The address of a pointer to a sampler interface (see [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4253f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4253f-117">Return value</span></span>

<span data-ttu-id="4253f-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4253f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4253f-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="4253f-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4253f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4253f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4253f-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="4253f-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4253f-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="4253f-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4253f-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4253f-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4253f-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4253f-124">Requirements</span></span>



| <span data-ttu-id="4253f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4253f-125">Requirement</span></span> | <span data-ttu-id="4253f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4253f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4253f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4253f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4253f-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4253f-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4253f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4253f-129">Library</span></span><br/> | <dl> <span data-ttu-id="4253f-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="4253f-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4253f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4253f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4253f-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="4253f-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 


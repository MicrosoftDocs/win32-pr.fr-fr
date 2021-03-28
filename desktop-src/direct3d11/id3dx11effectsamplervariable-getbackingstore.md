---
title: Méthode ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Méthode GetBackingStore Direct3D 11
- Méthode GetBackingStore Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323122"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="a0304-106">ID3DX11EffectSamplerVariable :: GetBackingStore, méthode</span><span class="sxs-lookup"><span data-stu-id="a0304-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="a0304-107">Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a0304-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0304-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0304-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a0304-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0304-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0304-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="a0304-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="a0304-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a0304-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a0304-112">Index dans un tableau de descriptions de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a0304-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="a0304-113">S’il n’existe qu’une seule variable d’échantillonneur dans l’effet, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="a0304-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="a0304-114">*pSamplerDesc*</span><span class="sxs-lookup"><span data-stu-id="a0304-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="a0304-115">Type : **[ **d3d11 \_ sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="a0304-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="a0304-116">Pointeur vers une description de l’échantillonneur (consultez [**d3d11 \_ sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span><span class="sxs-lookup"><span data-stu-id="a0304-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0304-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0304-117">Return value</span></span>

<span data-ttu-id="a0304-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0304-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0304-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="a0304-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0304-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a0304-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0304-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a0304-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a0304-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a0304-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a0304-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a0304-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0304-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a0304-124">Requirements</span></span>



| <span data-ttu-id="a0304-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0304-125">Requirement</span></span> | <span data-ttu-id="a0304-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0304-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0304-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0304-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a0304-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0304-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a0304-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0304-129">Library</span></span><br/> | <dl> <span data-ttu-id="a0304-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a0304-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0304-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0304-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0304-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="a0304-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 


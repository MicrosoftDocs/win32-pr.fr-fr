---
title: Méthode ID3DX11EffectSamplerVariable UndoSetSampler (D3dx11effect. h)
description: Rétablir un état d’échantillonneur précédemment défini.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Méthode UndoSetSampler Direct3D 11
- Méthode UndoSetSampler Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode UndoSetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323281"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="f947a-106">ID3DX11EffectSamplerVariable :: UndoSetSampler, méthode</span><span class="sxs-lookup"><span data-stu-id="f947a-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="f947a-107">Rétablir un état d’échantillonneur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="f947a-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f947a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f947a-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f947a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f947a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f947a-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f947a-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f947a-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f947a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f947a-112">Index dans un tableau d’interfaces d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="f947a-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="f947a-113">S’il n’existe qu’une seule interface d’échantillonnage, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="f947a-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f947a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f947a-114">Return value</span></span>

<span data-ttu-id="f947a-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f947a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f947a-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="f947a-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f947a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f947a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f947a-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="f947a-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f947a-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="f947a-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f947a-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f947a-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f947a-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f947a-121">Requirements</span></span>



| <span data-ttu-id="f947a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f947a-122">Requirement</span></span> | <span data-ttu-id="f947a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f947a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f947a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f947a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f947a-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f947a-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f947a-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f947a-126">Library</span></span><br/> | <dl> <span data-ttu-id="f947a-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="f947a-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f947a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f947a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f947a-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="f947a-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 


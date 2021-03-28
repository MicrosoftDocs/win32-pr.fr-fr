---
title: Méthode ID3DX11EffectTechnique GetDesc (D3dx11effect. h)
description: Obtenir une description technique.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992165"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a><span data-ttu-id="5c77e-106">ID3DX11EffectTechnique :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="5c77e-106">ID3DX11EffectTechnique::GetDesc method</span></span>

<span data-ttu-id="5c77e-107">Obtenir une description technique.</span><span class="sxs-lookup"><span data-stu-id="5c77e-107">Get a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c77e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c77e-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5c77e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c77e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c77e-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="5c77e-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5c77e-111">Type : **[ **D3DX11 \_ technique \_ desc**](d3dx11-technique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c77e-111">Type: **[**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)\***</span></span>

<span data-ttu-id="5c77e-112">Pointeur vers une description de technique (voir [**\_ technique D3DX11 \_ desc**](d3dx11-technique-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="5c77e-112">A pointer to a technique description (see [**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c77e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c77e-113">Return value</span></span>

<span data-ttu-id="5c77e-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c77e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c77e-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5c77e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c77e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5c77e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c77e-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="5c77e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5c77e-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="5c77e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5c77e-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5c77e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c77e-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5c77e-120">Requirements</span></span>



| <span data-ttu-id="5c77e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c77e-121">Requirement</span></span> | <span data-ttu-id="5c77e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c77e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c77e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c77e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5c77e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c77e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5c77e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5c77e-125">Library</span></span><br/> | <dl> <span data-ttu-id="5c77e-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="5c77e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c77e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c77e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c77e-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="5c77e-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 






---
title: Méthode ID3DX11EffectRenderTargetViewVariable SetRenderTargetArray (D3dx11effect. h)
description: Définissez un tableau de cibles de rendu.
ms.assetid: 03e1c4ea-292c-439f-a647-070b9e91a044
keywords:
- Méthode SetRenderTargetArray Direct3D 11
- Méthode SetRenderTargetArray Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, méthode SetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ff8a1931e95df4fd78d67a3a71d53150875400
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974487"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertargetarray-method"></a><span data-ttu-id="c9f02-106">ID3DX11EffectRenderTargetViewVariable :: SetRenderTargetArray, méthode</span><span class="sxs-lookup"><span data-stu-id="c9f02-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTargetArray method</span></span>

<span data-ttu-id="c9f02-107">Définissez un tableau de cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="c9f02-107">Set an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f02-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9f02-108">Syntax</span></span>


```C++
HRESULT SetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="c9f02-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9f02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f02-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="c9f02-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="c9f02-111">Type : **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9f02-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="c9f02-112">Définissez un tableau d’interfaces Render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="c9f02-112">Set an array of render-target-view interfaces.</span></span> <span data-ttu-id="c9f02-113">Consultez [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="c9f02-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="c9f02-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c9f02-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c9f02-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9f02-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9f02-116">Index de tableau de base zéro pour stocker la première interface.</span><span class="sxs-lookup"><span data-stu-id="c9f02-116">The zero-based array index to store the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="c9f02-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="c9f02-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c9f02-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9f02-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9f02-119">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="c9f02-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f02-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9f02-120">Return value</span></span>

<span data-ttu-id="c9f02-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9f02-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9f02-122">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="c9f02-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f02-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c9f02-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9f02-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c9f02-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9f02-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c9f02-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9f02-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c9f02-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9f02-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9f02-127">Requirements</span></span>



| <span data-ttu-id="c9f02-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9f02-128">Requirement</span></span> | <span data-ttu-id="c9f02-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9f02-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f02-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9f02-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c9f02-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f02-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c9f02-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9f02-132">Library</span></span><br/> | <dl> <span data-ttu-id="c9f02-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c9f02-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f02-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9f02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f02-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="c9f02-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 


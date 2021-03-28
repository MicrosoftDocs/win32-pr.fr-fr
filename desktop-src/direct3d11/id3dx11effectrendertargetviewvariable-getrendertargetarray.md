---
title: Méthode ID3DX11EffectRenderTargetViewVariable GetRenderTargetArray (D3dx11effect. h)
description: Obtient un tableau de cibles de rendu.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- Méthode GetRenderTargetArray Direct3D 11
- Méthode GetRenderTargetArray Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, méthode GetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996253"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a><span data-ttu-id="22eb9-106">ID3DX11EffectRenderTargetViewVariable :: GetRenderTargetArray, méthode</span><span class="sxs-lookup"><span data-stu-id="22eb9-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTargetArray method</span></span>

<span data-ttu-id="22eb9-107">Obtient un tableau de cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="22eb9-107">Get an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="22eb9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22eb9-108">Syntax</span></span>


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="22eb9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22eb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22eb9-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="22eb9-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="22eb9-111">Type : **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="22eb9-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="22eb9-112">Pointeur vers un tableau d’interfaces de vue de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="22eb9-112">A pointer to an array of render-target-view interfaces.</span></span> <span data-ttu-id="22eb9-113">Consultez [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="22eb9-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="22eb9-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="22eb9-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="22eb9-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22eb9-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22eb9-116">Index de tableau de base zéro permettant d’accéder à la première interface.</span><span class="sxs-lookup"><span data-stu-id="22eb9-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="22eb9-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="22eb9-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="22eb9-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="22eb9-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="22eb9-119">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="22eb9-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22eb9-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22eb9-120">Return value</span></span>

<span data-ttu-id="22eb9-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22eb9-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22eb9-122">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="22eb9-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22eb9-123">Notes</span><span class="sxs-lookup"><span data-stu-id="22eb9-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22eb9-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="22eb9-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="22eb9-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="22eb9-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="22eb9-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="22eb9-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22eb9-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22eb9-127">Requirements</span></span>



| <span data-ttu-id="22eb9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22eb9-128">Requirement</span></span> | <span data-ttu-id="22eb9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="22eb9-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22eb9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="22eb9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="22eb9-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="22eb9-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="22eb9-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22eb9-132">Library</span></span><br/> | <dl> <span data-ttu-id="22eb9-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="22eb9-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22eb9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22eb9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22eb9-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="22eb9-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 


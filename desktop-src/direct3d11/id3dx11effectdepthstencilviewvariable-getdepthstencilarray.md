---
title: Méthode ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect. h)
description: Obtenir un tableau de ressources de profondeur-stencil-vue.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Méthode GetDepthStencilArray Direct3D 11
- Méthode GetDepthStencilArray Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, méthode GetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974674"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a><span data-ttu-id="77d38-106">ID3DX11EffectDepthStencilViewVariable :: GetDepthStencilArray, méthode</span><span class="sxs-lookup"><span data-stu-id="77d38-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray method</span></span>

<span data-ttu-id="77d38-107">Obtenir un tableau de ressources de profondeur-stencil-vue.</span><span class="sxs-lookup"><span data-stu-id="77d38-107">Get an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d38-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77d38-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="77d38-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77d38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d38-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="77d38-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="77d38-111">Type : **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="77d38-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="77d38-112">Pointeur vers un tableau d’interfaces Depth-View-View.</span><span class="sxs-lookup"><span data-stu-id="77d38-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="77d38-113">Consultez [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="77d38-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="77d38-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="77d38-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="77d38-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77d38-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77d38-116">Index de tableau de base zéro permettant d’accéder à la première interface.</span><span class="sxs-lookup"><span data-stu-id="77d38-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="77d38-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="77d38-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="77d38-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77d38-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77d38-119">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="77d38-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d38-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77d38-120">Return value</span></span>

<span data-ttu-id="77d38-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77d38-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77d38-122">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="77d38-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77d38-123">Notes</span><span class="sxs-lookup"><span data-stu-id="77d38-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="77d38-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="77d38-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="77d38-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="77d38-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="77d38-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="77d38-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77d38-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77d38-127">Requirements</span></span>



| <span data-ttu-id="77d38-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77d38-128">Requirement</span></span> | <span data-ttu-id="77d38-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="77d38-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d38-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="77d38-130">Header</span></span><br/>  | <dl> <span data-ttu-id="77d38-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d38-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="77d38-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77d38-132">Library</span></span><br/> | <dl> <span data-ttu-id="77d38-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="77d38-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d38-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77d38-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d38-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="77d38-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 


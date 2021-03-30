---
title: Méthode ID3DX11EffectDepthStencilViewVariable SetDepthStencilArray (D3dx11effect. h)
description: Définir un tableau de ressources de profondeur-stencil-affichage.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- Méthode SetDepthStencilArray Direct3D 11
- Méthode SetDepthStencilArray Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, méthode SetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329f91fff70d78c51475b799a08dec1c6d34a157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974578"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a><span data-ttu-id="f8d67-106">ID3DX11EffectDepthStencilViewVariable :: SetDepthStencilArray, méthode</span><span class="sxs-lookup"><span data-stu-id="f8d67-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencilArray method</span></span>

<span data-ttu-id="f8d67-107">Définir un tableau de ressources de profondeur-stencil-affichage.</span><span class="sxs-lookup"><span data-stu-id="f8d67-107">Set an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d67-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8d67-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="f8d67-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8d67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d67-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="f8d67-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d67-111">Type : **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="f8d67-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="f8d67-112">Pointeur vers un tableau d’interfaces Depth-View-View.</span><span class="sxs-lookup"><span data-stu-id="f8d67-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="f8d67-113">Consultez [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="f8d67-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="f8d67-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="f8d67-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d67-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8d67-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8d67-116">Index de tableau de base zéro pour définir la première interface.</span><span class="sxs-lookup"><span data-stu-id="f8d67-116">The zero-based array index to set the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="f8d67-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="f8d67-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d67-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8d67-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8d67-119">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f8d67-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d67-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8d67-120">Return value</span></span>

<span data-ttu-id="f8d67-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8d67-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8d67-122">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="f8d67-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8d67-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f8d67-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8d67-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="f8d67-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f8d67-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="f8d67-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f8d67-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f8d67-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8d67-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8d67-127">Requirements</span></span>



| <span data-ttu-id="f8d67-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8d67-128">Requirement</span></span> | <span data-ttu-id="f8d67-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8d67-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d67-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8d67-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f8d67-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d67-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f8d67-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8d67-132">Library</span></span><br/> | <dl> <span data-ttu-id="f8d67-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="f8d67-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8d67-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8d67-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d67-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="f8d67-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 


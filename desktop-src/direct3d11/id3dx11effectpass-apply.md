---
title: ID3DX11EffectPass Apply, méthode (D3dx11effect. h)
description: Définit l’État contenu dans un passage à l’appareil.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Appliquer la méthode Direct3D 11
- Appliquer la méthode Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974543"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="9097e-106">ID3DX11EffectPass :: apply, méthode</span><span class="sxs-lookup"><span data-stu-id="9097e-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="9097e-107">Définit l’État contenu dans un passage à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9097e-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9097e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9097e-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="9097e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9097e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9097e-110">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="9097e-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="9097e-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9097e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9097e-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="9097e-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9097e-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="9097e-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9097e-114">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="9097e-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="9097e-115">[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) auquel appliquer la passe.</span><span class="sxs-lookup"><span data-stu-id="9097e-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9097e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9097e-116">Return value</span></span>

<span data-ttu-id="9097e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9097e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9097e-118">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="9097e-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9097e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9097e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9097e-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="9097e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9097e-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="9097e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9097e-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9097e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9097e-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9097e-123">Requirements</span></span>



| <span data-ttu-id="9097e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9097e-124">Requirement</span></span> | <span data-ttu-id="9097e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9097e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9097e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9097e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9097e-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9097e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9097e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9097e-128">Library</span></span><br/> | <dl> <span data-ttu-id="9097e-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="9097e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9097e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9097e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9097e-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="9097e-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 


---
title: Méthode ID3DX11Effect GetDevice (D3dx11effect. h)
description: Récupérez l’appareil qui a créé l’effet.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Méthode GetDevice Direct3D 11
- Méthode GetDevice Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211894"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="db555-106">ID3DX11Effect :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="db555-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="db555-107">Récupérez l’appareil qui a créé l’effet.</span><span class="sxs-lookup"><span data-stu-id="db555-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="db555-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db555-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="db555-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db555-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db555-110">*ppDevice*</span><span class="sxs-lookup"><span data-stu-id="db555-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="db555-111">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="db555-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="db555-112">Pointeur vers un [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="db555-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db555-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db555-113">Return value</span></span>

<span data-ttu-id="db555-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db555-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db555-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="db555-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db555-116">Notes</span><span class="sxs-lookup"><span data-stu-id="db555-116">Remarks</span></span>

<span data-ttu-id="db555-117">Un effet est créé pour un appareil spécifique, en appelant une fonction telle que [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="db555-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="db555-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="db555-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db555-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="db555-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db555-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="db555-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db555-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db555-121">Requirements</span></span>



| <span data-ttu-id="db555-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db555-122">Requirement</span></span> | <span data-ttu-id="db555-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="db555-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db555-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="db555-124">Header</span></span><br/>  | <dl> <span data-ttu-id="db555-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db555-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db555-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db555-126">Library</span></span><br/> | <dl> <span data-ttu-id="db555-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="db555-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db555-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db555-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db555-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="db555-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 






---
title: D3DX11UnsetAllDeviceObjects, fonction (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode ID3D11DeviceContext ClearState.'
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Fonction D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323113"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="1fcb0-105">D3DX11UnsetAllDeviceObjects fonction)</span><span class="sxs-lookup"><span data-stu-id="1fcb0-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="1fcb0-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="1fcb0-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode [**ID3D11DeviceContext :: ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .</span><span class="sxs-lookup"><span data-stu-id="1fcb0-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="1fcb0-108">Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="1fcb0-109">Cela doit être appelé lors de l’arrêt de votre application.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="1fcb0-110">Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcb0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fcb0-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="1fcb0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fcb0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcb0-113">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fcb0-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcb0-114">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="1fcb0-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="1fcb0-115">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="1fcb0-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcb0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fcb0-116">Return value</span></span>

<span data-ttu-id="1fcb0-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fcb0-118">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1fcb0-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcb0-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1fcb0-119">Requirements</span></span>



| <span data-ttu-id="1fcb0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fcb0-120">Requirement</span></span> | <span data-ttu-id="1fcb0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fcb0-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcb0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fcb0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1fcb0-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcb0-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1fcb0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fcb0-124">Library</span></span><br/> | <dl> <span data-ttu-id="1fcb0-125"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fcb0-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fcb0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fcb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcb0-127">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="1fcb0-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 






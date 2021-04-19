---
description: Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'ID3DXEffect :: OnLostDevice, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af2d17c99f0b694a8b27924c34faa2a1f633fafb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523811"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="6feda-104">ID3DXEffect :: OnLostDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="6feda-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="6feda-105">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="6feda-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="6feda-106">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="6feda-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6feda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6feda-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="6feda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6feda-108">Parameters</span></span>

<span data-ttu-id="6feda-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6feda-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6feda-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6feda-110">Return value</span></span>

<span data-ttu-id="6feda-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6feda-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6feda-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6feda-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6feda-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6feda-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6feda-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6feda-114">Remarks</span></span>

<span data-ttu-id="6feda-115">Cette méthode doit être appelée chaque fois que l’appareil est perdu ou avant que l’utilisateur n’appelle [**IDirect3DDevice9 :: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="6feda-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="6feda-116">Même si l’appareil n’a pas été réellement perdu, **ID3DXEffect :: OnLostDevice** est responsable de la libération de stateblocks et d’autres ressources qui doivent être libérées avant la réinitialisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6feda-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="6feda-117">Par conséquent, l’objet font ne peut pas être réutilisé avant d’appeler **IDirect3DDevice9 :: Reset** , puis [**ID3DXEffect :: OnResetDevice**](id3dxeffect--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6feda-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6feda-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6feda-118">Requirements</span></span>



| <span data-ttu-id="6feda-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6feda-119">Requirement</span></span> | <span data-ttu-id="6feda-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6feda-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6feda-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6feda-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6feda-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6feda-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6feda-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6feda-123">Library</span></span><br/> | <dl> <span data-ttu-id="6feda-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6feda-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6feda-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6feda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6feda-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6feda-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 





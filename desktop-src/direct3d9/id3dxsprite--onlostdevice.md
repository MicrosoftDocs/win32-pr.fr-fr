---
description: Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: 'ID3DXSprite :: OnLostDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f6b2b676e95b48f50b5c25a4bfc3a1bf3e7d610d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323033"
---
# <a name="id3dxspriteonlostdevice-method"></a><span data-ttu-id="e34ba-104">ID3DXSprite :: OnLostDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="e34ba-104">ID3DXSprite::OnLostDevice method</span></span>

<span data-ttu-id="e34ba-105">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="e34ba-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="e34ba-106">Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="e34ba-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e34ba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e34ba-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="e34ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e34ba-108">Parameters</span></span>

<span data-ttu-id="e34ba-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e34ba-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e34ba-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e34ba-110">Return value</span></span>

<span data-ttu-id="e34ba-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e34ba-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e34ba-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e34ba-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e34ba-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e34ba-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34ba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e34ba-114">Remarks</span></span>

<span data-ttu-id="e34ba-115">Cette méthode doit être appelée chaque fois que l’appareil est perdu ou avant que l’utilisateur n’appelle [**IDirect3DDevice9 :: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e34ba-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="e34ba-116">Même si l’appareil n’a pas été réellement perdu, **ID3DXSprite :: OnLostDevice** est responsable de la libération de stateblocks et d’autres ressources qui doivent être libérées avant la réinitialisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e34ba-116">Even if the device was not actually lost, **ID3DXSprite::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="e34ba-117">Par conséquent, l’objet font ne peut pas être réutilisé avant d’appeler **IDirect3DDevice9 :: Reset** , puis [**ID3DXSprite :: OnResetDevice**](id3dxsprite--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e34ba-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e34ba-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e34ba-118">Requirements</span></span>



| <span data-ttu-id="e34ba-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e34ba-119">Requirement</span></span> | <span data-ttu-id="e34ba-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e34ba-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e34ba-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e34ba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e34ba-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e34ba-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e34ba-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e34ba-123">Library</span></span><br/> | <dl> <span data-ttu-id="e34ba-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e34ba-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e34ba-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e34ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34ba-126">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="e34ba-126">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 





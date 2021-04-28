---
description: 'ID3DXRenderToEnvMap :: OnLostDevice, méthode : utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'ID3DXRenderToEnvMap :: OnLostDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88f27c259262eb7abb57246e547ad66866bb3dcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107197"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="912d7-104">ID3DXRenderToEnvMap :: OnLostDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="912d7-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="912d7-105">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="912d7-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="912d7-106">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="912d7-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="912d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="912d7-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="912d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="912d7-108">Parameters</span></span>

<span data-ttu-id="912d7-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="912d7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="912d7-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="912d7-110">Return value</span></span>

<span data-ttu-id="912d7-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="912d7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="912d7-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="912d7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="912d7-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="912d7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="912d7-114">Notes </span><span class="sxs-lookup"><span data-stu-id="912d7-114">Remarks</span></span>

<span data-ttu-id="912d7-115">Cette méthode doit être appelée chaque fois que l’appareil est perdu ou avant que l’utilisateur n’appelle [**IDirect3DDevice9 :: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="912d7-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="912d7-116">Même si l’appareil n’a pas été réellement perdu, **ID3DXRenderToEnvMap :: OnLostDevice** est responsable de la libération de stateblocks et d’autres ressources qui doivent être libérées avant la réinitialisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="912d7-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="912d7-117">Par conséquent, l’objet font ne peut pas être réutilisé avant d’appeler **IDirect3DDevice9 :: Reset** , puis [**ID3DXRenderToEnvMap :: OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="912d7-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="912d7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="912d7-118">Requirements</span></span>



| <span data-ttu-id="912d7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="912d7-119">Requirement</span></span> | <span data-ttu-id="912d7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="912d7-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="912d7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="912d7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="912d7-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="912d7-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="912d7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="912d7-123">Library</span></span><br/> | <dl> <span data-ttu-id="912d7-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="912d7-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="912d7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="912d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912d7-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="912d7-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 





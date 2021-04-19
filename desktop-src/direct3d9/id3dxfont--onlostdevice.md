---
description: Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'ID3DXFont :: OnLostDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542170"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="e82c5-104">ID3DXFont :: OnLostDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="e82c5-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="e82c5-105">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="e82c5-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="e82c5-106">Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="e82c5-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e82c5-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="e82c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e82c5-108">Parameters</span></span>

<span data-ttu-id="e82c5-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e82c5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e82c5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e82c5-110">Return value</span></span>

<span data-ttu-id="e82c5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e82c5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e82c5-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e82c5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e82c5-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e82c5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e82c5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e82c5-114">Remarks</span></span>

<span data-ttu-id="e82c5-115">Cette méthode doit être appelée chaque fois que l’appareil est perdu ou avant la [**réinitialisation**](/windows/desktop/api)des appels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e82c5-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="e82c5-116">Même si l’appareil n’a pas été réellement perdu, **OnLostDevice** est responsable de la libération de stateblocks et d’autres ressources qui devront peut-être être libérées avant la réinitialisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e82c5-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="e82c5-117">Par conséquent, l’objet font ne peut pas être réutilisé avant l’appel de **Reset** , puis [**OnResetDevice**](id3dxfont--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e82c5-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e82c5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e82c5-118">Requirements</span></span>



| <span data-ttu-id="e82c5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e82c5-119">Requirement</span></span> | <span data-ttu-id="e82c5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e82c5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e82c5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e82c5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e82c5-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e82c5-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e82c5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e82c5-123">Library</span></span><br/> | <dl> <span data-ttu-id="e82c5-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e82c5-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e82c5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e82c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82c5-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="e82c5-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 





---
description: 'Appelle ID3DXSprite :: Flush et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de ID3DXSprite :: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394184"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="0e07d-103">ID3DXSprite :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="0e07d-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="0e07d-104">Appelle [**ID3DXSprite :: Flush**](id3dxsprite--flush.md) et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de [**ID3DXSprite :: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="0e07d-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e07d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e07d-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="0e07d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e07d-106">Parameters</span></span>

<span data-ttu-id="0e07d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e07d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e07d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e07d-108">Return value</span></span>

<span data-ttu-id="0e07d-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e07d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e07d-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e07d-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0e07d-111">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="0e07d-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="0e07d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0e07d-112">Remarks</span></span>

<span data-ttu-id="0e07d-113">**ID3DXSprite :: end** ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="0e07d-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e07d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e07d-114">Requirements</span></span>



| <span data-ttu-id="0e07d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e07d-115">Requirement</span></span> | <span data-ttu-id="0e07d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e07d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e07d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e07d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0e07d-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e07d-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0e07d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e07d-119">Library</span></span><br/> | <dl> <span data-ttu-id="0e07d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e07d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e07d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e07d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e07d-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="0e07d-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="0e07d-123">**ID3DXSprite :: Begin**</span><span class="sxs-lookup"><span data-stu-id="0e07d-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 





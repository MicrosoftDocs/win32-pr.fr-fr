---
description: Récupère l’appareil associé à l’objet Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'ID3DXSprite :: GetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394192"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="33baa-103">ID3DXSprite :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="33baa-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="33baa-104">Récupère l’appareil associé à l’objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="33baa-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33baa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33baa-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="33baa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33baa-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="33baa-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="33baa-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="33baa-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="33baa-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à l’objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="33baa-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33baa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33baa-110">Return value</span></span>

<span data-ttu-id="33baa-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33baa-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33baa-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33baa-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="33baa-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="33baa-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="33baa-114">Notes</span><span class="sxs-lookup"><span data-stu-id="33baa-114">Remarks</span></span>

<span data-ttu-id="33baa-115">L’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="33baa-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="33baa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33baa-116">Requirements</span></span>



| <span data-ttu-id="33baa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33baa-117">Requirement</span></span> | <span data-ttu-id="33baa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="33baa-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33baa-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="33baa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="33baa-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="33baa-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33baa-121">Library</span></span><br/> | <dl> <span data-ttu-id="33baa-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33baa-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33baa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33baa-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="33baa-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 

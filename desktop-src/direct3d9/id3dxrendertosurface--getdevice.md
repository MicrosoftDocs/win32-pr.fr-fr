---
description: Récupère le périphérique Direct3D associé à la surface de rendu.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'ID3DXRenderToSurface :: GetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323310"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a><span data-ttu-id="d828b-103">ID3DXRenderToSurface :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="d828b-103">ID3DXRenderToSurface::GetDevice method</span></span>

<span data-ttu-id="d828b-104">Récupère le périphérique Direct3D associé à la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="d828b-104">Retrieves the Direct3D device associated with the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d828b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d828b-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d828b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d828b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d828b-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d828b-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d828b-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="d828b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="d828b-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="d828b-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d828b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d828b-110">Return value</span></span>

<span data-ttu-id="d828b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d828b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d828b-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d828b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d828b-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d828b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="d828b-114">L’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="d828b-114">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="d828b-115">Veillez à appeler [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) lorsque vous avez fini d’utiliser cette interface **IDirect3DDevice9** , sinon vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d828b-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="d828b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d828b-116">Requirements</span></span>



| <span data-ttu-id="d828b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d828b-117">Requirement</span></span> | <span data-ttu-id="d828b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d828b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d828b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d828b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d828b-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d828b-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d828b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d828b-121">Library</span></span><br/> | <dl> <span data-ttu-id="d828b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d828b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d828b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d828b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d828b-124">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="d828b-124">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 

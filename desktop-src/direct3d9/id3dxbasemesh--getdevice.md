---
description: Récupère l’appareil associé à la maille.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'ID3DXBaseMesh :: GetDevice, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043128"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="16626-103">ID3DXBaseMesh :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="16626-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="16626-104">Récupère l’appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="16626-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="16626-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16626-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="16626-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16626-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="16626-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="16626-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="16626-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="16626-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="16626-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16626-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16626-110">Return value</span></span>

<span data-ttu-id="16626-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16626-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16626-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16626-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16626-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="16626-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="16626-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16626-114">Remarks</span></span>

<span data-ttu-id="16626-115">L’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="16626-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="16626-116">Veillez à appeler [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) lorsque vous avez fini d’utiliser cette interface **IDirect3DDevice9** , sinon vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="16626-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="16626-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16626-117">Requirements</span></span>



| <span data-ttu-id="16626-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16626-118">Requirement</span></span> | <span data-ttu-id="16626-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="16626-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16626-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="16626-120">Header</span></span><br/>  | <dl> <span data-ttu-id="16626-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="16626-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="16626-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16626-122">Library</span></span><br/> | <dl> <span data-ttu-id="16626-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16626-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16626-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16626-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16626-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="16626-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 

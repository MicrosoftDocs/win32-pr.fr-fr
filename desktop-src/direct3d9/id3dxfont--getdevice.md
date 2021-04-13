---
description: Récupère le périphérique Direct3D associé à l’objet font.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'ID3DXFont :: GetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323318"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="a5378-103">ID3DXFont :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="a5378-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="a5378-104">Récupère le périphérique Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="a5378-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5378-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5378-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a5378-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5378-107">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5378-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5378-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="a5378-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="a5378-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="a5378-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5378-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5378-110">Return value</span></span>

<span data-ttu-id="a5378-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5378-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5378-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5378-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5378-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="a5378-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5378-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a5378-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5378-115">L’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="a5378-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="a5378-116">Veillez à appeler [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) lorsque vous avez fini d’utiliser cette interface **IDirect3DDevice9** , sinon vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a5378-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5378-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5378-117">Requirements</span></span>



| <span data-ttu-id="a5378-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5378-118">Requirement</span></span> | <span data-ttu-id="a5378-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5378-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5378-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5378-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a5378-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5378-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a5378-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5378-122">Library</span></span><br/> | <dl> <span data-ttu-id="a5378-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5378-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5378-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5378-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5378-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="a5378-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 

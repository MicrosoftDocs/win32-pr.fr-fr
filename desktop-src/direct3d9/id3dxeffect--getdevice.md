---
description: Récupère l’appareil associé à l’effet.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'ID3DXEffect :: GetDevice, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537294"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="54653-103">ID3DXEffect :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="54653-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="54653-104">Récupère l’appareil associé à l’effet.</span><span class="sxs-lookup"><span data-stu-id="54653-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="54653-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54653-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="54653-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54653-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54653-107">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54653-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54653-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="54653-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="54653-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à l’effet.</span><span class="sxs-lookup"><span data-stu-id="54653-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54653-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54653-110">Return value</span></span>

<span data-ttu-id="54653-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54653-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54653-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54653-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54653-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54653-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="54653-114">Notes</span><span class="sxs-lookup"><span data-stu-id="54653-114">Remarks</span></span>

<span data-ttu-id="54653-115">L’appel de cette méthode augmente le nombre de références internes pour l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="54653-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="54653-116">Veillez à appeler IUnknown :: Release lorsque vous avez fini d’utiliser l’interface **IDirect3DDevice9** ou une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="54653-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="54653-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54653-117">Requirements</span></span>



| <span data-ttu-id="54653-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54653-118">Requirement</span></span> | <span data-ttu-id="54653-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="54653-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54653-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="54653-120">Header</span></span><br/>  | <dl> <span data-ttu-id="54653-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="54653-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="54653-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54653-122">Library</span></span><br/> | <dl> <span data-ttu-id="54653-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54653-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54653-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54653-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54653-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="54653-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 

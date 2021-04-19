---
description: Associe un objet ID3DXTextureGutterHelper à l’objet ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer :: AttachGH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542176"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="bb8e1-103">ID3DXPRTBuffer :: AttachGH, méthode</span><span class="sxs-lookup"><span data-stu-id="bb8e1-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="bb8e1-104">Associe un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bb8e1-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb8e1-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="bb8e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb8e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb8e1-107">*pGH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb8e1-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8e1-108">Type : **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="bb8e1-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="bb8e1-109">Pointeur vers l’interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) d’un objet qui contient les données de la marge de texture.</span><span class="sxs-lookup"><span data-stu-id="bb8e1-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb8e1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb8e1-110">Return value</span></span>

<span data-ttu-id="bb8e1-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb8e1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb8e1-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb8e1-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8e1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bb8e1-113">Remarks</span></span>

<span data-ttu-id="bb8e1-114">Le décompte de références de l’objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) est automatiquement incrémenté d’une unité.</span><span class="sxs-lookup"><span data-stu-id="bb8e1-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="bb8e1-115">Tous les pointeurs **ID3DXTextureGutterHelper** existants seront libérés.</span><span class="sxs-lookup"><span data-stu-id="bb8e1-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="bb8e1-116">Vous devez vous assurer que le nombre d’appels **ID3DXPRTBuffer :: AttachGH** correspond au nombre d’appels [**ID3DXPRTBuffer :: ReleaseGH**](id3dxprtbuffer--releasegh.md) .</span><span class="sxs-lookup"><span data-stu-id="bb8e1-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="bb8e1-117">Après l’appel de **ID3DXPRTBuffer :: ReleaseGH**, le pointeur pGH retourné par **ID3DXPRTBuffer :: AttachGH** ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bb8e1-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8e1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb8e1-118">Requirements</span></span>



| <span data-ttu-id="bb8e1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb8e1-119">Requirement</span></span> | <span data-ttu-id="bb8e1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb8e1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8e1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb8e1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bb8e1-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e1-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb8e1-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb8e1-123">Library</span></span><br/> | <dl> <span data-ttu-id="bb8e1-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e1-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb8e1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb8e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8e1-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="bb8e1-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="bb8e1-127">**ID3DXPRTBuffer::ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="bb8e1-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 





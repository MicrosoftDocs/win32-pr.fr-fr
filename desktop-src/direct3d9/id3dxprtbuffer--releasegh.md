---
description: Dissocie un objet ID3DXTextureGutterHelper joint avec l’objet ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer :: ReleaseGH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394259"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="4e630-103">ID3DXPRTBuffer :: ReleaseGH, méthode</span><span class="sxs-lookup"><span data-stu-id="4e630-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="4e630-104">Dissocie un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) joint avec l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4e630-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e630-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e630-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="4e630-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e630-106">Parameters</span></span>

<span data-ttu-id="4e630-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e630-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e630-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e630-108">Return value</span></span>

<span data-ttu-id="4e630-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e630-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e630-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e630-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e630-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4e630-111">Remarks</span></span>

<span data-ttu-id="4e630-112">Cette méthode libère le pointeur vers l’interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="4e630-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="4e630-113">Vous devez vous assurer que le nombre d’appels [**ID3DXPRTBuffer :: AttachGH**](id3dxprtbuffer--attachgh.md) correspond au nombre d’appels **ID3DXPRTBuffer :: ReleaseGH** .</span><span class="sxs-lookup"><span data-stu-id="4e630-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="4e630-114">Après l’appel de **ID3DXPRTBuffer :: ReleaseGH**, le pointeur pGH retourné par **ID3DXPRTBuffer :: AttachGH** ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="4e630-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e630-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e630-115">Requirements</span></span>



| <span data-ttu-id="4e630-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e630-116">Requirement</span></span> | <span data-ttu-id="4e630-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e630-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e630-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e630-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4e630-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e630-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4e630-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e630-120">Library</span></span><br/> | <dl> <span data-ttu-id="4e630-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e630-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e630-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e630-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e630-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="4e630-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="4e630-124">**ID3DXPRTBuffer::AttachGH**</span><span class="sxs-lookup"><span data-stu-id="4e630-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 





---
description: Récupérez l’appareil associé à l’objet Sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite :: GetDevice, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323422"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="49c2b-103">ID3DX10Sprite :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="49c2b-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="49c2b-104">Récupérez l’appareil associé à l’objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="49c2b-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49c2b-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="49c2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49c2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c2b-107">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49c2b-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49c2b-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="49c2b-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="49c2b-109">Adresse d’un pointeur vers une interface ID3D10Device, représentant l’objet appareil Direct3D associé à l’objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="49c2b-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49c2b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49c2b-110">Return value</span></span>

<span data-ttu-id="49c2b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49c2b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49c2b-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49c2b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49c2b-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="49c2b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="49c2b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="49c2b-114">Remarks</span></span>

<span data-ttu-id="49c2b-115">L’appel de cette méthode augmente le nombre de références internes sur l’interface ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="49c2b-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c2b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49c2b-116">Requirements</span></span>



| <span data-ttu-id="49c2b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49c2b-117">Requirement</span></span> | <span data-ttu-id="49c2b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="49c2b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49c2b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="49c2b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="49c2b-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c2b-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="49c2b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49c2b-121">Library</span></span><br/> | <dl> <span data-ttu-id="49c2b-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49c2b-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c2b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49c2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c2b-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="49c2b-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="49c2b-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="49c2b-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





---
description: Récupérez l’appareil Direct3D associé à l’objet font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font :: GetDevice, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535179"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="9e239-103">ID3DX10Font :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="9e239-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="9e239-104">Récupérez l’appareil Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="9e239-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e239-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e239-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9e239-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e239-107">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e239-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e239-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e239-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="9e239-109">Adresse d’un pointeur vers une interface ID3D10Device, représentant l’objet appareil Direct3D associé à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="9e239-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e239-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e239-110">Return value</span></span>

<span data-ttu-id="9e239-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e239-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e239-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e239-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9e239-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="9e239-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e239-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9e239-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e239-115">L’appel de cette méthode augmente le nombre de références internes sur l’interface ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="9e239-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="9e239-116">Veillez à appeler IUnknown lorsque vous avez fini d’utiliser cette interface ID3D10Device, sinon vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9e239-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e239-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e239-117">Requirements</span></span>



| <span data-ttu-id="9e239-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e239-118">Requirement</span></span> | <span data-ttu-id="9e239-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e239-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e239-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e239-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9e239-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e239-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e239-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e239-122">Library</span></span><br/> | <dl> <span data-ttu-id="9e239-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e239-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e239-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e239-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e239-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="9e239-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="9e239-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9e239-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





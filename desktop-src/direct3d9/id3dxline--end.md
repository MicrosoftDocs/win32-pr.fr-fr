---
description: 'Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de ID3DXLine :: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531574"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="d7537-103">ID3DXLine :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="d7537-103">ID3DXLine::End method</span></span>

<span data-ttu-id="d7537-104">Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de [**ID3DXLine :: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="d7537-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7537-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7537-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="d7537-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7537-106">Parameters</span></span>

<span data-ttu-id="d7537-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d7537-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7537-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7537-108">Return value</span></span>

<span data-ttu-id="d7537-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7537-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7537-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7537-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d7537-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="d7537-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7537-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7537-112">Remarks</span></span>

<span data-ttu-id="d7537-113">**ID3DXLine :: end** ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="d7537-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7537-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7537-114">Requirements</span></span>



| <span data-ttu-id="d7537-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7537-115">Requirement</span></span> | <span data-ttu-id="d7537-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7537-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7537-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7537-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d7537-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7537-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d7537-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7537-119">Library</span></span><br/> | <dl> <span data-ttu-id="d7537-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7537-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7537-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7537-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7537-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="d7537-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="d7537-123">**ID3DXLine :: Begin**</span><span class="sxs-lookup"><span data-stu-id="d7537-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 





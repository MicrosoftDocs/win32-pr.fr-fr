---
description: Fonction proxy pour la méthode GetBitsPerPixel.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529380"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="a640d-103">IWICPixelFormatInfo \_ \_ fonction proxy GetBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="a640d-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="a640d-104">Fonction proxy pour la méthode [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .</span><span class="sxs-lookup"><span data-stu-id="a640d-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a640d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a640d-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="a640d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a640d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a640d-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a640d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a640d-108">Tapez : \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a640d-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="a640d-109">Pointeur vers cet objet [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="a640d-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="a640d-110">*puiBitsPerPixel* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a640d-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a640d-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="a640d-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="a640d-112">Pointeur qui reçoit les BPP du format de pixel.</span><span class="sxs-lookup"><span data-stu-id="a640d-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a640d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a640d-113">Return value</span></span>

<span data-ttu-id="a640d-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a640d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a640d-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a640d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a640d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a640d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a640d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a640d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a640d-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a640d-118">Requirements</span></span>



| <span data-ttu-id="a640d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a640d-119">Requirement</span></span> | <span data-ttu-id="a640d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a640d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a640d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a640d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a640d-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a640d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a640d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a640d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a640d-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a640d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a640d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a640d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a640d-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a640d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





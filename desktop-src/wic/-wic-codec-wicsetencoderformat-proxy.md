---
description: Fonction proxy pour négocier le format de pixel et la palette pour l’encodeur.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541820"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="b2b44-103">\_Fonction proxy WICSetEncoderFormat</span><span class="sxs-lookup"><span data-stu-id="b2b44-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="b2b44-104">Fonction proxy pour négocier le format de pixel et la palette pour l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="b2b44-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b44-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="b2b44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b44-107">*pSourceIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b44-108">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b2b44-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b2b44-109">Pointeur vers la bitmap source.</span><span class="sxs-lookup"><span data-stu-id="b2b44-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b2b44-110">_pIPalette \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b44-111">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b2b44-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b2b44-112">Pointeur vers la palette à utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="b2b44-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="b2b44-113">_pIFrameEncode \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b44-114">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="b2b44-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="b2b44-115">Pointeur vers l’objet de codage de frame.</span><span class="sxs-lookup"><span data-stu-id="b2b44-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="b2b44-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b44-117">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b2b44-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="b2b44-118">Pointeur qui reçoit un pointeur vers la source de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2b44-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b44-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2b44-119">Return value</span></span>

<span data-ttu-id="b2b44-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b2b44-120">Type: **HRESULT**</span></span>

<span data-ttu-id="b2b44-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2b44-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2b44-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2b44-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b44-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b2b44-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b44-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b2b44-124">Requirements</span></span>



| <span data-ttu-id="b2b44-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2b44-125">Requirement</span></span> | <span data-ttu-id="b2b44-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2b44-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b44-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b44-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b44-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b2b44-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b44-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b44-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2b44-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b2b44-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b44-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b44-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2b44-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





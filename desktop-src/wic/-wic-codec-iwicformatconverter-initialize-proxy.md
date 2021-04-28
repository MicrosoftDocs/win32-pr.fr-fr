---
description: IWICFormatConverter_Initialize_Proxy fonction-proxy pour la méthode Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d70d852adc8f810438ce46dc30345e68fa27e0fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097157"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="a9597-103">IWICFormatConverter \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="a9597-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="a9597-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="a9597-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9597-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9597-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="a9597-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9597-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-108">Type : **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span><span class="sxs-lookup"><span data-stu-id="a9597-108">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span></span>

<span data-ttu-id="a9597-109">Pointeur vers cet objet [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="a9597-109">Pointer to this [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="a9597-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="a9597-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="a9597-112">Bitmap d’entrée à convertir.</span><span class="sxs-lookup"><span data-stu-id="a9597-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="a9597-113">*dstFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-113">*dstFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-114">Type : **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="a9597-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="a9597-115">GUID du format de pixel de destination.</span><span class="sxs-lookup"><span data-stu-id="a9597-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="a9597-116">*tramage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-117">Type : **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="a9597-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="a9597-118">[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) utilisé pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="a9597-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="a9597-119">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-120">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="a9597-120">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="a9597-121">Palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="a9597-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="a9597-122">*alphaThresholdPercent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-122">*alphaThresholdPercent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-123">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="a9597-123">Type: **double**</span></span>

<span data-ttu-id="a9597-124">Seuil alpha à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="a9597-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="a9597-125">*paletteTranslate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9597-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9597-126">Type : **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="a9597-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="a9597-127">Type de traduction de palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="a9597-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9597-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9597-128">Return value</span></span>

<span data-ttu-id="a9597-129">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a9597-129">Type: **HRESULT**</span></span>

<span data-ttu-id="a9597-130">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9597-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9597-131">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9597-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9597-132">Notes</span><span class="sxs-lookup"><span data-stu-id="a9597-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a9597-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9597-133">Requirements</span></span>



| <span data-ttu-id="a9597-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9597-134">Requirement</span></span> | <span data-ttu-id="a9597-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9597-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9597-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9597-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9597-137">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9597-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a9597-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9597-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9597-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9597-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a9597-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a9597-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9597-141"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9597-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





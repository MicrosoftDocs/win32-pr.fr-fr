---
description: Fonction proxy pour la méthode Initialize.
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
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209914"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="b486d-103">IWICFormatConverter \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="b486d-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="b486d-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="b486d-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b486d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b486d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b486d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b486d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b486d-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-108">Tapez : \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="b486d-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="b486d-109">Pointeur vers cet objet [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="b486d-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="b486d-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b486d-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b486d-112">Bitmap d’entrée à convertir.</span><span class="sxs-lookup"><span data-stu-id="b486d-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="b486d-113">_dstFormat \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-114">Type : **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="b486d-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="b486d-115">GUID du format de pixel de destination.</span><span class="sxs-lookup"><span data-stu-id="b486d-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="b486d-116">*tramage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-117">Type : **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="b486d-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="b486d-118">[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) utilisé pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="b486d-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b486d-119">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-120">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b486d-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b486d-121">Palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="b486d-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b486d-122">_alphaThresholdPercent \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-123">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="b486d-123">Type: **double**</span></span>

<span data-ttu-id="b486d-124">Seuil alpha à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="b486d-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b486d-125">*paletteTranslate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b486d-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b486d-126">Type : **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="b486d-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="b486d-127">Type de traduction de palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="b486d-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b486d-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b486d-128">Return value</span></span>

<span data-ttu-id="b486d-129">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b486d-129">Type: **HRESULT**</span></span>

<span data-ttu-id="b486d-130">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b486d-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b486d-131">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b486d-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b486d-132">Notes</span><span class="sxs-lookup"><span data-stu-id="b486d-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b486d-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b486d-133">Requirements</span></span>



| <span data-ttu-id="b486d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b486d-134">Requirement</span></span> | <span data-ttu-id="b486d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b486d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b486d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b486d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b486d-137">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b486d-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b486d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b486d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b486d-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b486d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b486d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b486d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b486d-141"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b486d-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





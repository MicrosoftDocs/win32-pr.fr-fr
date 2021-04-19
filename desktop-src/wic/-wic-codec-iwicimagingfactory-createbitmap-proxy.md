---
description: Fonction proxy pour la méthode CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536584"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="fd063-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmap</span><span class="sxs-lookup"><span data-stu-id="fd063-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="fd063-104">Fonction proxy pour la méthode [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .</span><span class="sxs-lookup"><span data-stu-id="fd063-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd063-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd063-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="fd063-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd063-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd063-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="fd063-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="fd063-109">_uiWidth \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd063-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="fd063-110">Type: **UINT**</span></span>

<span data-ttu-id="fd063-111">Largeur de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="fd063-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="fd063-112">*uiHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd063-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="fd063-113">Type: **UINT**</span></span>

<span data-ttu-id="fd063-114">Hauteur de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="fd063-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="fd063-115">*PixelFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd063-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-116">Type : **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="fd063-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="fd063-117">Format de pixel de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="fd063-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="fd063-118">*option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd063-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-119">Type : **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="fd063-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="fd063-120">Options de création du cache de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="fd063-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="fd063-121">*ppIBitmap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fd063-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd063-122">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="fd063-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="fd063-123">Pointeur qui reçoit un pointeur vers la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="fd063-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd063-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd063-124">Return value</span></span>

<span data-ttu-id="fd063-125">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd063-125">Type: **HRESULT**</span></span>

<span data-ttu-id="fd063-126">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd063-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd063-127">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd063-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd063-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fd063-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fd063-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd063-129">Requirements</span></span>



| <span data-ttu-id="fd063-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd063-130">Requirement</span></span> | <span data-ttu-id="fd063-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd063-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd063-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd063-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd063-133">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd063-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fd063-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd063-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd063-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd063-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fd063-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fd063-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd063-137"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd063-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





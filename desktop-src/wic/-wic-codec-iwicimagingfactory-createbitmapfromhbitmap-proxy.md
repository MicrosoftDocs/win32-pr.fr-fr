---
description: Fonction proxy pour la méthode CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523366"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="46e7a-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromHBITMAP</span><span class="sxs-lookup"><span data-stu-id="46e7a-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="46e7a-104">Fonction proxy pour la méthode [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .</span><span class="sxs-lookup"><span data-stu-id="46e7a-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e7a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46e7a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="46e7a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46e7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e7a-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e7a-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="46e7a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-109">_hBitmap \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e7a-110">Type : **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="46e7a-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="46e7a-111">Handle de bitmap à partir duquel créer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="46e7a-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-112">*HPALETTE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e7a-113">Type : **HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="46e7a-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="46e7a-114">Handle de palette utilisé pour créer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="46e7a-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-115">*options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e7a-116">Type : **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="46e7a-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="46e7a-117">Options de canal alpha pour créer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="46e7a-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="46e7a-118">*ppIBitmap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e7a-119">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="46e7a-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="46e7a-120">Pointeur qui reçoit un pointeur vers la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="46e7a-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e7a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46e7a-121">Return value</span></span>

<span data-ttu-id="46e7a-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46e7a-122">Type: **HRESULT**</span></span>

<span data-ttu-id="46e7a-123">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46e7a-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46e7a-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46e7a-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e7a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="46e7a-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="46e7a-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46e7a-126">Requirements</span></span>



| <span data-ttu-id="46e7a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46e7a-127">Requirement</span></span> | <span data-ttu-id="46e7a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="46e7a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e7a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46e7a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="46e7a-130">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="46e7a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46e7a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="46e7a-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46e7a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="46e7a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="46e7a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e7a-134"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46e7a-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Fonction proxy pour la méthode CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535535"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="ba25e-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromMemory</span><span class="sxs-lookup"><span data-stu-id="ba25e-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="ba25e-104">Fonction proxy pour la méthode [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .</span><span class="sxs-lookup"><span data-stu-id="ba25e-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba25e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba25e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="ba25e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba25e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba25e-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ba25e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-109">_uiWidth \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ba25e-110">Type: **UINT**</span></span>

<span data-ttu-id="ba25e-111">Largeur de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba25e-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-112">*uiHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ba25e-113">Type: **UINT**</span></span>

<span data-ttu-id="ba25e-114">Hauteur de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba25e-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-115">*PixelFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-116">Type : **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="ba25e-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="ba25e-117">Format de pixel de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba25e-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-118">*cbStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ba25e-119">Type: **UINT**</span></span>

<span data-ttu-id="ba25e-120">[*Stride*](/windows) des données de pixels données.</span><span class="sxs-lookup"><span data-stu-id="ba25e-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-121">*cbBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-122">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="ba25e-122">Type: **UINT**</span></span>

<span data-ttu-id="ba25e-123">Taille de *pbBuffer*.</span><span class="sxs-lookup"><span data-stu-id="ba25e-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-124">*pbBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-125">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="ba25e-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ba25e-126">Mémoire tampon utilisée pour créer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba25e-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ba25e-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba25e-128">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="ba25e-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="ba25e-129">Pointeur qui reçoit un pointeur vers la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="ba25e-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba25e-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba25e-130">Return value</span></span>

<span data-ttu-id="ba25e-131">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ba25e-131">Type: **HRESULT**</span></span>

<span data-ttu-id="ba25e-132">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba25e-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba25e-133">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba25e-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba25e-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ba25e-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ba25e-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ba25e-135">Requirements</span></span>



| <span data-ttu-id="ba25e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba25e-136">Requirement</span></span> | <span data-ttu-id="ba25e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba25e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba25e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba25e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ba25e-139">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ba25e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba25e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ba25e-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba25e-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ba25e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ba25e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba25e-143"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba25e-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


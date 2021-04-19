---
description: Fonction proxy pour la méthode CreateFastMetadataEncoderFromFrameDecode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532157"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="9da4c-103">IWICImagingFactory \_ \_ fonction proxy CreateFastMetadataEncoderFromFrameDecode</span><span class="sxs-lookup"><span data-stu-id="9da4c-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="9da4c-104">Fonction proxy pour la méthode [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) .</span><span class="sxs-lookup"><span data-stu-id="9da4c-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9da4c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="9da4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9da4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da4c-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9da4c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9da4c-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="9da4c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="9da4c-109">_pIFrameDecoder \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9da4c-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9da4c-110">Tapez : \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="9da4c-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="9da4c-111">[_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) à partir duquel créer le [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="9da4c-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="9da4c-112">*ppIFME* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9da4c-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9da4c-113">Type : **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="9da4c-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="9da4c-114">Pointeur qui reçoit un pointeur vers un nouveau [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="9da4c-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da4c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9da4c-115">Return value</span></span>

<span data-ttu-id="9da4c-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9da4c-116">Type: **HRESULT**</span></span>

<span data-ttu-id="9da4c-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9da4c-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9da4c-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9da4c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9da4c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9da4c-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9da4c-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9da4c-120">Requirements</span></span>



| <span data-ttu-id="9da4c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9da4c-121">Requirement</span></span> | <span data-ttu-id="9da4c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9da4c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da4c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9da4c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9da4c-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9da4c-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9da4c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9da4c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9da4c-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9da4c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9da4c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9da4c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9da4c-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9da4c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





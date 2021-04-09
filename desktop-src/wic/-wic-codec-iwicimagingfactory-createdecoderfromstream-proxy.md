---
description: Fonction proxy pour la méthode CreateDecoderFromStream.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: IWICImagingFactory_CreateDecoderFromStream_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760191"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="7dee7-103">IWICImagingFactory \_ \_ fonction proxy CreateDecoderFromStream</span><span class="sxs-lookup"><span data-stu-id="7dee7-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="7dee7-104">Fonction proxy pour la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="7dee7-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dee7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dee7-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="7dee7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dee7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dee7-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="7dee7-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-109">_pIStream \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-110">Type : \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="7dee7-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="7dee7-111">Flux à partir duquel créer le décodeur.</span><span class="sxs-lookup"><span data-stu-id="7dee7-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-112">_pguidVendor \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="7dee7-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="7dee7-114">GUID du fournisseur pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="7dee7-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-115">_metadataOptions \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-116">Type : **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="7dee7-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="7dee7-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) à utiliser lors de la création du décodeur.</span><span class="sxs-lookup"><span data-stu-id="7dee7-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="7dee7-118">*ppIDecoder* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dee7-119">Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="7dee7-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="7dee7-120">Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="7dee7-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dee7-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dee7-121">Return value</span></span>

<span data-ttu-id="7dee7-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7dee7-122">Type: **HRESULT**</span></span>

<span data-ttu-id="7dee7-123">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7dee7-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7dee7-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7dee7-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dee7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7dee7-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7dee7-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7dee7-126">Requirements</span></span>



| <span data-ttu-id="7dee7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dee7-127">Requirement</span></span> | <span data-ttu-id="7dee7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dee7-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dee7-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dee7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7dee7-130">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7dee7-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dee7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7dee7-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dee7-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7dee7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7dee7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dee7-134"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dee7-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


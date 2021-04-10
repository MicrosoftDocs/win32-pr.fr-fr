---
description: Fonction proxy pour la méthode CreateDecoderFromFileHandle.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952192"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="5d502-103">IWICImagingFactory \_ \_ fonction proxy CreateDecoderFromFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d502-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="5d502-104">Fonction proxy pour la méthode [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .</span><span class="sxs-lookup"><span data-stu-id="5d502-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d502-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d502-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="5d502-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d502-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d502-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d502-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5d502-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5d502-109">_hFile \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d502-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d502-110">Type : **ULong \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="5d502-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="5d502-111">Handle de fichier à partir duquel créer le décodeur.</span><span class="sxs-lookup"><span data-stu-id="5d502-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="5d502-112">*pGuidVendor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d502-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d502-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="5d502-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="5d502-114">GUID du fournisseur pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="5d502-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="5d502-115">_metadataOptions \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d502-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d502-116">Type : **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="5d502-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="5d502-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) à utiliser lors de la création du décodeur.</span><span class="sxs-lookup"><span data-stu-id="5d502-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="5d502-118">*ppIDecoder* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d502-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d502-119">Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d502-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="5d502-120">Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="5d502-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d502-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d502-121">Return value</span></span>

<span data-ttu-id="5d502-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d502-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5d502-123">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d502-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d502-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d502-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d502-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5d502-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5d502-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d502-126">Requirements</span></span>



| <span data-ttu-id="5d502-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d502-127">Requirement</span></span> | <span data-ttu-id="5d502-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d502-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d502-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d502-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d502-130">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d502-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5d502-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d502-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d502-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d502-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5d502-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5d502-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d502-134"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d502-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





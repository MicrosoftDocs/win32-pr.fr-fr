---
description: Fonction proxy pour la méthode CreateFastMetadataEncoderFromDecoder.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522027"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="910e6-103">IWICImagingFactory \_ \_ fonction proxy CreateFastMetadataEncoderFromDecoder</span><span class="sxs-lookup"><span data-stu-id="910e6-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="910e6-104">Fonction proxy pour la méthode [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .</span><span class="sxs-lookup"><span data-stu-id="910e6-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="910e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="910e6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="910e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="910e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="910e6-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="910e6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910e6-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="910e6-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="910e6-109">_pIDecoder \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="910e6-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910e6-110">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="910e6-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="910e6-111">Décodeur à partir duquel créer le [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="910e6-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="910e6-112">*ppIFME* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="910e6-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="910e6-113">Type : **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="910e6-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="910e6-114">Pointeur qui reçoit un pointeur vers le nouvel [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="910e6-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="910e6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="910e6-115">Return value</span></span>

<span data-ttu-id="910e6-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="910e6-116">Type: **HRESULT**</span></span>

<span data-ttu-id="910e6-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="910e6-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="910e6-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="910e6-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="910e6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="910e6-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="910e6-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="910e6-120">Requirements</span></span>



| <span data-ttu-id="910e6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="910e6-121">Requirement</span></span> | <span data-ttu-id="910e6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="910e6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="910e6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="910e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="910e6-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="910e6-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="910e6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="910e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="910e6-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="910e6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="910e6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="910e6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="910e6-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="910e6-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





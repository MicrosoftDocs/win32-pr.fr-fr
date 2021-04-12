---
description: Fonction proxy pour la méthode GetMetadataQueryReader.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: IWICBitmapDecoder_GetMetadataQueryReader_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318265"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="638f3-103">\_Fonction de \_ proxy IWICBitmapDecoder GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="638f3-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="638f3-104">Fonction proxy pour la méthode [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="638f3-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="638f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="638f3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="638f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="638f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="638f3-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="638f3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="638f3-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="638f3-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="638f3-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="638f3-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="638f3-110">*ppIMetadataQueryReader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="638f3-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="638f3-111">Type : **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="638f3-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="638f3-112">Pointeur qui reçoit un pointeur vers les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="638f3-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="638f3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="638f3-113">Return value</span></span>

<span data-ttu-id="638f3-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="638f3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="638f3-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="638f3-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="638f3-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="638f3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="638f3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="638f3-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="638f3-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="638f3-118">Requirements</span></span>



| <span data-ttu-id="638f3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="638f3-119">Requirement</span></span> | <span data-ttu-id="638f3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="638f3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="638f3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="638f3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="638f3-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="638f3-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="638f3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="638f3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="638f3-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="638f3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="638f3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="638f3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="638f3-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="638f3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





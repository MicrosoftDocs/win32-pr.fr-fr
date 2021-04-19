---
description: Fonction proxy pour la méthode GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530834"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="4882c-103">\_ \_ Fonction proxy GetMetadataQueryReader IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="4882c-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="4882c-104">Fonction proxy pour la méthode [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="4882c-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4882c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4882c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="4882c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4882c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4882c-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4882c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4882c-108">Tapez : \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="4882c-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="4882c-109">Pointeur vers cet objet [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="4882c-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="4882c-110">*ppIMetadataQueryReader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4882c-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4882c-111">Type : **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="4882c-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="4882c-112">Pointeur qui reçoit un pointeur vers un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="4882c-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4882c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4882c-113">Return value</span></span>

<span data-ttu-id="4882c-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4882c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4882c-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4882c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4882c-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4882c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4882c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4882c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4882c-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4882c-118">Requirements</span></span>



| <span data-ttu-id="4882c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4882c-119">Requirement</span></span> | <span data-ttu-id="4882c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4882c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4882c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4882c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4882c-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4882c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4882c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4882c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4882c-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4882c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4882c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4882c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4882c-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4882c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





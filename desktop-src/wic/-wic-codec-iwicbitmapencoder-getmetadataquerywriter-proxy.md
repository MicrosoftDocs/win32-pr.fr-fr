---
description: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy fonction de proxy de fonction pour la méthode GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091167"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="3020e-103">IWICBitmapEncoder \_ \_ fonction proxy GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="3020e-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="3020e-104">Fonction proxy pour la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="3020e-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3020e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3020e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="3020e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3020e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3020e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3020e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3020e-108">Type : **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="3020e-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="3020e-109">Pointeur vers cet objet [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="3020e-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="3020e-110">*ppIMetadataQueryWriter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3020e-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3020e-111">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="3020e-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="3020e-112">Pointeur qui reçoit un pointeur vers un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="3020e-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3020e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3020e-113">Return value</span></span>

<span data-ttu-id="3020e-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3020e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3020e-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3020e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3020e-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3020e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3020e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3020e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3020e-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3020e-118">Requirements</span></span>



| <span data-ttu-id="3020e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3020e-119">Requirement</span></span> | <span data-ttu-id="3020e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3020e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3020e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3020e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3020e-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3020e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3020e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3020e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3020e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3020e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3020e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3020e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3020e-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3020e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





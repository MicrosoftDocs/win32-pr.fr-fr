---
description: Fonction proxy pour la méthode GetFrameCount.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: IWICBitmapDecoder_GetFrameCount_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751237"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="6e73d-103">\_Fonction de \_ proxy IWICBitmapDecoder GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="6e73d-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="6e73d-104">Fonction proxy pour la méthode [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="6e73d-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e73d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e73d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="6e73d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e73d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e73d-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e73d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e73d-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6e73d-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="6e73d-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="6e73d-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6e73d-110">*pCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e73d-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e73d-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="6e73d-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="6e73d-112">Pointeur qui reçoit le nombre total de frames dans l’image.</span><span class="sxs-lookup"><span data-stu-id="6e73d-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e73d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e73d-113">Return value</span></span>

<span data-ttu-id="6e73d-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6e73d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6e73d-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e73d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e73d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e73d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e73d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6e73d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6e73d-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6e73d-118">Requirements</span></span>



| <span data-ttu-id="6e73d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e73d-119">Requirement</span></span> | <span data-ttu-id="6e73d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e73d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e73d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e73d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e73d-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e73d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6e73d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e73d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e73d-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e73d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6e73d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e73d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e73d-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e73d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





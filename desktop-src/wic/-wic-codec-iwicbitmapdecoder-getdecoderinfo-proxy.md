---
description: Fonction proxy pour la méthode GetDecoderInfo.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: IWICBitmapDecoder_GetDecoderInfo_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484769"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="100f7-103">\_Fonction de \_ proxy IWICBitmapDecoder GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="100f7-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="100f7-104">Fonction proxy pour la méthode [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="100f7-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="100f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="100f7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="100f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="100f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100f7-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="100f7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100f7-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="100f7-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="100f7-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="100f7-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="100f7-110">*ppIDecoderInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="100f7-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="100f7-111">Type : **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="100f7-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="100f7-112">Pointeur qui reçoit un pointeur vers un [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span><span class="sxs-lookup"><span data-stu-id="100f7-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100f7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="100f7-113">Return value</span></span>

<span data-ttu-id="100f7-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="100f7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="100f7-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="100f7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="100f7-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="100f7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="100f7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="100f7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="100f7-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="100f7-118">Requirements</span></span>



| <span data-ttu-id="100f7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="100f7-119">Requirement</span></span> | <span data-ttu-id="100f7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="100f7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="100f7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="100f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="100f7-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="100f7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="100f7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="100f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="100f7-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="100f7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="100f7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="100f7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="100f7-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="100f7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





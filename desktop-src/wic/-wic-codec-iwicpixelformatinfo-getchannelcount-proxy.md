---
description: Fonction proxy pour la méthode GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525746"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="74949-103">IWICPixelFormatInfo \_ \_ fonction proxy GetChannelCount</span><span class="sxs-lookup"><span data-stu-id="74949-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="74949-104">Fonction proxy pour la méthode [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .</span><span class="sxs-lookup"><span data-stu-id="74949-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74949-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74949-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="74949-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74949-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74949-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74949-108">Tapez : \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="74949-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="74949-109">Pointeur vers cet objet [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="74949-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="74949-110">*puiChannelCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="74949-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74949-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="74949-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="74949-112">Pointeur qui reçoit le nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="74949-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74949-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74949-113">Return value</span></span>

<span data-ttu-id="74949-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="74949-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="74949-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="74949-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74949-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74949-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74949-117">Notes</span><span class="sxs-lookup"><span data-stu-id="74949-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="74949-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="74949-118">Requirements</span></span>



| <span data-ttu-id="74949-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74949-119">Requirement</span></span> | <span data-ttu-id="74949-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="74949-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74949-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74949-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74949-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74949-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="74949-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74949-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74949-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74949-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="74949-125">DLL</span><span class="sxs-lookup"><span data-stu-id="74949-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74949-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74949-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Fonction proxy pour la méthode GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201386"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="3cdea-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="3cdea-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="3cdea-104">Fonction proxy pour la méthode [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="3cdea-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cdea-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3cdea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cdea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cdea-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cdea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdea-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3cdea-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="3cdea-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="3cdea-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="3cdea-110">*pguidContainerFormat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3cdea-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdea-111">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="3cdea-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="3cdea-112">Pointeur qui reçoit le GUID du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3cdea-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cdea-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cdea-113">Return value</span></span>

<span data-ttu-id="3cdea-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3cdea-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3cdea-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3cdea-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3cdea-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3cdea-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cdea-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3cdea-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3cdea-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3cdea-118">Requirements</span></span>



| <span data-ttu-id="3cdea-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cdea-119">Requirement</span></span> | <span data-ttu-id="3cdea-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cdea-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdea-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cdea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3cdea-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cdea-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3cdea-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cdea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3cdea-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cdea-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3cdea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3cdea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cdea-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cdea-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





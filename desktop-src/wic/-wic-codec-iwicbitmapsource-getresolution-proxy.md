---
description: Fonction proxy pour la méthode GetResolution.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203232"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="6eefb-103">IWICBitmapSource \_ \_ fonction proxy GetResolution</span><span class="sxs-lookup"><span data-stu-id="6eefb-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="6eefb-104">Fonction proxy pour la méthode [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) .</span><span class="sxs-lookup"><span data-stu-id="6eefb-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eefb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6eefb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="6eefb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6eefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eefb-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eefb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eefb-108">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="6eefb-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="6eefb-109">Pointeur vers cet objet [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="6eefb-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="6eefb-110">*pDpiX* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6eefb-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eefb-111">Type : \**double \** _</span><span class="sxs-lookup"><span data-stu-id="6eefb-111">Type: \**double\** _</span></span>

<span data-ttu-id="6eefb-112">Pointeur qui reçoit la résolution PPP de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="6eefb-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="6eefb-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6eefb-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eefb-114">Type : \**double \** _</span><span class="sxs-lookup"><span data-stu-id="6eefb-114">Type: \**double\** _</span></span>

<span data-ttu-id="6eefb-115">Pointeur qui reçoit la résolution PPP de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="6eefb-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eefb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6eefb-116">Return value</span></span>

<span data-ttu-id="6eefb-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6eefb-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6eefb-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6eefb-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6eefb-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6eefb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eefb-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6eefb-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6eefb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6eefb-121">Requirements</span></span>



| <span data-ttu-id="6eefb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eefb-122">Requirement</span></span> | <span data-ttu-id="6eefb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eefb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eefb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eefb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6eefb-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eefb-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6eefb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eefb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6eefb-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eefb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6eefb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6eefb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eefb-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eefb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





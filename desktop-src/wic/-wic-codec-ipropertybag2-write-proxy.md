---
description: 'Fonction proxy WIC (Windows Imaging Component) pour IPropertyBag2 :: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: IPropertyBag2_Write_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318277"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="843e2-103">IPropertyBag2 \_ fonction de proxy d’écriture \_</span><span class="sxs-lookup"><span data-stu-id="843e2-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="843e2-104">Fonction proxy WIC (Windows Imaging Component) pour IPropertyBag2 :: Write.</span><span class="sxs-lookup"><span data-stu-id="843e2-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="843e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="843e2-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="843e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="843e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843e2-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="843e2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843e2-108">Tapez : \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="843e2-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="843e2-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="843e2-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="843e2-110">_cProperties \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="843e2-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843e2-111">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="843e2-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="843e2-112">*ppropBag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="843e2-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843e2-113">Tapez : \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="843e2-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="843e2-114">_pvarValue \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="843e2-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843e2-115">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="843e2-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="843e2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="843e2-116">Return value</span></span>

<span data-ttu-id="843e2-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="843e2-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="843e2-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="843e2-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="843e2-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="843e2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="843e2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="843e2-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="843e2-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="843e2-121">Requirements</span></span>



| <span data-ttu-id="843e2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="843e2-122">Requirement</span></span> | <span data-ttu-id="843e2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="843e2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843e2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="843e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="843e2-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="843e2-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="843e2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="843e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="843e2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="843e2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="843e2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="843e2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="843e2-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="843e2-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


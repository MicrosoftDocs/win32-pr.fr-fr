---
description: 'Fonction proxy WIC (Windows Imaging Component) pour IEnumString :: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513209"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="1e1d2-103">IEnumString \_ réinitialisation de la \_ \_ fonction proxy WIC</span><span class="sxs-lookup"><span data-stu-id="1e1d2-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="1e1d2-104">Fonction proxy WIC (Windows Imaging Component) pour IEnumString :: Reset.</span><span class="sxs-lookup"><span data-stu-id="1e1d2-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e1d2-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="1e1d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e1d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1d2-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1d2-108">Tapez : \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="1e1d2-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="1e1d2-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="1e1d2-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="1e1d2-110">_celt \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1d2-111">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="1e1d2-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="1e1d2-112">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1d2-113">Tapez : \**LPOLESTR \** _</span><span class="sxs-lookup"><span data-stu-id="1e1d2-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="1e1d2-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1d2-115">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="1e1d2-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1d2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e1d2-116">Return value</span></span>

<span data-ttu-id="1e1d2-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1e1d2-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1e1d2-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e1d2-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e1d2-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e1d2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e1d2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1e1d2-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1d2-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e1d2-121">Requirements</span></span>



| <span data-ttu-id="1e1d2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e1d2-122">Requirement</span></span> | <span data-ttu-id="1e1d2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e1d2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1d2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1d2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1d2-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1e1d2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1d2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1d2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e1d2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1e1d2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1e1d2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e1d2-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e1d2-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
title: FreeUiInfo, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à une structure UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo fonction NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103285"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="a80e8-104">FreeUiInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="a80e8-104">FreeUiInfo function</span></span>

<span data-ttu-id="a80e8-105">La fonction **FreeUiInfo** libère la mémoire allouée en interne à une structure [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) .</span><span class="sxs-lookup"><span data-stu-id="a80e8-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="a80e8-106">Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a80e8-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a80e8-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a80e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a80e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80e8-109">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a80e8-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80e8-110">Tapez : \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a80e8-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="a80e8-111">Structure.</span><span class="sxs-lookup"><span data-stu-id="a80e8-111">The structure.</span></span> <span data-ttu-id="a80e8-112">La mémoire allouée vers laquelle pointe cette structure sera libérée.</span><span class="sxs-lookup"><span data-stu-id="a80e8-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80e8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a80e8-113">Return value</span></span>

<span data-ttu-id="a80e8-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a80e8-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80e8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a80e8-115">Requirements</span></span>



| <span data-ttu-id="a80e8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a80e8-116">Requirement</span></span> | <span data-ttu-id="a80e8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a80e8-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80e8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a80e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a80e8-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a80e8-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a80e8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a80e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a80e8-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a80e8-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a80e8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a80e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80e8-123"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80e8-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80e8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a80e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80e8-125">_ *UiInfo*\*</span><span class="sxs-lookup"><span data-stu-id="a80e8-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="a80e8-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="a80e8-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


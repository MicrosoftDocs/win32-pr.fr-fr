---
title: FreeHelperAttributes, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures d' \_ attributs d’assistance.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes fonction NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464822"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="ac939-104">FreeHelperAttributes fonction)</span><span class="sxs-lookup"><span data-stu-id="ac939-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="ac939-105">La fonction **FreeHelperAttributes** libère la mémoire allouée en interne à un tableau de structures d' [**\_ attributs d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="ac939-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="ac939-106">Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ac939-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac939-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac939-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="ac939-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac939-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac939-109">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac939-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac939-110">Type : \**\* [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="ac939-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="ac939-111">Tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="ac939-111">The array of structures.</span></span> <span data-ttu-id="ac939-112">La mémoire allouée pointée par ces structures sera libérée.</span><span class="sxs-lookup"><span data-stu-id="ac939-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="ac939-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="ac939-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="ac939-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ac939-114">Type: **ULONG**</span></span>

<span data-ttu-id="ac939-115">Nombre de structures dans le tableau pointé par *pinfo*.</span><span class="sxs-lookup"><span data-stu-id="ac939-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="ac939-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="ac939-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="ac939-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="ac939-117">Type: **BOOL**</span></span>

<span data-ttu-id="ac939-118">True si le tableau de structures doit également être supprimé ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="ac939-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac939-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac939-119">Return value</span></span>

<span data-ttu-id="ac939-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ac939-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac939-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac939-121">Requirements</span></span>



| <span data-ttu-id="ac939-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac939-122">Requirement</span></span> | <span data-ttu-id="ac939-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac939-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac939-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac939-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ac939-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac939-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac939-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac939-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ac939-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac939-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ac939-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac939-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac939-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac939-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac939-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac939-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac939-131">**attribut d’assistance \_**</span><span class="sxs-lookup"><span data-stu-id="ac939-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="ac939-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="ac939-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


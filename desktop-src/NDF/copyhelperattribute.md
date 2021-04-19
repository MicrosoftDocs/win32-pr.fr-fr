---
title: CopyHelperAttribute, fonction (Ndattributils. h)
description: Crée une copie d’une structure d' \_ attribut d’assistance.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute fonction NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509095"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="2d4cd-104">CopyHelperAttribute fonction)</span><span class="sxs-lookup"><span data-stu-id="2d4cd-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="2d4cd-105">La fonction **CopyHelperAttribute** crée une copie d’une structure d' [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="2d4cd-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d4cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d4cd-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="2d4cd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d4cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d4cd-108">*Dest* \[ . à\]</span><span class="sxs-lookup"><span data-stu-id="2d4cd-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d4cd-109">Type : \**\* [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="2d4cd-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="2d4cd-110">Structure à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="2d4cd-111">_Source \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d4cd-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d4cd-112">Type : \**\* [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)const* _</span><span class="sxs-lookup"><span data-stu-id="2d4cd-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="2d4cd-113">Structure existante à copier.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d4cd-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d4cd-114">Return value</span></span>

<span data-ttu-id="2d4cd-115">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2d4cd-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2d4cd-116">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2d4cd-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2d4cd-117">Return code</span></span>                                                                                   | <span data-ttu-id="2d4cd-118">Description</span><span class="sxs-lookup"><span data-stu-id="2d4cd-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d4cd-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d4cd-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2d4cd-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="2d4cd-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2d4cd-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2d4cd-122">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="2d4cd-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2d4cd-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2d4cd-124">La mémoire disponible est insuffisante pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="2d4cd-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d4cd-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d4cd-125">Requirements</span></span>



| <span data-ttu-id="2d4cd-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d4cd-126">Requirement</span></span> | <span data-ttu-id="2d4cd-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d4cd-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4cd-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d4cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2d4cd-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d4cd-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d4cd-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d4cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2d4cd-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d4cd-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2d4cd-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d4cd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d4cd-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d4cd-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d4cd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d4cd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4cd-135">**attribut d’assistance \_**</span><span class="sxs-lookup"><span data-stu-id="2d4cd-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 






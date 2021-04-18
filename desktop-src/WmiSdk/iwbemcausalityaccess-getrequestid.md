---
description: La méthode GetRequestId retourne une valeur d’identificateur global unique (GUID) pour une demande. Un GUID est un nombre 128 bits unique.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess :: GetRequestId, méthode (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536178"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="ce71b-104">IWbemCausalityAccess :: GetRequestId, méthode</span><span class="sxs-lookup"><span data-stu-id="ce71b-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="ce71b-105">La méthode **GetRequestId** retourne une valeur d’identificateur global unique (Guid) pour une demande.</span><span class="sxs-lookup"><span data-stu-id="ce71b-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="ce71b-106">Un GUID est un nombre 128 bits unique.</span><span class="sxs-lookup"><span data-stu-id="ce71b-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce71b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce71b-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="ce71b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce71b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce71b-109">*PID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ce71b-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce71b-110">Valeur GUID qui identifie de façon unique une demande.</span><span class="sxs-lookup"><span data-stu-id="ce71b-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="ce71b-111">Par exemple, 5b2fc63a-8AF4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="ce71b-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce71b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce71b-112">Return value</span></span>

<span data-ttu-id="ce71b-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ce71b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce71b-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce71b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce71b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce71b-115">Requirements</span></span>



| <span data-ttu-id="ce71b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce71b-116">Requirement</span></span> | <span data-ttu-id="ce71b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce71b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce71b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce71b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce71b-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce71b-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce71b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce71b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce71b-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce71b-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce71b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce71b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce71b-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce71b-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="ce71b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ce71b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce71b-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce71b-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce71b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce71b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce71b-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="ce71b-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 





---
description: 'IEnumUserIdentity :: Next n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'IEnumUserIdentity :: Next, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991528"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="12c01-104">IEnumUserIdentity :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="12c01-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="12c01-105">\[**IEnumUserIdentity :: Next** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="12c01-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="12c01-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="12c01-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="12c01-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="12c01-107">Deprecated.</span></span> <span data-ttu-id="12c01-108">Récupère un tableau d’interfaces d’identité d’utilisateur à partir de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="12c01-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c01-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12c01-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="12c01-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c01-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12c01-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c01-112">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="12c01-112">Type: **ULONG**</span></span>

<span data-ttu-id="12c01-113">Valeur **ULong** qui représente le nombre d’interfaces à récupérer.</span><span class="sxs-lookup"><span data-stu-id="12c01-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="12c01-114">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12c01-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12c01-115">Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="12c01-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="12c01-116">Adresse d’un pointeur qui reçoit les interfaces.</span><span class="sxs-lookup"><span data-stu-id="12c01-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="12c01-117">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12c01-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12c01-118">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="12c01-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="12c01-119">Adresse d’un pointeur qui reçoit le nombre d’interfaces récupérées avec succès.</span><span class="sxs-lookup"><span data-stu-id="12c01-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c01-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12c01-120">Return value</span></span>

<span data-ttu-id="12c01-121">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="12c01-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="12c01-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="12c01-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12c01-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12c01-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c01-124">Notes</span><span class="sxs-lookup"><span data-stu-id="12c01-124">Remarks</span></span>

<span data-ttu-id="12c01-125">[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée.</span><span class="sxs-lookup"><span data-stu-id="12c01-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="12c01-126">Plusieurs appels à cette méthode ne réinitialisent pas ce nombre.</span><span class="sxs-lookup"><span data-stu-id="12c01-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="12c01-127">Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="12c01-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="12c01-128">Pour incrémenter le nombre sans récupérer les interfaces, appelez [**IEnumUserIdentity :: Skip**](ienumuseridentity-skip.md).</span><span class="sxs-lookup"><span data-stu-id="12c01-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="12c01-129">La valeur de *celt* ne doit pas dépasser la valeur retournée par [**IEnumUserIdentity :: GetCount**](ienumuseridentity-getcount.md).</span><span class="sxs-lookup"><span data-stu-id="12c01-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c01-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="12c01-130">Requirements</span></span>



| <span data-ttu-id="12c01-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12c01-131">Requirement</span></span> | <span data-ttu-id="12c01-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="12c01-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c01-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="12c01-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c01-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="12c01-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="12c01-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c01-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12c01-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="12c01-137">End of client support</span></span><br/>    | <span data-ttu-id="12c01-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="12c01-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="12c01-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="12c01-139">End of server support</span></span><br/>    | <span data-ttu-id="12c01-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12c01-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="12c01-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="12c01-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c01-142"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="12c01-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="12c01-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="12c01-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12c01-144"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12c01-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="12c01-145">DLL</span><span class="sxs-lookup"><span data-stu-id="12c01-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12c01-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c01-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c01-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12c01-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c01-148">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="12c01-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="12c01-149">**IEnumUserIdentity :: Skip**</span><span class="sxs-lookup"><span data-stu-id="12c01-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="12c01-150">**IEnumUserIdentity :: Reset**</span><span class="sxs-lookup"><span data-stu-id="12c01-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="12c01-151">**IEnumUserIdentity :: GetCount**</span><span class="sxs-lookup"><span data-stu-id="12c01-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 

---
description: 'IEnumUserIdentity :: Skip n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'IEnumUserIdentity :: Skip, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991524"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="7e48b-104">IEnumUserIdentity :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="7e48b-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="7e48b-105">\[**IEnumUserIdentity :: Skip** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="7e48b-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7e48b-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7e48b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7e48b-107">Ignore un nombre donné d’interfaces d’identité utilisateur dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7e48b-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="7e48b-108">Utilisé lors de la récupération des interfaces.</span><span class="sxs-lookup"><span data-stu-id="7e48b-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e48b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e48b-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="7e48b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e48b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e48b-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e48b-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e48b-112">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="7e48b-112">Type: **ULONG**</span></span>

<span data-ttu-id="7e48b-113">Nombre d'interfaces à ignorer.</span><span class="sxs-lookup"><span data-stu-id="7e48b-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e48b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e48b-114">Return value</span></span>

<span data-ttu-id="7e48b-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7e48b-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7e48b-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7e48b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e48b-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e48b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e48b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7e48b-118">Remarks</span></span>

<span data-ttu-id="7e48b-119">[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée.</span><span class="sxs-lookup"><span data-stu-id="7e48b-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="7e48b-120">Pour incrémenter ce nombre sans récupérer les interfaces, appelez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7e48b-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="7e48b-121">Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="7e48b-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e48b-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7e48b-122">Requirements</span></span>



| <span data-ttu-id="7e48b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e48b-123">Requirement</span></span> | <span data-ttu-id="7e48b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e48b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e48b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e48b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e48b-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e48b-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7e48b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e48b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e48b-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e48b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e48b-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7e48b-129">End of client support</span></span><br/>    | <span data-ttu-id="7e48b-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e48b-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7e48b-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7e48b-131">End of server support</span></span><br/>    | <span data-ttu-id="7e48b-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e48b-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7e48b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e48b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e48b-134"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e48b-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e48b-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="7e48b-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e48b-136"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e48b-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7e48b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7e48b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e48b-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e48b-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e48b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e48b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e48b-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="7e48b-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="7e48b-141">**IEnumUserIdentity :: Reset**</span><span class="sxs-lookup"><span data-stu-id="7e48b-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="7e48b-142">**IEnumUserIdentity :: suivant**</span><span class="sxs-lookup"><span data-stu-id="7e48b-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="7e48b-143">**IEnumUserIdentity :: GetCount**</span><span class="sxs-lookup"><span data-stu-id="7e48b-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 





---
description: Réinitialise le nombre interne d’interfaces récupérées dans l’énumération.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'IEnumUserIdentity :: Reset, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202772"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="0c7e3-103">IEnumUserIdentity :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="0c7e3-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="0c7e3-104">\[**IEnumUserIdentity :: Reset** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0c7e3-105">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="0c7e3-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="0c7e3-106">Réinitialise le nombre interne d’interfaces récupérées dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7e3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c7e3-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="0c7e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c7e3-108">Parameters</span></span>

<span data-ttu-id="0c7e3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c7e3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c7e3-110">Return value</span></span>

<span data-ttu-id="0c7e3-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c7e3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0c7e3-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c7e3-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c7e3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c7e3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0c7e3-114">Remarks</span></span>

<span data-ttu-id="0c7e3-115">[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="0c7e3-116">L’appel de cette méthode permet de réinitialiser la valeur de ce nombre.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7e3-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c7e3-117">Requirements</span></span>



| <span data-ttu-id="0c7e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c7e3-118">Requirement</span></span> | <span data-ttu-id="0c7e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c7e3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7e3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7e3-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c7e3-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0c7e3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7e3-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c7e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c7e3-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0c7e3-124">End of client support</span></span><br/>    | <span data-ttu-id="0c7e3-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c7e3-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="0c7e3-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0c7e3-126">End of server support</span></span><br/>    | <span data-ttu-id="0c7e3-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c7e3-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0c7e3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c7e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c7e3-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e3-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c7e3-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="0c7e3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c7e3-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e3-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0c7e3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0c7e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c7e3-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e3-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7e3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7e3-135">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="0c7e3-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="0c7e3-136">**IEnumUserIdentity :: Skip**</span><span class="sxs-lookup"><span data-stu-id="0c7e3-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="0c7e3-137">**IEnumUserIdentity :: GetCount**</span><span class="sxs-lookup"><span data-stu-id="0c7e3-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="0c7e3-138">**IEnumUserIdentity :: suivant**</span><span class="sxs-lookup"><span data-stu-id="0c7e3-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 





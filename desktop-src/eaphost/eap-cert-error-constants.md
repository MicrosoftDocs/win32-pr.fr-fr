---
title: '\_Constantes d’erreur de certificat EAP (Eaphosterror. h)'
description: Définir des erreurs liées aux certificats communes à toutes les technologies d’API EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508401"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="fd3fa-103">\_Constantes d’erreur de certificat EAP</span><span class="sxs-lookup"><span data-stu-id="fd3fa-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="fd3fa-104">Ces constantes définissent les erreurs liées aux certificats communes à toutes les technologies d’API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="fd3fa-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_certificat EAP en \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-106">0x0</span><span class="sxs-lookup"><span data-stu-id="fd3fa-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-107">Définit la limite des rapports d’erreurs ; toutes les erreurs de certificat se produisent entre le certificat **\_ EAP en \_ \_ premier** et le **\_ \_ \_ dernier certificat EAP**.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_dernier certificat \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-109">0xF</span><span class="sxs-lookup"><span data-stu-id="fd3fa-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-110">Définit la limite des rapports d’erreurs ; toutes les erreurs de certificat se produisent entre le certificat **\_ EAP en \_ \_ premier** et le **\_ \_ \_ dernier certificat EAP**.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificat EAP \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-112">0x1</span><span class="sxs-lookup"><span data-stu-id="fd3fa-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-113">Aucun certificat utilisateur n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificat EAP \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-115">0x2</span><span class="sxs-lookup"><span data-stu-id="fd3fa-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-116">Le certificat utilisateur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificat EAP \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-118">0x3</span><span class="sxs-lookup"><span data-stu-id="fd3fa-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-119">Le certificat de l’utilisateur a expiré.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificat EAP \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-121">0x4</span><span class="sxs-lookup"><span data-stu-id="fd3fa-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-122">Le certificat utilisateur a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ autre erreur de certificat EAP \_**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-124">0x5</span><span class="sxs-lookup"><span data-stu-id="fd3fa-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-125">Une erreur liée au certificat est inconnue.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificat EAP \_ rejeté**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-127">0x6</span><span class="sxs-lookup"><span data-stu-id="fd3fa-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-128">Le certificat utilisateur a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_nom de certificat EAP \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-130">0x7</span><span class="sxs-lookup"><span data-stu-id="fd3fa-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-131">Le certificat utilisateur requiert un nom.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP- \_ général en \_ premier**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-133">0x10</span><span class="sxs-lookup"><span data-stu-id="fd3fa-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-134">Définit la limite des rapports d’erreurs ; toute erreur générale EAP se produira entre **\_ EAP \_ général en \_ premier** et **\_ EAP \_ général en \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd3fa-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_dernière général \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="fd3fa-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3fa-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="fd3fa-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="fd3fa-137">Définit la limite des rapports d’erreurs ; toute erreur générale EAP se produira entre **\_ EAP \_ général en \_ premier** et **\_ EAP \_ général en \_ dernier**.</span><span class="sxs-lookup"><span data-stu-id="fd3fa-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd3fa-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd3fa-138">Requirements</span></span>



| <span data-ttu-id="fd3fa-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd3fa-139">Requirement</span></span> | <span data-ttu-id="fd3fa-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd3fa-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3fa-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd3fa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3fa-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd3fa-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fd3fa-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd3fa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3fa-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd3fa-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fd3fa-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd3fa-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3fa-146"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd3fa-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3fa-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd3fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3fa-148">Constantes EAPHost communes</span><span class="sxs-lookup"><span data-stu-id="fd3fa-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 






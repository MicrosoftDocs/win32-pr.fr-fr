---
description: Répertorie les types d’entrées du contrôle d’accès actuellement définis.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525015"
---
# <a name="ace"></a><span data-ttu-id="7e52c-103">MAILLOTS</span><span class="sxs-lookup"><span data-stu-id="7e52c-103">ACE</span></span>

<span data-ttu-id="7e52c-104">Une **ACE** est une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) dans une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="7e52c-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="7e52c-105">Le tableau suivant répertorie les types d' **entrées** du contrôle d’accès actuellement définis.</span><span class="sxs-lookup"><span data-stu-id="7e52c-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e52c-106">Type d’entrée de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-106">ACE type</span></span></th>
<th><span data-ttu-id="7e52c-107">Structure</span><span class="sxs-lookup"><span data-stu-id="7e52c-107">Structure</span></span></th>
<th><span data-ttu-id="7e52c-108">Type ACL</span><span class="sxs-lookup"><span data-stu-id="7e52c-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-109">Accès autorisé</span><span class="sxs-lookup"><span data-stu-id="7e52c-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-111">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-112">Accès autorisé</span><span class="sxs-lookup"><span data-stu-id="7e52c-112">Access allowed</span></span></li>
<li><span data-ttu-id="7e52c-113">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-115">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-116">Accès autorisé</span><span class="sxs-lookup"><span data-stu-id="7e52c-116">Access allowed</span></span></li>
<li><span data-ttu-id="7e52c-117">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-119">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-120">Accès autorisé</span><span class="sxs-lookup"><span data-stu-id="7e52c-120">Access allowed</span></span></li>
<li><span data-ttu-id="7e52c-121">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-121">Object specific</span></span></li>
<li><span data-ttu-id="7e52c-122">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-124">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-125">Accès refusé</span><span class="sxs-lookup"><span data-stu-id="7e52c-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-127">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-128">Accès refusé</span><span class="sxs-lookup"><span data-stu-id="7e52c-128">Access denied</span></span></li>
<li><span data-ttu-id="7e52c-129">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-131">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-132">Accès refusé</span><span class="sxs-lookup"><span data-stu-id="7e52c-132">Access denied</span></span></li>
<li><span data-ttu-id="7e52c-133">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-133">Object specific</span></span></li>
<li><span data-ttu-id="7e52c-134">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-136">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-137">Accès refusé</span><span class="sxs-lookup"><span data-stu-id="7e52c-137">Access denied</span></span></li>
<li><span data-ttu-id="7e52c-138">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-140">Discrétionnaire</span><span class="sxs-lookup"><span data-stu-id="7e52c-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-141">Alarme système</span><span class="sxs-lookup"><span data-stu-id="7e52c-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-143">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-144">Alarme système</span><span class="sxs-lookup"><span data-stu-id="7e52c-144">System alarm</span></span></li>
<li><span data-ttu-id="7e52c-145">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-147">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-148">Alarme système</span><span class="sxs-lookup"><span data-stu-id="7e52c-148">System alarm</span></span></li>
<li><span data-ttu-id="7e52c-149">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-149">Object specific</span></span></li>
<li><span data-ttu-id="7e52c-150">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-152">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-153">Alarme système</span><span class="sxs-lookup"><span data-stu-id="7e52c-153">System alarm</span></span></li>
<li><span data-ttu-id="7e52c-154">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-156">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-157">Audit du système</span><span class="sxs-lookup"><span data-stu-id="7e52c-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-159">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-160">Audit du système</span><span class="sxs-lookup"><span data-stu-id="7e52c-160">System audit</span></span></li>
<li><span data-ttu-id="7e52c-161">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-163">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e52c-164">Audit du système</span><span class="sxs-lookup"><span data-stu-id="7e52c-164">System audit</span></span></li>
<li><span data-ttu-id="7e52c-165">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-165">Object specific</span></span></li>
<li><span data-ttu-id="7e52c-166">Autorise le rappel lors de la vérification de l’accès</span><span class="sxs-lookup"><span data-stu-id="7e52c-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-168">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7e52c-169">Audit du système</span><span class="sxs-lookup"><span data-stu-id="7e52c-169">System audit</span></span></li>
<li><span data-ttu-id="7e52c-170">Spécifique à l’objet</span><span class="sxs-lookup"><span data-stu-id="7e52c-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="7e52c-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e52c-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="7e52c-172">Système</span><span class="sxs-lookup"><span data-stu-id="7e52c-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e52c-173">Les ACE d’alarme système propre à l’objet et à l’alarme système ne sont pas prises en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="7e52c-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="7e52c-174">Chaque entrée du contrôle d’accès commence par une structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="7e52c-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="7e52c-175">Le format des données suivant l’en-tête varie en fonction du type d’entrée du contrôle d’accès spécifié dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7e52c-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e52c-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e52c-176">Requirements</span></span>



| <span data-ttu-id="7e52c-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e52c-177">Requirement</span></span> | <span data-ttu-id="7e52c-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e52c-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e52c-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e52c-179">Minimum supported client</span></span><br/> | <span data-ttu-id="7e52c-180">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e52c-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7e52c-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e52c-181">Minimum supported server</span></span><br/> | <span data-ttu-id="7e52c-182">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e52c-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7e52c-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e52c-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e52c-184"><dt>Winnt. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e52c-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e52c-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e52c-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e52c-186">**AddAce**</span><span class="sxs-lookup"><span data-stu-id="7e52c-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="7e52c-187">**ACCÈS \_ ACE autorisé pour l’accès \_**</span><span class="sxs-lookup"><span data-stu-id="7e52c-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="7e52c-188">**ACCÈS \_ refusé \_**</span><span class="sxs-lookup"><span data-stu-id="7e52c-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="7e52c-189">**ACL**</span><span class="sxs-lookup"><span data-stu-id="7e52c-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="7e52c-190">**\_ACE d’alarme système \_**</span><span class="sxs-lookup"><span data-stu-id="7e52c-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="7e52c-191">**\_ACE d’audit système \_**</span><span class="sxs-lookup"><span data-stu-id="7e52c-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>


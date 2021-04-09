---
description: Explique les chaînes utilisées dans une entrée de contrôle d’accès.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Chaînes ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756188"
---
# <a name="ace-strings"></a><span data-ttu-id="647dc-103">Chaînes ACE</span><span class="sxs-lookup"><span data-stu-id="647dc-103">ACE Strings</span></span>

<span data-ttu-id="647dc-104">Le [langage SDDL (Security Descriptor Definition Language](security-descriptor-definition-language.md) ) utilise des chaînes ACE dans les composants DACL et SACL d’une chaîne de [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="647dc-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="647dc-105">Comme indiqué dans les exemples de [format de chaîne de descripteur de sécurité](security-descriptor-string-format.md) , chaque entrée du contrôle d’accès dans une chaîne de descripteur de sécurité est placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="647dc-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="647dc-106">Les champs de l’entrée du contrôle d’accès sont dans l’ordre suivant et sont séparés par des points-virgules (;).</span><span class="sxs-lookup"><span data-stu-id="647dc-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="647dc-107">Il existe un format différent pour les [*entrées du contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) par rapport aux autres types ACE.</span><span class="sxs-lookup"><span data-stu-id="647dc-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="647dc-108">Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="647dc-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="647dc-109">Champs</span><span class="sxs-lookup"><span data-stu-id="647dc-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="647dc-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**type d’entrée de contrôle d’accès \_**</span><span class="sxs-lookup"><span data-stu-id="647dc-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-111">Chaîne qui indique la valeur du membre **AceType** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="647dc-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="647dc-112">La chaîne de type ACE peut être l’une des chaînes suivantes définies dans SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="647dc-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="647dc-113">Chaîne de type ACE</span><span class="sxs-lookup"><span data-stu-id="647dc-113">ACE type string</span></span> | <span data-ttu-id="647dc-114">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="647dc-115">Valeur AceType</span><span class="sxs-lookup"><span data-stu-id="647dc-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647dc-116">« A »</span><span class="sxs-lookup"><span data-stu-id="647dc-116">"A"</span></span>             | <span data-ttu-id="647dc-117">\_accès SDDL \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="647dc-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="647dc-118">TYPE d’entrée du contrôle d’accès \_ autorisé \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="647dc-119">« D »</span><span class="sxs-lookup"><span data-stu-id="647dc-119">"D"</span></span>             | <span data-ttu-id="647dc-120">\_accès SDDL \_ refusé</span><span class="sxs-lookup"><span data-stu-id="647dc-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="647dc-121">TYPE d’entrée du contrôle d’accès \_ refusé \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="647dc-122">FONCTIONNEMENT</span><span class="sxs-lookup"><span data-stu-id="647dc-122">"OA"</span></span>            | <span data-ttu-id="647dc-123">\_ \_ accès à l’objet SDDL \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="647dc-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="647dc-124">\_type d' \_ ACE d’objet autorisé \_ d’accès \_</span><span class="sxs-lookup"><span data-stu-id="647dc-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="647dc-125">DIAMÈTRE</span><span class="sxs-lookup"><span data-stu-id="647dc-125">"OD"</span></span>            | <span data-ttu-id="647dc-126">\_ \_ accès à l’objet SDDL \_ refusé</span><span class="sxs-lookup"><span data-stu-id="647dc-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="647dc-127">\_type d' \_ ACE d’objet accès refusé \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="647dc-128">UA</span><span class="sxs-lookup"><span data-stu-id="647dc-128">"AU"</span></span>            | <span data-ttu-id="647dc-129">\_audit SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="647dc-130">\_type d' \_ entrée du contrôle d’accès système \_</span><span class="sxs-lookup"><span data-stu-id="647dc-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="647dc-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="647dc-131">"AL"</span></span>            | <span data-ttu-id="647dc-132">\_alarme SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="647dc-133">\_type d' \_ ACE d’alarme système \_</span><span class="sxs-lookup"><span data-stu-id="647dc-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="647dc-134">Organisation</span><span class="sxs-lookup"><span data-stu-id="647dc-134">"OU"</span></span>            | <span data-ttu-id="647dc-135">\_audit des objets SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="647dc-136">\_type d' \_ ACE d’objet d’audit système \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="647dc-137">OL</span><span class="sxs-lookup"><span data-stu-id="647dc-137">"OL"</span></span>            | <span data-ttu-id="647dc-138">\_alarme d’objet SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="647dc-139">\_type d' \_ ACE d’objet d’alarme système \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="647dc-140">ENVIRON</span><span class="sxs-lookup"><span data-stu-id="647dc-140">"ML"</span></span>            | <span data-ttu-id="647dc-141">étiquette de SDDL \_ obligatoire \_</span><span class="sxs-lookup"><span data-stu-id="647dc-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="647dc-142">\_type d' \_ ACE d’étiquette obligatoire \_ du système \_</span><span class="sxs-lookup"><span data-stu-id="647dc-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="647dc-143">XA</span><span class="sxs-lookup"><span data-stu-id="647dc-143">"XA"</span></span>            | <span data-ttu-id="647dc-144">\_ \_ accès au rappel SDDL \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="647dc-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="647dc-145">TYPE d’entrée du contrôle d’accès autorisé pour le \_ \_ rappel \_ \_ **windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="647dc-146">VERROUILLAGE</span><span class="sxs-lookup"><span data-stu-id="647dc-146">"XD"</span></span>            | <span data-ttu-id="647dc-147">\_ \_ accès au rappel SDDL \_ refusé</span><span class="sxs-lookup"><span data-stu-id="647dc-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="647dc-148">\_Type d' \_ ACE de rappel de refus d’accès \_ \_ **windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="647dc-149">INSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="647dc-149">"RA"</span></span>            | <span data-ttu-id="647dc-150">\_attribut de ressource SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="647dc-151">\_Type d’ACE d’attribut de ressource système \_ \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="647dc-152">SR</span><span class="sxs-lookup"><span data-stu-id="647dc-152">"SP"</span></span>            | <span data-ttu-id="647dc-153">ID de stratégie de l' \_ étendue SDDL \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="647dc-154">\_ \_ Type d’ACE de l’ID de stratégie système \_ \_ \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="647dc-155">"XU"</span><span class="sxs-lookup"><span data-stu-id="647dc-155">"XU"</span></span>            | <span data-ttu-id="647dc-156">\_audit de rappel SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="647dc-157">\_Type d’entrée de contrôle d’accès de rappel du système \_ \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="647dc-158">ARMÉNIENNE</span><span class="sxs-lookup"><span data-stu-id="647dc-158">"ZA"</span></span>            | <span data-ttu-id="647dc-159">\_ \_ accès à l’objet de rappel SDDL \_ \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="647dc-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="647dc-160">TYPE d’entrée du contrôle d’accès autorisé pour le \_ \_ rappel \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows Vista et Windows Server 2003 :** non disponible.</span><span class="sxs-lookup"><span data-stu-id="647dc-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="647dc-161">Si le type d' **entrée \_** du contrôle d’accès est \_ \_ \_ \_ un type d’ACE d’objet autorisé d’accès [](/windows/win32/api/guiddef/ns-guiddef-guid) et que le GUID d’objet n’est pas spécifié pour le GUID de l’objet, [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) convertit le **\_ type d’entrée** du contrôle d’accès en type ACE **\_ \_** **\_** \_ autorisé \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="647dc-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="647dc-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_indicateurs ACE**</span><span class="sxs-lookup"><span data-stu-id="647dc-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-163">Chaîne qui indique la valeur du membre **AceFlags** de la structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="647dc-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="647dc-164">La chaîne d’indicateurs ACE peut être une concaténation des chaînes suivantes définies dans SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="647dc-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="647dc-165">Chaîne des indicateurs ACE</span><span class="sxs-lookup"><span data-stu-id="647dc-165">ACE flags string</span></span> | <span data-ttu-id="647dc-166">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="647dc-167">Valeur AceFlag</span><span class="sxs-lookup"><span data-stu-id="647dc-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="647dc-168">CI</span><span class="sxs-lookup"><span data-stu-id="647dc-168">"CI"</span></span>             | <span data-ttu-id="647dc-169">\_hériter du conteneur SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="647dc-170">\_ACE d’héritage de conteneur \_</span><span class="sxs-lookup"><span data-stu-id="647dc-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="647dc-171">OI</span><span class="sxs-lookup"><span data-stu-id="647dc-171">"OI"</span></span>             | <span data-ttu-id="647dc-172">l' \_ objet SDDL \_ hérite</span><span class="sxs-lookup"><span data-stu-id="647dc-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="647dc-173">l’objet \_ hérite de l' \_ ACE</span><span class="sxs-lookup"><span data-stu-id="647dc-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="647dc-174">ENTRANT</span><span class="sxs-lookup"><span data-stu-id="647dc-174">"NP"</span></span>             | <span data-ttu-id="647dc-175">SDDL \_ non \_ propagé</span><span class="sxs-lookup"><span data-stu-id="647dc-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="647dc-176">AUCUNE \_ propagation d' \_ entrée de contrôle d’accès \_</span><span class="sxs-lookup"><span data-stu-id="647dc-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="647dc-177">ENTRÉES</span><span class="sxs-lookup"><span data-stu-id="647dc-177">"IO"</span></span>             | <span data-ttu-id="647dc-178">SDDL \_ hérite \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="647dc-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="647dc-179">HÉRITer \_ uniquement \_ ACE</span><span class="sxs-lookup"><span data-stu-id="647dc-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="647dc-180">« ID »</span><span class="sxs-lookup"><span data-stu-id="647dc-180">"ID"</span></span>             | <span data-ttu-id="647dc-181">SDDL \_ hérité</span><span class="sxs-lookup"><span data-stu-id="647dc-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="647dc-182">\_ACE hérité</span><span class="sxs-lookup"><span data-stu-id="647dc-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="647dc-183">SA</span><span class="sxs-lookup"><span data-stu-id="647dc-183">"SA"</span></span>             | <span data-ttu-id="647dc-184">\_réussite de l’audit SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="647dc-185">\_ \_ indicateur ACE d’accès réussi \_</span><span class="sxs-lookup"><span data-stu-id="647dc-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="647dc-186">Param</span><span class="sxs-lookup"><span data-stu-id="647dc-186">"FA"</span></span>             | <span data-ttu-id="647dc-187">\_échec de l’audit SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="647dc-188">\_ \_ indicateur ACE d’accès en échec \_</span><span class="sxs-lookup"><span data-stu-id="647dc-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="647dc-189"><span id="rights"></span><span id="RIGHTS"></span>**autorisations**</span><span class="sxs-lookup"><span data-stu-id="647dc-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-190">Chaîne qui indique les [droits d’accès](access-rights-and-access-masks.md) contrôlés par l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="647dc-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="647dc-191">Cette chaîne peut être une représentation sous forme de chaîne hexadécimale des droits d’accès, par exemple « 0x7800003F », ou il peut s’agir d’une concaténation des chaînes suivantes.</span><span class="sxs-lookup"><span data-stu-id="647dc-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="647dc-192">Droits d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="647dc-192">Generic access rights</span></span>

| <span data-ttu-id="647dc-193">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-193">Access rights string</span></span> | <span data-ttu-id="647dc-194">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-194">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-195">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-196">DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="647dc-196">"GA"</span></span>                 | <span data-ttu-id="647dc-197">SDDL \_ générique \_ tout</span><span class="sxs-lookup"><span data-stu-id="647dc-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="647dc-198">GÉNÉRIQUE \_ tout</span><span class="sxs-lookup"><span data-stu-id="647dc-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="647dc-199">EM</span><span class="sxs-lookup"><span data-stu-id="647dc-199">"GR"</span></span>                 | <span data-ttu-id="647dc-200">\_lecture générique \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="647dc-201">\_lecture générique</span><span class="sxs-lookup"><span data-stu-id="647dc-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="647dc-202">ENTREPÔT</span><span class="sxs-lookup"><span data-stu-id="647dc-202">"GW"</span></span>                 | <span data-ttu-id="647dc-203">\_écriture générique \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="647dc-204">\_écriture générique</span><span class="sxs-lookup"><span data-stu-id="647dc-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="647dc-205">GX</span><span class="sxs-lookup"><span data-stu-id="647dc-205">"GX"</span></span>                 | <span data-ttu-id="647dc-206">\_Exécution générique \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="647dc-207">\_Exécution générique</span><span class="sxs-lookup"><span data-stu-id="647dc-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="647dc-208">Droits d’accès standard</span><span class="sxs-lookup"><span data-stu-id="647dc-208">Standard access rights</span></span>

| <span data-ttu-id="647dc-209">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-209">Access rights string</span></span> | <span data-ttu-id="647dc-210">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-210">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-211">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-212">Release</span><span class="sxs-lookup"><span data-stu-id="647dc-212">"RC"</span></span>                 | <span data-ttu-id="647dc-213">\_contrôle de lecture SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="647dc-214">LIRE \_ le contrôle</span><span class="sxs-lookup"><span data-stu-id="647dc-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="647dc-215">DP</span><span class="sxs-lookup"><span data-stu-id="647dc-215">"SD"</span></span>                 | <span data-ttu-id="647dc-216">\_suppression standard \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="647dc-217">Suppression</span><span class="sxs-lookup"><span data-stu-id="647dc-217">DELETE</span></span>          |
| <span data-ttu-id="647dc-218">WD</span><span class="sxs-lookup"><span data-stu-id="647dc-218">"WD"</span></span>                 | <span data-ttu-id="647dc-219">\_écriture DAC d’écriture SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="647dc-220">ÉCRITURE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="647dc-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="647dc-221">WO</span><span class="sxs-lookup"><span data-stu-id="647dc-221">"WO"</span></span>                 | <span data-ttu-id="647dc-222">\_propriétaire d’écriture SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="647dc-223">propriétaire en écriture \_</span><span class="sxs-lookup"><span data-stu-id="647dc-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="647dc-224">Droits d’accès à l’objet service d’annuaire</span><span class="sxs-lookup"><span data-stu-id="647dc-224">Directory service object access rights</span></span>

| <span data-ttu-id="647dc-225">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-225">Access rights string</span></span> | <span data-ttu-id="647dc-226">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-226">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-227">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-228">PR</span><span class="sxs-lookup"><span data-stu-id="647dc-228">"RP"</span></span>                 | <span data-ttu-id="647dc-229">\_propriété de lecture SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="647dc-230">\_lecture de \_ la \_ \_ prop DS droite des publicités</span><span class="sxs-lookup"><span data-stu-id="647dc-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="647dc-231">EP</span><span class="sxs-lookup"><span data-stu-id="647dc-231">"WP"</span></span>                 | <span data-ttu-id="647dc-232">\_propriété d’écriture SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="647dc-233">\_Prop. \_ d' \_ écriture DS droit \_ ads</span><span class="sxs-lookup"><span data-stu-id="647dc-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="647dc-234">CC</span><span class="sxs-lookup"><span data-stu-id="647dc-234">"CC"</span></span>                 | <span data-ttu-id="647dc-235">SDDL- \_ créer un \_ enfant</span><span class="sxs-lookup"><span data-stu-id="647dc-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="647dc-236">création d’un enfant ad \_ Right \_ DS \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="647dc-237">MÉTAFICHIER</span><span class="sxs-lookup"><span data-stu-id="647dc-237">"DC"</span></span>                 | <span data-ttu-id="647dc-238">\_enfant de suppression SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="647dc-239">\_enfant ad droit \_ supprimer un \_ \_ enfant</span><span class="sxs-lookup"><span data-stu-id="647dc-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="647dc-240">EUROS</span><span class="sxs-lookup"><span data-stu-id="647dc-240">"LC"</span></span>                 | <span data-ttu-id="647dc-241">enfants de la \_ liste SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="647dc-242">\_liste des \_ ACTRL \_ DS \_ pour les publicités</span><span class="sxs-lookup"><span data-stu-id="647dc-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="647dc-243">EPP</span><span class="sxs-lookup"><span data-stu-id="647dc-243">"SW"</span></span>                 | <span data-ttu-id="647dc-244">écriture SDDL en \_ \_ écriture</span><span class="sxs-lookup"><span data-stu-id="647dc-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="647dc-245">active \_ Directory avec droit ad \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="647dc-246">Lo</span><span class="sxs-lookup"><span data-stu-id="647dc-246">"LO"</span></span>                  | <span data-ttu-id="647dc-247">\_objet de liste SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="647dc-248">\_objet de \_ \_ liste DS Right ad \_</span><span class="sxs-lookup"><span data-stu-id="647dc-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="647dc-249">DIV</span><span class="sxs-lookup"><span data-stu-id="647dc-249">"DT"</span></span>                 | <span data-ttu-id="647dc-250">\_arborescence de suppression SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="647dc-251">\_arborescence de \_ suppression du service d’annuaire AD Right \_ \_</span><span class="sxs-lookup"><span data-stu-id="647dc-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="647dc-252">CR</span><span class="sxs-lookup"><span data-stu-id="647dc-252">"CR"</span></span>                  | <span data-ttu-id="647dc-253">\_ \_ accès au contrôle SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="647dc-254">\_ \_ \_ accès au contrôle du service d’annuaire AD Right \_</span><span class="sxs-lookup"><span data-stu-id="647dc-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="647dc-255">Droits d’accès au fichier</span><span class="sxs-lookup"><span data-stu-id="647dc-255">File access rights</span></span>

| <span data-ttu-id="647dc-256">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-256">Access rights string</span></span> | <span data-ttu-id="647dc-257">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-257">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-258">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-259">Param</span><span class="sxs-lookup"><span data-stu-id="647dc-259">"FA"</span></span>                 | <span data-ttu-id="647dc-260">\_fichier SDDL \_ tout</span><span class="sxs-lookup"><span data-stu-id="647dc-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="647dc-261">FICHIER \_ tout \_ accès</span><span class="sxs-lookup"><span data-stu-id="647dc-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="647dc-262">FR</span><span class="sxs-lookup"><span data-stu-id="647dc-262">"FR"</span></span>                 | <span data-ttu-id="647dc-263">\_lecture du fichier SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="647dc-264">\_lecture générique du fichier \_</span><span class="sxs-lookup"><span data-stu-id="647dc-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="647dc-265">PARE</span><span class="sxs-lookup"><span data-stu-id="647dc-265">"FW"</span></span>                 | <span data-ttu-id="647dc-266">\_écriture de fichier SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="647dc-267">\_écriture générique du fichier \_</span><span class="sxs-lookup"><span data-stu-id="647dc-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="647dc-268">ROTATION</span><span class="sxs-lookup"><span data-stu-id="647dc-268">"FX"</span></span>                 | <span data-ttu-id="647dc-269">\_exécution du fichier SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="647dc-270">FICHIER \_ générique \_ exécuter</span><span class="sxs-lookup"><span data-stu-id="647dc-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="647dc-271">Droits d’accès à la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="647dc-271">Registry key access rights</span></span>

| <span data-ttu-id="647dc-272">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-272">Access rights string</span></span> | <span data-ttu-id="647dc-273">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-273">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-274">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-275">Ka</span><span class="sxs-lookup"><span data-stu-id="647dc-275">"KA"</span></span>                 | <span data-ttu-id="647dc-276">\_clé SDDL \_ tout</span><span class="sxs-lookup"><span data-stu-id="647dc-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="647dc-277">\_tout \_ accéder à la clé</span><span class="sxs-lookup"><span data-stu-id="647dc-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="647dc-278">Corée</span><span class="sxs-lookup"><span data-stu-id="647dc-278">"KR"</span></span>                 | <span data-ttu-id="647dc-279">lecture de la \_ clé SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="647dc-280">lecture de la clé \_</span><span class="sxs-lookup"><span data-stu-id="647dc-280">KEY\_READ</span></span>          |
| <span data-ttu-id="647dc-281">KWh</span><span class="sxs-lookup"><span data-stu-id="647dc-281">"KW"</span></span>                 | <span data-ttu-id="647dc-282">écriture de la \_ clé SDDL \_</span><span class="sxs-lookup"><span data-stu-id="647dc-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="647dc-283">écriture de clé \_</span><span class="sxs-lookup"><span data-stu-id="647dc-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="647dc-284">"KX"</span><span class="sxs-lookup"><span data-stu-id="647dc-284">"KX"</span></span>                 | <span data-ttu-id="647dc-285">\_clé SDDL \_ exécutée</span><span class="sxs-lookup"><span data-stu-id="647dc-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="647dc-286">exécution de la clé \_</span><span class="sxs-lookup"><span data-stu-id="647dc-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="647dc-287">Droits d’étiquette obligatoires</span><span class="sxs-lookup"><span data-stu-id="647dc-287">Mandatory label rights</span></span>

| <span data-ttu-id="647dc-288">Chaîne de droits d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-288">Access rights string</span></span> | <span data-ttu-id="647dc-289">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-289">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-290">Valeur du droit d’accès</span><span class="sxs-lookup"><span data-stu-id="647dc-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="647dc-291">Nr</span><span class="sxs-lookup"><span data-stu-id="647dc-291">"NR"</span></span>                 | <span data-ttu-id="647dc-292">SDDL \_ non \_ lu \_</span><span class="sxs-lookup"><span data-stu-id="647dc-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="647dc-293">\_étiquette obligatoire \_ système \_ non \_ lue \_</span><span class="sxs-lookup"><span data-stu-id="647dc-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="647dc-294">11LE</span><span class="sxs-lookup"><span data-stu-id="647dc-294">"NW"</span></span>                 | <span data-ttu-id="647dc-295">SDDL \_ non \_ écrit \_</span><span class="sxs-lookup"><span data-stu-id="647dc-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="647dc-296">\_étiquette obligatoire \_ système \_ non en \_ écriture \_</span><span class="sxs-lookup"><span data-stu-id="647dc-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="647dc-297">NX</span><span class="sxs-lookup"><span data-stu-id="647dc-297">"NX"</span></span>                 | <span data-ttu-id="647dc-298">SDDL \_ non \_ exécuté \_</span><span class="sxs-lookup"><span data-stu-id="647dc-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="647dc-299">\_étiquette obligatoire \_ système \_ non \_ exécutée \_</span><span class="sxs-lookup"><span data-stu-id="647dc-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="647dc-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID de l’objet \_**</span><span class="sxs-lookup"><span data-stu-id="647dc-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-301">Représentation sous forme de chaîne d’un GUID qui indique la valeur du membre **ObjectType** d’une structure d’entrée du contrôle d’accès spécifique à l’objet, telle que l' [**\_ ACE access allowed \_ Object \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="647dc-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="647dc-302">La chaîne GUID utilise le format retourné par la fonction [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="647dc-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="647dc-303">Le tableau suivant répertorie certains GUID d’objets couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="647dc-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="647dc-304">Droits et GUID</span><span class="sxs-lookup"><span data-stu-id="647dc-304">Rights and GUID</span></span>                         | <span data-ttu-id="647dc-305">Autorisation</span><span class="sxs-lookup"><span data-stu-id="647dc-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="647dc-306">CR ; ab721a53-1e2f-11D0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="647dc-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="647dc-307">Modifier le mot de passe</span><span class="sxs-lookup"><span data-stu-id="647dc-307">Change password</span></span> |
| <span data-ttu-id="647dc-308">CR ; 00299570-246d-11D0-A768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="647dc-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="647dc-309">Réinitialiser le mot de passe</span><span class="sxs-lookup"><span data-stu-id="647dc-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="647dc-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**hériter du \_ GUID d’objet \_**</span><span class="sxs-lookup"><span data-stu-id="647dc-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-311">Représentation sous forme de chaîne d’un GUID qui indique la valeur du membre **InheritedObjectType** d’une structure ACE spécifique à un objet.</span><span class="sxs-lookup"><span data-stu-id="647dc-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="647dc-312">La chaîne GUID utilise le format [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="647dc-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="647dc-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**sid du compte \_**</span><span class="sxs-lookup"><span data-stu-id="647dc-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-314">[Chaîne sid](sid-strings.md) qui identifie le [tiers de confiance](trustees.md) de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="647dc-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="647dc-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**attribut de ressource \_**</span><span class="sxs-lookup"><span data-stu-id="647dc-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="647dc-316">\[FACULTATIF \] l' \_ attribut de ressource est uniquement destiné aux ACE de ressource et est facultatif.</span><span class="sxs-lookup"><span data-stu-id="647dc-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="647dc-317">Chaîne qui indique le type de données.</span><span class="sxs-lookup"><span data-stu-id="647dc-317">A string that indicates the data type.</span></span> <span data-ttu-id="647dc-318">Le type de données de l’ACE de l’attribut de ressource peut être l’un des types de données suivants définis dans SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="647dc-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="647dc-319">Le \# signe « » est synonyme de «0 » dans les attributs de ressource.</span><span class="sxs-lookup"><span data-stu-id="647dc-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="647dc-320">Par exemple, D :AI (XA ; OICI ; FA ;;; WD ; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) est équivalent à et interprété comme D :ai (XA ; oici ; FA ;;; WD ; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="647dc-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="647dc-321">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista et Windows server 2003 :** Les attributs de ressource ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="647dc-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="647dc-322">Chaîne de type de données ACE attribut de ressource</span><span class="sxs-lookup"><span data-stu-id="647dc-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="647dc-323">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="647dc-323">Constant in Sddl.h</span></span> | <span data-ttu-id="647dc-324">Type de données</span><span class="sxs-lookup"><span data-stu-id="647dc-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="647dc-325">ÉC</span><span class="sxs-lookup"><span data-stu-id="647dc-325">"TI"</span></span>                                    | <span data-ttu-id="647dc-326">SDDL \_ int</span><span class="sxs-lookup"><span data-stu-id="647dc-326">SDDL\_INT</span></span>          | <span data-ttu-id="647dc-327">Entier signé</span><span class="sxs-lookup"><span data-stu-id="647dc-327">Signed integer</span></span>   |
| <span data-ttu-id="647dc-328">PÉTAL</span><span class="sxs-lookup"><span data-stu-id="647dc-328">"TU"</span></span>                                    | <span data-ttu-id="647dc-329">SDDL \_ uint</span><span class="sxs-lookup"><span data-stu-id="647dc-329">SDDL\_UINT</span></span>         | <span data-ttu-id="647dc-330">Entier non signé</span><span class="sxs-lookup"><span data-stu-id="647dc-330">Unsigned integer</span></span> |
| <span data-ttu-id="647dc-331">TS</span><span class="sxs-lookup"><span data-stu-id="647dc-331">"TS"</span></span>                                    | <span data-ttu-id="647dc-332">\_WSTRING SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="647dc-333">Chaîne étendue</span><span class="sxs-lookup"><span data-stu-id="647dc-333">Wide string</span></span>      |
| <span data-ttu-id="647dc-334">ÉQUIPEMENTS</span><span class="sxs-lookup"><span data-stu-id="647dc-334">"TD"</span></span>                                    | <span data-ttu-id="647dc-335">\_sid SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-335">SDDL\_SID</span></span>          | <span data-ttu-id="647dc-336">SID</span><span class="sxs-lookup"><span data-stu-id="647dc-336">SID</span></span>              |
| <span data-ttu-id="647dc-337">ÉMETTEUR</span><span class="sxs-lookup"><span data-stu-id="647dc-337">"TX"</span></span>                                    | <span data-ttu-id="647dc-338">\_objet BLOB SDDL</span><span class="sxs-lookup"><span data-stu-id="647dc-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="647dc-339">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="647dc-339">Octet string</span></span>     |
| <span data-ttu-id="647dc-340">TO</span><span class="sxs-lookup"><span data-stu-id="647dc-340">"TB"</span></span>                                    | <span data-ttu-id="647dc-341">SDDL \_ booléen</span><span class="sxs-lookup"><span data-stu-id="647dc-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="647dc-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="647dc-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="647dc-343">L’exemple suivant illustre une chaîne ACE pour une entrée du contrôle d’accès autorisée.</span><span class="sxs-lookup"><span data-stu-id="647dc-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="647dc-344">Comme il ne s’agit pas d’une entrée du contrôle d’accès spécifique à un objet, elle ne contient pas d’informations dans les champs **\_ GUID d’objet** et **hériter du \_ \_ GUID d’objet** .</span><span class="sxs-lookup"><span data-stu-id="647dc-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="647dc-345">Le **champ \_ indicateurs ACE** est également vide, ce qui indique qu’aucun des indicateurs ACE n’est défini.</span><span class="sxs-lookup"><span data-stu-id="647dc-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="647dc-346">La chaîne ACE présentée ci-dessus décrit les informations ACE suivantes.</span><span class="sxs-lookup"><span data-stu-id="647dc-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="647dc-347">L’exemple suivant montre un fichier classé avec les revendications de ressource pour Windows et langage SQL (SQL) avec secret défini sur un impact professionnel élevé.</span><span class="sxs-lookup"><span data-stu-id="647dc-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="647dc-348">La chaîne ACE présentée ci-dessus décrit les informations ACE suivantes.</span><span class="sxs-lookup"><span data-stu-id="647dc-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="647dc-349">Pour plus d’informations, consultez [format de chaîne du descripteur de sécurité](security-descriptor-string-format.md) et [chaînes sid](sid-strings.md).</span><span class="sxs-lookup"><span data-stu-id="647dc-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="647dc-350">Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="647dc-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="647dc-351">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="647dc-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="647dc-352">[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="647dc-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>


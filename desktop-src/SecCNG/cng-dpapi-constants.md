---
description: Les constantes suivantes sont utilisées par l’API de protection des données CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes CNG CNG (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484289"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="db95b-103">Constantes CNG CNG</span><span class="sxs-lookup"><span data-stu-id="db95b-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="db95b-104">Les constantes suivantes sont utilisées par l’API de protection des données CNG.</span><span class="sxs-lookup"><span data-stu-id="db95b-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="db95b-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_délimiteur de la description NCRYPT \_ \_ et**</span><span class="sxs-lookup"><span data-stu-id="db95b-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-106">L "ET"</span><span class="sxs-lookup"><span data-stu-id="db95b-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="db95b-107">Peut être utilisé pour tester une chaîne de descripteur de protection pour un et un délimiteur.</span><span class="sxs-lookup"><span data-stu-id="db95b-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**le \_ descr \_ est égal à**</span><span class="sxs-lookup"><span data-stu-id="db95b-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-109">L "="</span><span class="sxs-lookup"><span data-stu-id="db95b-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="db95b-110">Peut être utilisé pour tester une chaîne de descripteur de protection pour un signe égal.</span><span class="sxs-lookup"><span data-stu-id="db95b-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_délimiteur de la description NCRYPT \_ \_ ou**</span><span class="sxs-lookup"><span data-stu-id="db95b-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-112">L "OU"</span><span class="sxs-lookup"><span data-stu-id="db95b-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="db95b-113">Peut être utilisé pour tester une chaîne de descripteur de protection pour un délimiteur ou.</span><span class="sxs-lookup"><span data-stu-id="db95b-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algorithme de protection de clé NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="db95b-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-115">"LOCAL"</span><span class="sxs-lookup"><span data-stu-id="db95b-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-116">Le descripteur de protection LOCAL protège le contenu de l’ouverture de session, de l’utilisateur actuel ou de l’ordinateur local, tel qu’il est identifié par les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="db95b-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="db95b-117">**\_protection de clé NCRYPT \_ \_ \_ connexion locale**</span><span class="sxs-lookup"><span data-stu-id="db95b-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="db95b-118">**\_protection de clé NCRYPT \_ \_ \_ utilisateur local**</span><span class="sxs-lookup"><span data-stu-id="db95b-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="db95b-119">**\_ \_ ordinateur local de protection de clé NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_ \_ \_ SDDL algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-121">SDDL</span><span class="sxs-lookup"><span data-stu-id="db95b-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-122">Protège le contenu d’une chaîne SDDL (Security Descriptor Definition Language) qui contient des informations de descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="db95b-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID de \_ l' \_ algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-124">SID</span><span class="sxs-lookup"><span data-stu-id="db95b-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-125">Le descripteur de protection SID contient un groupe ou une identité de principal.</span><span class="sxs-lookup"><span data-stu-id="db95b-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_ \_ \_ informations d’identification de l’algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-127">« Informations d’identification webconnexion »</span><span class="sxs-lookup"><span data-stu-id="db95b-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-128">Protège les informations d’identification du compte Web d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db95b-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_protection de clé NCRYPT \_ \_ \_ connexion locale**</span><span class="sxs-lookup"><span data-stu-id="db95b-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-130">horaire</span><span class="sxs-lookup"><span data-stu-id="db95b-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-131">Protège le contenu de l’ouverture de session actuelle.</span><span class="sxs-lookup"><span data-stu-id="db95b-131">Protects content to the current logon session.</span></span> <span data-ttu-id="db95b-132">Les utilisateurs ne seront pas en mesure de déchiffrer le contenu protégé après la déconnexion ou le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="db95b-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ ordinateur local de protection de clé NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-134">usinage</span><span class="sxs-lookup"><span data-stu-id="db95b-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-135">Protège le contenu de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="db95b-135">Protects content to the local computer.</span></span> <span data-ttu-id="db95b-136">Tous les utilisateurs de l’ordinateur local peuvent déchiffrer le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="db95b-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_protection de clé NCRYPT \_ \_ \_ utilisateur local**</span><span class="sxs-lookup"><span data-stu-id="db95b-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-138">utilisateur</span><span class="sxs-lookup"><span data-stu-id="db95b-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-139">Protège le contenu de la session utilisateur en cours.</span><span class="sxs-lookup"><span data-stu-id="db95b-139">Protects content to the current user session.</span></span> <span data-ttu-id="db95b-140">Seul cet utilisateur sur l’ordinateur local sera en mesure de déchiffrer le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="db95b-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_fournisseur de \_ protection de clés MS \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-142">« Fournisseur de protection de clé Microsoft »</span><span class="sxs-lookup"><span data-stu-id="db95b-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-143">Représente le fournisseur de protection de clés Microsoft qui prend en charge les formats représentés par les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="db95b-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="db95b-144">**\_SID de \_ l' \_ algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="db95b-145">**\_algorithme de protection de clé NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="db95b-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="db95b-146">**\_ \_ \_ SDDL algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db95b-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_fournisseur de \_ protection de clé client \_ Windows \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db95b-148">« Fournisseur de protection de clé client Windows »</span><span class="sxs-lookup"><span data-stu-id="db95b-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="db95b-149">Représente le fournisseur de protection de clé Microsoft qui est disponible uniquement sur le client et qui prend en charge les formats représentés par les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="db95b-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="db95b-150">**\_ \_ \_ informations d’identification de l’algorithme de protection de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="db95b-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db95b-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db95b-151">Requirements</span></span>



| <span data-ttu-id="db95b-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db95b-152">Requirement</span></span> | <span data-ttu-id="db95b-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="db95b-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="db95b-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db95b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="db95b-155">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db95b-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db95b-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db95b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="db95b-157">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db95b-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="db95b-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="db95b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="db95b-159"><dt>NCryptprotect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db95b-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 





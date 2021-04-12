---
description: Décrit les codes d’erreur 1300-1699 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Codes d’erreur système (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483320"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="d24d9-103">Codes d’erreur système (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="d24d9-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="d24d9-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="d24d9-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d24d9-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="d24d9-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1300 à 1699.</span><span class="sxs-lookup"><span data-stu-id="d24d9-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="d24d9-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="d24d9-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="d24d9-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="d24d9-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERREUR \_ non \_ \_ assignée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="d24d9-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-111">Tous les privilèges ou groupes référencés ne sont pas assignés à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d24d9-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERREUR \_ \_ non \_ mappée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="d24d9-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-114">Un mappage entre les noms de compte et les ID de sécurité n’a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="d24d9-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERREUR \_ aucun \_ quota \_ pour le \_ compte**</span><span class="sxs-lookup"><span data-stu-id="d24d9-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="d24d9-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-117">Aucune limite de quota système n’est définie spécifiquement pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="d24d9-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERREUR \_ de \_ \_ clé de session d’utilisateur local \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="d24d9-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-120">Aucune clé de chiffrement n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-120">No encryption key is available.</span></span> <span data-ttu-id="d24d9-121">Une clé de chiffrement connue a été retournée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERREUR \_ \_ \_ de mot de passe LM null**</span><span class="sxs-lookup"><span data-stu-id="d24d9-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="d24d9-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-124">Le mot de passe est trop complexe pour être converti en mot de passe LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="d24d9-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="d24d9-125">Le mot de passe du gestionnaire LAN Manager retourné est une chaîne **null** .</span><span class="sxs-lookup"><span data-stu-id="d24d9-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERREUR \_ de \_ révision inconnue**</span><span class="sxs-lookup"><span data-stu-id="d24d9-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="d24d9-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-128">Le niveau de révision est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d24d9-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**incompatibilité de révision d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-131">Indique que deux niveaux de révision sont incompatibles.</span><span class="sxs-lookup"><span data-stu-id="d24d9-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERREUR \_ propriétaire non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-134">Cet ID de sécurité ne peut pas être assigné en tant que propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="d24d9-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERREUR \_ de \_ groupe principal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-137">Cet ID de sécurité ne peut pas être affecté en tant que groupe principal d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d24d9-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERREUR \_ aucun \_ jeton d’emprunt d’identité \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-140">Une tentative a été effectuée pour fonctionner sur un jeton d’emprunt d’identité par un thread qui n’emprunte pas actuellement l’identité d’un client.</span><span class="sxs-lookup"><span data-stu-id="d24d9-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERREUR \_ Impossible de \_ désactiver le \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d24d9-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-143">Le groupe n’est peut-être pas désactivé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERREUR \_ aucun \_ serveur d’ouverture de session \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-146">Aucun serveur d’ouverture de session n’est actuellement disponible pour traiter la demande d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="d24d9-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERREUR \_ aucune \_ \_ ouverture de session de ce type \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="d24d9-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-149">Une session ouverte spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-149">A specified logon session does not exist.</span></span> <span data-ttu-id="d24d9-150">Elle a peut-être déjà été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERREUR \_ non liée à \_ ce type de \_ privilège**</span><span class="sxs-lookup"><span data-stu-id="d24d9-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="d24d9-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-153">Un privilège spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**privilège d’erreur \_ \_ non \_ détenu**</span><span class="sxs-lookup"><span data-stu-id="d24d9-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="d24d9-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-156">Le client ne dispose pas d'un privilège qui est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d24d9-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERREUR \_ \_ nom de compte non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="d24d9-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-159">Le nom fourni n’est pas un nom de compte correctement formé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**l’utilisateur de l’erreur \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="d24d9-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-162">Le compte spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d24d9-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERREUR \_ non de \_ ce type d' \_ utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d24d9-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="d24d9-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-165">Le compte spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**le \_ groupe d’erreurs \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="d24d9-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-168">Le groupe spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d24d9-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERREUR \_ non liée à \_ ce \_ groupe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="d24d9-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-171">Le groupe spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_membre \_ d’erreur dans le \_ groupe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="d24d9-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-174">Soit le compte d’utilisateur spécifié est déjà membre du groupe spécifié, soit le groupe spécifié ne peut pas être supprimé parce qu’il contient un membre.</span><span class="sxs-lookup"><span data-stu-id="d24d9-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**\_membre \_ d’erreur non dans le \_ \_ groupe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="d24d9-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-177">Le compte d’utilisateur spécifié n’est pas membre du compte de groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="d24d9-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERREUR de la \_ dernière \_ administration**</span><span class="sxs-lookup"><span data-stu-id="d24d9-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-180">Cette opération n’est pas autorisée, car elle peut entraîner la désactivation ou la suppression d’un compte d’administration ou l’impossibilité d’ouvrir une session.</span><span class="sxs-lookup"><span data-stu-id="d24d9-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**\_ \_ mot de passe erroné**</span><span class="sxs-lookup"><span data-stu-id="d24d9-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-183">Impossible de mettre à jour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-183">Unable to update the password.</span></span> <span data-ttu-id="d24d9-184">La valeur fournie en tant que mot de passe actuel est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="d24d9-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERREUR \_ \_ \_ de mot de passe incorrect**</span><span class="sxs-lookup"><span data-stu-id="d24d9-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-187">Impossible de mettre à jour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-187">Unable to update the password.</span></span> <span data-ttu-id="d24d9-188">La valeur fournie pour le nouveau mot de passe contient des valeurs qui ne sont pas autorisées dans les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restriction de mot de passe d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-190">1325 (0x52D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-191">Impossible de mettre à jour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-191">Unable to update the password.</span></span> <span data-ttu-id="d24d9-192">La valeur fournie pour le nouveau mot de passe ne répond pas aux exigences de longueur, de complexité ou d’historique du domaine.</span><span class="sxs-lookup"><span data-stu-id="d24d9-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERREUR \_ d’ouverture de session \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-195">Le nom d'utilisateur ou le mot de passe est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restriction de compte d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-198">Les restrictions de compte empêchent cet utilisateur de se connecter.</span><span class="sxs-lookup"><span data-stu-id="d24d9-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="d24d9-199">Par exemple : les mots de passe vides ne sont pas autorisés, les heures de connexion sont limitées ou une restriction de stratégie a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERREUR \_ \_ d’heures d’ouverture de session non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="d24d9-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-202">Votre compte a des restrictions de temps qui vous empêchent de vous connecter pour le moment.</span><span class="sxs-lookup"><span data-stu-id="d24d9-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERREUR \_ de \_ station de travail non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="d24d9-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-205">Cet utilisateur n’est pas autorisé à se connecter à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**\_mot de passe d’erreur \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="d24d9-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="d24d9-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-208">Le mot de passe de ce compte a expiré.</span><span class="sxs-lookup"><span data-stu-id="d24d9-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**compte d’erreur \_ \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="d24d9-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-211">Cet utilisateur ne peut pas se connecter, car ce compte est actuellement désactivé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERREUR \_ aucune \_ mappée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="d24d9-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-214">Aucun mappage entre les noms de compte et les ID de sécurité n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="d24d9-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERREUR \_ trop \_ de \_ LUID \_ demandée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="d24d9-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-217">Trop d’identificateurs d’utilisateur local (LUID) ont été demandés à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d24d9-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERREUR \_ LUID \_ épuisée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="d24d9-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-220">Aucun autre identificateur d’utilisateur local (LUID) n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERREUR \_ de \_ sous-autorité non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="d24d9-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-223">La partie sous-autorité d’un ID de sécurité n’est pas valide pour cette utilisation particulière.</span><span class="sxs-lookup"><span data-stu-id="d24d9-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERREUR \_ de \_ liste de contrôle d’accès non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="d24d9-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-226">La structure de la liste de contrôle d’accès (ACL) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERREUR \_ sid non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="d24d9-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-229">La structure de l’ID de sécurité n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERREUR \_ de \_ Description de sécurité non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-232">La structure du descripteur de sécurité n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERREUR \_ de \_ liste de contrôle d’héritage incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-234">1340 (0x53C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-235">La liste de contrôle d’accès (ACL) ou l’entrée de contrôle d’accès (ACE) héritée n’a pas pu être créée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**serveur d’erreur \_ \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-238">Le serveur est actuellement désactivé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**serveur d’erreurs \_ \_ non \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-241">Le serveur est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERREUR \_ \_ ID d' \_ autorité non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-244">La valeur fournie est une valeur non valide pour une autorité d’identificateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERREUR de dépassement de l' \_ \_ espace alloué \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="d24d9-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-247">Il n’y a plus de mémoire disponible pour les mises à jour des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d24d9-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERREUR \_ d' \_ attributs de groupe non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="d24d9-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-250">Les attributs spécifiés ne sont pas valides ou sont incompatibles avec les attributs du groupe dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="d24d9-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERREUR \_ de \_ niveau d’emprunt d’identité incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="d24d9-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-253">Soit un niveau d'emprunt d'identité requis n'a pas été fourni, soit le niveau d'emprunt d'identité fourni n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERREUR \_ Impossible d' \_ ouvrir \_ anonyme**</span><span class="sxs-lookup"><span data-stu-id="d24d9-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="d24d9-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-256">Impossible d’ouvrir un jeton de sécurité de niveau anonyme.</span><span class="sxs-lookup"><span data-stu-id="d24d9-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERREUR \_ , \_ classe de validation incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="d24d9-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-259">La classe d’informations de validation demandée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERREUR \_ de \_ type de jeton incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="d24d9-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-262">Le type du jeton n’est pas approprié pour sa tentative d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERREUR \_ aucune \_ sécurité \_ sur l' \_ objet**</span><span class="sxs-lookup"><span data-stu-id="d24d9-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="d24d9-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-265">Impossible d’effectuer une opération de sécurité sur un objet qui n’a pas de sécurité associée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERREUR \_ Impossible d' \_ accéder aux \_ informations de domaine \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="d24d9-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-268">Impossible de lire les informations de configuration à partir du contrôleur de domaine, soit parce que l’ordinateur n’est pas disponible, soit parce que l’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERREUR \_ d' \_ État du serveur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="d24d9-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-271">Le gestionnaire de comptes de sécurité (SAM) ou le serveur de l’autorité de sécurité locale (LSA) est dans un état incorrect pour effectuer l’opération de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d24d9-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERREUR \_ d' \_ État de domaine non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="d24d9-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-274">Le domaine était dans un état incorrect pour effectuer l’opération de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d24d9-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERREUR \_ de \_ rôle de domaine non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-277">Cette opération est autorisée uniquement pour le contrôleur de domaine principal du domaine.</span><span class="sxs-lookup"><span data-stu-id="d24d9-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERREUR \_ non de \_ ce type de \_ domaine**</span><span class="sxs-lookup"><span data-stu-id="d24d9-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-279">1355 (0x54B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-280">Le domaine spécifié n’existe pas ou n’a pas pu être contacté.</span><span class="sxs-lookup"><span data-stu-id="d24d9-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**le \_ domaine d’erreur \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-283">Le domaine spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d24d9-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**limite de domaine d’erreur \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-285">1357 (0x54D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-286">Une tentative a été effectuée pour dépasser la limite du nombre de domaines par serveur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERREUR d’altération de la \_ \_ base de DB interne \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-288">1358 (0x54E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-289">Impossible d’effectuer l’opération demandée en raison d’une panne de support catastrophique ou d’une corruption de la structure de données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d24d9-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**erreur \_ interne \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="d24d9-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-291">1359 (0x54F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-292">Une erreur interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d24d9-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERREUR \_ générique \_ non \_ mappée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="d24d9-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-295">Les types d’accès génériques étaient contenus dans un masque d’accès qui doit déjà être mappé à des types non génériques.</span><span class="sxs-lookup"><span data-stu-id="d24d9-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERREUR \_ de \_ format de descripteur incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="d24d9-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-298">Un descripteur de sécurité n’est pas dans le format approprié (absolu ou auto-relatif).</span><span class="sxs-lookup"><span data-stu-id="d24d9-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERREUR lors du \_ \_ processus d’ouverture de session \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="d24d9-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-301">L’action demandée est restreinte pour une utilisation par les processus d’ouverture de session uniquement.</span><span class="sxs-lookup"><span data-stu-id="d24d9-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="d24d9-302">Le processus appelant n’a pas été inscrit en tant que processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="d24d9-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERREUR de \_ session d’ouverture de \_ session \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="d24d9-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-305">Impossible de démarrer une nouvelle ouverture de session avec un ID qui est déjà en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERREUR \_ aucun \_ package de ce type \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="d24d9-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-308">Un package d’authentification spécifié est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d24d9-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERREUR \_ \_ d’état de session de connexion incorrecte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="d24d9-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-311">La session d’ouverture de session n’est pas dans un état cohérent avec l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERREUR \_ de \_ collision de session de connexion \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="d24d9-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-314">L’ID de session d’ouverture de session est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERREUR \_ de \_ type d’ouverture de session non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="d24d9-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-317">Une demande d’ouverture de session contenait une valeur de type d’ouverture de session non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERREUR \_ Impossible d' \_ emprunter l’identité**</span><span class="sxs-lookup"><span data-stu-id="d24d9-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="d24d9-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-320">Impossible d’emprunter l’identité à l’aide d’un canal nommé tant que les données n’ont pas été lues à partir de ce canal.</span><span class="sxs-lookup"><span data-stu-id="d24d9-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERREUR \_ RXACT \_ État non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="d24d9-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-323">L’état de transaction d’une sous-arborescence du Registre est incompatible avec l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**erreur de validation d’erreur \_ RXACT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-325">1370 (0x55A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-326">Une corruption de base de données de sécurité interne a été détectée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_compte spécial d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-328">1371 (0x55B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-329">Impossible d’effectuer cette opération sur les comptes intégrés.</span><span class="sxs-lookup"><span data-stu-id="d24d9-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_Groupe spécial d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-331">1372 (0x55C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-332">Impossible d’effectuer cette opération sur ce groupe spécial intégré.</span><span class="sxs-lookup"><span data-stu-id="d24d9-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_utilisateur spécial d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-335">Impossible d’effectuer cette opération sur cet utilisateur spécial intégré.</span><span class="sxs-lookup"><span data-stu-id="d24d9-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ groupe principal d’erreurs membres \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-338">L’utilisateur ne peut pas être supprimé d’un groupe, car le groupe est actuellement le groupe principal de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_jeton \_ d’erreur \_ déjà \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-340">1375 (0x55F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-341">Le jeton est déjà utilisé en tant que jeton principal.</span><span class="sxs-lookup"><span data-stu-id="d24d9-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERREUR \_ de \_ ce type d' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="d24d9-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="d24d9-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-344">Le groupe local spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_membre \_ d’erreur non \_ dans l' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="d24d9-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="d24d9-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-347">Le nom de compte spécifié n’est pas membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_membre \_ d’erreur dans l' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="d24d9-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="d24d9-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-350">Le nom de compte spécifié est déjà membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="d24d9-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**l' \_ alias d’erreur \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d24d9-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="d24d9-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-353">Le groupe local spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d24d9-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERREUR \_ d’ouverture de session \_ non \_ accordée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="d24d9-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-356">Échec de l’ouverture de session : l’utilisateur n’a pas obtenu le type d’ouverture de session demandé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERREUR \_ trop \_ de \_ secrets**</span><span class="sxs-lookup"><span data-stu-id="d24d9-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="d24d9-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-359">Le nombre maximal de secrets qui peuvent être stockés dans un seul système a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**SECRET d’erreur \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="d24d9-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="d24d9-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-362">La longueur d’un secret dépasse la longueur maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**erreur \_ interne de la \_ base de \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="d24d9-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-365">La base de données de l’autorité de sécurité locale contient une incohérence interne.</span><span class="sxs-lookup"><span data-stu-id="d24d9-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERREUR \_ trop \_ d' \_ ID de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="d24d9-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-368">Pendant une tentative de connexion, le contexte de sécurité de l’utilisateur a accumulé trop d’ID de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d24d9-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_type d’erreur d’ouverture de session \_ \_ non \_ accordé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="d24d9-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-371">Échec de l’ouverture de session : l’utilisateur n’a pas obtenu le type d’ouverture de session demandé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERREUR \_ de \_ \_ chiffrement croisé NT \_ requis**</span><span class="sxs-lookup"><span data-stu-id="d24d9-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-374">Un mot de passe à chiffrement croisé est nécessaire pour modifier le mot de passe d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERREUR \_ non \_ membre de ce type \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-377">Impossible d’ajouter ou de supprimer un membre du groupe local, car le membre n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERREUR \_ membre non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-380">Impossible d’ajouter un nouveau membre à un groupe local, car le type de compte du membre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERREUR \_ trop \_ de \_ sid**</span><span class="sxs-lookup"><span data-stu-id="d24d9-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-383">Un trop grand nombre d’ID de sécurité a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="d24d9-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERREUR \_ LM \_ de \_ chiffrement croisé \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d24d9-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-386">Un mot de passe à chiffrement croisé est nécessaire pour modifier ce mot de passe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERREUR \_ aucun \_ héritage**</span><span class="sxs-lookup"><span data-stu-id="d24d9-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-388">1391 (0x56F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-389">Indique qu’une liste de contrôle d’accès ne contient aucun composant pouvant être hérité.</span><span class="sxs-lookup"><span data-stu-id="d24d9-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**fichier d’erreur \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="d24d9-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-392">Le fichier ou le répertoire est endommagé et illisible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERREUR \_ disque \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="d24d9-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-395">La structure du disque est endommagée et illisible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERREUR \_ aucune \_ \_ clé de session utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="d24d9-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-398">Il n’existe aucune clé de session utilisateur pour la session d’ouverture de session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_dépassement du \_ quota de licences d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="d24d9-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-401">Le service auquel vous accédez a une licence pour un nombre particulier de connexions.</span><span class="sxs-lookup"><span data-stu-id="d24d9-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="d24d9-402">Aucune autre connexion ne peut être établie au service pour l’instant, car il existe déjà autant de connexions que le service peut accepter.</span><span class="sxs-lookup"><span data-stu-id="d24d9-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERREUR \_ \_ nom cible \_ erroné**</span><span class="sxs-lookup"><span data-stu-id="d24d9-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="d24d9-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-405">Le nom du compte cible est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERREUR \_ l' \_ authentification mutuelle \_ a échoué**</span><span class="sxs-lookup"><span data-stu-id="d24d9-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="d24d9-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-408">L’authentification mutuelle a échoué.</span><span class="sxs-lookup"><span data-stu-id="d24d9-408">Mutual Authentication failed.</span></span> <span data-ttu-id="d24d9-409">Le mot de passe du serveur est obsolète sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="d24d9-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**décalage de l’heure d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="d24d9-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-412">Il y a une différence de temps et/ou de date entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERREUR \_ \_ domaine actuel \_ non \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="d24d9-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-415">Cette opération ne peut pas être effectuée sur le domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="d24d9-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERREUR \_ de \_ handle de fenêtre non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="d24d9-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-418">Handle de fenêtre non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERREUR \_ de \_ handle de menu non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="d24d9-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-421">Descripteur de menu non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERREUR \_ de \_ handle de curseur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-424">Handle de curseur non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERREUR \_ de \_ handle d’accélération non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-427">Handle de table d’accélérateurs non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERREUR \_ de \_ handle de hook non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-429">1404 (0x57C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-430">Handle de hook non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERREUR \_ de \_ handle DWP non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-433">Handle non valide vers une structure de position à plusieurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="d24d9-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERREUR \_ TLW \_ avec \_ WSCHILD**</span><span class="sxs-lookup"><span data-stu-id="d24d9-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-435">1406 (0x57E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-436">Impossible de créer une fenêtre enfant de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERREUR \_ Impossible de \_ trouver la \_ \_ classe WND**</span><span class="sxs-lookup"><span data-stu-id="d24d9-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-438">1407 (0x57F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-439">Impossible de trouver la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d24d9-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_fenêtre \_ d’erreur d’un \_ autre \_ thread**</span><span class="sxs-lookup"><span data-stu-id="d24d9-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="d24d9-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-442">Fenêtre non valide ; elle appartient à un autre thread.</span><span class="sxs-lookup"><span data-stu-id="d24d9-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERREUR de \_ raccourci \_ déjà \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="d24d9-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-444">1409 (0x581)</span><span class="sxs-lookup"><span data-stu-id="d24d9-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-445">La touche d’accès rapide est déjà inscrite.</span><span class="sxs-lookup"><span data-stu-id="d24d9-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**la \_ classe d’erreur \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="d24d9-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="d24d9-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-448">La classe existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d24d9-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**la \_ classe d’erreur \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="d24d9-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="d24d9-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-451">La classe n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**la \_ classe Error \_ contient \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="d24d9-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="d24d9-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-454">La classe a toujours des fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="d24d9-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERREUR \_ d' \_ index non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="d24d9-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-457">Index non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**HANDLE d’icône d’erreur \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="d24d9-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-460">Handle d’icône non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERREUR \_ d' \_ index de boîte de dialogue privé \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="d24d9-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-463">Utilisation de mots de boîte de dialogue privés.</span><span class="sxs-lookup"><span data-stu-id="d24d9-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ID de zone de liste d’erreurs \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="d24d9-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="d24d9-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-466">L’identificateur de la zone de liste est introuvable.</span><span class="sxs-lookup"><span data-stu-id="d24d9-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERREUR \_ aucun caractère \_ générique \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="d24d9-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-469">Aucun caractère générique n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERREUR \_ du presse-papiers \_ non \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="d24d9-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-471">1418 (0x58A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-472">Le thread n’a pas de presse-papiers ouvert.</span><span class="sxs-lookup"><span data-stu-id="d24d9-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERREUR de \_ raccourci \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="d24d9-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-474">1419 (0x58B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-475">La touche d’accès rapide n’est pas inscrite.</span><span class="sxs-lookup"><span data-stu-id="d24d9-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**fenêtre d’erreur, \_ \_ pas de boîte de \_ dialogue**</span><span class="sxs-lookup"><span data-stu-id="d24d9-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-477">1420 (0x58C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-478">La fenêtre n’est pas une fenêtre de boîte de dialogue valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ID de contrôle d’erreur \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="d24d9-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-480">1421 (0x58D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-481">ID de contrôle introuvable.</span><span class="sxs-lookup"><span data-stu-id="d24d9-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**MESSAGE d’erreur de \_ ComboBox non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-483">1422 (0x58E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-484">Message non valide pour une zone de liste déroulante, car il ne dispose pas d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d24d9-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**fenêtre d’erreur \_ \_ non \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="d24d9-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-486">1423 (0x58F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-487">La fenêtre n’est pas une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d24d9-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERREUR de modification de la \_ \_ hauteur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="d24d9-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-490">La hauteur doit être inférieure à 256.</span><span class="sxs-lookup"><span data-stu-id="d24d9-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_DC d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="d24d9-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="d24d9-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-493">Handle de contexte de périphérique (DC) non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERREUR \_ de \_ filtre de hook non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="d24d9-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-496">Type de procédure de raccordement non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERREUR \_ de \_ procédure de filtre non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="d24d9-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-499">Procédure de hook non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**raccordement d’erreur \_ \_ nécessitant \_ HMOD**</span><span class="sxs-lookup"><span data-stu-id="d24d9-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="d24d9-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-502">Impossible de définir un hook non local sans un handle de module.</span><span class="sxs-lookup"><span data-stu-id="d24d9-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_crochet global \_ uniquement d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="d24d9-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-505">Cette procédure de hook ne peut être définie que globalement.</span><span class="sxs-lookup"><span data-stu-id="d24d9-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_ensemble de \_ raccordements du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="d24d9-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-508">La procédure de hook du journal est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**HOOK d’erreur \_ \_ non \_ installé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="d24d9-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-511">La procédure de hook n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERREUR \_ de \_ message lb non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="d24d9-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-514">Message non valide pour une zone de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="d24d9-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERREUR \_ SETCOUNT \_ sur \_ Bad \_ lb**</span><span class="sxs-lookup"><span data-stu-id="d24d9-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="d24d9-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-517">LB \_ SETCOUNT envoyé à une zone de liste non différée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERREUR \_ lb \_ sans \_ TABSTOPS**</span><span class="sxs-lookup"><span data-stu-id="d24d9-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-519">1434 (0x59A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-520">Cette zone de liste ne prend pas en charge les taquets de tabulation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERREUR \_ \_ de destruction de l’objet d’un \_ \_ autre \_ thread**</span><span class="sxs-lookup"><span data-stu-id="d24d9-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-522">1435 (0x59B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-523">Impossible de détruire un objet créé par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="d24d9-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menu de \_ fenêtre \_ enfant d’erreur**</span><span class="sxs-lookup"><span data-stu-id="d24d9-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-525">1436 (0x59C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-526">Les fenêtres enfants ne peuvent pas avoir de menus.</span><span class="sxs-lookup"><span data-stu-id="d24d9-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERREUR \_ \_ \_ -menu système**</span><span class="sxs-lookup"><span data-stu-id="d24d9-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-528">1437 (0x59D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-529">La fenêtre n’a pas de menu système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERREUR \_ de \_ style MsgBox non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-531">1438 (0x59E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-532">Style de boîte de message non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERREUR \_ \_ valeur SPI non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-534">1439 (0x59F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-535">Paramètre au niveau du système (SPI) non valide \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d24d9-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**écran d’erreur \_ \_ déjà \_ verrouillé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-537">1440 (0x5A0)</span><span class="sxs-lookup"><span data-stu-id="d24d9-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-538">Écran déjà verrouillé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERREUR les \_ HWND \_ ont un \_ \_ parent diff**</span><span class="sxs-lookup"><span data-stu-id="d24d9-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-540">1441 (0x5A1)</span><span class="sxs-lookup"><span data-stu-id="d24d9-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-541">Tous les descripteurs de Windows dans une structure de position à fenêtres multiples doivent avoir le même parent.</span><span class="sxs-lookup"><span data-stu-id="d24d9-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**fenêtre d’erreur \_ non \_ enfant \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-543">1442 (0x5A2)</span><span class="sxs-lookup"><span data-stu-id="d24d9-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-544">La fenêtre n’est pas une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="d24d9-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERREUR \_ de \_ commande GW non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-546">1443 (0x5A3)</span><span class="sxs-lookup"><span data-stu-id="d24d9-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-547">Commande GW non valide \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d24d9-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**\_ID de \_ thread non valide d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-549">1444 (0x5A4)</span><span class="sxs-lookup"><span data-stu-id="d24d9-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-550">Identificateur de thread non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**\_fenêtre erreur non- \_ MDICHILD \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-552">1445 (0x5A5)</span><span class="sxs-lookup"><span data-stu-id="d24d9-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-553">Impossible de traiter un message à partir d’une fenêtre qui n’est pas une fenêtre d’interface multidocument (MDI).</span><span class="sxs-lookup"><span data-stu-id="d24d9-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_fenêtre contextuelle d’erreur \_ déjà \_ active**</span><span class="sxs-lookup"><span data-stu-id="d24d9-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-555">1446 (0x5A6)</span><span class="sxs-lookup"><span data-stu-id="d24d9-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-556">Menu contextuel déjà actif.</span><span class="sxs-lookup"><span data-stu-id="d24d9-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERREUR \_ aucune \_ barre de défilement**</span><span class="sxs-lookup"><span data-stu-id="d24d9-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-558">1447 (0x5A7)</span><span class="sxs-lookup"><span data-stu-id="d24d9-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-559">La fenêtre n’a pas de barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="d24d9-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERREUR \_ de \_ plage de barre de défilement non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-561">1448 (0x5A8)</span><span class="sxs-lookup"><span data-stu-id="d24d9-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-562">La plage de la barre de défilement ne peut pas être supérieure à MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="d24d9-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERREUR \_ de \_ commande SHOWWIN non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-564">1449 (0x5A9)</span><span class="sxs-lookup"><span data-stu-id="d24d9-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-565">Impossible d’afficher ou de supprimer la fenêtre de la manière spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERREUR \_ aucune \_ \_ ressource système**</span><span class="sxs-lookup"><span data-stu-id="d24d9-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-567">1450 (0x5AA)</span><span class="sxs-lookup"><span data-stu-id="d24d9-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-568">Les ressources système sont insuffisantes pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**\_ressources système non paginées de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-570">1451 (0x5AB)</span><span class="sxs-lookup"><span data-stu-id="d24d9-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-571">Les ressources système sont insuffisantes pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ressources système d’erreur \_ paginée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-573">1452 (0x5AC)</span><span class="sxs-lookup"><span data-stu-id="d24d9-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-574">Les ressources système sont insuffisantes pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**QUOTA de la plage de travail des erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-576">1453 (0x5AD)</span><span class="sxs-lookup"><span data-stu-id="d24d9-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-577">Quota insuffisant pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERREUR de \_ quota du fichier d’échange \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-579">1454 (0x5AE)</span><span class="sxs-lookup"><span data-stu-id="d24d9-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-580">Quota insuffisant pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_limite d’engagement d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-582">1455 (0x5AF)</span><span class="sxs-lookup"><span data-stu-id="d24d9-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-583">Le fichier d’échange est trop petit pour que cette opération se termine.</span><span class="sxs-lookup"><span data-stu-id="d24d9-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**élément de menu d’erreur \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="d24d9-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-585">1456 (0x5B0)</span><span class="sxs-lookup"><span data-stu-id="d24d9-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-586">Élément de menu introuvable.</span><span class="sxs-lookup"><span data-stu-id="d24d9-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERREUR \_ de \_ handle de clavier non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-588">1457 (0x5B1)</span><span class="sxs-lookup"><span data-stu-id="d24d9-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-589">Handle de disposition de clavier non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**TYPE de raccordement d’erreur \_ \_ \_ non \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-591">1458 (0x5B2)</span><span class="sxs-lookup"><span data-stu-id="d24d9-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-592">Type de raccordement non autorisé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**l’erreur \_ requiert un \_ \_ WINDOWSTATION interactif**</span><span class="sxs-lookup"><span data-stu-id="d24d9-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-594">1459 (0x5B3)</span><span class="sxs-lookup"><span data-stu-id="d24d9-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-595">Cette opération nécessite une station Windows Interactive.</span><span class="sxs-lookup"><span data-stu-id="d24d9-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_délai d’erreur**</span><span class="sxs-lookup"><span data-stu-id="d24d9-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-597">1460 (0x5B4)</span><span class="sxs-lookup"><span data-stu-id="d24d9-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-598">Cette opération a été renvoyée car le délai d'attente a expiré.</span><span class="sxs-lookup"><span data-stu-id="d24d9-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERREUR \_ de \_ handle de moniteur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-600">1461 (0x5B5)</span><span class="sxs-lookup"><span data-stu-id="d24d9-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-601">Handle de moniteur non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERREUR de \_ taille incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-603">1462 (0x5B6)</span><span class="sxs-lookup"><span data-stu-id="d24d9-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-604">Argument de taille incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERREUR \_ de \_ classe symlink \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-606">1463 (0x5B7)</span><span class="sxs-lookup"><span data-stu-id="d24d9-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-607">Le lien symbolique ne peut pas être suivi, car son type est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERREUR \_ symlink \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="d24d9-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-609">1464 (0x5B8)</span><span class="sxs-lookup"><span data-stu-id="d24d9-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-610">Cette application ne prend pas en charge l’opération en cours sur les liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="d24d9-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**erreur \_ d' \_ analyse XML d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-612">1465 (0x5B9)</span><span class="sxs-lookup"><span data-stu-id="d24d9-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-613">Windows n’a pas pu analyser les données XML demandées.</span><span class="sxs-lookup"><span data-stu-id="d24d9-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**erreur \_ XMLDSIG \_ erreur XMLDSIG**</span><span class="sxs-lookup"><span data-stu-id="d24d9-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-615">1466 (0x5BA)</span><span class="sxs-lookup"><span data-stu-id="d24d9-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-616">Une erreur s’est produite lors du traitement d’une signature numérique XML.</span><span class="sxs-lookup"><span data-stu-id="d24d9-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERREUR de \_ redémarrage de l' \_ application**</span><span class="sxs-lookup"><span data-stu-id="d24d9-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-618">1467 (0x5BB)</span><span class="sxs-lookup"><span data-stu-id="d24d9-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-619">Cette application doit être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERREUR \_ de \_ compartiment incorrect**</span><span class="sxs-lookup"><span data-stu-id="d24d9-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-621">1468 (0x5BC)</span><span class="sxs-lookup"><span data-stu-id="d24d9-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-622">L’appelant a effectué la demande de connexion dans le compartiment de routage incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERREUR \_ AUTHIP \_ échec**</span><span class="sxs-lookup"><span data-stu-id="d24d9-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-624">1469 (0x5BD)</span><span class="sxs-lookup"><span data-stu-id="d24d9-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-625">Un échec AuthIP s’est produite lors de la tentative de connexion à l’hôte distant.</span><span class="sxs-lookup"><span data-stu-id="d24d9-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERREUR \_ aucune \_ \_ ressource NVRAM**</span><span class="sxs-lookup"><span data-stu-id="d24d9-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-627">1470 (0x5BE)</span><span class="sxs-lookup"><span data-stu-id="d24d9-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-628">Des ressources NVRAM insuffisantes existent pour terminer le service demandé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="d24d9-629">Un redémarrage peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d24d9-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERREUR \_ pas de traitement de l' \_ interface graphique \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-631">1471 (0x5BF)</span><span class="sxs-lookup"><span data-stu-id="d24d9-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-632">Impossible de terminer l’opération demandée, car le processus spécifié n’est pas un processus GUI.</span><span class="sxs-lookup"><span data-stu-id="d24d9-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERREUR \_ \_ fichier journal \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-634">1500 (0x5DC)</span><span class="sxs-lookup"><span data-stu-id="d24d9-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-635">Le fichier journal des événements est endommagé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERREUR \_ EventLog \_ Impossible de \_ Démarrer**</span><span class="sxs-lookup"><span data-stu-id="d24d9-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-637">1501 (0x5DD)</span><span class="sxs-lookup"><span data-stu-id="d24d9-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-638">Aucun fichier journal des événements n’a pu être ouvert. le service de journalisation des événements n’a donc pas démarré.</span><span class="sxs-lookup"><span data-stu-id="d24d9-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**\_fichier journal des erreurs \_ \_ plein**</span><span class="sxs-lookup"><span data-stu-id="d24d9-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-640">1502 (0x5DE)</span><span class="sxs-lookup"><span data-stu-id="d24d9-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-641">Le fichier journal des événements est plein.</span><span class="sxs-lookup"><span data-stu-id="d24d9-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERREUR \_ de \_ fichier EventLog \_ modifié**</span><span class="sxs-lookup"><span data-stu-id="d24d9-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-643">1503 (0x5DF)</span><span class="sxs-lookup"><span data-stu-id="d24d9-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-644">Le fichier journal des événements a changé entre les opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="d24d9-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERREUR \_ \_ nom de tâche non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-647">Le nom de tâche spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERREUR \_ d' \_ index de tâche non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-650">L’index de tâche spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_thread \_ d’erreur déjà dans la \_ \_ tâche**</span><span class="sxs-lookup"><span data-stu-id="d24d9-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="d24d9-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-653">Le thread spécifié est déjà joint à une tâche.</span><span class="sxs-lookup"><span data-stu-id="d24d9-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERREUR lors de l’installation de l' \_ \_ échec du service \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="d24d9-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-656">Impossible d’accéder au service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="d24d9-657">Cela peut se produire si le Windows Installer n’est pas correctement installé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="d24d9-658">Contactez votre service de support technique pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERREUR lors de l' \_ installation de \_ USEREXIT**</span><span class="sxs-lookup"><span data-stu-id="d24d9-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="d24d9-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-661">Installation annulée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERREUR d' \_ installation \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="d24d9-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-664">Erreur irrécupérable lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERREUR d' \_ installation d' \_ interruption**</span><span class="sxs-lookup"><span data-stu-id="d24d9-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="d24d9-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-667">Installation interrompue, incomplète.</span><span class="sxs-lookup"><span data-stu-id="d24d9-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERREUR \_ de \_ produit inconnu**</span><span class="sxs-lookup"><span data-stu-id="d24d9-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="d24d9-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-670">Cette action est valide uniquement pour les produits actuellement installés.</span><span class="sxs-lookup"><span data-stu-id="d24d9-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**\_fonctionnalité inconnue d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="d24d9-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-673">L’ID de fonctionnalité n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="d24d9-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERREUR \_ de \_ composant inconnu**</span><span class="sxs-lookup"><span data-stu-id="d24d9-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="d24d9-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-676">L’ID du composant n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="d24d9-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERREUR \_ , \_ propriété inconnue**</span><span class="sxs-lookup"><span data-stu-id="d24d9-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="d24d9-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-679">Propriété inconnue.</span><span class="sxs-lookup"><span data-stu-id="d24d9-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERREUR \_ d' \_ État de handle non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="d24d9-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-682">Le descripteur est dans un État non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERREUR de \_ configuration incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-684">1610 (0x64A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-685">Les données de configuration de ce produit sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="d24d9-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="d24d9-686">Contactez votre service de support technique.</span><span class="sxs-lookup"><span data-stu-id="d24d9-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**INDEX d’erreurs \_ \_ absent**</span><span class="sxs-lookup"><span data-stu-id="d24d9-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-688">1611 (0x64B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-689">Qualificateur de composant absent.</span><span class="sxs-lookup"><span data-stu-id="d24d9-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERREUR d’installation de la \_ \_ source \_ absente**</span><span class="sxs-lookup"><span data-stu-id="d24d9-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-691">1612 (0x64C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-692">La source d’installation de ce produit n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-692">The installation source for this product is not available.</span></span> <span data-ttu-id="d24d9-693">Vérifiez que la source existe et que vous êtes en mesure d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="d24d9-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERREUR d’installation de la \_ \_ version du package \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-695">1613 (0x64D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-696">Ce package d’installation ne peut pas être installé par le service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="d24d9-697">Vous devez installer un Service Pack Windows qui contient une version plus récente du service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERREUR de \_ produit \_ désinstallée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-699">1614 (0x64E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-700">Le produit est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERREUR \_ de \_ syntaxe de requête incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-702">1615 (0x64F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-703">Syntaxe de requête SQL non valide ou non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d24d9-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**champ d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="d24d9-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-706">Le champ d’enregistrement n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d24d9-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**périphérique d’erreur \_ \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="d24d9-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="d24d9-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-709">L’appareil a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="d24d9-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERREUR d' \_ installation \_ déjà \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="d24d9-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="d24d9-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-712">Une autre installation est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="d24d9-712">Another installation is already in progress.</span></span> <span data-ttu-id="d24d9-713">Terminez cette installation avant de procéder à cette installation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERREUR \_ d' \_ \_ échec d’ouverture du package d’installation \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="d24d9-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-716">Ce package d’installation n’a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="d24d9-716">This installation package could not be opened.</span></span> <span data-ttu-id="d24d9-717">Vérifiez que le package existe et que vous pouvez y accéder, ou contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de Windows Installer valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERREUR lors de l' \_ installation du \_ package \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="d24d9-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-720">Ce package d’installation n’a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="d24d9-720">This installation package could not be opened.</span></span> <span data-ttu-id="d24d9-721">Contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de Windows Installer valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERREUR d' \_ installation de \_ l’interface utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="d24d9-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-724">Une erreur s’est produite lors du démarrage de l’interface utilisateur du service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="d24d9-725">Contactez votre service de support technique.</span><span class="sxs-lookup"><span data-stu-id="d24d9-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERREUR d’installation de l' \_ \_ échec du journal \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="d24d9-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-728">Erreur lors de l’ouverture du fichier journal d’installation.</span><span class="sxs-lookup"><span data-stu-id="d24d9-728">Error opening installation log file.</span></span> <span data-ttu-id="d24d9-729">Vérifiez que l’emplacement du fichier journal spécifié existe et que vous pouvez y écrire.</span><span class="sxs-lookup"><span data-stu-id="d24d9-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERREUR d’installation de la \_ \_ langue \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="d24d9-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="d24d9-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-732">Le langage de ce package d’installation n’est pas pris en charge par votre système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERREUR lors de l’installation de l’échec de la \_ \_ transformation \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="d24d9-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-735">Erreur lors de l’application des transformations.</span><span class="sxs-lookup"><span data-stu-id="d24d9-735">Error applying transforms.</span></span> <span data-ttu-id="d24d9-736">Vérifiez que les chemins d’accès de transformation spécifiés sont valides.</span><span class="sxs-lookup"><span data-stu-id="d24d9-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERREUR lors de l' \_ installation du \_ package \_ rejeté**</span><span class="sxs-lookup"><span data-stu-id="d24d9-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="d24d9-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-739">Cette installation est interdite par la stratégie système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="d24d9-740">Contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="d24d9-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**fonction d’erreur \_ \_ non \_ appelée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-742">1626 (0x65A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-743">Impossible d’exécuter la fonction.</span><span class="sxs-lookup"><span data-stu-id="d24d9-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**échec de la fonction d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-745">1627 (0x65B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-746">Échec de la fonction pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d24d9-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**TABLE d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-748">1628 (0x65C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-749">Table spécifiée non valide ou inconnue.</span><span class="sxs-lookup"><span data-stu-id="d24d9-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**incompatibilité de type de données d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-751">1629 (0x65D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-752">Le type des données fournies est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d24d9-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**TYPE d’erreur \_ non pris en charge \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-754">1630 (0x65E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-755">Les données de ce type ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d24d9-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**échec de la création d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-757">1631 (0x65F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-758">Échec du démarrage du service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="d24d9-759">Contactez votre service de support technique.</span><span class="sxs-lookup"><span data-stu-id="d24d9-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERREUR lors de l' \_ installation de \_ temp \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="d24d9-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-762">Le dossier temporaire se trouve sur un lecteur qui est saturé ou inaccessible.</span><span class="sxs-lookup"><span data-stu-id="d24d9-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="d24d9-763">Libérez de l’espace sur le lecteur ou vérifiez que vous disposez de l’autorisation en écriture sur le dossier temporaire.</span><span class="sxs-lookup"><span data-stu-id="d24d9-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERREUR d' \_ installation de \_ plateforme \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="d24d9-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="d24d9-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-766">Ce package d’installation n’est pas pris en charge par ce type de processeur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="d24d9-767">Contactez le fournisseur de votre produit.</span><span class="sxs-lookup"><span data-stu-id="d24d9-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERREUR lors de l' \_ installation de \_ NOTUSED**</span><span class="sxs-lookup"><span data-stu-id="d24d9-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="d24d9-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-770">Composant non utilisé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d24d9-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERREUR \_ échec de l’ouverture du \_ package correctif \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="d24d9-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-773">Impossible d’ouvrir ce package de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d24d9-773">This update package could not be opened.</span></span> <span data-ttu-id="d24d9-774">Vérifiez que le package de mise à jour existe et que vous pouvez y accéder, ou contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de mise à jour Windows Installer valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERREUR \_ de \_ package correctif \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="d24d9-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-777">Impossible d’ouvrir ce package de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d24d9-777">This update package could not be opened.</span></span> <span data-ttu-id="d24d9-778">Contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de mise à jour Windows Installer valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERREUR \_ \_ package correctif \_ non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d24d9-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="d24d9-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-781">Ce package de mise à jour ne peut pas être traité par le service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="d24d9-782">Vous devez installer un Service Pack Windows qui contient une version plus récente du service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_version du produit d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="d24d9-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-785">Une autre version de ce produit est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-785">Another version of this product is already installed.</span></span> <span data-ttu-id="d24d9-786">L’installation de cette version ne peut pas continuer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="d24d9-787">Pour configurer ou supprimer la version existante de ce produit, utilisez Ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d24d9-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERREUR \_ \_ ligne de commande non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="d24d9-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-790">Argument de ligne de commande non valide.</span><span class="sxs-lookup"><span data-stu-id="d24d9-790">Invalid command line argument.</span></span> <span data-ttu-id="d24d9-791">Pour obtenir une aide détaillée sur la ligne de commande, consultez le kit de développement logiciel Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d24d9-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERREUR d' \_ installation \_ distante non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="d24d9-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-794">Seuls les administrateurs ont l’autorisation d’ajouter, de supprimer ou de configurer le logiciel serveur pendant une session à distance des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d24d9-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="d24d9-795">Si vous souhaitez installer ou configurer le logiciel sur le serveur, contactez votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="d24d9-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERREUR \_ de \_ redémarrage de réussite \_ lancée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="d24d9-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-798">L’opération demandée s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d24d9-798">The requested operation completed successfully.</span></span> <span data-ttu-id="d24d9-799">Le système va être redémarré pour que les modifications puissent être prises en compte.</span><span class="sxs-lookup"><span data-stu-id="d24d9-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERREUR de la \_ cible du correctif \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="d24d9-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-801">1642 (0x66A)</span><span class="sxs-lookup"><span data-stu-id="d24d9-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-802">La mise à niveau ne peut pas être installée par le service Windows Installer, car le programme à mettre à niveau est peut-être manquant ou la mise à niveau peut mettre à jour une autre version du programme.</span><span class="sxs-lookup"><span data-stu-id="d24d9-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="d24d9-803">Vérifiez que le programme à mettre à niveau existe sur votre ordinateur et que vous disposez de la mise à niveau appropriée.</span><span class="sxs-lookup"><span data-stu-id="d24d9-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERREUR \_ de \_ rejet du package de correctifs \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-805">1643 (0x66B)</span><span class="sxs-lookup"><span data-stu-id="d24d9-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-806">Le package de mise à jour n’est pas autorisé par la stratégie de restriction logicielle.</span><span class="sxs-lookup"><span data-stu-id="d24d9-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERREUR d’installation de la \_ \_ transformation \_ rejetée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-808">1644 (0x66C)</span><span class="sxs-lookup"><span data-stu-id="d24d9-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-809">Une ou plusieurs personnalisations ne sont pas autorisées par la stratégie de restriction logicielle.</span><span class="sxs-lookup"><span data-stu-id="d24d9-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERREUR \_ d' \_ installation \_ interdite à distance**</span><span class="sxs-lookup"><span data-stu-id="d24d9-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="d24d9-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-812">Le Windows Installer ne permet pas l’installation à partir d’un Connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d24d9-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERREUR \_ de \_ Suppression de correctif \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="d24d9-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="d24d9-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-815">La désinstallation du package de mise à jour n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d24d9-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERREUR \_ de \_ correctif inconnu**</span><span class="sxs-lookup"><span data-stu-id="d24d9-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-817">1647 (0x66F)</span><span class="sxs-lookup"><span data-stu-id="d24d9-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-818">La mise à jour n’est pas appliquée à ce produit.</span><span class="sxs-lookup"><span data-stu-id="d24d9-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**correctif d’erreur- \_ \_ aucune \_ séquence**</span><span class="sxs-lookup"><span data-stu-id="d24d9-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="d24d9-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-821">Aucune séquence valide n’a été trouvée pour l’ensemble de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="d24d9-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERREUR de \_ Suppression de correctif non \_ \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="d24d9-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-824">La suppression de la mise à jour a été interdite par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d24d9-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERREUR \_ de \_ code XML de correctif non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d24d9-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="d24d9-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-827">Les données de mise à jour XML ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d24d9-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERREUR de mise à \_ jour du \_ \_ \_ produit publié**</span><span class="sxs-lookup"><span data-stu-id="d24d9-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="d24d9-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-830">Windows Installer n’autorise pas la mise à jour des produits publiés gérés.</span><span class="sxs-lookup"><span data-stu-id="d24d9-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="d24d9-831">Au moins une fonctionnalité du produit doit être installée avant l’application de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d24d9-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERREUR lors de l' \_ installation du \_ service \_ SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="d24d9-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="d24d9-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-834">Le service Windows Installer n’est pas accessible en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="d24d9-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="d24d9-835">Réessayez si votre ordinateur n’est pas en mode sans échec ou si vous pouvez utiliser la restauration du système pour ramener votre ordinateur à un état correct précédent.</span><span class="sxs-lookup"><span data-stu-id="d24d9-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERREUR d’échec de l' \_ \_ \_ exception rapide**</span><span class="sxs-lookup"><span data-stu-id="d24d9-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="d24d9-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-838">Une exception Fail Fast s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d24d9-838">A fail fast exception occurred.</span></span> <span data-ttu-id="d24d9-839">Les gestionnaires d’exceptions ne sont pas appelés et le processus se termine immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d24d9-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d24d9-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERREUR d' \_ installation \_ rejetée**</span><span class="sxs-lookup"><span data-stu-id="d24d9-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24d9-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="d24d9-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="d24d9-842">L’application que vous essayez d’exécuter n’est pas prise en charge sur cette version de Windows.</span><span class="sxs-lookup"><span data-stu-id="d24d9-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d24d9-843">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d24d9-843">Requirements</span></span>



| <span data-ttu-id="d24d9-844">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d24d9-844">Requirement</span></span> | <span data-ttu-id="d24d9-845">Valeur</span><span class="sxs-lookup"><span data-stu-id="d24d9-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d24d9-846">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d24d9-846">Minimum supported client</span></span><br/> | <span data-ttu-id="d24d9-847">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d24d9-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d24d9-848">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d24d9-848">Minimum supported server</span></span><br/> | <span data-ttu-id="d24d9-849">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d24d9-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d24d9-850">En-tête</span><span class="sxs-lookup"><span data-stu-id="d24d9-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="d24d9-851"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="d24d9-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d24d9-852">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d24d9-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d24d9-853">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="d24d9-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





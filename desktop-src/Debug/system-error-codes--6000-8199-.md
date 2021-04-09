---
description: Décrit les codes d’erreur 6000-8199 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Codes d’erreur système (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861377"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="7c282-103">Codes d’erreur système (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="7c282-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="7c282-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="7c282-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="7c282-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c282-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="7c282-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 6000 à 8199).</span><span class="sxs-lookup"><span data-stu-id="7c282-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="7c282-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="7c282-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="7c282-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="7c282-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="7c282-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**\_échec du chiffrement de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="7c282-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-111">Le fichier spécifié n’a pas pu être chiffré.</span><span class="sxs-lookup"><span data-stu-id="7c282-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_échec du déchiffrement de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="7c282-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-114">Impossible de déchiffrer le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7c282-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**fichier d’erreur \_ \_ chiffré**</span><span class="sxs-lookup"><span data-stu-id="7c282-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="7c282-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-117">Le fichier spécifié est chiffré et l’utilisateur n’a pas la possibilité de le déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="7c282-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERREUR \_ aucune \_ stratégie de récupération \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="7c282-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-120">Aucune stratégie de récupération de chiffrement valide n’est configurée pour ce système.</span><span class="sxs-lookup"><span data-stu-id="7c282-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERREUR \_ non \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="7c282-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="7c282-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-123">Le pilote de chiffrement requis n’est pas chargé pour ce système.</span><span class="sxs-lookup"><span data-stu-id="7c282-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERREUR \_ EFS incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="7c282-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-126">Le fichier a été chiffré avec un autre pilote de chiffrement que celui actuellement chargé.</span><span class="sxs-lookup"><span data-stu-id="7c282-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERREUR \_ aucune \_ \_ clé utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7c282-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="7c282-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-129">Aucune clé EFS n’est définie pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**fichier d’erreur \_ \_ non \_ chiffré**</span><span class="sxs-lookup"><span data-stu-id="7c282-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="7c282-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-132">Le fichier spécifié n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="7c282-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERREUR lors de l' \_ \_ exportation du \_ format**</span><span class="sxs-lookup"><span data-stu-id="7c282-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="7c282-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-135">Le fichier spécifié n’est pas dans le format d’exportation EFS défini.</span><span class="sxs-lookup"><span data-stu-id="7c282-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**fichier d’erreur \_ \_ en lecture \_ seule**</span><span class="sxs-lookup"><span data-stu-id="7c282-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="7c282-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-138">Le fichier spécifié est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7c282-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERREUR dans le \_ répertoire \_ EFS non \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="7c282-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-140">6010 (0x177A)</span><span class="sxs-lookup"><span data-stu-id="7c282-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-141">Le répertoire a été désactivé pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="7c282-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERREUR \_ \_ serveur EFS \_ non \_ approuvé**</span><span class="sxs-lookup"><span data-stu-id="7c282-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-143">6011 (0x177B)</span><span class="sxs-lookup"><span data-stu-id="7c282-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-144">Le serveur n’est pas approuvé pour l’opération de chiffrement à distance.</span><span class="sxs-lookup"><span data-stu-id="7c282-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERREUR \_ de \_ stratégie de récupération incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-146">6012 (0x177C)</span><span class="sxs-lookup"><span data-stu-id="7c282-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-147">La stratégie de récupération configurée pour ce système contient un certificat de récupération non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERREUR \_ EFS \_ ALG \_ \_ trop \_ volumineux**</span><span class="sxs-lookup"><span data-stu-id="7c282-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-149">6013 (0x177D)</span><span class="sxs-lookup"><span data-stu-id="7c282-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-150">L’algorithme de chiffrement utilisé sur le fichier source a besoin d’une mémoire tampon de clé supérieure à celle du fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="7c282-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**le \_ volume d’erreurs \_ ne \_ prend pas en charge \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="7c282-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-152">6014 (0x177E)</span><span class="sxs-lookup"><span data-stu-id="7c282-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-153">La partition de disque ne prend pas en charge le chiffrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="7c282-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERREUR \_ EFS \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7c282-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-155">6015 (0x177F)</span><span class="sxs-lookup"><span data-stu-id="7c282-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-156">Cet ordinateur est désactivé pour le chiffrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="7c282-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERREUR \_ \_ \_ non \_ prise en charge par la version EFS**</span><span class="sxs-lookup"><span data-stu-id="7c282-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="7c282-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-159">Un système plus récent est nécessaire pour déchiffrer ce fichier chiffré.</span><span class="sxs-lookup"><span data-stu-id="7c282-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERREUR \_ de \_ chiffrement de la \_ réponse du serveur non valide \_ \_ CS**</span><span class="sxs-lookup"><span data-stu-id="7c282-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="7c282-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-162">Le serveur distant a envoyé une réponse non valide pour un fichier ouvert avec le chiffrement côté client.</span><span class="sxs-lookup"><span data-stu-id="7c282-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERREUR \_ de \_ chiffrement du \_ serveur non pris en charge par le chiffrement cs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="7c282-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-165">Le chiffrement côté client n’est pas pris en charge par le serveur distant, même s’il prétend le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERREUR \_ du \_ chiffrement du \_ \_ fichier chiffré existant \_ du CS**</span><span class="sxs-lookup"><span data-stu-id="7c282-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="7c282-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-168">Le fichier est chiffré et doit être ouvert en mode de chiffrement côté client.</span><span class="sxs-lookup"><span data-stu-id="7c282-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERREUR \_ cs \_ chiffrement du \_ nouveau \_ \_ fichier chiffré**</span><span class="sxs-lookup"><span data-stu-id="7c282-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="7c282-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-171">Un nouveau fichier chiffré est créé et un $EFS doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="7c282-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERREUR \_ du \_ fichier de chiffrement cs \_ \_ non \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="7c282-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="7c282-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-174">Le client SMB a demandé un FSCTL CSE sur un fichier non-CSE.</span><span class="sxs-lookup"><span data-stu-id="7c282-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**la \_ stratégie de chiffrement des erreurs \_ refuse l' \_ \_ opération**</span><span class="sxs-lookup"><span data-stu-id="7c282-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="7c282-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-177">L’opération demandée a été bloquée par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7c282-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="7c282-178">Pour plus d’informations, contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="7c282-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERREUR \_ aucun \_ serveur de navigateur \_ \_ trouvé**</span><span class="sxs-lookup"><span data-stu-id="7c282-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-180">6118 (0x17E6)</span><span class="sxs-lookup"><span data-stu-id="7c282-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-181">La liste des serveurs de ce groupe de travail n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="7c282-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**\_service sched \_ E \_ non \_ LOCALSYSTEM**</span><span class="sxs-lookup"><span data-stu-id="7c282-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="7c282-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-184">Le service de Planificateur de tâches doit être configuré pour s’exécuter dans le compte système pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="7c282-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="7c282-185">Des tâches individuelles peuvent être configurées pour s’exécuter dans d’autres comptes.</span><span class="sxs-lookup"><span data-stu-id="7c282-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**secteur du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-187">6600 (0x19C8)</span><span class="sxs-lookup"><span data-stu-id="7c282-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-188">Le service de journalisation a rencontré un secteur de journal non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**parité du secteur du journal des erreurs \_ \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-190">6601 (0x19C9)</span><span class="sxs-lookup"><span data-stu-id="7c282-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-191">Le service de journalisation a rencontré un secteur de journal avec parité de bloc non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**Journal des erreurs- \_ \_ secteur \_ remappé**</span><span class="sxs-lookup"><span data-stu-id="7c282-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-193">6602 (0x19CA)</span><span class="sxs-lookup"><span data-stu-id="7c282-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-194">Le service de journalisation a rencontré un secteur de journal remappé.</span><span class="sxs-lookup"><span data-stu-id="7c282-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloc du journal des erreurs \_ \_ \_ incomplet**</span><span class="sxs-lookup"><span data-stu-id="7c282-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-196">6603 (0x19CB)</span><span class="sxs-lookup"><span data-stu-id="7c282-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-197">Le service de journalisation a rencontré un bloc de journal partiel ou incomplet.</span><span class="sxs-lookup"><span data-stu-id="7c282-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ plage non valide du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-199">6604 (0x19CC)</span><span class="sxs-lookup"><span data-stu-id="7c282-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-200">Le service de journalisation a rencontré une tentative d’accès aux données en dehors de la plage de journal active.</span><span class="sxs-lookup"><span data-stu-id="7c282-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**blocs de journal des erreurs \_ \_ \_ épuisés**</span><span class="sxs-lookup"><span data-stu-id="7c282-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-202">6605 (0x19CD)</span><span class="sxs-lookup"><span data-stu-id="7c282-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-203">Les mémoires tampons de tri de l’utilisateur du service de journalisation sont épuisées.</span><span class="sxs-lookup"><span data-stu-id="7c282-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexte de lecture du journal des erreurs \_ \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-205">6606 (0x19CE)</span><span class="sxs-lookup"><span data-stu-id="7c282-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-206">Le service de journalisation a rencontré une tentative de lecture à partir d’une zone de marshaling avec un contexte de lecture non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**redémarrage du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-208">6607 (0x19CF)</span><span class="sxs-lookup"><span data-stu-id="7c282-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-209">Le service de journalisation a rencontré une zone de redémarrage du journal non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_version du \_ bloc du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-211">6608 (0x19D0)</span><span class="sxs-lookup"><span data-stu-id="7c282-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-212">Le service de journalisation a rencontré une version de bloc de journal non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloc du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-214">6609 (0x19D1)</span><span class="sxs-lookup"><span data-stu-id="7c282-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-215">Le service de journalisation a rencontré un bloc de journal non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**MODE de lecture du journal des erreurs \_ \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-217">6610 (0x19D2)</span><span class="sxs-lookup"><span data-stu-id="7c282-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-218">Le service de journalisation a rencontré une tentative de lecture du journal avec un mode de lecture non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**Journal des erreurs- \_ \_ \_ redémarrage non**</span><span class="sxs-lookup"><span data-stu-id="7c282-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-220">6611 (0x19D3)</span><span class="sxs-lookup"><span data-stu-id="7c282-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-221">Le service de journalisation a rencontré un flux de journal sans zone de reprise.</span><span class="sxs-lookup"><span data-stu-id="7c282-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**\_métadonnées du journal des erreurs \_ \_ endommagées**</span><span class="sxs-lookup"><span data-stu-id="7c282-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-223">6612 (0x19D4)</span><span class="sxs-lookup"><span data-stu-id="7c282-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-224">Le service de journalisation a rencontré un fichier de métadonnées endommagé.</span><span class="sxs-lookup"><span data-stu-id="7c282-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**\_métadonnées du journal des erreurs \_ \_ non valides**</span><span class="sxs-lookup"><span data-stu-id="7c282-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-226">6613 (0x19D5)</span><span class="sxs-lookup"><span data-stu-id="7c282-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-227">Le service de journalisation a rencontré un fichier de métadonnées qui n’a pas pu être créé par le système de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="7c282-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**\_métadonnées du journal des erreurs \_ \_ incohérentes**</span><span class="sxs-lookup"><span data-stu-id="7c282-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-229">6614 (0x19D6)</span><span class="sxs-lookup"><span data-stu-id="7c282-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-230">Le service de journalisation a rencontré un fichier de métadonnées avec des données incohérentes.</span><span class="sxs-lookup"><span data-stu-id="7c282-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**réservation du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-232">6615 (0x19D7)</span><span class="sxs-lookup"><span data-stu-id="7c282-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-233">Le service de journalisation a rencontré une tentative d’allocation ou de suppression d’espace de réservation.</span><span class="sxs-lookup"><span data-stu-id="7c282-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**erreur \_ de \_ suppression du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-235">6616 (0x19D8)</span><span class="sxs-lookup"><span data-stu-id="7c282-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-236">Le service de journalisation ne peut pas supprimer le fichier journal ou le conteneur du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c282-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite du conteneur du journal des erreurs \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="7c282-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-238">6617 (0x19D9)</span><span class="sxs-lookup"><span data-stu-id="7c282-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-239">Le service de journalisation a atteint le nombre maximal de conteneurs autorisés alloués à un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**journal \_ des erreurs- \_ début \_ du \_ Journal**</span><span class="sxs-lookup"><span data-stu-id="7c282-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-241">6618 (0x19DA)</span><span class="sxs-lookup"><span data-stu-id="7c282-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-242">Le service de journalisation a tenté de lire ou d’écrire vers l’arrière au-delà du début du journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**stratégie du journal des erreurs \_ \_ \_ déjà \_ installée**</span><span class="sxs-lookup"><span data-stu-id="7c282-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-244">6619 (0x19DB)</span><span class="sxs-lookup"><span data-stu-id="7c282-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-245">La stratégie du journal n’a pas pu être installée car une stratégie du même type est déjà présente.</span><span class="sxs-lookup"><span data-stu-id="7c282-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**stratégie du journal des erreurs \_ \_ \_ non \_ installée**</span><span class="sxs-lookup"><span data-stu-id="7c282-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-247">6620 (0x19DC)</span><span class="sxs-lookup"><span data-stu-id="7c282-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-248">La stratégie de journalisation en question n’a pas été installée au moment de la demande.</span><span class="sxs-lookup"><span data-stu-id="7c282-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**stratégie du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-250">6621 (0x19DD)</span><span class="sxs-lookup"><span data-stu-id="7c282-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-251">Le jeu de stratégies installé sur le journal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflit de \_ stratégie du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-253">6622 (0x19DE)</span><span class="sxs-lookup"><span data-stu-id="7c282-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-254">Une stratégie sur la connexion en question A empêché l’exécution de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c282-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_fin de \_ l' \_ archivage épinglé du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-256">6623 (0x19DF)</span><span class="sxs-lookup"><span data-stu-id="7c282-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-257">Impossible de récupérer l’espace du journal car le journal est épinglé par la fin de l’archivage.</span><span class="sxs-lookup"><span data-stu-id="7c282-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**enregistrement du journal des erreurs \_ \_ \_ inexistant**</span><span class="sxs-lookup"><span data-stu-id="7c282-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-259">6624 (0x19E0)</span><span class="sxs-lookup"><span data-stu-id="7c282-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-260">L’enregistrement du journal n’est pas un enregistrement dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**enregistrements du journal des erreurs \_ \_ \_ réservés \_ non valides**</span><span class="sxs-lookup"><span data-stu-id="7c282-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-262">6625 (0x19E1)</span><span class="sxs-lookup"><span data-stu-id="7c282-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-263">Le nombre d’enregistrements de journal réservés ou l’ajustement du nombre d’enregistrements de journal réservés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**espace du journal des erreurs \_ \_ \_ réservé \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-265">6626 (0x19E2)</span><span class="sxs-lookup"><span data-stu-id="7c282-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-266">L’espace du journal réservé ou la modification de l’espace du journal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**fin du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-268">6627 (0x19E3)</span><span class="sxs-lookup"><span data-stu-id="7c282-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-269">Une fin ou base d’archive nouvelle ou existante du journal actif n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**Journal des erreurs \_ \_ complet**</span><span class="sxs-lookup"><span data-stu-id="7c282-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-271">6628 (0x19E4)</span><span class="sxs-lookup"><span data-stu-id="7c282-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-272">L’espace du journal est épuisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERREUR \_ Impossible \_ de \_ redimensionner le \_ Journal**</span><span class="sxs-lookup"><span data-stu-id="7c282-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-274">6629 (0x19E5)</span><span class="sxs-lookup"><span data-stu-id="7c282-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-275">Le journal n’a pas pu être défini à la taille demandée.</span><span class="sxs-lookup"><span data-stu-id="7c282-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**Journal des erreurs \_ \_ multiplexé**</span><span class="sxs-lookup"><span data-stu-id="7c282-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-277">6630 (0x19E6)</span><span class="sxs-lookup"><span data-stu-id="7c282-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-278">Le journal est multiplexé, aucune écriture directe dans le journal physique n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="7c282-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**Journal des erreurs \_ \_ dédié**</span><span class="sxs-lookup"><span data-stu-id="7c282-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-280">6631 (0x19E7)</span><span class="sxs-lookup"><span data-stu-id="7c282-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-281">L’opération a échoué, car le journal est un journal dédié.</span><span class="sxs-lookup"><span data-stu-id="7c282-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ Archive du journal \_ des erreurs non \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="7c282-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-283">6632 (0x19E8)</span><span class="sxs-lookup"><span data-stu-id="7c282-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-284">L’opération requiert un contexte d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7c282-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ Archive du journal \_ des erreurs en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="7c282-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-286">6633 (0x19E9)</span><span class="sxs-lookup"><span data-stu-id="7c282-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-287">Archivage des journaux en cours.</span><span class="sxs-lookup"><span data-stu-id="7c282-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**Journal des erreurs \_ \_ éphémère**</span><span class="sxs-lookup"><span data-stu-id="7c282-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-289">6634 (0x19EA)</span><span class="sxs-lookup"><span data-stu-id="7c282-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-290">L’opération nécessite un journal non éphémère, mais le journal est éphémère.</span><span class="sxs-lookup"><span data-stu-id="7c282-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**le \_ Journal des erreurs \_ ne dispose pas de \_ suffisamment de \_ conteneurs**</span><span class="sxs-lookup"><span data-stu-id="7c282-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-292">6635 (0x19EB)</span><span class="sxs-lookup"><span data-stu-id="7c282-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-293">Le journal doit avoir au moins deux conteneurs pour pouvoir être lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="7c282-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**Journal des erreurs \_ \_ client \_ déjà \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="7c282-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-295">6636 (0x19EC)</span><span class="sxs-lookup"><span data-stu-id="7c282-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-296">Un client de journal a déjà été inscrit sur le flux.</span><span class="sxs-lookup"><span data-stu-id="7c282-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**Journal des erreurs \_ \_ client \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="7c282-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-298">6637 (0x19ED)</span><span class="sxs-lookup"><span data-stu-id="7c282-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-299">Un client de journal n’a pas été inscrit sur le flux.</span><span class="sxs-lookup"><span data-stu-id="7c282-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ Gestionnaire complet du journal \_ des erreurs en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="7c282-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-301">6638 (0x19EE)</span><span class="sxs-lookup"><span data-stu-id="7c282-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-302">Une demande a déjà été effectuée pour gérer la condition de journal saturé.</span><span class="sxs-lookup"><span data-stu-id="7c282-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_échec de \_ lecture du conteneur du journal des erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-304">6639 (0x19EF)</span><span class="sxs-lookup"><span data-stu-id="7c282-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-305">Le service de journalisation a rencontré une erreur lors de la tentative de lecture d’un conteneur de journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**échec de l’écriture du conteneur du \_ Journal des erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-307">6640 (0x19F0)</span><span class="sxs-lookup"><span data-stu-id="7c282-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-308">Le service de journalisation a rencontré une erreur lors de la tentative d’écriture dans un conteneur de journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**échec de l’ouverture du conteneur du \_ Journal des erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-310">6641 (0x19F1)</span><span class="sxs-lookup"><span data-stu-id="7c282-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-311">Le service de journalisation a rencontré une erreur lors de la tentative d’ouverture d’un conteneur de journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**État du conteneur du journal des erreurs \_ \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-313">6642 (0x19F2)</span><span class="sxs-lookup"><span data-stu-id="7c282-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-314">Le service de journalisation a rencontré un état de conteneur non valide lors de la tentative d’action demandée.</span><span class="sxs-lookup"><span data-stu-id="7c282-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**État du journal des erreurs \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-316">6643 (0x19F3)</span><span class="sxs-lookup"><span data-stu-id="7c282-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-317">Le service de journalisation n’est pas dans l’état approprié pour effectuer une action demandée.</span><span class="sxs-lookup"><span data-stu-id="7c282-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**Journal des erreurs \_ \_ épinglé**</span><span class="sxs-lookup"><span data-stu-id="7c282-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-319">6644 (0x19F4)</span><span class="sxs-lookup"><span data-stu-id="7c282-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-320">Impossible de récupérer l’espace du journal car le journal est épinglé.</span><span class="sxs-lookup"><span data-stu-id="7c282-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_échec du \_ vidage des métadonnées du journal des \_ Erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-322">6645 (0x19F5)</span><span class="sxs-lookup"><span data-stu-id="7c282-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-323">Le vidage des métadonnées du journal a échoué.</span><span class="sxs-lookup"><span data-stu-id="7c282-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**Journal des erreurs- \_ \_ sécurité incohérente \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-325">6646 (0x19F6)</span><span class="sxs-lookup"><span data-stu-id="7c282-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-326">La sécurité du journal et de ses conteneurs est incohérente.</span><span class="sxs-lookup"><span data-stu-id="7c282-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**\_échec du \_ vidage du \_ Journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-328">6647 (0x19F7)</span><span class="sxs-lookup"><span data-stu-id="7c282-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-329">Des enregistrements ont été ajoutés au journal ou des modifications de réservation ont été apportées, mais le journal n’a pas pu être vidé.</span><span class="sxs-lookup"><span data-stu-id="7c282-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ réservation épinglée du journal des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-331">6648 (0x19F8)</span><span class="sxs-lookup"><span data-stu-id="7c282-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-332">Le journal est épinglé en raison d’une réservation consommant la plus grande partie de l’espace du journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="7c282-333">Libérez des enregistrements réservés pour libérer de l’espace.</span><span class="sxs-lookup"><span data-stu-id="7c282-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERREUR \_ de \_ transaction non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-335">6700 (0x1A2C)</span><span class="sxs-lookup"><span data-stu-id="7c282-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-336">Le descripteur de transaction associé à cette opération n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**TRANSACTION d’erreur \_ \_ non \_ active**</span><span class="sxs-lookup"><span data-stu-id="7c282-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-338">6701 (0x1A2D)</span><span class="sxs-lookup"><span data-stu-id="7c282-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-339">L’opération demandée a été effectuée dans le contexte d’une transaction qui n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="7c282-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**demande de transaction d’erreur \_ \_ \_ non \_ valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-341">6702 (0x1A2E)</span><span class="sxs-lookup"><span data-stu-id="7c282-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-342">L’opération demandée n’est pas valide sur l’objet de transaction dans son état actuel.</span><span class="sxs-lookup"><span data-stu-id="7c282-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**TRANSACTION d’erreur \_ \_ non \_ demandée**</span><span class="sxs-lookup"><span data-stu-id="7c282-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-344">6703 (0x1A2F)</span><span class="sxs-lookup"><span data-stu-id="7c282-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-345">L’appelant a appelé une API de réponse, mais la réponse n’est pas attendue car le gestionnaire de la requête n’a pas émis la demande correspondante à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7c282-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**TRANSACTION d’erreur \_ \_ déjà \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="7c282-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="7c282-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-348">Il est trop tard pour effectuer l’opération demandée, car la transaction a déjà été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="7c282-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**TRANSACTION d’erreur \_ \_ déjà \_ validée**</span><span class="sxs-lookup"><span data-stu-id="7c282-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-350">6705 (0x1A31)</span><span class="sxs-lookup"><span data-stu-id="7c282-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-351">Il est trop tard pour effectuer l’opération demandée, car la transaction a déjà été validée.</span><span class="sxs-lookup"><span data-stu-id="7c282-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**\_échec de \_ l’initialisation du gestionnaire de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-353">6706 (0x1A32)</span><span class="sxs-lookup"><span data-stu-id="7c282-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-354">Le gestionnaire de transactions n’a pas pu être initialisé correctement.</span><span class="sxs-lookup"><span data-stu-id="7c282-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="7c282-355">Les opérations traitées ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERREUR \_ RESOURCEMANAGER \_ lecture \_ seule**</span><span class="sxs-lookup"><span data-stu-id="7c282-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-357">6707 (0x1A33)</span><span class="sxs-lookup"><span data-stu-id="7c282-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-358">Le ResourceManager spécifié n’a apporté aucune modification ou mise à jour à la ressource dans le cadre de cette transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**TRANSACTION d’erreur \_ \_ non \_ jointe**</span><span class="sxs-lookup"><span data-stu-id="7c282-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-360">6708 (0x1A34)</span><span class="sxs-lookup"><span data-stu-id="7c282-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-361">Le gestionnaire de ressources a tenté de préparer une transaction qui n’a pas été correctement jointe.</span><span class="sxs-lookup"><span data-stu-id="7c282-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**l’erreur de la \_ transaction \_ supérieure \_ existe**</span><span class="sxs-lookup"><span data-stu-id="7c282-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-363">6709 (0x1A35)</span><span class="sxs-lookup"><span data-stu-id="7c282-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-364">L’objet de transaction a déjà une inscription supérieure, et l’appelant a tenté une opération qui aurait créé un nouveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7c282-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="7c282-365">Seul un enrôlement supérieur est autorisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERREUR \_ le \_ protocole \_ CRM \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="7c282-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-367">6710 (0x1A36)</span><span class="sxs-lookup"><span data-stu-id="7c282-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-368">Le gestionnaire de transactions a essayé d’inscrire un protocole qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7c282-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**échec de la propagation de la transaction d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-370">6711 (0x1A37)</span><span class="sxs-lookup"><span data-stu-id="7c282-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-371">La tentative de propagation de la transaction a échoué.</span><span class="sxs-lookup"><span data-stu-id="7c282-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERREUR \_ de \_ protocole \_ CRM \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-373">6712 (0x1A38)</span><span class="sxs-lookup"><span data-stu-id="7c282-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-374">Le protocole de propagation demandé n’a pas été inscrit en tant que CRM.</span><span class="sxs-lookup"><span data-stu-id="7c282-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**la \_ transaction d’erreur \_ est une \_ mémoire tampon de Marshall non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-376">6713 (0x1A39)</span><span class="sxs-lookup"><span data-stu-id="7c282-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-377">Le format de la mémoire tampon transmise à PushTransaction ou PullTransaction n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERREUR \_ transaction en cours \_ \_ non \_ valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-379">6714 (0x1A3A)</span><span class="sxs-lookup"><span data-stu-id="7c282-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-380">Le contexte de transaction actuel associé au thread n’est pas un handle valide pour un objet de transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_transaction d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-382">6715 (0x1A3B)</span><span class="sxs-lookup"><span data-stu-id="7c282-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-383">Impossible d’ouvrir l’objet de transaction spécifié, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERREUR \_ RESOURCEMANAGER \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-385">6716 (0x1A3C)</span><span class="sxs-lookup"><span data-stu-id="7c282-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-386">Impossible d’ouvrir l’objet ResourceManager spécifié, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**INSCRIPTION d’erreur \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-388">6717 (0x1A3D)</span><span class="sxs-lookup"><span data-stu-id="7c282-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-389">Impossible d’ouvrir l’objet d’inscription spécifié, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERREUR \_ TRANSACTIONMANAGER \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-391">6718 (0x1A3E)</span><span class="sxs-lookup"><span data-stu-id="7c282-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-392">L’objet TransactionManager spécifié n’a pas pu être ouvert, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERREUR \_ TRANSACTIONMANAGER \_ non \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="7c282-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-394">6719 (0x1A3F)</span><span class="sxs-lookup"><span data-stu-id="7c282-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-395">Impossible de créer ou d’ouvrir l’objet spécifié, car son TransactionManager associé n’est pas en ligne.</span><span class="sxs-lookup"><span data-stu-id="7c282-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="7c282-396">Le TransactionManager doit être entièrement en ligne en appelant RecoverTransactionManager pour effectuer une récupération à la fin de son fichier journal avant que les objets de sa transaction ou de ses espaces de noms ResourceManager puissent être ouverts.</span><span class="sxs-lookup"><span data-stu-id="7c282-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="7c282-397">En outre, les erreurs d’écriture d’enregistrements dans son fichier journal peuvent entraîner la mise hors connexion d’un TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="7c282-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERREUR \_ du \_ nom de récupération du TRANSACTIONMANAGER. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-399">6720 (0x1A40)</span><span class="sxs-lookup"><span data-stu-id="7c282-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-400">L’TransactionManager spécifié n’a pas pu créer les objets contenus dans son fichier journal dans l’espace de noms ob.</span><span class="sxs-lookup"><span data-stu-id="7c282-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="7c282-401">Par conséquent, l’TransactionManager n’a pas pu être récupéré.</span><span class="sxs-lookup"><span data-stu-id="7c282-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**TRANSACTION d’erreur \_ \_ non \_ racine**</span><span class="sxs-lookup"><span data-stu-id="7c282-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-403">6721 (0x1A41)</span><span class="sxs-lookup"><span data-stu-id="7c282-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-404">L’appel pour créer une inscription supérieure sur cet objet de transaction n’a pas pu aboutir, car l’objet de transaction spécifié pour l’inscription est une branche subordonnée de la transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="7c282-405">Seule la racine de la transaction peut être inscrite en tant que supérieur.</span><span class="sxs-lookup"><span data-stu-id="7c282-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objet de transaction d’erreur \_ \_ \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="7c282-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-407">6722 (0x1A42)</span><span class="sxs-lookup"><span data-stu-id="7c282-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-408">Étant donné que le gestionnaire de transactions ou le gestionnaire de ressources associé a été fermé, le descripteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**réponse de la transaction d’erreur \_ \_ \_ non \_ inscrite**</span><span class="sxs-lookup"><span data-stu-id="7c282-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-410">6723 (0x1A43)</span><span class="sxs-lookup"><span data-stu-id="7c282-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-411">L’opération spécifiée n’a pas pu être effectuée sur cet enrôlement supérieur, car l’inscription n’a pas été créée avec la réponse d’achèvement correspondante dans le NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="7c282-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**l’enregistrement de la transaction d’erreur est \_ \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="7c282-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-413">6724 (0x1A44)</span><span class="sxs-lookup"><span data-stu-id="7c282-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-414">Impossible d’effectuer l’opération spécifiée, car l’enregistrement qui serait enregistré était trop long.</span><span class="sxs-lookup"><span data-stu-id="7c282-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="7c282-415">Cela peut se produire pour deux raisons : soit il y a trop d’enlistions sur cette transaction, soit le RecoveryInformation combiné qui est enregistré pour le compte de ces enlistions est trop long.</span><span class="sxs-lookup"><span data-stu-id="7c282-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_transaction implicite d’erreur \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="7c282-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-417">6725 (0x1A45)</span><span class="sxs-lookup"><span data-stu-id="7c282-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-418">La transaction implicite n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERREUR d’intégrité de la \_ transaction non \_ \_ respectée**</span><span class="sxs-lookup"><span data-stu-id="7c282-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-420">6726 (0x1A46)</span><span class="sxs-lookup"><span data-stu-id="7c282-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-421">Le gestionnaire de transactions du noyau devait abandonner ou oublier la transaction, car elle a bloqué la progression vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="7c282-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERREUR \_ d' \_ incompatibilité d’identité TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-423">6727 (0x1A47)</span><span class="sxs-lookup"><span data-stu-id="7c282-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-424">L’identité TransactionManager qui a été fournie ne correspondait pas à celle enregistrée dans le fichier journal de l’TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="7c282-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**l’erreur \_ RM \_ ne peut pas \_ être \_ figée \_ pour l' \_ instantané**</span><span class="sxs-lookup"><span data-stu-id="7c282-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-426">6728 (0x1A48)</span><span class="sxs-lookup"><span data-stu-id="7c282-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-427">Cette opération d’instantané ne peut pas continuer, car un gestionnaire de ressources de transaction ne peut pas être figé dans son état actuel.</span><span class="sxs-lookup"><span data-stu-id="7c282-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="7c282-428">Réessayez.</span><span class="sxs-lookup"><span data-stu-id="7c282-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transaction d’erreur \_ doit \_ WRITETHROUGH**</span><span class="sxs-lookup"><span data-stu-id="7c282-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-430">6729 (0x1A49)</span><span class="sxs-lookup"><span data-stu-id="7c282-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-431">La transaction ne peut pas être inscrite dans avec le EnlistmentMask spécifié, car la transaction a déjà terminé la phase de prépréparation.</span><span class="sxs-lookup"><span data-stu-id="7c282-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="7c282-432">Pour garantir l’exactitude, ResourceManager doit basculer vers un mode d’écriture et arrêter la mise en cache des données dans cette transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="7c282-433">L’inscription pour uniquement les phases de transaction suivantes peut encore échouer.</span><span class="sxs-lookup"><span data-stu-id="7c282-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**TRANSACTION d’erreur \_ \_ non \_ supérieure**</span><span class="sxs-lookup"><span data-stu-id="7c282-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-435">6730 (0x1A4A)</span><span class="sxs-lookup"><span data-stu-id="7c282-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-436">La transaction n’a pas d’inscription supérieure.</span><span class="sxs-lookup"><span data-stu-id="7c282-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**erreur heuristique d’erreur d' \_ \_ endommagement \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-438">6731 (0x1A4B)</span><span class="sxs-lookup"><span data-stu-id="7c282-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-439">La tentative de validation de la transaction est terminée, mais il est possible qu’une partie de l’arborescence des transactions n’ait pas été validée en raison de l’heuristique.</span><span class="sxs-lookup"><span data-stu-id="7c282-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="7c282-440">Par conséquent, il est possible que certaines données modifiées dans la transaction ne soient pas validées, ce qui entraîne une incohérence transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="7c282-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="7c282-441">Si possible, vérifiez la cohérence des données associées.</span><span class="sxs-lookup"><span data-stu-id="7c282-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERREUR de \_ conflit transactionnel \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-443">6800 (0x1A90)</span><span class="sxs-lookup"><span data-stu-id="7c282-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-444">La fonction a tenté d’utiliser un nom qui est réservé pour être utilisé par une autre transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERREUR \_ RM \_ non \_ active**</span><span class="sxs-lookup"><span data-stu-id="7c282-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-446">6801 (0x1A91)</span><span class="sxs-lookup"><span data-stu-id="7c282-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-447">La prise en charge des transactions dans le gestionnaire de ressources spécifié n’est pas démarrée ou a été arrêtée en raison d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="7c282-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERREUR \_ de \_ métadonnées RM \_ endommagées**</span><span class="sxs-lookup"><span data-stu-id="7c282-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-449">6802 (0x1A92)</span><span class="sxs-lookup"><span data-stu-id="7c282-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-450">Les métadonnées de la RM ont été endommagées.</span><span class="sxs-lookup"><span data-stu-id="7c282-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="7c282-451">Le RM ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="7c282-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Répertoire d’erreurs \_ \_ non \_ RM**</span><span class="sxs-lookup"><span data-stu-id="7c282-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-453">6803 (0x1A93)</span><span class="sxs-lookup"><span data-stu-id="7c282-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-454">Le répertoire spécifié ne contient pas de gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="7c282-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**TRANSACTIONS d’erreur \_ \_ à distance non prises en charge \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-456">6805 (0x1A95)</span><span class="sxs-lookup"><span data-stu-id="7c282-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-457">Le serveur ou partage distant ne prend pas en charge les opérations de fichiers transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="7c282-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**taille du journal des erreurs \_ \_ \_ taille non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-459">6806 (0x1A96)</span><span class="sxs-lookup"><span data-stu-id="7c282-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-460">La taille de journal demandée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**l' \_ objet d’erreur \_ n' \_ \_ existe plus**</span><span class="sxs-lookup"><span data-stu-id="7c282-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-462">6807 (0x1A97)</span><span class="sxs-lookup"><span data-stu-id="7c282-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-463">L’objet (fichier, flux, lien) correspondant au descripteur a été supprimé par une restauration de point de enregistrement de transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**le \_ flux d’erreurs \_ MINIVERSION est \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-465">6808 (0x1A98)</span><span class="sxs-lookup"><span data-stu-id="7c282-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-466">Le fichier miniversion spécifié est introuvable pour ce fichier Traité ouvert.</span><span class="sxs-lookup"><span data-stu-id="7c282-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**MINIVERSION de flux d’erreurs \_ \_ \_ non \_ valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-468">6809 (0x1A99)</span><span class="sxs-lookup"><span data-stu-id="7c282-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-469">Le fichier spécifié miniversion a été trouvé mais n’a pas été validé.</span><span class="sxs-lookup"><span data-stu-id="7c282-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="7c282-470">La cause la plus probable est la restauration d’un point de enregistrement de transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERREUR \_ MINIVERSION \_ inaccessible \_ à partir de la \_ \_ transaction spécifiée**</span><span class="sxs-lookup"><span data-stu-id="7c282-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-472">6810 (0x1A9A)</span><span class="sxs-lookup"><span data-stu-id="7c282-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-473">Un miniversion peut uniquement être ouvert dans le contexte de la transaction qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="7c282-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERREUR \_ Impossible \_ \_ d’ouvrir \_ MINIVERSION \_ avec \_ intention de modification**</span><span class="sxs-lookup"><span data-stu-id="7c282-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-475">6811 (0x1A9B)</span><span class="sxs-lookup"><span data-stu-id="7c282-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-476">Il n’est pas possible d’ouvrir un miniversion avec l’accès en modification.</span><span class="sxs-lookup"><span data-stu-id="7c282-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERREUR \_ Impossible de \_ créer \_ plus de \_ flux \_ MINIVERSIONS**</span><span class="sxs-lookup"><span data-stu-id="7c282-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-478">6812 (0x1A9C)</span><span class="sxs-lookup"><span data-stu-id="7c282-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-479">Il n’est pas possible de créer d’autres miniversions pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="7c282-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de version de fichier distant \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-481">6814 (0x1A9E)</span><span class="sxs-lookup"><span data-stu-id="7c282-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-482">Le serveur distant a envoyé un numéro de version ou un FID qui ne correspond pas à un fichier ouvert avec des transactions.</span><span class="sxs-lookup"><span data-stu-id="7c282-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**le \_ descripteur d’erreur \_ n' \_ est plus \_ valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-484">6815 (0x1A9F)</span><span class="sxs-lookup"><span data-stu-id="7c282-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-485">Le descripteur a été invalidé par une transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="7c282-486">La cause la plus probable est la présence d’un mappage de mémoire sur un fichier ou d’un descripteur ouvert lorsque la transaction se termine ou est restaurée sur un point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7c282-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERREUR \_ aucune \_ \_ métadonnée TxF**</span><span class="sxs-lookup"><span data-stu-id="7c282-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-488">6816 (0x1AA0)</span><span class="sxs-lookup"><span data-stu-id="7c282-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-489">Il n’y a pas de métadonnées de transaction sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="7c282-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**CORRUPTION du journal des erreurs \_ \_ \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="7c282-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-491">6817 (0x1AA1)</span><span class="sxs-lookup"><span data-stu-id="7c282-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-492">Les données du journal sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="7c282-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERREUR \_ Impossible \_ \_ de récupérer avec le \_ handle \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="7c282-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-494">6818 (0x1AA2)</span><span class="sxs-lookup"><span data-stu-id="7c282-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-495">Impossible de récupérer le fichier, car un descripteur est toujours ouvert dessus.</span><span class="sxs-lookup"><span data-stu-id="7c282-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERREUR \_ RM \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="7c282-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-497">6819 (0x1AA3)</span><span class="sxs-lookup"><span data-stu-id="7c282-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-498">Le résultat de la transaction n’est pas disponible, car le gestionnaire de ressources qui en est responsable s’est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="7c282-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**INSCRIPTION d’erreur \_ \_ non \_ supérieure**</span><span class="sxs-lookup"><span data-stu-id="7c282-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-500">6820 (0x1AA4)</span><span class="sxs-lookup"><span data-stu-id="7c282-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-501">La demande a été rejetée, car l’inscription en question n’est pas une inscription supérieure.</span><span class="sxs-lookup"><span data-stu-id="7c282-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**récupération d’erreur \_ \_ non \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="7c282-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-503">6821 (0x1AA5)</span><span class="sxs-lookup"><span data-stu-id="7c282-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-504">Le gestionnaire de ressources de transaction est déjà cohérent.</span><span class="sxs-lookup"><span data-stu-id="7c282-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="7c282-505">La récupération n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7c282-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERREUR \_ RM \_ déjà \_ démarrée**</span><span class="sxs-lookup"><span data-stu-id="7c282-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-507">6822 (0x1AA6)</span><span class="sxs-lookup"><span data-stu-id="7c282-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-508">Le gestionnaire de ressources de transaction a déjà été démarré.</span><span class="sxs-lookup"><span data-stu-id="7c282-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**l' \_ identité du fichier d’erreur \_ n’est \_ pas \_ persistante**</span><span class="sxs-lookup"><span data-stu-id="7c282-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-510">6823 (0x1AA7)</span><span class="sxs-lookup"><span data-stu-id="7c282-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-511">Impossible d’ouvrir le fichier de façon transactionnelle, car son identité dépend du résultat d’une transaction non résolue.</span><span class="sxs-lookup"><span data-stu-id="7c282-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERREUR \_ Impossible de \_ rompre la \_ \_ dépendance transactionnelle**</span><span class="sxs-lookup"><span data-stu-id="7c282-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-513">6824 (0x1AA8)</span><span class="sxs-lookup"><span data-stu-id="7c282-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-514">L’opération ne peut pas être effectuée, car une autre transaction dépend du fait que cette propriété ne changera pas.</span><span class="sxs-lookup"><span data-stu-id="7c282-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERREUR de déconnexion de la \_ \_ \_ limite inter RM \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-516">6825 (0x1AA9)</span><span class="sxs-lookup"><span data-stu-id="7c282-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-517">L’opération implique un seul fichier avec deux gestionnaires de ressources transactionnels et n’est donc pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERREUR \_ TxF \_ dir \_ non \_ vide**</span><span class="sxs-lookup"><span data-stu-id="7c282-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-519">6826 (0x1AAA)</span><span class="sxs-lookup"><span data-stu-id="7c282-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-520">Le répertoire de $Txf doit être vide pour que cette opération aboutisse.</span><span class="sxs-lookup"><span data-stu-id="7c282-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**des \_ transactions INCERTAINES erronées \_ \_ existent**</span><span class="sxs-lookup"><span data-stu-id="7c282-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-522">6827 (0x1AAB)</span><span class="sxs-lookup"><span data-stu-id="7c282-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-523">L’opération laisse un gestionnaire de ressources transactionnelles dans un état incohérent et n’est donc pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERREUR du gestionnaire de mémoire \_ \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="7c282-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-525">6828 (0x1AAC)</span><span class="sxs-lookup"><span data-stu-id="7c282-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-526">L’opération n’a pas pu aboutir car le gestionnaire de transactions n’a pas de journal.</span><span class="sxs-lookup"><span data-stu-id="7c282-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERREUR de restauration de la \_ \_ minuterie \_ expirée**</span><span class="sxs-lookup"><span data-stu-id="7c282-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-528">6829 (0x1AAD)</span><span class="sxs-lookup"><span data-stu-id="7c282-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-529">Une restauration n’a pas pu être planifiée, car une restauration précédemment planifiée a déjà été exécutée ou a été mise en file d’attente pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7c282-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERREUR de l' \_ \_ attribut TxF \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="7c282-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-531">6830 (0x1AAE)</span><span class="sxs-lookup"><span data-stu-id="7c282-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-532">L’attribut de métadonnées transactionnelles sur le fichier ou le répertoire est endommagé et illisible.</span><span class="sxs-lookup"><span data-stu-id="7c282-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERREUR \_ EFS \_ non \_ autorisée \_ dans la \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-534">6831 (0x1AAF)</span><span class="sxs-lookup"><span data-stu-id="7c282-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-535">L’opération de chiffrement n’a pas pu aboutir car une transaction est active.</span><span class="sxs-lookup"><span data-stu-id="7c282-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERREUR \_ transaction \_ Open \_ non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="7c282-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-537">6832 (0x1AB0)</span><span class="sxs-lookup"><span data-stu-id="7c282-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-538">Cet objet ne peut pas être ouvert dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**échec de la croissance du journal des erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-540">6833 (0x1AB1)</span><span class="sxs-lookup"><span data-stu-id="7c282-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-541">Une tentative de création d’espace dans le journal du gestionnaire des ressources transactionnelles a échoué.</span><span class="sxs-lookup"><span data-stu-id="7c282-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="7c282-542">L’état de l’échec a été enregistré dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="7c282-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERREUR de \_ mappage des transactions \_ \_ distantes non prises en charge \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-544">6834 (0x1AB2)</span><span class="sxs-lookup"><span data-stu-id="7c282-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-545">Le mappage de mémoire (création d’une section mappée) d’un fichier distant sous une transaction n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERREUR \_ de \_ métadonnées TxF \_ déjà \_ présentes**</span><span class="sxs-lookup"><span data-stu-id="7c282-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-547">6835 (0x1AB3)</span><span class="sxs-lookup"><span data-stu-id="7c282-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-548">Les métadonnées de transaction sont déjà présentes dans ce fichier et ne peuvent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="7c282-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_rappels d’étendue de transaction d’erreur \_ \_ \_ non \_ définis**</span><span class="sxs-lookup"><span data-stu-id="7c282-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-550">6836 (0x1AB4)</span><span class="sxs-lookup"><span data-stu-id="7c282-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-551">Une étendue de transaction n’a pas pu être entrée, car le gestionnaire de portée n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**PROMOTION de la transaction d’erreur \_ \_ requise \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-553">6837 (0x1AB5)</span><span class="sxs-lookup"><span data-stu-id="7c282-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-554">La promotion était nécessaire pour permettre à Resource Manager de s’inscrire, mais la transaction a été définie pour l’interdire.</span><span class="sxs-lookup"><span data-stu-id="7c282-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERREUR \_ Impossible \_ d’exécuter le \_ fichier \_ dans la \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-556">6838 (0x1AB6)</span><span class="sxs-lookup"><span data-stu-id="7c282-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-557">Ce fichier est ouvert pour modification dans une transaction non résolue et peut être ouvert pour une exécution uniquement par un lecteur traité.</span><span class="sxs-lookup"><span data-stu-id="7c282-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**TRANSACTIONS d’erreur \_ \_ non \_ figées**</span><span class="sxs-lookup"><span data-stu-id="7c282-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-559">6839 (0x1AB7)</span><span class="sxs-lookup"><span data-stu-id="7c282-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-560">La demande de libération des transactions gelées a été ignorée, car les transactions n’avaient pas été figées précédemment.</span><span class="sxs-lookup"><span data-stu-id="7c282-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**\_ \_ blocage de la transaction d’erreur \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="7c282-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-562">6840 (0x1AB8)</span><span class="sxs-lookup"><span data-stu-id="7c282-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-563">Les transactions ne peuvent pas être figées, car un blocage est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="7c282-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERREUR \_ non \_ snapshot du \_ volume**</span><span class="sxs-lookup"><span data-stu-id="7c282-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-565">6841 (0x1AB9)</span><span class="sxs-lookup"><span data-stu-id="7c282-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-566">Le volume cible n’est pas un volume d’instantané.</span><span class="sxs-lookup"><span data-stu-id="7c282-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="7c282-567">Cette opération n’est valide que sur un volume monté en tant qu’instantané.</span><span class="sxs-lookup"><span data-stu-id="7c282-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERREUR \_ aucun \_ point \_ de enregistrement avec les \_ \_ fichiers ouverts**</span><span class="sxs-lookup"><span data-stu-id="7c282-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-569">6842 (0x1ABA)</span><span class="sxs-lookup"><span data-stu-id="7c282-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-570">L’opération de point d’enregistrement a échoué car des fichiers sont ouverts sur la transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="7c282-571">Cela n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERREUR de \_ réparation de données \_ perdues \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-573">6843 (0x1ABB)</span><span class="sxs-lookup"><span data-stu-id="7c282-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-574">Windows a détecté une corruption dans un fichier, et ce fichier a été réparé depuis.</span><span class="sxs-lookup"><span data-stu-id="7c282-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="7c282-575">Une perte de données est peut-être survenue.</span><span class="sxs-lookup"><span data-stu-id="7c282-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERREUR \_ épars \_ non \_ autorisée \_ dans la \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-577">6844 (0x1ABC)</span><span class="sxs-lookup"><span data-stu-id="7c282-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-578">L’opération éparse n’a pas pu aboutir car une transaction est active sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="7c282-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de l’identité du gestionnaire \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-580">6845 (0x1ABD)</span><span class="sxs-lookup"><span data-stu-id="7c282-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-581">L’appel pour créer un objet TransactionManager a échoué, car l’identité de TM stockée dans le fichier journal ne correspond pas à l’identité TM qui a été transmise en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="7c282-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERREUR de \_ section flottante \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-583">6846 (0x1ABE)</span><span class="sxs-lookup"><span data-stu-id="7c282-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-584">Des e/s ont été tentées sur un objet de section qui a été dissocié à la suite d’une transaction se terminant.</span><span class="sxs-lookup"><span data-stu-id="7c282-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="7c282-585">Il n’y a pas de données valides.</span><span class="sxs-lookup"><span data-stu-id="7c282-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**l’erreur \_ ne peut pas \_ accepter le \_ \_ travail traité**</span><span class="sxs-lookup"><span data-stu-id="7c282-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-587">6847 (0x1ABF)</span><span class="sxs-lookup"><span data-stu-id="7c282-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-588">Le gestionnaire de ressources transactionnelles ne peut pas actuellement accepter le travail transactionnel en raison d’une condition temporaire telle que des ressources insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="7c282-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERREUR \_ Impossible d' \_ abandonner les \_ transactions**</span><span class="sxs-lookup"><span data-stu-id="7c282-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-590">6848 (0x1AC0)</span><span class="sxs-lookup"><span data-stu-id="7c282-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-591">Le gestionnaire de ressources de transaction a trop d’transactions en suspens qui n’ont pas pu être abandonnés.</span><span class="sxs-lookup"><span data-stu-id="7c282-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="7c282-592">Le gestionnaire de ressources de transaction a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="7c282-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERREUR \_ de \_ clusters incorrects**</span><span class="sxs-lookup"><span data-stu-id="7c282-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-594">6849 (0x1AC1)</span><span class="sxs-lookup"><span data-stu-id="7c282-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-595">L’opération n’a pas pu aboutir en raison de clusters incorrects sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7c282-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_compression \_ d’erreur non \_ autorisée dans la \_ \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-597">6850 (0x1AC2)</span><span class="sxs-lookup"><span data-stu-id="7c282-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-598">L’opération de compression n’a pas pu aboutir car une transaction est active sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="7c282-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**\_intégrité du volume d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-600">6851 (0x1AC3)</span><span class="sxs-lookup"><span data-stu-id="7c282-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-601">L’opération n’a pas pu aboutir car le volume est impropre.</span><span class="sxs-lookup"><span data-stu-id="7c282-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="7c282-602">Exécutez CHKDSK et réessayez.</span><span class="sxs-lookup"><span data-stu-id="7c282-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERREUR \_ aucun \_ \_ suivi \_ de lien dans la \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-604">6852 (0x1AC4)</span><span class="sxs-lookup"><span data-stu-id="7c282-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-605">Impossible d’effectuer l’opération de suivi des liaisons, car une transaction est active.</span><span class="sxs-lookup"><span data-stu-id="7c282-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_l’opération \_ d’erreur n’est pas \_ prise en charge \_ dans la \_ transaction**</span><span class="sxs-lookup"><span data-stu-id="7c282-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-607">6853 (0x1AC5)</span><span class="sxs-lookup"><span data-stu-id="7c282-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-608">Cette opération ne peut pas être effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERREUR \_ de \_ handle expiré**</span><span class="sxs-lookup"><span data-stu-id="7c282-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-610">6854 (0x1AC6)</span><span class="sxs-lookup"><span data-stu-id="7c282-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-611">Le descripteur n’est plus correctement associé à sa transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="7c282-612">Il a peut-être été ouvert dans un gestionnaire de ressources de transaction qui a été ensuite forcé à redémarrer.</span><span class="sxs-lookup"><span data-stu-id="7c282-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="7c282-613">Fermez le descripteur et ouvrez-en un nouveau.</span><span class="sxs-lookup"><span data-stu-id="7c282-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**TRANSACTION d’erreur \_ \_ non \_ inscrite**</span><span class="sxs-lookup"><span data-stu-id="7c282-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-615">6855 (0x1AC7)</span><span class="sxs-lookup"><span data-stu-id="7c282-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-616">Impossible d’effectuer l’opération spécifiée, car le gestionnaire de ressources n’est pas inscrit dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="7c282-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERREUR \_ nom de la \_ station de \_ nom \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-618">7001 (0x1B59)</span><span class="sxs-lookup"><span data-stu-id="7c282-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-619">Le nom de session spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERREUR \_ CTX \_ le \_ PD non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-621">7002 (0x1B5A)</span><span class="sxs-lookup"><span data-stu-id="7c282-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-622">Le pilote de protocole spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERREUR \_ CTX \_ PD \_ non \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="7c282-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-624">7003 (0x1B5B)</span><span class="sxs-lookup"><span data-stu-id="7c282-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-625">Le pilote de protocole spécifié est introuvable dans le chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="7c282-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERREUR \_ CTX \_ WD \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-627">7004 (0x1B5C)</span><span class="sxs-lookup"><span data-stu-id="7c282-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-628">Le pilote de connexion de terminal spécifié est introuvable dans le chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="7c282-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERREUR \_ CTX \_ Impossible de \_ créer l' \_ \_ entrée EventLog**</span><span class="sxs-lookup"><span data-stu-id="7c282-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-630">7005 (0x1B5D)</span><span class="sxs-lookup"><span data-stu-id="7c282-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-631">Impossible de créer une clé de Registre pour la journalisation des événements pour cette session.</span><span class="sxs-lookup"><span data-stu-id="7c282-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERREUR \_ de \_ \_ collision de nom de service CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-633">7006 (0x1B5E)</span><span class="sxs-lookup"><span data-stu-id="7c282-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-634">Un service du même nom existe déjà sur le système.</span><span class="sxs-lookup"><span data-stu-id="7c282-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERREUR \_ CTX \_ fermeture \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="7c282-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-636">7007 (0x1B5F)</span><span class="sxs-lookup"><span data-stu-id="7c282-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-637">Une opération de fermeture est en attente sur la session.</span><span class="sxs-lookup"><span data-stu-id="7c282-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERREUR \_ CTX \_ non \_ OUTBUF**</span><span class="sxs-lookup"><span data-stu-id="7c282-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-639">7008 (0x1B60)</span><span class="sxs-lookup"><span data-stu-id="7c282-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-640">Aucune mémoire tampon de sortie libre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="7c282-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERREUR \_ de \_ modem CTX \_ fichier INF \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-642">7009 (0x1B61)</span><span class="sxs-lookup"><span data-stu-id="7c282-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-643">Le MODEM. Fichier INF introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERREUR \_ CTX \_ MODEMNAME non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-645">7010 (0x1B62)</span><span class="sxs-lookup"><span data-stu-id="7c282-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-646">Le nom du modem est introuvable dans le fichier MODEM. INF.</span><span class="sxs-lookup"><span data-stu-id="7c282-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**erreur \_ de \_ réponse du modem CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-648">7011 (0x1B63)</span><span class="sxs-lookup"><span data-stu-id="7c282-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-649">Le modem n’a pas accepté la commande qui lui a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="7c282-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="7c282-650">Vérifiez que le nom du modem configuré correspond au modem attaché.</span><span class="sxs-lookup"><span data-stu-id="7c282-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERREUR \_ de \_ \_ réponse \_ du modem CTX**</span><span class="sxs-lookup"><span data-stu-id="7c282-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-652">7012 (0x1B64)</span><span class="sxs-lookup"><span data-stu-id="7c282-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-653">Le modem n’a pas répondu à la commande qui lui a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="7c282-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="7c282-654">Vérifiez que le modem est correctement câblé et sous tension.</span><span class="sxs-lookup"><span data-stu-id="7c282-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_ non \_ transporteur**</span><span class="sxs-lookup"><span data-stu-id="7c282-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-656">7013 (0x1B65)</span><span class="sxs-lookup"><span data-stu-id="7c282-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-657">La détection de porteuse a échoué ou le transporteur a été abandonné en raison d’une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="7c282-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERREUR \_ de \_ réponse du modem CTX \_ pas de \_ \_ tonalité**</span><span class="sxs-lookup"><span data-stu-id="7c282-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-659">7014 (0x1B66)</span><span class="sxs-lookup"><span data-stu-id="7c282-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-660">Tonalité non détectée dans le délai imparti.</span><span class="sxs-lookup"><span data-stu-id="7c282-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="7c282-661">Vérifiez que le câble téléphonique est correctement attaché et fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="7c282-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_ occupée**</span><span class="sxs-lookup"><span data-stu-id="7c282-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-663">7015 (0x1B67)</span><span class="sxs-lookup"><span data-stu-id="7c282-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-664">Signal occupé détecté sur le site distant lors du rappel.</span><span class="sxs-lookup"><span data-stu-id="7c282-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-666">7016 (0x1B68)</span><span class="sxs-lookup"><span data-stu-id="7c282-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-667">Voix détectée sur le site distant lors du rappel.</span><span class="sxs-lookup"><span data-stu-id="7c282-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**erreur de l’erreur \_ CTX \_ TD \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-669">7017 (0x1B69)</span><span class="sxs-lookup"><span data-stu-id="7c282-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-670">Erreur du pilote de transport.</span><span class="sxs-lookup"><span data-stu-id="7c282-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERREUR \_ CTX \_ station \_ de \_ recherche introuvable**</span><span class="sxs-lookup"><span data-stu-id="7c282-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-672">7022 (0x1B6E)</span><span class="sxs-lookup"><span data-stu-id="7c282-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-673">La session spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7c282-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**une erreur de la \_ \_ station de terminal CTX \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="7c282-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-675">7023 (0x1B6F)</span><span class="sxs-lookup"><span data-stu-id="7c282-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-676">Le nom de session spécifié est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c282-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERREUR CTX de la station de l' \_ \_ \_ activité**</span><span class="sxs-lookup"><span data-stu-id="7c282-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-678">7024 (0x1B70)</span><span class="sxs-lookup"><span data-stu-id="7c282-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-679">La tâche que vous essayez d’effectuer ne peut pas être effectuée car Services Bureau à distance est actuellement occupé.</span><span class="sxs-lookup"><span data-stu-id="7c282-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="7c282-680">Réessayez dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="7c282-680">Please try again in a few minutes.</span></span> <span data-ttu-id="7c282-681">Les autres utilisateurs doivent toujours être en mesure d’ouvrir une session.</span><span class="sxs-lookup"><span data-stu-id="7c282-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERREUR \_ CTX \_ \_ mode vidéo incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-683">7025 (0x1B71)</span><span class="sxs-lookup"><span data-stu-id="7c282-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-684">Une tentative a été effectuée pour se connecter à une session dont le mode vidéo n’est pas pris en charge par le client actuel.</span><span class="sxs-lookup"><span data-stu-id="7c282-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERREUR \_ \_ graphiques CTX \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-686">7035 (0x1B7B)</span><span class="sxs-lookup"><span data-stu-id="7c282-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-687">L’application a essayé d’activer le mode graphique DOS.</span><span class="sxs-lookup"><span data-stu-id="7c282-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="7c282-688">Le mode graphique DOS n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERREUR \_ \_ d’ouverture de session CTX \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7c282-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-690">7037 (0x1B7D)</span><span class="sxs-lookup"><span data-stu-id="7c282-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-691">Votre privilège d’ouverture de session interactive a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="7c282-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="7c282-692">Contactez l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERREUR \_ CTX \_ non \_ console**</span><span class="sxs-lookup"><span data-stu-id="7c282-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-694">7038 (0x1B7E)</span><span class="sxs-lookup"><span data-stu-id="7c282-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-695">L’opération demandée ne peut être effectuée que sur la console système.</span><span class="sxs-lookup"><span data-stu-id="7c282-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="7c282-696">C’est généralement le résultat d’un pilote ou d’une DLL système nécessitant un accès direct à la console.</span><span class="sxs-lookup"><span data-stu-id="7c282-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERREUR \_ d’expiration de la \_ requête cliente CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-698">7040 (0x1B80)</span><span class="sxs-lookup"><span data-stu-id="7c282-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-699">Le client n’a pas pu répondre au message de connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="7c282-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERREUR \_ de \_ déconnexion de la console CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-701">7041 (0x1B81)</span><span class="sxs-lookup"><span data-stu-id="7c282-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-702">La déconnexion de la session de la console n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERREUR de connexion à la \_ \_ console CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-704">7042 (0x1B82)</span><span class="sxs-lookup"><span data-stu-id="7c282-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-705">La reconnexion d’une session déconnectée à la console n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERREUR de l' \_ \_ ombre CTX \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="7c282-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-707">7044 (0x1B84)</span><span class="sxs-lookup"><span data-stu-id="7c282-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-708">La demande de contrôle d’une autre session à distance a été refusée.</span><span class="sxs-lookup"><span data-stu-id="7c282-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERREUR \_ de \_ \_ l’accès à la station de message CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-710">7045 (0x1B85)</span><span class="sxs-lookup"><span data-stu-id="7c282-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-711">L’accès à la session demandé est refusé.</span><span class="sxs-lookup"><span data-stu-id="7c282-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERREUR \_ CTX \_ WD non valide \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-713">7049 (0x1B89)</span><span class="sxs-lookup"><span data-stu-id="7c282-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-714">Le pilote de connexion Terminal Server spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERREUR de l' \_ \_ ombre CTX \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-716">7050 (0x1B8A)</span><span class="sxs-lookup"><span data-stu-id="7c282-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-717">La session demandée ne peut pas être contrôlée à distance.</span><span class="sxs-lookup"><span data-stu-id="7c282-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="7c282-718">Cela peut être dû au fait que la session est déconnectée ou qu’aucun utilisateur n’est actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="7c282-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERREUR de l' \_ \_ ombre CTX \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7c282-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-720">7051 (0x1B8B)</span><span class="sxs-lookup"><span data-stu-id="7c282-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-721">La session demandée n’est pas configurée pour autoriser le contrôle à distance.</span><span class="sxs-lookup"><span data-stu-id="7c282-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERREUR \_ \_ \_ de licence client CTX \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="7c282-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-723">7052 (0x1B8C)</span><span class="sxs-lookup"><span data-stu-id="7c282-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-724">Votre demande de connexion à ce Terminal Server a été rejetée.</span><span class="sxs-lookup"><span data-stu-id="7c282-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="7c282-725">Votre numéro de licence client Terminal Server est actuellement utilisé par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="7c282-726">Contactez votre administrateur système pour obtenir un numéro de licence unique.</span><span class="sxs-lookup"><span data-stu-id="7c282-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERREUR de la \_ \_ licence client CTX \_ \_ non \_ définie**</span><span class="sxs-lookup"><span data-stu-id="7c282-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-728">7053 (0x1B8D)</span><span class="sxs-lookup"><span data-stu-id="7c282-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-729">Votre demande de connexion à ce Terminal Server a été rejetée.</span><span class="sxs-lookup"><span data-stu-id="7c282-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="7c282-730">Votre numéro de licence client Terminal Server n’a pas été entré pour cette copie du client Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="7c282-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="7c282-731">Contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="7c282-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERREUR \_ de \_ licence CTX \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="7c282-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-733">7054 (0x1B8E)</span><span class="sxs-lookup"><span data-stu-id="7c282-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-734">Le nombre de connexions à cet ordinateur est limité et toutes les connexions sont actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="7c282-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="7c282-735">Essayez de vous connecter ultérieurement ou contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="7c282-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERREUR \_ de \_ licence CTX \_ client \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="7c282-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-737">7055 (0x1B8F)</span><span class="sxs-lookup"><span data-stu-id="7c282-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-738">Le client que vous utilisez n’a pas de licence d’utilisation de ce système.</span><span class="sxs-lookup"><span data-stu-id="7c282-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="7c282-739">Votre demande d’ouverture de session est refusée.</span><span class="sxs-lookup"><span data-stu-id="7c282-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERREUR d’expiration de la \_ \_ licence CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-741">7056 (0x1B90)</span><span class="sxs-lookup"><span data-stu-id="7c282-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-742">La licence du système a expiré.</span><span class="sxs-lookup"><span data-stu-id="7c282-742">The system license has expired.</span></span> <span data-ttu-id="7c282-743">Votre demande d’ouverture de session est refusée.</span><span class="sxs-lookup"><span data-stu-id="7c282-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERREUR de l' \_ \_ ombre CTX \_ non \_ exécutée**</span><span class="sxs-lookup"><span data-stu-id="7c282-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-745">7057 (0x1B91)</span><span class="sxs-lookup"><span data-stu-id="7c282-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-746">Impossible d’arrêter le contrôle à distance, car la session spécifiée n’est pas actuellement contrôlée à distance.</span><span class="sxs-lookup"><span data-stu-id="7c282-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**erreur \_ lors \_ de \_ la \_ \_ modification du mode par l’ombre \_ CTX**</span><span class="sxs-lookup"><span data-stu-id="7c282-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-748">7058 (0x1B92)</span><span class="sxs-lookup"><span data-stu-id="7c282-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-749">Le contrôle à distance de la console a été interrompu, car le mode d’affichage a été modifié.</span><span class="sxs-lookup"><span data-stu-id="7c282-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="7c282-750">La modification du mode d’affichage dans une session de contrôle à distance n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7c282-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_nombre d’activations d’erreur \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="7c282-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-752">7059 (0x1B93)</span><span class="sxs-lookup"><span data-stu-id="7c282-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-753">L’activation a déjà été réinitialisée le nombre maximal de fois pour cette installation.</span><span class="sxs-lookup"><span data-stu-id="7c282-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="7c282-754">Votre minuteur d’activation n’est pas effacé.</span><span class="sxs-lookup"><span data-stu-id="7c282-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERREUR \_ CTX \_ WINSTATIONS \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="7c282-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-756">7060 (0x1B94)</span><span class="sxs-lookup"><span data-stu-id="7c282-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-757">Les connexions distantes sont actuellement désactivées.</span><span class="sxs-lookup"><span data-stu-id="7c282-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERREUR \_ \_ niveau de chiffrement CTX \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="7c282-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-759">7061 (0x1B95)</span><span class="sxs-lookup"><span data-stu-id="7c282-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-760">Vous ne disposez pas du niveau de chiffrement approprié pour accéder à cette session.</span><span class="sxs-lookup"><span data-stu-id="7c282-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERREUR \_ \_ de session CTX \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="7c282-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-762">7062 (0x1B96)</span><span class="sxs-lookup"><span data-stu-id="7c282-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-763">L’utilisateur% s \\ \\ % s est actuellement connecté à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="7c282-764">Seul l’utilisateur actuel ou un administrateur peut se connecter à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERREUR \_ CTX \_ non \_ forcer la \_ fermeture de session**</span><span class="sxs-lookup"><span data-stu-id="7c282-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-766">7063 (0x1B97)</span><span class="sxs-lookup"><span data-stu-id="7c282-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-767">L’utilisateur% s \\ \\ % s est déjà connecté à la console de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="7c282-768">Vous n’êtes pas autorisé à vous connecter pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7c282-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="7c282-769">Pour résoudre ce problème, contactez% s \\ \\ % s et demandez-leur de fermer la session.</span><span class="sxs-lookup"><span data-stu-id="7c282-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERREUR \_ de \_ restriction de compte CTX \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-771">7064 (0x1B98)</span><span class="sxs-lookup"><span data-stu-id="7c282-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-772">Impossible de vous connecter en raison d’une restriction de compte.</span><span class="sxs-lookup"><span data-stu-id="7c282-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**erreur \_ de \_ protocole \_ RDP**</span><span class="sxs-lookup"><span data-stu-id="7c282-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-774">7065 (0x1B99)</span><span class="sxs-lookup"><span data-stu-id="7c282-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-775">Le composant de protocole RDP %2 a détecté une erreur dans le flux de protocole et a déconnecté le client.</span><span class="sxs-lookup"><span data-stu-id="7c282-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERREUR \_ CTX \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="7c282-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-777">7066 (0x1B9A)</span><span class="sxs-lookup"><span data-stu-id="7c282-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-778">Le service de mappage de lecteur client s’est connecté à la connexion de terminal.</span><span class="sxs-lookup"><span data-stu-id="7c282-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERREUR \_ de \_ \_ déconnexion de CTX**</span><span class="sxs-lookup"><span data-stu-id="7c282-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-780">7067 (0x1B9B)</span><span class="sxs-lookup"><span data-stu-id="7c282-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-781">Le service de mappage de lecteur client s’est déconnecté de la connexion de terminal.</span><span class="sxs-lookup"><span data-stu-id="7c282-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**erreur \_ de \_ couche de sécurité CTX \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-783">7068 (0x1B9C)</span><span class="sxs-lookup"><span data-stu-id="7c282-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-784">La couche de sécurité Terminal Server a détecté une erreur dans le flux de protocole et a déconnecté le client.</span><span class="sxs-lookup"><span data-stu-id="7c282-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERREUR \_ de \_ sessions incompatibles TS \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-786">7069 (0x1B9D)</span><span class="sxs-lookup"><span data-stu-id="7c282-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-787">La session cible est incompatible avec la session active.</span><span class="sxs-lookup"><span data-stu-id="7c282-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**erreur \_ de \_ \_ sous-système d’erreur TS vidéo \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-789">7070 (0x1B9E)</span><span class="sxs-lookup"><span data-stu-id="7c282-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-790">Windows ne peut pas se connecter à votre session, car un problème s’est produit dans le sous-système vidéo Windows.</span><span class="sxs-lookup"><span data-stu-id="7c282-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="7c282-791">Essayez de vous reconnecter ultérieurement, ou contactez l’administrateur du serveur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="7c282-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_séquence d' \_ API non valide de l’erreur FRS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-793">8001 (0x1F41)</span><span class="sxs-lookup"><span data-stu-id="7c282-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-794">L’API du service de réplication de fichiers a été appelée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="7c282-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_service de \_ démarrage d’Err FRS \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-796">8002 (0x1F42)</span><span class="sxs-lookup"><span data-stu-id="7c282-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-797">Impossible de démarrer le service de réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c282-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_service d' \_ arrêt d’erreur FRS \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-799">8003 (0x1F43)</span><span class="sxs-lookup"><span data-stu-id="7c282-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-800">Impossible d’arrêter le service de réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c282-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interne FRS \_ Err**</span><span class="sxs-lookup"><span data-stu-id="7c282-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-802">8004 (0x1F44)</span><span class="sxs-lookup"><span data-stu-id="7c282-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-803">L’API du service de réplication de fichiers a mis fin à la requête.</span><span class="sxs-lookup"><span data-stu-id="7c282-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="7c282-804">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_erreur FRS \_ interne**</span><span class="sxs-lookup"><span data-stu-id="7c282-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-806">8005 (0x1F45)</span><span class="sxs-lookup"><span data-stu-id="7c282-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-807">Le service de réplication de fichiers a mis fin à la requête.</span><span class="sxs-lookup"><span data-stu-id="7c282-807">The file replication service terminated the request.</span></span> <span data-ttu-id="7c282-808">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_ \_ comm service FRS \_ Err**</span><span class="sxs-lookup"><span data-stu-id="7c282-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-810">8006 (0x1F46)</span><span class="sxs-lookup"><span data-stu-id="7c282-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-811">Impossible de contacter le service de réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c282-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="7c282-812">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**\_erreur FRS \_ insuffisante \_ priv**</span><span class="sxs-lookup"><span data-stu-id="7c282-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-814">8007 (0x1F47)</span><span class="sxs-lookup"><span data-stu-id="7c282-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-815">Le service de réplication de fichiers ne peut pas satisfaire la requête, car l’utilisateur ne dispose pas de privilèges suffisants.</span><span class="sxs-lookup"><span data-stu-id="7c282-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="7c282-816">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**authentification FRS de \_ \_ l’erreur**</span><span class="sxs-lookup"><span data-stu-id="7c282-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-818">8008 (0x1F48)</span><span class="sxs-lookup"><span data-stu-id="7c282-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-819">Le service de réplication de fichiers ne peut pas satisfaire la requête, car le RPC authentifié n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7c282-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="7c282-820">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**le parent de l’Err FRS est \_ \_ \_ insuffisant \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-822">8009 (0x1F49)</span><span class="sxs-lookup"><span data-stu-id="7c282-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-823">Le service de réplication de fichiers ne peut pas satisfaire la requête, car l’utilisateur ne dispose pas de privilèges suffisants sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="7c282-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="7c282-824">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ authentification parente Err FRS \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-826">8010 (0x1F4A)</span><span class="sxs-lookup"><span data-stu-id="7c282-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-827">Le service de réplication de fichiers ne peut pas satisfaire la requête, car le RPC authentifié n’est pas disponible sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="7c282-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="7c282-828">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**réplication \_ \_ d’un enfant Err vers un \_ \_ \_ comm parent**</span><span class="sxs-lookup"><span data-stu-id="7c282-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-830">8011 (0x1F4B)</span><span class="sxs-lookup"><span data-stu-id="7c282-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-831">Le service de réplication de fichiers ne peut pas communiquer avec le service de réplication de fichiers sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="7c282-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="7c282-832">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**réplication \_ de l’erreur \_ \_ du parent de la \_ comm. enfant \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-834">8012 (0x1F4C)</span><span class="sxs-lookup"><span data-stu-id="7c282-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-835">Le service de réplication de fichiers sur le contrôleur de domaine ne peut pas communiquer avec le service de réplication de fichiers sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c282-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="7c282-836">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_ \_ remplissage SYSVOL de l’erreur FRS \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-838">8013 (0x1F4D)</span><span class="sxs-lookup"><span data-stu-id="7c282-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-839">Le service de réplication de fichiers ne peut pas remplir le volume système en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="7c282-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="7c282-840">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ \_ délai d’attente de remplissage SYSVOL de l’erreur FRS**</span><span class="sxs-lookup"><span data-stu-id="7c282-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-842">8014 (0x1F4E)</span><span class="sxs-lookup"><span data-stu-id="7c282-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-843">Le service de réplication de fichiers ne peut pas remplir le volume système en raison d’un délai d’attente interne.</span><span class="sxs-lookup"><span data-stu-id="7c282-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="7c282-844">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**le \_ volume d’erreur FRS \_ \_ est \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="7c282-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-846">8015 (0x1F4F)</span><span class="sxs-lookup"><span data-stu-id="7c282-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-847">Le service de réplication de fichiers ne peut pas traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="7c282-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="7c282-848">Le volume système est occupé par une demande précédente.</span><span class="sxs-lookup"><span data-stu-id="7c282-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err \_ SYSVOL \_ rétrograder**</span><span class="sxs-lookup"><span data-stu-id="7c282-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-850">8016 (0x1F50)</span><span class="sxs-lookup"><span data-stu-id="7c282-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-851">Le service de réplication de fichiers ne peut pas arrêter la réplication du volume système en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="7c282-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="7c282-852">Le journal des événements peut contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7c282-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c282-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_paramètre de service FRS Err \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c282-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c282-854">8017 (0x1F51)</span><span class="sxs-lookup"><span data-stu-id="7c282-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="7c282-855">Le service de réplication de fichiers a détecté un paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="7c282-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c282-856">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c282-856">Requirements</span></span>



| <span data-ttu-id="7c282-857">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c282-857">Requirement</span></span> | <span data-ttu-id="7c282-858">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c282-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c282-859">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c282-859">Minimum supported client</span></span><br/> | <span data-ttu-id="7c282-860">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c282-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c282-861">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c282-861">Minimum supported server</span></span><br/> | <span data-ttu-id="7c282-862">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c282-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c282-863">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c282-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c282-864"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c282-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c282-865">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c282-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c282-866">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="7c282-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





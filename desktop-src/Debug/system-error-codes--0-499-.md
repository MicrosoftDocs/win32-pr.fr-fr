---
description: Décrit les codes d’erreur 0-499 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Codes d’erreur système (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861205"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="9ecab-103">Codes d’erreur système (0-499)</span><span class="sxs-lookup"><span data-stu-id="9ecab-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="9ecab-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="9ecab-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ecab-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="9ecab-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs comprises entre 0 et 499).</span><span class="sxs-lookup"><span data-stu-id="9ecab-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="9ecab-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="9ecab-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="9ecab-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="9ecab-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERREUR de \_ réussite**</span><span class="sxs-lookup"><span data-stu-id="9ecab-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-110">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-111">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="9ecab-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**fonction d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ecab-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-114">Fonction incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_fichier d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-116">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9ecab-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-117">Le système ne peut pas trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_chemin d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-119">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="9ecab-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-120">Le système ne peut pas trouver le chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERREUR \_ trop \_ de \_ \_ fichiers ouverts**</span><span class="sxs-lookup"><span data-stu-id="9ecab-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="9ecab-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-123">Le système ne peut pas ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="9ecab-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-126">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="9ecab-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-129">Le handle n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERREUR de la \_ \_ Corbeille**</span><span class="sxs-lookup"><span data-stu-id="9ecab-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-131">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-132">Les blocs de contrôle de stockage ont été détruits.</span><span class="sxs-lookup"><span data-stu-id="9ecab-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="9ecab-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-135">Nombre de ressources mémoire disponibles insuffisant pour traiter cette commande.</span><span class="sxs-lookup"><span data-stu-id="9ecab-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**bloc d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="9ecab-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-138">L’adresse du bloc de contrôle de stockage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERREUR \_ d' \_ environnement incorrect**</span><span class="sxs-lookup"><span data-stu-id="9ecab-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-140">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-141">L’environnement est incorrect.</span><span class="sxs-lookup"><span data-stu-id="9ecab-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_format incorrect de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="9ecab-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-144">Tentative de chargement d’un programme au format incorrect.</span><span class="sxs-lookup"><span data-stu-id="9ecab-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERREUR \_ d' \_ accès non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-146">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="9ecab-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-147">Le code d’accès n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERREUR de \_ données non valides \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="9ecab-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-150">Les données ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="9ecab-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERREUR \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="9ecab-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-152">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-153">Espace de stockage insuffisant pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="9ecab-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERREUR \_ de \_ lecteur non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="9ecab-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-156">Le système ne trouve pas le lecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERREUR dans le \_ \_ répertoire actuel**</span><span class="sxs-lookup"><span data-stu-id="9ecab-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="9ecab-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-159">Le répertoire ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERREUR sur le \_ \_ même \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="9ecab-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="9ecab-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-162">Le système ne peut pas déplacer le fichier vers un autre lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="9ecab-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERREUR \_ \_ plus aucun \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="9ecab-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-164">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="9ecab-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-165">Il n’y a plus de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ecab-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERREUR \_ de \_ protection en écriture**</span><span class="sxs-lookup"><span data-stu-id="9ecab-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="9ecab-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-168">Le média est protégé en écriture.</span><span class="sxs-lookup"><span data-stu-id="9ecab-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERREUR \_ unité incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="9ecab-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-171">Le système ne peut pas trouver l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERREUR \_ non \_ prête**</span><span class="sxs-lookup"><span data-stu-id="9ecab-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="9ecab-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-174">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="9ecab-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERREUR de \_ commande incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="9ecab-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-177">L’appareil ne reconnaît pas la commande.</span><span class="sxs-lookup"><span data-stu-id="9ecab-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERREUR \_ CRC**</span><span class="sxs-lookup"><span data-stu-id="9ecab-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="9ecab-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-180">Erreur de données (vérification de redondance cyclique).</span><span class="sxs-lookup"><span data-stu-id="9ecab-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERREUR de \_ longueur incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="9ecab-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-183">Le programme a émis une commande, mais la longueur de la commande est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**recherche d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="9ecab-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-186">Le lecteur ne peut pas localiser une zone ou une piste spécifique sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9ecab-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERREUR \_ \_ : disque non DOS \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-189">Impossible d’accéder au disque ou à la disquette spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9ecab-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_secteur d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-192">Le lecteur ne peut pas trouver le secteur demandé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERREUR \_ \_ de dépassement du \_ papier**</span><span class="sxs-lookup"><span data-stu-id="9ecab-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-195">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**erreur d’écriture d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-198">Le système ne peut pas écrire sur le périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**erreur de lecture de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-201">Le système ne peut pas lire à partir du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**\_échec de génération d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-204">Un appareil attaché au système ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="9ecab-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violation de partage d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="9ecab-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-207">Le processus ne peut pas accéder au fichier car ce fichier est utilisé par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="9ecab-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violation de verrouillage d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="9ecab-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-210">Le processus ne peut pas accéder au fichier, car un autre processus a verrouillé une partie du fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERREUR \_ disque incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-212">34 (0X22)</span><span class="sxs-lookup"><span data-stu-id="9ecab-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-213">La mauvaise disquette est dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="9ecab-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="9ecab-214">Insérez %2 (numéro de série du volume : %3) dans le lecteur %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**\_mémoire tampon de partage des erreurs \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="9ecab-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-217">Trop de fichiers ouverts pour le partage.</span><span class="sxs-lookup"><span data-stu-id="9ecab-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**\_EOF de handle d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-219">38 (égale 0x26)</span><span class="sxs-lookup"><span data-stu-id="9ecab-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-220">La fin du fichier a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**HANDLE d’erreur \_ \_ disque \_ plein**</span><span class="sxs-lookup"><span data-stu-id="9ecab-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="9ecab-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-223">Le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="9ecab-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERREUR \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-225">50 (0x32)</span><span class="sxs-lookup"><span data-stu-id="9ecab-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-226">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9ecab-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERREUR \_ REM \_ non \_ List**</span><span class="sxs-lookup"><span data-stu-id="9ecab-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="9ecab-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-229">Windows ne peut pas trouver le chemin d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="9ecab-229">Windows cannot find the network path.</span></span> <span data-ttu-id="9ecab-230">Vérifiez que le chemin d’accès réseau est correct et que l’ordinateur de destination n’est pas occupé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="9ecab-231">Si Windows ne trouve toujours pas le chemin d’accès réseau, contactez votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="9ecab-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**nom de l’erreur \_ DUP \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="9ecab-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-234">Vous n’êtes pas connecté, car il existe un nom dupliqué sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9ecab-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="9ecab-235">Si vous joignez un domaine, accédez à système dans le panneau de configuration pour modifier le nom de l’ordinateur, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="9ecab-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="9ecab-236">Si vous joignez un groupe de travail, choisissez un autre nom de groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="9ecab-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERREUR \_ \_ netpath incorrect**</span><span class="sxs-lookup"><span data-stu-id="9ecab-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="9ecab-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-239">Le chemin d’accès réseau est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERREUR \_ réseau \_ occupée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="9ecab-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-242">Le réseau est occupé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERREUR \_ de \_ développement \_ inexistant**</span><span class="sxs-lookup"><span data-stu-id="9ecab-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="9ecab-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-245">La ressource réseau ou l’appareil spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERREUR \_ trop \_ de \_ Cmds**</span><span class="sxs-lookup"><span data-stu-id="9ecab-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="9ecab-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-248">La limite de commandes du BIOS réseau a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERREUR \_ adap \_ HDW \_ Err**</span><span class="sxs-lookup"><span data-stu-id="9ecab-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="9ecab-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-251">Une erreur matérielle de la carte réseau s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9ecab-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERREUR \_ de \_ réponse nette incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-253">58 (0x3A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-254">Le serveur spécifié ne peut pas exécuter l'opération demandée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERREUR \_ UNEXP \_ NET \_ Err**</span><span class="sxs-lookup"><span data-stu-id="9ecab-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-257">Une erreur réseau inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9ecab-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERREUR \_ mauvais \_ REM \_ adap**</span><span class="sxs-lookup"><span data-stu-id="9ecab-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-260">La carte à distance n’est pas compatible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERREUR \_ PRINTQ \_ complète**</span><span class="sxs-lookup"><span data-stu-id="9ecab-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-263">La file d’attente de l’imprimante est pleine.</span><span class="sxs-lookup"><span data-stu-id="9ecab-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERREUR \_ aucun \_ espace de spouleur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-265">62 (0x3E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-266">L’espace de stockage du fichier en attente d’impression n’est pas disponible sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9ecab-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERREUR d' \_ impression \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-268">63 (0x3F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-269">Votre fichier en attente d’impression a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERREUR \_ NetName \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="9ecab-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-272">Le nom de réseau spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERREUR \_ \_ accès réseau \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-274">65 (0x41 vers)</span><span class="sxs-lookup"><span data-stu-id="9ecab-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-275">Accès réseau refusé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERREUR \_ \_ type de développement incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="9ecab-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-278">Le type de ressource réseau n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERREUR \_ \_ nom de réseau incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-280">67 (0x43)</span><span class="sxs-lookup"><span data-stu-id="9ecab-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-281">Le nom du réseau est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERREUR \_ de \_ noms trop nombreux \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-283">68 (0x44)</span><span class="sxs-lookup"><span data-stu-id="9ecab-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-284">La limite de noms de la carte réseau de l’ordinateur local a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERREUR \_ trop \_ de \_ sess**</span><span class="sxs-lookup"><span data-stu-id="9ecab-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="9ecab-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-287">La limite de session du BIOS réseau a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**partage d’erreurs \_ \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="9ecab-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="9ecab-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-290">Le serveur distant a été suspendu ou est en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="9ecab-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERREUR \_ req \_ non \_ ACCEP**</span><span class="sxs-lookup"><span data-stu-id="9ecab-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="9ecab-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-293">Aucune autre connexion ne peut être établie à cet ordinateur distant pour l’instant, car il existe déjà autant de connexions que l’ordinateur peut accepter.</span><span class="sxs-lookup"><span data-stu-id="9ecab-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**l’inverseur d’erreur est \_ \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="9ecab-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="9ecab-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-296">L’imprimante ou le périphérique de disque spécifié a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="9ecab-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**le \_ fichier d’erreur \_ existe**</span><span class="sxs-lookup"><span data-stu-id="9ecab-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="9ecab-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-299">Le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="9ecab-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERREUR \_ Impossible d' \_ effectuer**</span><span class="sxs-lookup"><span data-stu-id="9ecab-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="9ecab-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-302">Impossible de créer le répertoire ou le fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERREUR d' \_ échec \_ i24**</span><span class="sxs-lookup"><span data-stu-id="9ecab-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="9ecab-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-305">Échec sur INT 24.</span><span class="sxs-lookup"><span data-stu-id="9ecab-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**erreur \_ lors \_ de l’extraction des \_ structures**</span><span class="sxs-lookup"><span data-stu-id="9ecab-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="9ecab-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-308">Le stockage pour traiter cette demande n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERREUR \_ déjà \_ assignée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="9ecab-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-311">Le nom de l’appareil local est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERREUR \_ \_ de mot de passe non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="9ecab-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-314">Le mot de passe réseau spécifié n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="9ecab-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-317">Le paramètre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="9ecab-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERREUR \_ d' \_ écriture réseau de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="9ecab-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-320">Une erreur d’écriture s’est produite sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9ecab-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERREUR \_ aucun \_ emplacement de proc. \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="9ecab-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-323">Le système ne peut pas démarrer un autre processus pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="9ecab-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERREUR \_ trop \_ de \_ sémaphores**</span><span class="sxs-lookup"><span data-stu-id="9ecab-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="9ecab-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-326">Impossible de créer un autre sémaphore système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERREUR \_ excl avec le \_ SEM \_ déjà \_ détenu**</span><span class="sxs-lookup"><span data-stu-id="9ecab-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="9ecab-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-329">Le sémaphore exclusif appartient à un autre processus.</span><span class="sxs-lookup"><span data-stu-id="9ecab-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERREUR \_ SEM \_ \_ définie**</span><span class="sxs-lookup"><span data-stu-id="9ecab-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="9ecab-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-332">Le sémaphore est défini et ne peut pas être fermé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERREUR \_ trop \_ de \_ \_ demandes SEM**</span><span class="sxs-lookup"><span data-stu-id="9ecab-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="9ecab-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-335">Le sémaphore ne peut pas être de nouveau défini.</span><span class="sxs-lookup"><span data-stu-id="9ecab-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERREUR \_ non valide \_ au moment de l' \_ interruption \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="9ecab-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-338">Impossible de demander des sémaphores exclusifs au moment de l’interruption.</span><span class="sxs-lookup"><span data-stu-id="9ecab-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERREUR \_ SEM \_ propriétaire \_ mort**</span><span class="sxs-lookup"><span data-stu-id="9ecab-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="9ecab-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-341">La propriété précédente de ce sémaphore s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERREUR \_ de \_ limite utilisateur SEM \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-343">106 (0x6A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-344">Insérez la disquette pour le lecteur %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERREUR \_ de \_ modification du disque**</span><span class="sxs-lookup"><span data-stu-id="9ecab-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-346">107 (0x6B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-347">Le programme s’est arrêté, car une autre disquette n’a pas été insérée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**lecteur d’erreur \_ \_ verrouillé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-350">Le disque est en cours d’utilisation ou verrouillé par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="9ecab-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERREUR \_ de \_ canal rompu**</span><span class="sxs-lookup"><span data-stu-id="9ecab-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-352">109 (0x6D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-353">Le canal est terminé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**échec de l’ouverture de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-355">110 (0x6E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-356">Le système ne peut pas ouvrir le fichier ou l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_dépassement de mémoire tampon d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-359">Le nom du fichier est trop long.</span><span class="sxs-lookup"><span data-stu-id="9ecab-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**disque d’erreur \_ \_ plein**</span><span class="sxs-lookup"><span data-stu-id="9ecab-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-361">112 (0x70)</span><span class="sxs-lookup"><span data-stu-id="9ecab-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-362">Espace insuffisant sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9ecab-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERREUR \_ aucun \_ autre \_ handle de recherche \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="9ecab-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-365">Aucun autre identificateur de fichier interne n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERREUR \_ de \_ handle cible non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="9ecab-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-368">L’identificateur de fichier interne cible est incorrect.</span><span class="sxs-lookup"><span data-stu-id="9ecab-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**catégorie d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="9ecab-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-371">L’appel IOCTL effectué par le programme d’application n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERREUR \_ de \_ vérification du commutateur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="9ecab-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-374">La valeur du paramètre de vérification à l’écriture n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERREUR \_ de \_ niveau de pilote incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="9ecab-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-377">Le système ne prend pas en charge la commande demandée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**appel d’erreur \_ \_ non \_ implémenté**</span><span class="sxs-lookup"><span data-stu-id="9ecab-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="9ecab-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-380">Cette fonction n’est pas prise en charge sur ce système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERREUR \_ SEM \_ timeout**</span><span class="sxs-lookup"><span data-stu-id="9ecab-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="9ecab-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-383">Le délai d’expiration du sémaphore a expiré.</span><span class="sxs-lookup"><span data-stu-id="9ecab-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="9ecab-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-385">122 (0x7A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-386">La zone de données passée à un appel système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="9ecab-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERREUR \_ nom non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-389">La syntaxe du nom de fichier, du nom de répertoire ou de l’étiquette de volume est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**niveau d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-391">124 (0x7C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-392">Le niveau d’appel système est incorrect.</span><span class="sxs-lookup"><span data-stu-id="9ecab-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERREUR \_ aucun \_ nom de volume \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-395">Le disque n’a pas de nom de volume.</span><span class="sxs-lookup"><span data-stu-id="9ecab-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**la modification de l’erreur est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-398">Le module spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**PROC de l’erreur \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-400">127 (0x7F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-401">La procédure spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERREUR d' \_ attente \_ aucun \_ enfant**</span><span class="sxs-lookup"><span data-stu-id="9ecab-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="9ecab-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-404">Il n’y a aucun processus enfant à attendre.</span><span class="sxs-lookup"><span data-stu-id="9ecab-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**l' \_ enfant d’erreur \_ n’est pas \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="9ecab-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-407">L’application %1 ne peut pas être exécutée en mode Win32.</span><span class="sxs-lookup"><span data-stu-id="9ecab-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_handle d' \_ accès \_ direct d’erreur**</span><span class="sxs-lookup"><span data-stu-id="9ecab-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="9ecab-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-410">Tentative d’utilisation d’un descripteur de fichier sur une partition de disque ouverte pour une opération autre que des e/s de disque brutes.</span><span class="sxs-lookup"><span data-stu-id="9ecab-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERREUR \_ de \_ recherche négative**</span><span class="sxs-lookup"><span data-stu-id="9ecab-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="9ecab-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-413">Une tentative de déplacement du pointeur de fichier avant le début du fichier a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_recherche \_ d’erreur sur l' \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="9ecab-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="9ecab-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-416">Impossible de définir le pointeur de fichier sur le périphérique ou le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**l’erreur \_ est une \_ cible de jointure \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="9ecab-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-419">Une commande JOIN ou SUBSt ne peut pas être utilisée pour un lecteur qui contient des lecteurs précédemment joints.</span><span class="sxs-lookup"><span data-stu-id="9ecab-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**l’erreur \_ est \_ jointe**</span><span class="sxs-lookup"><span data-stu-id="9ecab-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="9ecab-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-422">Une tentative d’utilisation d’une commande JOIN ou SUBSt sur un lecteur qui a déjà été jointe a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERREUR \_ \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9ecab-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="9ecab-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-425">Une tentative d’utilisation d’une commande JOIN ou SUBSt sur un lecteur qui a déjà été remplacé a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERREUR \_ non \_ jointe**</span><span class="sxs-lookup"><span data-stu-id="9ecab-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="9ecab-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-428">Le système a tenté de supprimer la jointure d’un lecteur qui n’est pas joint.</span><span class="sxs-lookup"><span data-stu-id="9ecab-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERREUR \_ non \_ subsante**</span><span class="sxs-lookup"><span data-stu-id="9ecab-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="9ecab-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-431">Le système a essayé de supprimer la substitution d’un lecteur qui n’est pas substitué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**erreur \_ lors \_ de \_ la jointure**</span><span class="sxs-lookup"><span data-stu-id="9ecab-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-433">138 (0x8A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-434">Le système a essayé de joindre un lecteur à un répertoire sur un lecteur joint.</span><span class="sxs-lookup"><span data-stu-id="9ecab-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERREUR \_ de substitution \_ à \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9ecab-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-437">Le système a essayé de remplacer un lecteur par un répertoire sur un lecteur substitué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**erreur \_ lors \_ de la jointure à \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9ecab-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-439">140 (0x8C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-440">Le système a essayé de joindre un lecteur à un répertoire sur un lecteur substitué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERREUR \_ de substitution \_ pour la \_ jointure**</span><span class="sxs-lookup"><span data-stu-id="9ecab-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-442">141 (0x8D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-443">Le système a tenté de SUBSTITUer un lecteur à un répertoire sur un lecteur joint.</span><span class="sxs-lookup"><span data-stu-id="9ecab-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERREUR \_ de \_ lecteur occupé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-445">142 (0x8E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-446">Le système ne peut pas effectuer de jointure ou de substitution pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="9ecab-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERREUR du \_ même \_ lecteur**</span><span class="sxs-lookup"><span data-stu-id="9ecab-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-449">Le système ne peut pas joindre ou substituer un lecteur à ou à un répertoire sur le même lecteur.</span><span class="sxs-lookup"><span data-stu-id="9ecab-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERREUR \_ Rép \_ non \_ racine**</span><span class="sxs-lookup"><span data-stu-id="9ecab-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-451">144 (0X90)</span><span class="sxs-lookup"><span data-stu-id="9ecab-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-452">Le répertoire n’est pas un sous-répertoire du répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="9ecab-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**le \_ répertoire d’erreur \_ n’est pas \_ vide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="9ecab-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-455">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERREUR \_ : \_ subst \_ path**</span><span class="sxs-lookup"><span data-stu-id="9ecab-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="9ecab-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-458">Le chemin d’accès spécifié est utilisé dans un substitut.</span><span class="sxs-lookup"><span data-stu-id="9ecab-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**l’erreur \_ est un \_ chemin de jointure \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="9ecab-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-461">Les ressources disponibles sont insuffisantes pour traiter cette commande.</span><span class="sxs-lookup"><span data-stu-id="9ecab-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_chemin d’erreur \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="9ecab-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-464">Le chemin d’accès spécifié ne peut pas être utilisé pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="9ecab-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**l’erreur \_ est la \_ cible subst \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="9ecab-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-467">Une tentative a été faite pour joindre ou remplacer un lecteur pour lequel un répertoire sur le lecteur est la cible d’un substitut précédent.</span><span class="sxs-lookup"><span data-stu-id="9ecab-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_suivi du système d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="9ecab-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-470">Les informations de trace système n’ont pas été spécifiées dans votre fichier CONFIG.SYS, ou le suivi n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**nombre d’événements d’erreur \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="9ecab-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-473">Le nombre d’événements sémaphores spécifiés pour DosMuxSemWait n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERREUR \_ trop \_ de \_ MUXWAITERS**</span><span class="sxs-lookup"><span data-stu-id="9ecab-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="9ecab-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-476">DosMuxSemWait ne s’est pas exécutée ; trop de sémaphores sont déjà définis.</span><span class="sxs-lookup"><span data-stu-id="9ecab-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**\_format de \_ liste non valide d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="9ecab-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-479">La liste DosMuxSemWait n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**étiquette d’erreur \_ \_ trop \_ longue**</span><span class="sxs-lookup"><span data-stu-id="9ecab-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-481">154 (0x9A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-482">Le nom de volume que vous avez entré dépasse la limite de caractères d’étiquette du système de fichiers cible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERREUR \_ trop \_ de \_ TCBS**</span><span class="sxs-lookup"><span data-stu-id="9ecab-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-484">155 (0x9B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-485">Impossible de créer un autre thread.</span><span class="sxs-lookup"><span data-stu-id="9ecab-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**SIGNAL d’erreur \_ \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-488">Le processus du destinataire a refusé le signal.</span><span class="sxs-lookup"><span data-stu-id="9ecab-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERREUR \_ ignorée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-490">157 (0x9D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-491">Le segment est déjà ignoré et ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERREUR \_ non \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-494">Le segment est déjà déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**erreur de l’adresse de l’erreur \_ \_ THREADID \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-497">L’adresse de l’ID de thread est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9ecab-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERREUR d' \_ arguments incorrects \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-499">160 (0xA0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-500">Un ou plusieurs arguments ne sont pas corrects.</span><span class="sxs-lookup"><span data-stu-id="9ecab-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERREUR \_ de \_ nom de chemin incorrect**</span><span class="sxs-lookup"><span data-stu-id="9ecab-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="9ecab-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-503">Le chemin d’accès spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**SIGNAL d’erreur \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="9ecab-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="9ecab-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-506">Un signal est déjà en attente.</span><span class="sxs-lookup"><span data-stu-id="9ecab-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERREUR \_ Max \_ THRDS \_ atteinte**</span><span class="sxs-lookup"><span data-stu-id="9ecab-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-508">164 (0xA4)</span><span class="sxs-lookup"><span data-stu-id="9ecab-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-509">Aucun thread supplémentaire ne peut être créé dans le système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_échec du verrouillage de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-512">Impossible de verrouiller une région d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERREUR de \_ disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9ecab-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-514">170 (0xAA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-515">La ressource demandée est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9ecab-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERREUR \_ \_ de prise en charge \_ des périphériques en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="9ecab-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="9ecab-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-518">La détection de la prise en charge des commandes de l’appareil est en cours.</span><span class="sxs-lookup"><span data-stu-id="9ecab-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERREUR d' \_ annulation de \_ violation**</span><span class="sxs-lookup"><span data-stu-id="9ecab-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="9ecab-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-521">Aucune demande de verrou n’était en suspens pour la région d’annulation fournie.</span><span class="sxs-lookup"><span data-stu-id="9ecab-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERREUR \_ les \_ verrous atomiques \_ ne sont pas \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-523">174 (0xAE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-524">Le système de fichiers ne prend pas en charge les modifications atomiques du type de verrou.</span><span class="sxs-lookup"><span data-stu-id="9ecab-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERREUR \_ \_ numéro de segment non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="9ecab-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-527">Le système a détecté un numéro de segment qui n’était pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERREUR \_ ordinal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="9ecab-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-530">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**l' \_ erreur \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="9ecab-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-532">183 (0xB7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-533">Impossible de créer un fichier lorsque ce fichier existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9ecab-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERREUR \_ \_ numéro d’indicateur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-535">186 (0xBA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-536">L’indicateur passé n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERREUR \_ SEM \_ non \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="9ecab-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-539">Le nom du sémaphore système spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERREUR \_ de \_ démarrage de CODESEG non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="9ecab-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-542">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERREUR \_ STACKSEG non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-544">189 (0xBD)</span><span class="sxs-lookup"><span data-stu-id="9ecab-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-545">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERREUR \_ MODULETYPE non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-548">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERREUR \_ de \_ signature exe non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="9ecab-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-551">Impossible d’exécuter %1 en mode Win32.</span><span class="sxs-lookup"><span data-stu-id="9ecab-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERREUR \_ exe \_ marquée comme \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-554">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERREUR \_ \_ format exe \_ erroné**</span><span class="sxs-lookup"><span data-stu-id="9ecab-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="9ecab-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-557">%1 n’est pas une application Win32 valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Les \_ données itérées de l’erreur \_ \_ dépassent \_ 64 Ko**</span><span class="sxs-lookup"><span data-stu-id="9ecab-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="9ecab-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-560">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERREUR \_ MINALLOCSIZE non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-562">195 (0xC3)</span><span class="sxs-lookup"><span data-stu-id="9ecab-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-563">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERREUR \_ DynLink \_ de \_ l' \_ anneau non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-565">196 (0xC4)</span><span class="sxs-lookup"><span data-stu-id="9ecab-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-566">Le système d’exploitation ne peut pas exécuter ce programme d’application.</span><span class="sxs-lookup"><span data-stu-id="9ecab-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERREUR \_ iopl \_ non \_ activée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="9ecab-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-569">Le système d’exploitation n’est actuellement pas configuré pour exécuter cette application.</span><span class="sxs-lookup"><span data-stu-id="9ecab-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERREUR \_ SEGDPL non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-571">198 (0xC6)</span><span class="sxs-lookup"><span data-stu-id="9ecab-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-572">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**L’erreur \_ AUTODATASEG \_ dépasse \_ 64 Ko**</span><span class="sxs-lookup"><span data-stu-id="9ecab-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-574">199 (0xC7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-575">Le système d’exploitation ne peut pas exécuter ce programme d’application.</span><span class="sxs-lookup"><span data-stu-id="9ecab-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**L’erreur \_ RING2SEG \_ doit \_ être \_ mobile**</span><span class="sxs-lookup"><span data-stu-id="9ecab-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-577">200 (0xC8)</span><span class="sxs-lookup"><span data-stu-id="9ecab-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-578">Le segment de code ne peut pas être supérieur ou égal à 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="9ecab-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERREUR de \_ chaîne de réadressage \_ \_ XEEDS \_ SEGLIM**</span><span class="sxs-lookup"><span data-stu-id="9ecab-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="9ecab-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-581">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERREUR \_ INFLOOP \_ dans la \_ chaîne de réadressage \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-583">202 (0xCA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-584">Le système d’exploitation ne peut pas exécuter %1.</span><span class="sxs-lookup"><span data-stu-id="9ecab-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERREUR \_ ENVVAR \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="9ecab-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-587">Le système n’a pas pu trouver l’option d’environnement qui a été entrée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERREUR \_ aucun \_ signal \_ envoyé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="9ecab-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-590">Aucun processus dans la sous-arborescence de commandes n’a de gestionnaire de signal.</span><span class="sxs-lookup"><span data-stu-id="9ecab-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERREUR de \_ nom de fichier \_ EXCED \_ plage**</span><span class="sxs-lookup"><span data-stu-id="9ecab-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-592">206 (0xCE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-593">Le nom de fichier ou l’extension est trop long.</span><span class="sxs-lookup"><span data-stu-id="9ecab-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERREUR \_ \_ de pile RING2 \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="9ecab-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="9ecab-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-596">La pile Ring 2 est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9ecab-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERREUR lors de l' \_ \_ expansion meta \_ trop \_ longue**</span><span class="sxs-lookup"><span data-stu-id="9ecab-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-598">208 (0xD0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-599">Les caractères de nom de fichier globaux, \* ou ?, sont entrés de manière incorrecte ou un trop grand nombre de caractères de nom de fichier Global sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9ecab-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERREUR \_ \_ numéro de signal non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="9ecab-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-602">Le signal en cours de publication n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="9ecab-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERREUR \_ thread \_ 1 \_ inactive**</span><span class="sxs-lookup"><span data-stu-id="9ecab-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="9ecab-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-605">Impossible de définir le gestionnaire de signal.</span><span class="sxs-lookup"><span data-stu-id="9ecab-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERREUR \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-607">212 (0xD4)</span><span class="sxs-lookup"><span data-stu-id="9ecab-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-608">Le segment est verrouillé et ne peut pas être réalloué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERREUR \_ trop \_ de \_ modules**</span><span class="sxs-lookup"><span data-stu-id="9ecab-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-610">214 (0xD6)</span><span class="sxs-lookup"><span data-stu-id="9ecab-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-611">Un trop grand nombre de modules de lien dynamique sont attachés à ce programme ou à ce module de liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="9ecab-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_imbrication d’erreurs \_ non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-613">215 (0xD7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-614">Impossible d’imbriquer des appels à LoadModule.</span><span class="sxs-lookup"><span data-stu-id="9ecab-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type d’ordinateur exe \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="9ecab-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-617">Cette version de %1 n’est pas compatible avec la version de Windows que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="9ecab-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="9ecab-618">Vérifiez les informations système de votre ordinateur, puis contactez l’éditeur du logiciel.</span><span class="sxs-lookup"><span data-stu-id="9ecab-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**l’erreur \_ exe \_ ne peut pas \_ modifier le \_ \_ binaire signé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="9ecab-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-621">Le fichier image %1 est signé, impossible à modifier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**l’erreur \_ exe \_ ne peut pas \_ modifier un \_ \_ binaire signé fort \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-623">218 (0xDA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-624">Le fichier image %1 est signé avec une signature forte, impossible à modifier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**fichier d’erreur \_ \_ extrait \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-626">220 (0xDC)</span><span class="sxs-lookup"><span data-stu-id="9ecab-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-627">Ce fichier est extrait ou verrouillé pour modification par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ecab-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**récupération d’erreur \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="9ecab-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="9ecab-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-630">Le fichier doit être extrait avant d’enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="9ecab-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERREUR \_ de \_ type de fichier incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-632">222 (0xDE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-633">Le type de fichier en cours d’enregistrement ou de récupération a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**fichier d’erreur \_ \_ trop \_ volumineux**</span><span class="sxs-lookup"><span data-stu-id="9ecab-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="9ecab-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-636">La taille du fichier dépasse la limite autorisée et ne peut pas être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**authentification par formulaire d’erreur \_ \_ \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9ecab-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-639">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-639">Access Denied.</span></span> <span data-ttu-id="9ecab-640">Avant d’ouvrir des fichiers à cet emplacement, vous devez d’abord ajouter le site Web à votre liste de sites de confiance, accéder au site Web et sélectionner l’option de connexion automatique.</span><span class="sxs-lookup"><span data-stu-id="9ecab-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS d’erreur \_ \_ infecté**</span><span class="sxs-lookup"><span data-stu-id="9ecab-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-642">225 (0xE1)</span><span class="sxs-lookup"><span data-stu-id="9ecab-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-643">L’opération n’a pas abouti car le fichier contient un virus ou un logiciel potentiellement indésirable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**VIRUS d’erreur \_ \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-645">226 (0xE2)</span><span class="sxs-lookup"><span data-stu-id="9ecab-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-646">Ce fichier contient un virus ou un logiciel potentiellement indésirable et ne peut pas être ouvert.</span><span class="sxs-lookup"><span data-stu-id="9ecab-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="9ecab-647">En raison de la nature de ce virus ou d’un logiciel potentiellement indésirable, le fichier a été supprimé de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="9ecab-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**canal d’erreur \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="9ecab-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="9ecab-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-650">Le canal est local.</span><span class="sxs-lookup"><span data-stu-id="9ecab-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERREUR \_ de \_ canal incorrect**</span><span class="sxs-lookup"><span data-stu-id="9ecab-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-652">230 (0xE6)</span><span class="sxs-lookup"><span data-stu-id="9ecab-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-653">L’état du canal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**canal d’erreur \_ \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-656">Toutes les instances de canal sont occupées.</span><span class="sxs-lookup"><span data-stu-id="9ecab-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERREUR \_ aucune \_ donnée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-658">232 (0xE8)</span><span class="sxs-lookup"><span data-stu-id="9ecab-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-659">Le canal est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="9ecab-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**canal d’erreur \_ \_ non \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="9ecab-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="9ecab-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-662">Aucun traitement à l'autre extrémité du canal</span><span class="sxs-lookup"><span data-stu-id="9ecab-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERREUR \_ plus de \_ données**</span><span class="sxs-lookup"><span data-stu-id="9ecab-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="9ecab-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-665">More data is available.</span><span class="sxs-lookup"><span data-stu-id="9ecab-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERREUR \_ VC \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-667">240 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="9ecab-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-668">La session a été annulée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERREUR \_ \_ nom EA non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="9ecab-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-671">Le nom d’attribut étendu spécifié n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERREUR de \_ liste d’EA non \_ \_ cohérente**</span><span class="sxs-lookup"><span data-stu-id="9ecab-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="9ecab-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-674">Les attributs étendus sont incohérents.</span><span class="sxs-lookup"><span data-stu-id="9ecab-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_délai d’attente**</span><span class="sxs-lookup"><span data-stu-id="9ecab-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="9ecab-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-677">Expiration du délai d'attente de l'opération d'attente.</span><span class="sxs-lookup"><span data-stu-id="9ecab-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERREUR \_ aucun \_ autre \_ élément**</span><span class="sxs-lookup"><span data-stu-id="9ecab-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="9ecab-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-680">Aucune donnée n'est disponible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_Impossible de \_ copier l’erreur**</span><span class="sxs-lookup"><span data-stu-id="9ecab-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-683">Les fonctions de copie ne peuvent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="9ecab-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Répertoire d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-686">Le nom du répertoire n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERREUR \_ EAS \_ examinera \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="9ecab-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-689">Les attributs étendus ne tiennent pas dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9ecab-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERREUR \_ EA \_ fichier \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="9ecab-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="9ecab-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-692">Le fichier d’attributs étendus sur le système de fichiers monté est endommagé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERREUR \_ de \_ table EA \_ complète**</span><span class="sxs-lookup"><span data-stu-id="9ecab-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="9ecab-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-695">Le fichier de la table des attributs étendus est plein.</span><span class="sxs-lookup"><span data-stu-id="9ecab-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERREUR \_ de \_ handle EA non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="9ecab-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-698">Le handle d’attribut étendu spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERREUR \_ EAS \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-701">Le système de fichiers monté ne prend pas en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="9ecab-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERREUR \_ non \_ propriétaire**</span><span class="sxs-lookup"><span data-stu-id="9ecab-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="9ecab-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-704">Tentative de libération du mutex qui n’appartient pas à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9ecab-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERREUR \_ trop \_ de \_ publications**</span><span class="sxs-lookup"><span data-stu-id="9ecab-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-707">Un trop grand nombre de publications a été effectué sur un sémaphore.</span><span class="sxs-lookup"><span data-stu-id="9ecab-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERREUR \_ de \_ copie partielle**</span><span class="sxs-lookup"><span data-stu-id="9ecab-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-710">Seule une partie d’une requête ReadProcessMemory ou WriteProcessMemory a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERREUR \_ OPLOCK \_ non \_ accordée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-713">La demande oplock est refusée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERREUR \_ de \_ protocole OPLOCK non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-716">Un accusé de réception oplock non valide a été reçu par le système.</span><span class="sxs-lookup"><span data-stu-id="9ecab-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disque d’erreur \_ \_ trop \_ fragmenté**</span><span class="sxs-lookup"><span data-stu-id="9ecab-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-719">Le volume est trop fragmenté pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="9ecab-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERREUR de \_ suppression \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="9ecab-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-722">Impossible d’ouvrir le fichier, car il est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="9ecab-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERREUR \_ d’incompatibilité \_ avec le \_ paramètre de \_ \_ Registre de nom abrégé \_ global \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="9ecab-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-725">Les paramètres de nom abrégé ne peuvent pas être modifiés sur ce volume en raison du paramètre de registre global.</span><span class="sxs-lookup"><span data-stu-id="9ecab-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_noms courts \_ \_ d’erreur non \_ activés \_ sur le \_ volume**</span><span class="sxs-lookup"><span data-stu-id="9ecab-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="9ecab-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-728">Les noms courts ne sont pas activés sur ce volume.</span><span class="sxs-lookup"><span data-stu-id="9ecab-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**le \_ flux de sécurité d’erreur \_ \_ est \_ incohérent**</span><span class="sxs-lookup"><span data-stu-id="9ecab-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="9ecab-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-731">Le flux de sécurité du volume donné est dans un état incohérent.</span><span class="sxs-lookup"><span data-stu-id="9ecab-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="9ecab-732">Exécutez CHKDSK sur le volume.</span><span class="sxs-lookup"><span data-stu-id="9ecab-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERREUR \_ de \_ plage de verrouillage non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="9ecab-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-735">Une opération de verrouillage de fichier demandée ne peut pas être traitée en raison d’une plage d’octets non valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_ \_ sous-système d’image d' \_ erreur absent \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="9ecab-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-738">Le sous-système nécessaire pour prendre en charge le type d’image n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="9ecab-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notification d’erreur \_ \_ \_ déjà \_ défini**</span><span class="sxs-lookup"><span data-stu-id="9ecab-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="9ecab-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-741">Un GUID de notification est déjà associé au fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERREUR \_ de \_ Gestionnaire d’exceptions non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="9ecab-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-744">Une routine de gestionnaire d’exceptions non valide a été détectée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**privilèges d’erreur \_ dupliqués \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="9ecab-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-747">Des privilèges en double ont été spécifiés pour le jeton.</span><span class="sxs-lookup"><span data-stu-id="9ecab-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERREUR \_ aucune \_ plage \_ traitée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="9ecab-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-750">Aucune plage pour l’opération spécifiée n’a pu être traitée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERREUR \_ non \_ autorisée \_ sur \_ le \_ fichier système**</span><span class="sxs-lookup"><span data-stu-id="9ecab-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="9ecab-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-753">L’opération n’est pas autorisée sur un fichier interne du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ecab-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERREURS \_ de \_ ressources de disque \_ épuisées**</span><span class="sxs-lookup"><span data-stu-id="9ecab-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-755">314 (0x13A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-756">Les ressources physiques de ce disque ont été épuisées.</span><span class="sxs-lookup"><span data-stu-id="9ecab-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERREUR \_ de \_ jeton non valide**</span><span class="sxs-lookup"><span data-stu-id="9ecab-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-759">Le jeton représentant les données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**fonctionnalité de périphérique d’erreur \_ \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-762">L’appareil ne prend pas en charge la fonctionnalité de commande.</span><span class="sxs-lookup"><span data-stu-id="9ecab-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERREUR \_ Mr \_ Mid \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-765">Le système ne trouve pas de texte de message pour le numéro de message 0x %1 dans le fichier de message pour %2.</span><span class="sxs-lookup"><span data-stu-id="9ecab-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**étendue de l’erreur \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="9ecab-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-768">L’étendue spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ecab-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**\_étendue non définie par \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="9ecab-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-771">La stratégie d’accès centralisée spécifiée n’est pas définie sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERREUR \_ Cap non valide \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="9ecab-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-774">La stratégie d’accès centralisée obtenue à partir de Active Directory n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERREUR de \_ périphérique \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="9ecab-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="9ecab-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-777">L’appareil est inaccessible.</span><span class="sxs-lookup"><span data-stu-id="9ecab-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**périphérique d’erreur- \_ \_ aucune \_ ressource**</span><span class="sxs-lookup"><span data-stu-id="9ecab-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="9ecab-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-780">L’appareil cible ne dispose pas de ressources suffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="9ecab-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**erreur \_ de \_ somme de contrôle des données d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="9ecab-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-783">Une erreur de somme de contrôle d’intégrité des données s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9ecab-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="9ecab-784">Les données du flux de fichier sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="9ecab-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERREUR de l' \_ \_ \_ Opération EA \_ du noyau intermixed**</span><span class="sxs-lookup"><span data-stu-id="9ecab-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="9ecab-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-787">Une tentative a été effectuée pour modifier à la fois un noyau et un attribut étendu normal (EA) dans la même opération.</span><span class="sxs-lookup"><span data-stu-id="9ecab-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_suppression du niveau de fichier erreur \_ \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="9ecab-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-790">L’appareil ne prend pas en charge la suppression au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecab-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERREUR d' \_ alignement du décalage de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="9ecab-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-793">La commande a spécifié un décalage de données qui n’est pas aligné sur la granularité/l’alignement de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ecab-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_champ d’erreur non valide \_ dans la \_ \_ liste de paramètres \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="9ecab-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-796">La commande a spécifié un champ non valide dans sa liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9ecab-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERREUR \_ \_ de l’opération en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="9ecab-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="9ecab-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-799">Une opération est actuellement en cours avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ecab-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERREUR de chemin de l' \_ appareil incorrect \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-801">330 (0x14A)</span><span class="sxs-lookup"><span data-stu-id="9ecab-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-802">Une tentative d’envoi de la commande via un chemin d’accès non valide à l’appareil cible a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ecab-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERREUR \_ trop \_ nombreux \_ descripteurs**</span><span class="sxs-lookup"><span data-stu-id="9ecab-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="9ecab-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-805">La commande a spécifié plusieurs descripteurs qui ont dépassé le nombre maximal pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ecab-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERREUR de \_ nettoyage des \_ données \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="9ecab-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-807">332 (0x14C)</span><span class="sxs-lookup"><span data-stu-id="9ecab-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-808">Le nettoyage est désactivé sur le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ecab-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERREUR \_ de \_ stockage non redondant \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-810">333 (0x14D)</span><span class="sxs-lookup"><span data-stu-id="9ecab-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-811">Le périphérique de stockage ne fournit pas de redondance.</span><span class="sxs-lookup"><span data-stu-id="9ecab-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_fichier résident \_ erroné \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-814">Une opération n’est pas prise en charge sur un fichier résident.</span><span class="sxs-lookup"><span data-stu-id="9ecab-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERREUR \_ \_ fichier compressé \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-816">335 (0x14F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-817">Une opération n’est pas prise en charge sur un fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="9ecab-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Répertoire d’erreurs \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="9ecab-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="9ecab-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-820">Une opération n’est pas prise en charge sur un répertoire.</span><span class="sxs-lookup"><span data-stu-id="9ecab-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**erreur \_ lors \_ de la lecture \_ de la \_ copie**</span><span class="sxs-lookup"><span data-stu-id="9ecab-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="9ecab-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-823">Impossible de lire la copie spécifiée des données demandées.</span><span class="sxs-lookup"><span data-stu-id="9ecab-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERREUR d' \_ échec \_ NoAction de \_ redémarrage**</span><span class="sxs-lookup"><span data-stu-id="9ecab-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-825">350 (0x15E)</span><span class="sxs-lookup"><span data-stu-id="9ecab-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-826">Aucune action n’a été effectuée, car un redémarrage du système est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9ecab-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERREUR lors de l' \_ \_ arrêt**</span><span class="sxs-lookup"><span data-stu-id="9ecab-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-828">351 (0x15F)</span><span class="sxs-lookup"><span data-stu-id="9ecab-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-829">Échec de l’opération d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="9ecab-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**\_échec du \_ redémarrage de l’erreur**</span><span class="sxs-lookup"><span data-stu-id="9ecab-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="9ecab-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-832">L’opération de redémarrage a échoué.</span><span class="sxs-lookup"><span data-stu-id="9ecab-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERREUR \_ Max \_ sessions \_ atteintes**</span><span class="sxs-lookup"><span data-stu-id="9ecab-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="9ecab-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-835">Le nombre maximal de sessions a été atteint.</span><span class="sxs-lookup"><span data-stu-id="9ecab-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**le \_ mode thread d’erreur est \_ \_ déjà en \_ arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="9ecab-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="9ecab-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-838">Le thread est déjà en mode de traitement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9ecab-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**MODE de thread d’erreur \_ \_ \_ non en \_ arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="9ecab-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="9ecab-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-841">Le thread n’est pas en mode de traitement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9ecab-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**le mode de traitement des erreurs est \_ \_ \_ déjà en \_ arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="9ecab-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="9ecab-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-844">Le processus est déjà en mode de traitement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9ecab-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**erreur de mode de traitement d’erreur \_ \_ \_ non en \_ arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="9ecab-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="9ecab-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-847">Le processus n’est pas en mode de traitement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9ecab-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecab-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_adresse non valide de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="9ecab-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecab-849">487 (0x1E7)</span><span class="sxs-lookup"><span data-stu-id="9ecab-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="9ecab-850">Tentative d’accès à une adresse non valide.</span><span class="sxs-lookup"><span data-stu-id="9ecab-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="9ecab-851">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ecab-851">Requirements</span></span>



| <span data-ttu-id="9ecab-852">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ecab-852">Requirement</span></span> | <span data-ttu-id="9ecab-853">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ecab-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecab-854">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ecab-854">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecab-855">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ecab-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9ecab-856">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ecab-856">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecab-857">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ecab-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ecab-858">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ecab-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecab-859"><dt>WinError. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ecab-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ecab-860">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ecab-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecab-861">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="9ecab-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





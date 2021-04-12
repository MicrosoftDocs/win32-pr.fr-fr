---
description: Décrit les codes d’erreur 1000-1299 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Codes d’erreur système (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523716"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="4d144-103">Codes d’erreur système (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="4d144-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="4d144-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="4d144-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="4d144-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4d144-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="4d144-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1000 à 1299.</span><span class="sxs-lookup"><span data-stu-id="4d144-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="4d144-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="4d144-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="4d144-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="4d144-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="4d144-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_dépassement de pile d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-110">1001 (0x3E9)</span><span class="sxs-lookup"><span data-stu-id="4d144-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-111">Récurrence trop profonde ; dépassement de capacité de la pile.</span><span class="sxs-lookup"><span data-stu-id="4d144-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**MESSAGE d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-113">1002 (0x3EA)</span><span class="sxs-lookup"><span data-stu-id="4d144-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-114">La fenêtre ne peut pas agir sur le message envoyé.</span><span class="sxs-lookup"><span data-stu-id="4d144-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**l' \_ erreur \_ ne peut pas se \_ terminer**</span><span class="sxs-lookup"><span data-stu-id="4d144-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-116">1003 (0x3EB)</span><span class="sxs-lookup"><span data-stu-id="4d144-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-117">Impossible d’effectuer cette fonction.</span><span class="sxs-lookup"><span data-stu-id="4d144-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**indicateurs d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-119">1004 (0x3EC)</span><span class="sxs-lookup"><span data-stu-id="4d144-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-120">Indicateurs non valides.</span><span class="sxs-lookup"><span data-stu-id="4d144-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERREUR de \_ volume non reconnu \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-122">1005 (0x3ED)</span><span class="sxs-lookup"><span data-stu-id="4d144-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-123">Le volume ne contient pas de système de fichiers reconnu.</span><span class="sxs-lookup"><span data-stu-id="4d144-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="4d144-124">Assurez-vous que tous les pilotes de système de fichiers requis sont chargés et que le volume n’est pas endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**fichier d’erreur \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4d144-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="4d144-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-127">Le volume d’un fichier a été modifié en externe, de sorte que le fichier ouvert n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERREUR \_ de \_ mode plein écran**</span><span class="sxs-lookup"><span data-stu-id="4d144-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-129">1007 (0x3EF)</span><span class="sxs-lookup"><span data-stu-id="4d144-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-130">L’opération demandée ne peut pas être exécutée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="4d144-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERREUR \_ aucun \_ jeton**</span><span class="sxs-lookup"><span data-stu-id="4d144-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-132">1008 (0x3F0)</span><span class="sxs-lookup"><span data-stu-id="4d144-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-133">Une tentative de référence à un jeton qui n’existe pas a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4d144-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERREUR \_ BADDB**</span><span class="sxs-lookup"><span data-stu-id="4d144-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-135">1009 (0x3F1)</span><span class="sxs-lookup"><span data-stu-id="4d144-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-136">La base de données de registre de configuration est endommagée.</span><span class="sxs-lookup"><span data-stu-id="4d144-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERREUR \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="4d144-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-138">1010 (0x3F2)</span><span class="sxs-lookup"><span data-stu-id="4d144-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-139">La clé de registre de configuration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERREUR \_ CANTOPEN**</span><span class="sxs-lookup"><span data-stu-id="4d144-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-141">1011 (0x3F3)</span><span class="sxs-lookup"><span data-stu-id="4d144-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-142">Impossible d’ouvrir la clé de registre de configuration.</span><span class="sxs-lookup"><span data-stu-id="4d144-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERREUR \_ CANTREAD**</span><span class="sxs-lookup"><span data-stu-id="4d144-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-144">1012 (égal à 0x3f4)</span><span class="sxs-lookup"><span data-stu-id="4d144-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-145">Impossible de lire la clé de registre de configuration.</span><span class="sxs-lookup"><span data-stu-id="4d144-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERREUR \_ CANTWRITE**</span><span class="sxs-lookup"><span data-stu-id="4d144-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-147">1013 (0x3F5)</span><span class="sxs-lookup"><span data-stu-id="4d144-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-148">Impossible d’écrire la clé de registre de configuration.</span><span class="sxs-lookup"><span data-stu-id="4d144-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERREUR \_ de \_ récupération du Registre**</span><span class="sxs-lookup"><span data-stu-id="4d144-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-150">1014 (0x3F6)</span><span class="sxs-lookup"><span data-stu-id="4d144-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-151">L’un des fichiers de la base de données du registre a dû être récupéré à l’aide d’un journal ou d’une copie de remplacement.</span><span class="sxs-lookup"><span data-stu-id="4d144-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="4d144-152">La récupération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4d144-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**Registre des erreurs \_ \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="4d144-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-154">1015 (0x3F7)</span><span class="sxs-lookup"><span data-stu-id="4d144-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-155">Le Registre est endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-155">The registry is corrupted.</span></span> <span data-ttu-id="4d144-156">La structure de l’un des fichiers contenant les données du Registre est endommagée, l’image mémoire du système du fichier est endommagée, ou le fichier n’a pas pu être récupéré parce que l’autre copie ou le même journal est absent ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERREUR \_ échec de l' \_ e/s du Registre \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-158">1016 (0x3F8)</span><span class="sxs-lookup"><span data-stu-id="4d144-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-159">Une opération d’e/s initiée par le registre a échoué de façon irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="4d144-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="4d144-160">Le registre n’a pas pu lire ou écrire, ou vider, l’un des fichiers qui contiennent l’image du Registre du système.</span><span class="sxs-lookup"><span data-stu-id="4d144-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERREUR \_ non \_ fichier du Registre \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-162">1017 (0x3F9)</span><span class="sxs-lookup"><span data-stu-id="4d144-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-163">Le système a tenté de charger ou de restaurer un fichier dans le registre, mais le fichier spécifié n’est pas dans un format de fichier du Registre.</span><span class="sxs-lookup"><span data-stu-id="4d144-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**clé d’erreur \_ \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="4d144-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-165">1018 (0x3FA)</span><span class="sxs-lookup"><span data-stu-id="4d144-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-166">Opération non conforme tentée sur une clé de Registre marquée pour suppression.</span><span class="sxs-lookup"><span data-stu-id="4d144-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERREUR \_ aucun \_ espace du journal \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-168">1019 (0x3FB)</span><span class="sxs-lookup"><span data-stu-id="4d144-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-169">Le système n’a pas pu allouer l’espace requis dans un journal du Registre.</span><span class="sxs-lookup"><span data-stu-id="4d144-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**la \_ clé d’erreur \_ a des \_ enfants**</span><span class="sxs-lookup"><span data-stu-id="4d144-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-171">1020 (0x3FC)</span><span class="sxs-lookup"><span data-stu-id="4d144-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-172">Impossible de créer un lien symbolique dans une clé de Registre qui a déjà des sous-clés ou des valeurs.</span><span class="sxs-lookup"><span data-stu-id="4d144-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**l' \_ enfant d’erreur \_ doit \_ être \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="4d144-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-174">1021 (0x3FD)</span><span class="sxs-lookup"><span data-stu-id="4d144-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-175">Impossible de créer une sous-clé stable sous une clé parent volatile.</span><span class="sxs-lookup"><span data-stu-id="4d144-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERREUR de notification de l' \_ \_ énumération \_ dir**</span><span class="sxs-lookup"><span data-stu-id="4d144-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-177">1022 (0x3FE)</span><span class="sxs-lookup"><span data-stu-id="4d144-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-178">Une demande de notification de modification est en cours d’exécution et les informations ne sont pas retournées dans la mémoire tampon de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4d144-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="4d144-179">L’appelant doit à présent énumérer les fichiers pour rechercher les modifications.</span><span class="sxs-lookup"><span data-stu-id="4d144-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_services dépendants d’erreurs \_ \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="4d144-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-181">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="4d144-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-182">Un contrôle d’arrêt a été envoyé à un service dont dépendent d’autres services en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4d144-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERREUR \_ de \_ contrôle de service non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-184">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="4d144-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-185">Le contrôle demandé n’est pas valide pour ce service.</span><span class="sxs-lookup"><span data-stu-id="4d144-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERREUR \_ de \_ \_ délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="4d144-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-187">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="4d144-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-188">Le service n'a pas répondu à temps à la requête de démarrage ou de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d144-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**SERVICE d’erreur \_ \_ sans \_ thread**</span><span class="sxs-lookup"><span data-stu-id="4d144-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-190">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="4d144-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-191">Impossible de créer un thread pour le service.</span><span class="sxs-lookup"><span data-stu-id="4d144-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**\_base de données du service d’erreur \_ \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="4d144-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-193">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="4d144-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-194">La base de données du service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="4d144-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**SERVICE d’erreur \_ \_ déjà \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="4d144-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="4d144-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-197">Une instance du service est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4d144-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERREUR \_ de \_ compte de service non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="4d144-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-200">Le nom du compte n’est pas valide ou n’existe pas, ou le mot de passe n’est pas valide pour le nom de compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="4d144-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**SERVICE d’erreur \_ \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="4d144-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="4d144-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-203">Le service ne peut pas être démarré parce qu’il est désactivé ou qu’aucun appareil activé ne lui est associé.</span><span class="sxs-lookup"><span data-stu-id="4d144-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dépendance circulaire d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="4d144-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-206">Une dépendance de service circulaire a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4d144-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**le \_ service d’erreur \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="4d144-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="4d144-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-209">Le service spécifié n’existe pas en tant que service installé.</span><span class="sxs-lookup"><span data-stu-id="4d144-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**le \_ service d’erreur \_ ne peut pas \_ accepter la \_ touche Ctrl**</span><span class="sxs-lookup"><span data-stu-id="4d144-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="4d144-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-212">Le service ne peut pas accepter les messages de contrôle pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="4d144-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_service d' \_ erreur \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="4d144-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-214">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="4d144-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-215">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="4d144-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERREUR \_ échec \_ de \_ connexion du contrôleur de service \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="4d144-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-218">Le processus de service n’a pas pu se connecter au contrôleur de service.</span><span class="sxs-lookup"><span data-stu-id="4d144-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_exception \_ d’erreur dans le \_ service**</span><span class="sxs-lookup"><span data-stu-id="4d144-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="4d144-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-221">Une exception s’est produite dans le service lors du traitement de la demande de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d144-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**la \_ base de données d’erreurs \_ n' \_ \_ existe pas**</span><span class="sxs-lookup"><span data-stu-id="4d144-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="4d144-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-224">La base de données spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**erreur \_ spécifique au service d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-226">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="4d144-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-227">Le service a retourné un code d’erreur spécifique au service.</span><span class="sxs-lookup"><span data-stu-id="4d144-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**\_arrêt du processus d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-229">1067 (0x42B)</span><span class="sxs-lookup"><span data-stu-id="4d144-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-230">Le processus s’est arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="4d144-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**échec de la dépendance du service d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-232">1068 (0x42C)</span><span class="sxs-lookup"><span data-stu-id="4d144-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-233">Le service ou le groupe de dépendances n’a pas pu démarrer.</span><span class="sxs-lookup"><span data-stu-id="4d144-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**échec de l' \_ ouverture de session du service \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-235">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="4d144-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-236">Le service n'a pas démarré en raison d'une erreur d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="4d144-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERREUR de \_ démarrage du service d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-238">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="4d144-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-239">Après le démarrage, le service est suspendu dans un état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="4d144-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERREUR \_ de \_ verrou de service non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-241">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="4d144-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-242">Le verrou de base de données de service spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_service \_ d’erreur marqué \_ pour \_ suppression**</span><span class="sxs-lookup"><span data-stu-id="4d144-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="4d144-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-245">Le service spécifié a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="4d144-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**le \_ service d’erreur \_ existe**</span><span class="sxs-lookup"><span data-stu-id="4d144-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="4d144-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-248">Le service spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4d144-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERREUR lors de l' \_ \_ exécution de \_ correcte connue**</span><span class="sxs-lookup"><span data-stu-id="4d144-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="4d144-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-251">Le système est en cours d’exécution avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="4d144-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dépendance de service d’erreur \_ \_ \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="4d144-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="4d144-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-254">Le service de dépendances n’existe pas ou a été marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="4d144-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERREUR de \_ démarrage \_ déjà \_ acceptée**</span><span class="sxs-lookup"><span data-stu-id="4d144-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="4d144-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-257">Le démarrage actuel a déjà été accepté pour une utilisation en tant que dernier jeu de contrôle connu.</span><span class="sxs-lookup"><span data-stu-id="4d144-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**le \_ service d’erreur \_ n' \_ a jamais démarré**</span><span class="sxs-lookup"><span data-stu-id="4d144-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="4d144-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-260">Aucune tentative de démarrage du service n’a été effectuée depuis le dernier démarrage.</span><span class="sxs-lookup"><span data-stu-id="4d144-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERREUR \_ de \_ nom de service dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="4d144-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-263">Le nom est déjà utilisé en tant que nom de service ou nom d’affichage de service.</span><span class="sxs-lookup"><span data-stu-id="4d144-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERREUR \_ de \_ compte de service différent \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="4d144-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-266">Le compte spécifié pour ce service est différent du compte spécifié pour les autres services s’exécutant dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="4d144-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERREUR \_ Impossible de \_ détecter la \_ défaillance du pilote \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-268">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="4d144-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-269">Les actions d’échec ne peuvent être définies que pour les services Win32, et non pour les pilotes.</span><span class="sxs-lookup"><span data-stu-id="4d144-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERREUR \_ Impossible de \_ détecter l' \_ abandon du processus \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="4d144-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-272">Ce service s’exécute dans le même processus que le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="4d144-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="4d144-273">Par conséquent, le gestionnaire de contrôle des services ne peut pas agir si le processus de ce service se termine de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="4d144-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERREUR \_ pas \_ de \_ programme de récupération**</span><span class="sxs-lookup"><span data-stu-id="4d144-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-275">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="4d144-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-276">Aucun programme de récupération n’a été configuré pour ce service.</span><span class="sxs-lookup"><span data-stu-id="4d144-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERREUR \_ \_ de service introuvable \_ dans l' \_ exe**</span><span class="sxs-lookup"><span data-stu-id="4d144-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-278">1083 (0x43B)</span><span class="sxs-lookup"><span data-stu-id="4d144-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-279">Le programme exécutable dans lequel ce service est configuré pour s’exécuter n’implémente pas le service.</span><span class="sxs-lookup"><span data-stu-id="4d144-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERREUR \_ non \_ - \_ service SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="4d144-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-281">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="4d144-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-282">Ce service ne peut pas être démarré en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="4d144-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fin \_ du \_ support d’erreur**</span><span class="sxs-lookup"><span data-stu-id="4d144-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-284">1100 (0x44C)</span><span class="sxs-lookup"><span data-stu-id="4d144-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-285">La fin physique de la bande a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="4d144-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marque d’erreur \_ \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="4d144-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-287">1101 (0x44D)</span><span class="sxs-lookup"><span data-stu-id="4d144-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-288">Un accès à la bande a atteint un marqueur.</span><span class="sxs-lookup"><span data-stu-id="4d144-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERREUR \_ \_ de début de \_ support**</span><span class="sxs-lookup"><span data-stu-id="4d144-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-290">1102 (0x44E)</span><span class="sxs-lookup"><span data-stu-id="4d144-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-291">Le début de la bande ou d’une partition a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="4d144-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERREUR \_ SETMARK \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="4d144-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-293">1103 (0x44F)</span><span class="sxs-lookup"><span data-stu-id="4d144-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-294">Un accès à la bande a atteint la fin d’un ensemble de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4d144-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERREUR \_ aucune \_ donnée \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="4d144-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="4d144-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-297">Il n’y a plus de données sur la bande.</span><span class="sxs-lookup"><span data-stu-id="4d144-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**\_échec de partition d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="4d144-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-300">La bande n’a pas pu être partitionnée.</span><span class="sxs-lookup"><span data-stu-id="4d144-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERREUR \_ de \_ longueur de bloc non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="4d144-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-303">Lors de l’accès à une nouvelle bande d’une partition multivolume, la taille de bloc actuelle est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4d144-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERREUR de \_ périphérique \_ non \_ partitionné**</span><span class="sxs-lookup"><span data-stu-id="4d144-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="4d144-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-306">Les informations de partition de bande sont introuvables lors du chargement d’une bande.</span><span class="sxs-lookup"><span data-stu-id="4d144-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERREUR \_ Impossible \_ de \_ verrouiller le \_ support**</span><span class="sxs-lookup"><span data-stu-id="4d144-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="4d144-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-309">Impossible de verrouiller le mécanisme d’éjection de support.</span><span class="sxs-lookup"><span data-stu-id="4d144-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERREUR \_ Impossible \_ de \_ décharger le \_ média**</span><span class="sxs-lookup"><span data-stu-id="4d144-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="4d144-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-312">Impossible de décharger le média.</span><span class="sxs-lookup"><span data-stu-id="4d144-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**le \_ support d’erreur \_ a changé**</span><span class="sxs-lookup"><span data-stu-id="4d144-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="4d144-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-315">Le support présent dans le lecteur a peut-être changé.</span><span class="sxs-lookup"><span data-stu-id="4d144-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**réinitialisation du bus d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="4d144-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-318">Le bus des e/s a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="4d144-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERREUR \_ aucun \_ média \_ dans le \_ lecteur**</span><span class="sxs-lookup"><span data-stu-id="4d144-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="4d144-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-321">Aucun média dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="4d144-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERREUR \_ aucune \_ \_ traduction Unicode**</span><span class="sxs-lookup"><span data-stu-id="4d144-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="4d144-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-324">Il n’existe aucun mappage pour le caractère Unicode dans la page de codes multi-octets cible.</span><span class="sxs-lookup"><span data-stu-id="4d144-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**échec de l’initialisation de la dll d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-326">1114 (0x45A)</span><span class="sxs-lookup"><span data-stu-id="4d144-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-327">Échec de la routine d’initialisation d’une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="4d144-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERREUR \_ \_ d’arrêt en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="4d144-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-329">1115 (0x45B)</span><span class="sxs-lookup"><span data-stu-id="4d144-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-330">Un arrêt du système est en cours.</span><span class="sxs-lookup"><span data-stu-id="4d144-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERREUR \_ aucun \_ arrêt \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="4d144-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-332">1116 (0x45C)</span><span class="sxs-lookup"><span data-stu-id="4d144-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-333">Impossible d’abandonner l’arrêt du système, car aucun arrêt n’était en cours.</span><span class="sxs-lookup"><span data-stu-id="4d144-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERREUR d' \_ e/s \_ périphérique**</span><span class="sxs-lookup"><span data-stu-id="4d144-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-335">1117 (0x45D)</span><span class="sxs-lookup"><span data-stu-id="4d144-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-336">La requête n'a pas pu être exécutée en raison d'une erreur de périphérique d'E/S.</span><span class="sxs-lookup"><span data-stu-id="4d144-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERREUR \_ série \_ aucun \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="4d144-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-338">1118 (0x45E)</span><span class="sxs-lookup"><span data-stu-id="4d144-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-339">Aucun appareil série n’a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="4d144-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="4d144-340">Le pilote série sera déchargé.</span><span class="sxs-lookup"><span data-stu-id="4d144-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERREUR \_ IRQ \_ Busy**</span><span class="sxs-lookup"><span data-stu-id="4d144-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-342">1119 (0x45F)</span><span class="sxs-lookup"><span data-stu-id="4d144-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-343">Impossible d’ouvrir un appareil qui partageait une requête d’interruption (IRQ) avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="4d144-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="4d144-344">Au moins un autre périphérique qui utilise cette IRQ a déjà été ouvert.</span><span class="sxs-lookup"><span data-stu-id="4d144-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERREUR \_ plus d' \_ Écritures**</span><span class="sxs-lookup"><span data-stu-id="4d144-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="4d144-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-347">Une opération d’e/s série a été effectuée par une autre écriture sur le port série.</span><span class="sxs-lookup"><span data-stu-id="4d144-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="4d144-348">Le compteur de l' \_ XOFF série IOCTL a \_ \_ atteint zéro.)</span><span class="sxs-lookup"><span data-stu-id="4d144-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_ \_ délai d’attente du compteur d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="4d144-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="4d144-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-351">Une opération d’e/s série s’est terminée, car le délai d’attente a expiré.</span><span class="sxs-lookup"><span data-stu-id="4d144-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="4d144-352">Le \_ compteur de série \_ XOFF IOCTL \_ n’a pas atteint zéro.)</span><span class="sxs-lookup"><span data-stu-id="4d144-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERREUR de \_ marque d’ID de disquette \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="4d144-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-355">Aucune marque d’adresse d’ID n’a été trouvée sur la disquette.</span><span class="sxs-lookup"><span data-stu-id="4d144-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERREUR de \_ disque- \_ cylindre incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="4d144-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-358">Discordance entre le champ d’ID de secteur de disquette et l’adresse de piste du contrôleur de disquette.</span><span class="sxs-lookup"><span data-stu-id="4d144-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**erreur de \_ disquette \_ inconnue \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="4d144-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-361">Le contrôleur de disquette a signalé une erreur qui n’est pas reconnue par le pilote de disquette.</span><span class="sxs-lookup"><span data-stu-id="4d144-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**Erreurs de \_ registres de disquettes \_ erronées \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="4d144-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-364">Le contrôleur de disquette a retourné des résultats incohérents dans ses registres.</span><span class="sxs-lookup"><span data-stu-id="4d144-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**échec de l’étalonnage du disque d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="4d144-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-367">Lors de l’accès au disque dur, une opération de recalibrage a échoué, même après une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="4d144-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERREUR Échec de l’opération sur le \_ disque \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="4d144-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-370">Lors de l’accès au disque dur, une opération de disque a échoué même après une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="4d144-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERREUR \_ échec de la \_ réinitialisation du disque \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="4d144-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-373">Lors de l’accès au disque dur, une réinitialisation du contrôleur de disque était nécessaire, mais même cela a échoué.</span><span class="sxs-lookup"><span data-stu-id="4d144-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERREUR \_ FDM de \_ dépassement**</span><span class="sxs-lookup"><span data-stu-id="4d144-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="4d144-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-376">Fin de bande physique rencontrée.</span><span class="sxs-lookup"><span data-stu-id="4d144-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERREUR \_ de \_ mémoire insuffisante sur le \_ serveur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-378">1130 (0x46A)</span><span class="sxs-lookup"><span data-stu-id="4d144-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-379">Mémoire insuffisante sur le serveur pour traiter cette commande.</span><span class="sxs-lookup"><span data-stu-id="4d144-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERREUR \_ possible \_ blocage**</span><span class="sxs-lookup"><span data-stu-id="4d144-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-381">1131 (0x46B)</span><span class="sxs-lookup"><span data-stu-id="4d144-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-382">Une condition potentielle de blocage a été détectée.</span><span class="sxs-lookup"><span data-stu-id="4d144-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERREUR d' \_ \_ alignement mappé**</span><span class="sxs-lookup"><span data-stu-id="4d144-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-384">1132 (0x46C)</span><span class="sxs-lookup"><span data-stu-id="4d144-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-385">L’adresse de base ou le décalage de fichier spécifié n’a pas l’alignement approprié.</span><span class="sxs-lookup"><span data-stu-id="4d144-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERREUR de définition de l' \_ \_ État d’alimentation \_ \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="4d144-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="4d144-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-388">Une tentative de modification de l’état d’alimentation du système a été refusée par une autre application ou un autre pilote.</span><span class="sxs-lookup"><span data-stu-id="4d144-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**échec de définition de l' \_ \_ État d’alimentation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="4d144-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-391">Le BIOS du système n’a pas pu tenter de modifier l’état d’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="4d144-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERREUR \_ d' \_ un trop grand nombre de \_ liens**</span><span class="sxs-lookup"><span data-stu-id="4d144-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="4d144-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-394">Une tentative a été effectuée pour créer davantage de liens sur un fichier que celui pris en charge par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4d144-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERREUR \_ d' \_ ancienne \_ version Win**</span><span class="sxs-lookup"><span data-stu-id="4d144-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-396">1150 (0x47E)</span><span class="sxs-lookup"><span data-stu-id="4d144-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-397">Le programme spécifié requiert une version plus récente de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERREUR \_ de \_ \_ système d’exploitation incorrect**</span><span class="sxs-lookup"><span data-stu-id="4d144-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-399">1151 (0x47F)</span><span class="sxs-lookup"><span data-stu-id="4d144-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-400">Le programme spécifié n'est pas un programme Windows ou MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="4d144-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**\_application à \_ instance \_ unique d’erreur**</span><span class="sxs-lookup"><span data-stu-id="4d144-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="4d144-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-403">Impossible de démarrer plusieurs instances du programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="4d144-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERREUR \_ d' \_ application RMODE**</span><span class="sxs-lookup"><span data-stu-id="4d144-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="4d144-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-406">Le programme spécifié a été écrit pour une version antérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERREUR \_ dll non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="4d144-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-409">L’un des fichiers de bibliothèque requis pour exécuter cette application est endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERREUR \_ aucune \_ Association**</span><span class="sxs-lookup"><span data-stu-id="4d144-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="4d144-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-412">Aucune application n’est associée au fichier spécifié pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="4d144-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERREUR \_ DDE \_ échec**</span><span class="sxs-lookup"><span data-stu-id="4d144-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="4d144-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-415">Une erreur s’est produite lors de l’envoi de la commande à l’application.</span><span class="sxs-lookup"><span data-stu-id="4d144-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_dll d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="4d144-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-418">L’un des fichiers de bibliothèque requis pour exécuter cette application est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4d144-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERREUR \_ \_ plus de \_ \_ Handles utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4d144-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="4d144-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-421">Le processus en cours a utilisé toute l’allocation système des descripteurs pour les objets du gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="4d144-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**synchronisation des messages d’erreur \_ \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="4d144-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="4d144-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-424">Le message ne peut être utilisé qu’avec des opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="4d144-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_élément source d’erreur \_ \_ vide**</span><span class="sxs-lookup"><span data-stu-id="4d144-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="4d144-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-427">L’élément source indiqué n’a pas de support.</span><span class="sxs-lookup"><span data-stu-id="4d144-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERREUR de l' \_ élément de destination \_ \_ complet**</span><span class="sxs-lookup"><span data-stu-id="4d144-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="4d144-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-430">L’élément de destination indiqué contient déjà un média.</span><span class="sxs-lookup"><span data-stu-id="4d144-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERREUR \_ d' \_ adresse d’élément non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-432">1162 (0x48A)</span><span class="sxs-lookup"><span data-stu-id="4d144-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-433">L’élément indiqué n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERREUR \_ magazine \_ \_ absente**</span><span class="sxs-lookup"><span data-stu-id="4d144-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-435">1163 (0x48B)</span><span class="sxs-lookup"><span data-stu-id="4d144-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-436">L’élément indiqué fait partie d’un magazine qui n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="4d144-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERREUR \_ de \_ réinitialisation de périphérique \_ requise**</span><span class="sxs-lookup"><span data-stu-id="4d144-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-438">1164 (0x48C)</span><span class="sxs-lookup"><span data-stu-id="4d144-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-439">L’appareil indiqué requiert une réinitialisation en raison d’erreurs matérielles.</span><span class="sxs-lookup"><span data-stu-id="4d144-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**l' \_ appareil d’erreur \_ nécessite un \_ nettoyage**</span><span class="sxs-lookup"><span data-stu-id="4d144-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-441">1165 (0x48D)</span><span class="sxs-lookup"><span data-stu-id="4d144-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-442">L’appareil a indiqué que le nettoyage est nécessaire avant toute tentative d’opérations.</span><span class="sxs-lookup"><span data-stu-id="4d144-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERREUR d’ouverture de la \_ porte du périphérique \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-444">1166 (0x48E)</span><span class="sxs-lookup"><span data-stu-id="4d144-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-445">L’appareil a indiqué que sa porte est ouverte.</span><span class="sxs-lookup"><span data-stu-id="4d144-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**périphérique d’erreur \_ \_ non \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="4d144-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-447">1167 (0x48F)</span><span class="sxs-lookup"><span data-stu-id="4d144-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-448">L’appareil n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="4d144-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERREUR \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="4d144-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-451">Element not found.</span><span class="sxs-lookup"><span data-stu-id="4d144-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERREUR \_ aucune \_ correspondance**</span><span class="sxs-lookup"><span data-stu-id="4d144-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="4d144-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-454">Aucune correspondance n’a été trouvée pour la clé spécifiée dans l’index.</span><span class="sxs-lookup"><span data-stu-id="4d144-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERREUR \_ de \_ jeu \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="4d144-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-457">Le jeu de propriétés spécifié n’existe pas sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="4d144-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_point d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="4d144-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-460">Le point passé à GetMouseMovePoints n’est pas dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4d144-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERREUR \_ aucun \_ service de suivi \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="4d144-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-463">Le service de suivi (station de travail) n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4d144-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERREUR \_ aucun \_ ID de volume \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="4d144-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-466">L’ID de volume est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4d144-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERREUR \_ Impossible \_ de \_ supprimer le \_ remplacement**</span><span class="sxs-lookup"><span data-stu-id="4d144-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="4d144-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-469">Impossible de supprimer le fichier à remplacer.</span><span class="sxs-lookup"><span data-stu-id="4d144-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERREUR \_ Impossible \_ de \_ déplacer le \_ remplacement**</span><span class="sxs-lookup"><span data-stu-id="4d144-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="4d144-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-472">Impossible de déplacer le fichier de remplacement dans le fichier à remplacer.</span><span class="sxs-lookup"><span data-stu-id="4d144-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="4d144-473">Le fichier à remplacer a conservé son nom d’origine.</span><span class="sxs-lookup"><span data-stu-id="4d144-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERREUR \_ Impossible \_ de \_ déplacer le \_ remplacement \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4d144-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="4d144-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-476">Impossible de déplacer le fichier de remplacement dans le fichier à remplacer.</span><span class="sxs-lookup"><span data-stu-id="4d144-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="4d144-477">Le fichier à remplacer a été renommé à l’aide du nom de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="4d144-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ suppression du journal \_ des erreurs en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="4d144-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-479">1178 (0x49A)</span><span class="sxs-lookup"><span data-stu-id="4d144-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-480">Le journal de modification du volume est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4d144-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**\_Journal des \_ Erreurs \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="4d144-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-482">1179 (0x49B)</span><span class="sxs-lookup"><span data-stu-id="4d144-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-483">Le journal des modifications de volume n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="4d144-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_fichier potentiel d’erreur \_ \_ trouvé**</span><span class="sxs-lookup"><span data-stu-id="4d144-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-485">1180 (0x49C)</span><span class="sxs-lookup"><span data-stu-id="4d144-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-486">Un fichier a été trouvé, mais il n’est peut-être pas le bon fichier.</span><span class="sxs-lookup"><span data-stu-id="4d144-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrée du journal des erreurs \_ \_ \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="4d144-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-488">1181 (0x49D)</span><span class="sxs-lookup"><span data-stu-id="4d144-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-489">L’entrée du journal a été supprimée du journal.</span><span class="sxs-lookup"><span data-stu-id="4d144-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**l’arrêt de l’erreur \_ \_ est \_ planifié**</span><span class="sxs-lookup"><span data-stu-id="4d144-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-491">1190 (0x4A6)</span><span class="sxs-lookup"><span data-stu-id="4d144-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-492">Un arrêt du système a déjà été planifié.</span><span class="sxs-lookup"><span data-stu-id="4d144-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**erreur \_ lors \_ de l’arrêt \_ des utilisateurs connectés \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-494">1191 (0x4A7)</span><span class="sxs-lookup"><span data-stu-id="4d144-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-495">Impossible d’initier l’arrêt du système, car d’autres utilisateurs sont connectés à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4d144-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERREUR \_ de \_ périphérique incorrect**</span><span class="sxs-lookup"><span data-stu-id="4d144-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-497">1200 (0x4B0)</span><span class="sxs-lookup"><span data-stu-id="4d144-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-498">Le nom d’appareil spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERREUR de \_ connexion \_ indispo.**</span><span class="sxs-lookup"><span data-stu-id="4d144-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-500">1201 (0x4B1)</span><span class="sxs-lookup"><span data-stu-id="4d144-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-501">L’appareil n’est pas connecté actuellement, mais il s’agit d’une connexion mémorisée.</span><span class="sxs-lookup"><span data-stu-id="4d144-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERREUR de l' \_ appareil \_ déjà \_ mémorisé**</span><span class="sxs-lookup"><span data-stu-id="4d144-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-503">1202 (0x4B2)</span><span class="sxs-lookup"><span data-stu-id="4d144-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-504">Le nom de l’appareil local a une connexion mémorisée à une autre ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERREUR \_ non \_ NET \_ ou \_ \_ chemin d’accès incorrect**</span><span class="sxs-lookup"><span data-stu-id="4d144-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-506">1203 (0x4B3)</span><span class="sxs-lookup"><span data-stu-id="4d144-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-507">Le chemin d’accès réseau n’a pas été correctement tapé, n’existe pas ou le fournisseur réseau n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="4d144-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="4d144-508">Essayez de retaper le chemin d’accès ou contactez votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERREUR \_ fournisseur incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-510">1204 (0x4B4)</span><span class="sxs-lookup"><span data-stu-id="4d144-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-511">Le nom du fournisseur réseau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERREUR \_ Impossible d' \_ ouvrir le \_ profil**</span><span class="sxs-lookup"><span data-stu-id="4d144-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-513">1205 (0x4B5)</span><span class="sxs-lookup"><span data-stu-id="4d144-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-514">Impossible d’ouvrir le profil de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERREUR \_ de \_ Profil incorrect**</span><span class="sxs-lookup"><span data-stu-id="4d144-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-516">1206 (0x4B6)</span><span class="sxs-lookup"><span data-stu-id="4d144-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-517">Le profil de connexion réseau est endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERREUR \_ non \_ conteneur**</span><span class="sxs-lookup"><span data-stu-id="4d144-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-519">1207 (0x4B7)</span><span class="sxs-lookup"><span data-stu-id="4d144-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-520">Impossible d’énumérer un non-conteneur.</span><span class="sxs-lookup"><span data-stu-id="4d144-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**erreur \_ étendue d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-522">1208 (0x4B8)</span><span class="sxs-lookup"><span data-stu-id="4d144-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-523">Une erreur étendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4d144-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERREUR \_ GroupName non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-525">1209 (0x4B9)</span><span class="sxs-lookup"><span data-stu-id="4d144-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-526">Le format du nom de groupe spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERREUR \_ ComputerName non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-528">1210 (0x4BA)</span><span class="sxs-lookup"><span data-stu-id="4d144-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-529">Le format du nom d’ordinateur spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERREUR \_ NomÉvénement non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-531">1211 (0x4BB)</span><span class="sxs-lookup"><span data-stu-id="4d144-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-532">Le format du nom d’événement spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERREUR \_ nomdomaine non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-534">1212 (0x4BC)</span><span class="sxs-lookup"><span data-stu-id="4d144-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-535">Le format du nom de domaine spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERREUR \_ ServiceName non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-537">1213 (0x4BD)</span><span class="sxs-lookup"><span data-stu-id="4d144-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-538">Le format du nom de service spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERREUR \_ \_ NetName non valide**</span><span class="sxs-lookup"><span data-stu-id="4d144-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-540">1214 (0x4BE)</span><span class="sxs-lookup"><span data-stu-id="4d144-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-541">Le format du nom réseau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERREUR \_ de \_ Nom_Partage non valide**</span><span class="sxs-lookup"><span data-stu-id="4d144-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-543">1215 (0x4BF)</span><span class="sxs-lookup"><span data-stu-id="4d144-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-544">Le format du nom de partage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERREUR \_ PASSWORDNAME non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-546">1216 (0x4C0)</span><span class="sxs-lookup"><span data-stu-id="4d144-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-547">Le format du mot de passe spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERREUR \_ MESSAGENAME non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-549">1217 (0x4C1)</span><span class="sxs-lookup"><span data-stu-id="4d144-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-550">Le format du nom du message spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERREUR \_ MESSAGEDEST non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-552">1218 (0x4C2)</span><span class="sxs-lookup"><span data-stu-id="4d144-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-553">Le format de la destination de message spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERREUR \_ de \_ conflit d’informations d’identification de session \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-555">1219 (0x4C3)</span><span class="sxs-lookup"><span data-stu-id="4d144-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-556">L’utilisation de plusieurs connexions à un serveur ou à une ressource partagée par le même utilisateur, à l’aide de plusieurs noms d’utilisateur, n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="4d144-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="4d144-557">Déconnectez toutes les connexions précédentes au serveur ou à la ressource partagée, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="4d144-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERREUR \_ limite de session à distance \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="4d144-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-559">1220 (0x4C4)</span><span class="sxs-lookup"><span data-stu-id="4d144-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-560">Une tentative a été effectuée pour établir une session sur un serveur réseau, mais il existe déjà trop de sessions établies sur ce serveur.</span><span class="sxs-lookup"><span data-stu-id="4d144-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERREUR \_ DUP \_ nomdomaine**</span><span class="sxs-lookup"><span data-stu-id="4d144-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-562">1221 (0x4C5)</span><span class="sxs-lookup"><span data-stu-id="4d144-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-563">Le groupe de travail ou le nom de domaine est déjà utilisé par un autre ordinateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERREUR \_ aucun \_ réseau**</span><span class="sxs-lookup"><span data-stu-id="4d144-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-565">1222 (0x4C6)</span><span class="sxs-lookup"><span data-stu-id="4d144-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-566">Le réseau n’est pas présent ou n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="4d144-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERREUR \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="4d144-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-568">1223 (0x4C7)</span><span class="sxs-lookup"><span data-stu-id="4d144-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-569">L’opération a été annulée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d144-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERREUR \_ \_ fichier mappé utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-571">1224 (0x4C8)</span><span class="sxs-lookup"><span data-stu-id="4d144-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-572">L’opération demandée ne peut pas être effectuée sur un fichier dont la section mappée par l’utilisateur est ouverte.</span><span class="sxs-lookup"><span data-stu-id="4d144-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERREUR de \_ connexion \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="4d144-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-574">1225 (0x4C9)</span><span class="sxs-lookup"><span data-stu-id="4d144-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-575">L’ordinateur distant a refusé la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERREUR \_ de \_ déconnexion normale**</span><span class="sxs-lookup"><span data-stu-id="4d144-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-577">1226 (0x4CA)</span><span class="sxs-lookup"><span data-stu-id="4d144-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-578">La connexion réseau a été fermée normalement.</span><span class="sxs-lookup"><span data-stu-id="4d144-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**adresse d’erreur \_ \_ déjà \_ associée**</span><span class="sxs-lookup"><span data-stu-id="4d144-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-580">1227 (0x4CB)</span><span class="sxs-lookup"><span data-stu-id="4d144-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-581">Un point de terminaison de transport réseau est déjà associé à une adresse.</span><span class="sxs-lookup"><span data-stu-id="4d144-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**adresse d’erreur \_ \_ non \_ associée**</span><span class="sxs-lookup"><span data-stu-id="4d144-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-583">1228 (0x4CC)</span><span class="sxs-lookup"><span data-stu-id="4d144-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-584">Une adresse n’a pas encore été associée au point de terminaison réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**connexion d’erreur \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="4d144-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-586">1229 (0x4CD)</span><span class="sxs-lookup"><span data-stu-id="4d144-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-587">Une opération a été tentée sur une connexion réseau inexistante.</span><span class="sxs-lookup"><span data-stu-id="4d144-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**connexion d’erreur \_ \_ active**</span><span class="sxs-lookup"><span data-stu-id="4d144-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-589">1230 (0x4CE)</span><span class="sxs-lookup"><span data-stu-id="4d144-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-590">Une opération non valide a été tentée sur une connexion réseau active.</span><span class="sxs-lookup"><span data-stu-id="4d144-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERREUR \_ réseau \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4d144-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-592">1231 (0x4CF)</span><span class="sxs-lookup"><span data-stu-id="4d144-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-593">L’emplacement réseau ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="4d144-593">The network location cannot be reached.</span></span> <span data-ttu-id="4d144-594">Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**hôte d’erreur \_ \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4d144-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-596">1232 (0x4D0)</span><span class="sxs-lookup"><span data-stu-id="4d144-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-597">L’emplacement réseau ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="4d144-597">The network location cannot be reached.</span></span> <span data-ttu-id="4d144-598">Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**protocole d’erreur \_ \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4d144-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-600">1233 (0x4D1)</span><span class="sxs-lookup"><span data-stu-id="4d144-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-601">L’emplacement réseau ne peut pas être atteint.</span><span class="sxs-lookup"><span data-stu-id="4d144-601">The network location cannot be reached.</span></span> <span data-ttu-id="4d144-602">Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**PORT d’erreur \_ \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="4d144-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-604">1234 (0x4D2)</span><span class="sxs-lookup"><span data-stu-id="4d144-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-605">Aucun service ne fonctionne sur le point de terminaison du réseau de destination sur le système distant.</span><span class="sxs-lookup"><span data-stu-id="4d144-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**demande d’erreur \_ \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="4d144-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-607">1235 (0x4D3)</span><span class="sxs-lookup"><span data-stu-id="4d144-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-608">La demande a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="4d144-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERREUR de \_ connexion \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="4d144-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-610">1236 (0x4D4)</span><span class="sxs-lookup"><span data-stu-id="4d144-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-611">La connexion réseau a été abandonnée par le système local.</span><span class="sxs-lookup"><span data-stu-id="4d144-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**\_nouvelle tentative d’erreur**</span><span class="sxs-lookup"><span data-stu-id="4d144-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-613">1237 (0x4D5)</span><span class="sxs-lookup"><span data-stu-id="4d144-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-614">L'opération n'a pas pu être terminée.</span><span class="sxs-lookup"><span data-stu-id="4d144-614">The operation could not be completed.</span></span> <span data-ttu-id="4d144-615">Une nouvelle tentative doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="4d144-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_limite du \_ nombre de connexions d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-617">1238 (0x4D6)</span><span class="sxs-lookup"><span data-stu-id="4d144-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-618">Une connexion au serveur n’a pas pu être établie, car la limite du nombre de connexions simultanées pour ce compte a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="4d144-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_restriction d' \_ heure de connexion d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-620">1239 (0x4D7)</span><span class="sxs-lookup"><span data-stu-id="4d144-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-621">Tentative de connexion pendant une période de temps non autorisée pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="4d144-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERREUR de \_ connexion wksta de connexion \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-623">1240 (0x4D8)</span><span class="sxs-lookup"><span data-stu-id="4d144-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-624">Le compte n’est pas autorisé à se connecter à partir de cette station.</span><span class="sxs-lookup"><span data-stu-id="4d144-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERREUR d' \_ adresse incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-626">1241 (0x4D9)</span><span class="sxs-lookup"><span data-stu-id="4d144-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-627">L’adresse réseau n’a pas pu être utilisée pour l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="4d144-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERREUR \_ déjà \_ inscrite**</span><span class="sxs-lookup"><span data-stu-id="4d144-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-629">1242 (0x4DA)</span><span class="sxs-lookup"><span data-stu-id="4d144-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-630">Le service est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="4d144-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_service d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="4d144-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-632">1243 (0x4DB)</span><span class="sxs-lookup"><span data-stu-id="4d144-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-633">Le service spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERREUR \_ non \_ authentifiée**</span><span class="sxs-lookup"><span data-stu-id="4d144-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-635">1244 (0x4DC)</span><span class="sxs-lookup"><span data-stu-id="4d144-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-636">L’opération demandée n’a pas été effectuée car l’utilisateur n’a pas été authentifié.</span><span class="sxs-lookup"><span data-stu-id="4d144-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERREUR \_ non \_ connectée \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-638">1245 (0x4DD)</span><span class="sxs-lookup"><span data-stu-id="4d144-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-639">L’opération demandée n’a pas été effectuée car l’utilisateur ne s’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="4d144-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="4d144-640">Le service spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**l’erreur se \_ poursuit**</span><span class="sxs-lookup"><span data-stu-id="4d144-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-642">1246 (0x4DE)</span><span class="sxs-lookup"><span data-stu-id="4d144-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-643">Poursuivez le travail en cours.</span><span class="sxs-lookup"><span data-stu-id="4d144-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERREUR \_ déjà \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="4d144-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-645">1247 (0x4DF)</span><span class="sxs-lookup"><span data-stu-id="4d144-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-646">Une tentative a été effectuée pour effectuer une opération d’initialisation alors que l’initialisation a déjà été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4d144-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERREUR \_ \_ plus aucun \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="4d144-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-648">1248 (0x4E0)</span><span class="sxs-lookup"><span data-stu-id="4d144-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-649">Il n’y a plus d’appareils locaux.</span><span class="sxs-lookup"><span data-stu-id="4d144-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERREUR \_ aucun \_ site de ce type \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-651">1249 (0x4E1)</span><span class="sxs-lookup"><span data-stu-id="4d144-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-652">Le site spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**le \_ contrôleur de domaine d’erreur \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="4d144-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-654">1250 (0x4E2)</span><span class="sxs-lookup"><span data-stu-id="4d144-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-655">Un contrôleur de domaine portant le nom spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4d144-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERREUR \_ uniquement \_ si \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="4d144-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-657">1251 (0x4E3)</span><span class="sxs-lookup"><span data-stu-id="4d144-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-658">Cette opération est prise en charge uniquement lorsque vous êtes connecté au serveur.</span><span class="sxs-lookup"><span data-stu-id="4d144-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERREUR lors du \_ remplacement des \_ nochanges**</span><span class="sxs-lookup"><span data-stu-id="4d144-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-660">1252 (0x4E4)</span><span class="sxs-lookup"><span data-stu-id="4d144-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-661">L’infrastructure de stratégie de groupe doit appeler l’extension même si aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="4d144-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERREUR \_ de \_ profil utilisateur incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-663">1253 (0x4E5)</span><span class="sxs-lookup"><span data-stu-id="4d144-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-664">L’utilisateur spécifié n’a pas de profil valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERREUR \_ non \_ prise en charge \_ sur \_ SBS**</span><span class="sxs-lookup"><span data-stu-id="4d144-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-666">1254 (0x4E6)</span><span class="sxs-lookup"><span data-stu-id="4d144-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-667">Cette opération n’est pas prise en charge sur un ordinateur exécutant Windows Server 2003 pour Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="4d144-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**\_ \_ arrêt du serveur \_ d’erreur en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="4d144-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-669">1255 (0x4E7)</span><span class="sxs-lookup"><span data-stu-id="4d144-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-670">L’ordinateur serveur est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4d144-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERREUR de l' \_ hôte \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-672">1256 (0x4E8)</span><span class="sxs-lookup"><span data-stu-id="4d144-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-673">Le système distant n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="4d144-673">The remote system is not available.</span></span> <span data-ttu-id="4d144-674">Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d144-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERREUR \_ \_ sid sans compte \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-676">1257 (0x4E9)</span><span class="sxs-lookup"><span data-stu-id="4d144-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-677">L’identificateur de sécurité fourni ne provient pas d’un domaine de compte.</span><span class="sxs-lookup"><span data-stu-id="4d144-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERREUR \_ non liée au \_ \_ sid**</span><span class="sxs-lookup"><span data-stu-id="4d144-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-679">1258 (0x4EA)</span><span class="sxs-lookup"><span data-stu-id="4d144-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-680">L’identificateur de sécurité fourni n’a pas de composant de domaine.</span><span class="sxs-lookup"><span data-stu-id="4d144-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERREUR \_ APPHELP, \_ bloc**</span><span class="sxs-lookup"><span data-stu-id="4d144-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-682">1259 (0x4EB)</span><span class="sxs-lookup"><span data-stu-id="4d144-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-683">La boîte de dialogue AppHelp a été annulée, ce qui empêche le démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="4d144-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_accès aux erreurs \_ désactivé par la \_ \_ stratégie**</span><span class="sxs-lookup"><span data-stu-id="4d144-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-685">1260 (0x4EC)</span><span class="sxs-lookup"><span data-stu-id="4d144-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-686">Ce programme est bloqué par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4d144-686">This program is blocked by group policy.</span></span> <span data-ttu-id="4d144-687">Pour plus d’informations, contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="4d144-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERREUR \_ de \_ consommation NAT reg \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-689">1261 (0x4ED)</span><span class="sxs-lookup"><span data-stu-id="4d144-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-690">Un programme tente d’utiliser une valeur de Registre non valide.</span><span class="sxs-lookup"><span data-stu-id="4d144-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="4d144-691">Normalement dû à un registre non initialisé.</span><span class="sxs-lookup"><span data-stu-id="4d144-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="4d144-692">Cette erreur est spécifique à Itanium.</span><span class="sxs-lookup"><span data-stu-id="4d144-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERREUR \_ CSCSHARE \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4d144-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-694">1262 (0x4EE)</span><span class="sxs-lookup"><span data-stu-id="4d144-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-695">Le partage est actuellement hors connexion ou n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4d144-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERREUR \_ PKINIT en \_ échec**</span><span class="sxs-lookup"><span data-stu-id="4d144-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-697">1263 (0x4EF)</span><span class="sxs-lookup"><span data-stu-id="4d144-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-698">Le protocole Kerberos a rencontré une erreur lors de la validation du certificat KDC lors de la connexion par carte à puce.</span><span class="sxs-lookup"><span data-stu-id="4d144-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="4d144-699">Le journal des événements système contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4d144-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERREUR \_ de \_ défaillance du sous-système de la carte à puce \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-701">1264 (0x4F0)</span><span class="sxs-lookup"><span data-stu-id="4d144-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-702">Le protocole Kerberos a rencontré une erreur lors de la tentative d’utilisation du sous-système de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="4d144-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERREUR de \_ rétrogradation \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="4d144-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-704">1265 (0x4F1)</span><span class="sxs-lookup"><span data-stu-id="4d144-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-705">Le système ne peut pas contacter un contrôleur de domaine pour traiter la demande d’authentification.</span><span class="sxs-lookup"><span data-stu-id="4d144-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="4d144-706">Veuillez réessayer plus tard.</span><span class="sxs-lookup"><span data-stu-id="4d144-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERREUR de verrouillage de l' \_ ordinateur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-708">1271 (0x4F7)</span><span class="sxs-lookup"><span data-stu-id="4d144-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-709">L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option forcer.</span><span class="sxs-lookup"><span data-stu-id="4d144-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**le rappel d’erreur a \_ \_ fourni des \_ données non valides \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-711">1273 (0x4F9)</span><span class="sxs-lookup"><span data-stu-id="4d144-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-712">Un rappel défini par l’application a donné des données non valides lorsqu’il est appelé.</span><span class="sxs-lookup"><span data-stu-id="4d144-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERREUR de \_ synchronisation de \_ premier plan \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="4d144-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-714">1274 (0x4FA)</span><span class="sxs-lookup"><span data-stu-id="4d144-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-715">L’infrastructure de stratégie de groupe doit appeler l’extension dans l’actualisation synchrone de la stratégie de premier plan.</span><span class="sxs-lookup"><span data-stu-id="4d144-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**pilote d’erreur \_ \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="4d144-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-717">1275 (0x4FB)</span><span class="sxs-lookup"><span data-stu-id="4d144-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-718">Le chargement de ce pilote a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="4d144-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**erreur \_ lors \_ de l’importation \_ d’une \_ \_ dll non valide**</span><span class="sxs-lookup"><span data-stu-id="4d144-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-720">1276 (0x4FC)</span><span class="sxs-lookup"><span data-stu-id="4d144-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-721">Une bibliothèque de liens dynamiques (DLL) a référencé un module qui n’était ni une DLL ni l’image exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="4d144-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_WebBlade désactivé pour l’accès aux erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-723">1277 (0x4FD)</span><span class="sxs-lookup"><span data-stu-id="4d144-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-724">Windows ne peut pas ouvrir ce programme, car il a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="4d144-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERREUR d' \_ accès à la \_ \_ WebBlade désactivée pour l’accès \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-726">1278 (0x4FE)</span><span class="sxs-lookup"><span data-stu-id="4d144-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-727">Windows ne peut pas ouvrir ce programme, car le système d’application de la licence a été falsifié ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="4d144-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**échec de la récupération d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-729">1279 (0x4FF)</span><span class="sxs-lookup"><span data-stu-id="4d144-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-730">Une récupération de transaction a échoué.</span><span class="sxs-lookup"><span data-stu-id="4d144-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERREUR \_ déjà \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="4d144-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="4d144-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-733">Le thread actuel a déjà été converti en fibre.</span><span class="sxs-lookup"><span data-stu-id="4d144-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERREUR \_ déjà \_ thread**</span><span class="sxs-lookup"><span data-stu-id="4d144-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="4d144-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-736">Le thread actuel a déjà été converti à partir d’une fibre.</span><span class="sxs-lookup"><span data-stu-id="4d144-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_dépassement de \_ mémoire tampon \_ de la pile d’erreur**</span><span class="sxs-lookup"><span data-stu-id="4d144-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="4d144-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-739">Le système a détecté un dépassement de mémoire tampon basée sur la pile dans cette application.</span><span class="sxs-lookup"><span data-stu-id="4d144-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="4d144-740">Ce dépassement peut permettre à un utilisateur malveillant de prendre le contrôle de cette application.</span><span class="sxs-lookup"><span data-stu-id="4d144-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**QUOTA de paramètres d’erreur \_ \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="4d144-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="4d144-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-743">Les données présentes dans l’un des paramètres sont plus que la fonction peut fonctionner sur.</span><span class="sxs-lookup"><span data-stu-id="4d144-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**débogueur d’erreur \_ \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="4d144-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="4d144-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-746">Une tentative d’exécution d’une opération sur un objet de débogage a échoué, car l’objet est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4d144-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**\_échec du \_ chargement du délai d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="4d144-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-749">Une tentative de retarder le chargement d’un fichier. dll ou l’extraction d’une adresse de fonction dans un fichier. dll à chargement différé a échoué.</span><span class="sxs-lookup"><span data-stu-id="4d144-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERREUR \_ VDM non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="4d144-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="4d144-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-752">%1 est une application 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4d144-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="4d144-753">Vous ne disposez pas des autorisations nécessaires pour exécuter des applications 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4d144-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="4d144-754">Vérifiez vos autorisations avec votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="4d144-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**erreur non \_ identifiée \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="4d144-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-757">Des informations insuffisantes existent pour identifier la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="4d144-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERREUR \_ de \_ paramètre CRUNTIME non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="4d144-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-760">Le paramètre passé à une fonction Runtime C est incorrect.</span><span class="sxs-lookup"><span data-stu-id="4d144-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERREUR \_ au-delà de \_ VDL**</span><span class="sxs-lookup"><span data-stu-id="4d144-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="4d144-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-763">L’opération s’est produite au-delà de la longueur de données valide du fichier.</span><span class="sxs-lookup"><span data-stu-id="4d144-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERREUR de \_ type de SID de service INcompatible \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="4d144-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-766">Le démarrage du service a échoué car un ou plusieurs services du même processus ont un paramètre de type de SID de service incompatible.</span><span class="sxs-lookup"><span data-stu-id="4d144-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="4d144-767">Un service avec un type de SID de service restreint ne peut coexister que dans le même processus avec d’autres services avec un type de SID restreint.</span><span class="sxs-lookup"><span data-stu-id="4d144-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="4d144-768">Si le type de SID de service de ce service vient d’être configuré, le processus d’hébergement doit être redémarré pour pouvoir démarrer ce service.</span><span class="sxs-lookup"><span data-stu-id="4d144-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="4d144-769">Sur Windows Server 2003 et Windows XP, un service non restreint ne peut pas coexister dans le même processus avec d’autres services.</span><span class="sxs-lookup"><span data-stu-id="4d144-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="4d144-770">Le service avec le type de SID de service non restreint doit être déplacé vers un processus détenu pour pouvoir démarrer ce service.</span><span class="sxs-lookup"><span data-stu-id="4d144-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**\_arrêt du \_ processus de pilote d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="4d144-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-773">Le processus qui héberge le pilote de cet appareil a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="4d144-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite d’implémentation d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="4d144-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-776">Une opération a tenté de dépasser une limite définie par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4d144-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**le \_ processus d’erreur \_ est \_ protégé**</span><span class="sxs-lookup"><span data-stu-id="4d144-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="4d144-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-779">Soit le processus cible, soit le processus conteneur du thread cible, est un processus protégé.</span><span class="sxs-lookup"><span data-stu-id="4d144-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERREUR de \_ service de notification de \_ \_ retard du client \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="4d144-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-782">Le client de notification de service est trop en retard par rapport à l’état actuel des services de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4d144-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**QUOTA de disque d’erreur \_ \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="4d144-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="4d144-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-785">L’opération de fichier demandée a échoué, car le quota de stockage a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="4d144-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="4d144-786">Pour libérer de l’espace disque, déplacez les fichiers vers un autre emplacement ou supprimez les fichiers inutiles.</span><span class="sxs-lookup"><span data-stu-id="4d144-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="4d144-787">Pour plus d’informations, contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="4d144-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**contenu de l’erreur \_ \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="4d144-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="4d144-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-790">L’opération de fichier demandée a échoué, car la stratégie de stockage bloque ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="4d144-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="4d144-791">Pour plus d’informations, contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="4d144-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**privilège de service d’erreur \_ INcompatible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="4d144-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-794">Un privilège requis par le service pour fonctionner correctement n’existe pas dans la configuration du compte de service.</span><span class="sxs-lookup"><span data-stu-id="4d144-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="4d144-795">Vous pouvez utiliser le composant logiciel enfichable MMC (Microsoft Management Console) des services (services. msc) et le composant logiciel enfichable MMC paramètres de sécurité locale (secpol. msc) pour afficher la configuration du service et la configuration du compte.</span><span class="sxs-lookup"><span data-stu-id="4d144-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERREUR de blocage de l' \_ application \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="4d144-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-798">Un thread impliqué dans cette opération semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="4d144-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d144-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**étiquette d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="4d144-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d144-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="4d144-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="4d144-801">Indique qu’un ID de sécurité particulier ne peut pas être assigné en tant qu’étiquette d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4d144-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="4d144-802">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d144-802">Requirements</span></span>



| <span data-ttu-id="4d144-803">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d144-803">Requirement</span></span> | <span data-ttu-id="4d144-804">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d144-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d144-805">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d144-805">Minimum supported client</span></span><br/> | <span data-ttu-id="4d144-806">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d144-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d144-807">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d144-807">Minimum supported server</span></span><br/> | <span data-ttu-id="4d144-808">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d144-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d144-809">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d144-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d144-810"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d144-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d144-811">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d144-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d144-812">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="4d144-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





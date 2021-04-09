---
description: Décrit les codes d’erreur 4000-5999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Codes d’erreur système (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110775"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="5cd8f-103">Codes d’erreur système (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="5cd8f-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="5cd8f-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5cd8f-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="5cd8f-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 4000 à 5999.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="5cd8f-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="5cd8f-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="5cd8f-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERREUR de \_ WINS \_ interne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-110">4000 (0xFA0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-111">WINS a rencontré une erreur lors du traitement de la commande.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERREUR \_ \_ Impossible de \_ del \_ \_ WINS local**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-113">4001 (0xFA1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-114">Le WINS local ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**\_init statique d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-116">4002 (0xFA2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-117">L’importation à partir du fichier a échoué.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**sauvegarde d’erreur \_ Inc. \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-119">4003 (0xFA3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-120">La sauvegarde a échoué.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-120">The backup failed.</span></span> <span data-ttu-id="5cd8f-121">Une sauvegarde complète a-t-elle été effectuée avant ?</span><span class="sxs-lookup"><span data-stu-id="5cd8f-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_sauvegarde complète de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-123">4004 (0xFA4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-124">La sauvegarde a échoué.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-124">The backup failed.</span></span> <span data-ttu-id="5cd8f-125">Vérifiez le répertoire dans lequel vous sauvegardez la base de données.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**enregistrement d’erreur \_ \_ non \_ existant**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-127">4005 (0xFA5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-128">Le nom n’existe pas dans la base de données WINS.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERREUR \_ RPL \_ non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-130">4006 (0xFA6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-131">La réplication avec un partenaire non configuré n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**erreur PEERDIST- \_ \_ version de CONTENTINFO \_ \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-133">4050 (0xFD2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-134">La version des informations de contenu fournies n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_erreur PEERDIST \_ Impossible d' \_ analyser \_ CONTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-136">4051 (0xFD3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-137">Les informations de contenu fournies sont incorrectes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_erreur PEERDIST \_ données manquantes \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-139">4052 (0xFD4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-140">Les données demandées sont introuvables dans les caches locaux ou d’homologue.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_erreur PEERDIST \_ - \_ plus**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-142">4053 (0xFD5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-143">Aucune donnée supplémentaire n’est disponible ou requise.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_erreur PEERDIST \_ non \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-145">4054 (0xFD6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-146">L’objet fourni n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_erreur PEERDIST \_ déjà \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-148">4055 (0xFD7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-149">L’objet fourni a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ arrêt \_ de l’erreur PEERDIST en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-151">4056 (0xFD8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-152">Une opération d’arrêt est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_erreur PEERDIST \_ invalidée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-154">4057 (0xFD9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-155">L’objet fourni a déjà été invalidé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**l' \_ erreur \_ PEERDIST \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-157">4058 (0xFDA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-158">Un élément existe déjà et n’a pas été remplacé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_opération d’erreur PEERDIST \_ \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-160">4059 (0xFDB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-161">Impossible d’annuler l’opération demandée, car elle est déjà terminée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_erreur PEERDIST \_ déjà \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-163">4060 (0xFDC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-164">Impossible d’effectuer l’opération variante requise, car elle a déjà été exécutée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_erreur PEERDIST \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-166">4061 (0xFDD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-167">Une opération a accédé à des données au-delà des limites des données valides.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_version d’erreur PEERDIST \_ \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-169">4062 (0xFDE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-170">La version demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_erreur PEERDIST \_ configuration non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-172">4063 (0xFDF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-173">Une valeur de configuration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_erreur PEERDIST \_ non \_ concédée sous licence**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-175">4064 (0xFE0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-176">La référence SKU n’est pas sous licence.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_service d’erreur PEERDIST \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-178">4065 (0xFE1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-179">Le service PeerDist est toujours en cours d’initialisation et sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**échec de l' \_ approbation des erreurs PEERDIST \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-181">4066 (0xFE2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-182">La communication avec un ou plusieurs ordinateurs sera temporairement bloquée en raison d’erreurs récentes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERREUR \_ de \_ conflit d’adresses DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-185">Le client DHCP a obtenu une adresse IP qui est déjà en cours d’utilisation sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="5cd8f-186">L’interface locale sera désactivée jusqu’à ce que le client DHCP puisse obtenir une nouvelle adresse.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERREUR \_ \_ GUID WMI \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-189">Le GUID passé n’a pas été reconnu comme valide par un fournisseur de données WMI.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERREUR \_ l' \_ instance WMI est \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-192">Le nom d’instance passé n’a pas été reconnu comme valide par un fournisseur de données WMI.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERREUR \_ WMI \_ ID d’ID de service \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-194">4202 (0x106A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-195">L’ID d’élément de données passé n’a pas été reconnu comme valide par un fournisseur de données WMI.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERREUR \_ WMI de \_ Réessayer \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-197">4203 (0x106B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-198">La requête WMI n’a pas pu être terminée et doit être retentée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERREUR \_ WMI \_ DP \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-200">4204 (0x106C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-201">Le fournisseur de données WMI est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERREUR \_ WMI \_ de \_ référence d’instance non résolue \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-203">4205 (0x106D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-204">Le fournisseur de données WMI fait référence à un jeu d’instances qui n’a pas été inscrit.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERREUR \_ WMI \_ déjà \_ activée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-206">4206 (0x106E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-207">Le bloc de données WMI ou la notification d’événement a déjà été activé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERREUR \_ \_ GUID WMI \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-209">4207 (0x106F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-210">Le bloc de données WMI n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERREUR \_ \_ serveur WMI \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-213">Le service de données WMI n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERREUR \_ WMI \_ DP \_ échec**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-216">Le fournisseur de données WMI n’a pas pu effectuer la requête.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERREUR \_ \_ MOF non valide dans WMI \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-219">Les informations MOF WMI ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERREUR \_ WMI \_ non valide \_ REGINFO**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-222">Les informations d’inscription WMI ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERREUR \_ WMI \_ déjà \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-225">Le bloc de données WMI ou la notification d’événement a déjà été désactivé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERREUR \_ WMI \_ en lecture \_ seule**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-228">L’élément de données ou le bloc de données WMI est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERREUR \_ échec de la \_ définition WMI \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-231">Impossible de modifier l’élément de données ou le bloc de données WMI.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERREUR \_ non \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-233">4250 (0x109A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-234">Cette opération n’est valide que dans le contexte d’un conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERREUR \_ APPCONTAINER \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-236">4251 (0x109B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-237">Cette application ne peut s’exécuter que dans le contexte d’un conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERREUR \_ non \_ prise en charge \_ dans \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-239">4252 (0x109C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-240">Cette fonctionnalité n’est pas prise en charge dans le contexte d’un conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERREUR \_ de \_ \_ longueur du SID du package non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-242">4253 (0x109D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-243">La longueur du SID fourni n’est pas une longueur valide pour les SID de conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERREUR \_ de \_ support non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-245">4300 (0x10CC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-246">L’identificateur de média ne représente pas un support valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERREUR \_ de \_ bibliothèque non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-248">4301 (0x10CD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-249">L’identificateur de bibliothèque ne représente pas une bibliothèque valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERREUR \_ de \_ pool de supports non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-251">4302 (0x10CE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-252">L’identificateur du pool de médias ne représente pas un pool de médias valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**incompatibilité de support de lecteur d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-254">4303 (0x10CF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-255">Le lecteur et le support ne sont pas compatibles ou n’existent pas dans différentes bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**support d’erreur \_ \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-257">4304 (0x10D0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-258">Le support existe actuellement dans une bibliothèque hors connexion et doit être en ligne pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**bibliothèque d’erreurs \_ \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-260">4305 (0x10D1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-261">L’opération ne peut pas être effectuée sur une bibliothèque hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERREUR \_ vide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-263">4306 (0x10D2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-264">La bibliothèque, le lecteur ou le pool de supports est vide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERREUR \_ non \_ vide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-266">4307 (0x10D3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-267">La bibliothèque, le lecteur ou le pool de supports doit être vide pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**support d’erreur \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-269">4308 (0x10D4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-270">Aucun support n’est actuellement disponible dans ce pool de médias ou cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ressource d’erreur \_ \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-272">4309 (0x10D5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-273">Une ressource requise pour cette opération est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERREUR \_ de \_ nettoyage non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-275">4310 (0x10D6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-276">L’identificateur de média ne représente pas un nettoyeur valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERREUR \_ Impossible \_ de \_ nettoyer**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-278">4311 (0x10D7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-279">Le lecteur ne peut pas être nettoyé ou ne prend pas en charge le nettoyage.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_objet d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-281">4312 (0x10D8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-282">L’identificateur d’objet ne représente pas un objet valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**\_échec de la base de données d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-284">4313 (0x10D9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-285">Impossible de lire ou d’écrire dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_base de données d’erreurs \_ pleine**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-287">4314 (0x10DA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-288">La base de données est pleine.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**support d’erreur \_ \_ incompatible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-290">4315 (0x10DB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-291">Le support n’est pas compatible avec le périphérique ou le pool de supports.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_ressource d' \_ erreur \_ absente**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-293">4316 (0x10DC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-294">La ressource requise pour cette opération n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERREUR \_ d' \_ opération non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-296">4317 (0x10DD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-297">L’identificateur d’opération n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**le \_ support d’erreur \_ n’est pas \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-299">4318 (0x10DE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-300">Le support n’est pas monté ou n’est pas prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**périphérique d’erreur \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-302">4319 (0x10DF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-303">L’appareil n’est pas prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**demande d’erreur \_ \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-305">4320 (0x10E0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-306">L’opérateur ou l’administrateur a refusé la demande.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERREUR \_ d' \_ objet lecteur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-308">4321 (0x10E1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-309">L’identificateur de lecteur ne représente pas un lecteur valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**bibliothèque d’erreurs \_ \_ complète**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-311">4322 (0x10E2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-312">La bibliothèque est pleine.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-312">Library is full.</span></span> <span data-ttu-id="5cd8f-313">Aucun emplacement n’est disponible pour utilisation.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**support d’erreur \_ \_ non \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-315">4323 (0x10E3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-316">Le transport ne peut pas accéder au support.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERREUR \_ Impossible \_ de \_ charger le \_ support**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-318">4324 (0x10E4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-319">Impossible de charger le média dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERREUR \_ Impossible \_ d' \_ inventorier le \_ lecteur**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-321">4325 (0x10E5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-322">Impossible de récupérer l’état du lecteur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERREUR \_ Impossible \_ d' \_ inventorier l' \_ emplacement**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-324">4326 (0x10E6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-325">Impossible de récupérer l’état de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERREUR \_ Impossible \_ d' \_ inventorier le \_ transport**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-327">4327 (0x10E7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-328">Impossible de récupérer l’état du transport.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**TRANSPORT d’erreur \_ \_ complet**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-330">4328 (0x10E8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-331">Impossible d’utiliser le transport, car il est déjà en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERREUR de \_ contrôle de \_ insertion/éjection**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-333">4329 (0x10E9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-334">Impossible d’ouvrir ou de fermer le port d’insertion/éjection.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERREUR \_ Impossible \_ d' \_ éjecter le \_ \_ média monté**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-336">4330 (0x10EA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-337">Impossible d’éjecter le support, car il se trouve dans un lecteur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_jeu d' \_ emplacements de nettoyage d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-339">4331 (0x10EB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-340">Un emplacement de nettoyage est déjà réservé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**\_emplacement du nettoyeur d’erreur \_ \_ non \_ défini**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-342">4332 (0x10EC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-343">Un emplacement de nettoyage n’est pas réservé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**cartouche de nettoyage des erreurs \_ \_ \_ passée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-345">4333 (0x10ED)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-346">La cartouche de nettoyage a effectué le nombre maximal de nettoyages de lecteur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERREUR \_ Omid inattendue \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-348">4334 (0x10EE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-349">Identificateur on-medium inattendu.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERREUR \_ Impossible de \_ supprimer le \_ dernier \_ élément**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-351">4335 (0x10EF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-352">Le dernier élément restant dans ce groupe ou cette ressource ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**le \_ message d’erreur \_ dépasse la \_ \_ taille maximale**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-354">4336 (0x10F0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-355">Le message fourni dépasse la taille maximale autorisée pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**le \_ volume d’erreurs \_ contient des \_ \_ fichiers sys**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-357">4337 (0x10F1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-358">Le volume contient des fichiers système ou d’échange.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERREUR \_ \_ type autochtone**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-360">4338 (0x10F2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-361">Impossible de supprimer le type de média de cette bibliothèque, car au moins un lecteur de la bibliothèque peut prendre en charge ce type de média.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERREUR \_ aucun \_ lecteur de prise en charge \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-363">4339 (0x10F3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-364">Ce média hors connexion ne peut pas être monté sur ce système, car aucun lecteur activé ne peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**cartouche de nettoyage d’erreur \_ \_ \_ installée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-366">4340 (0x10F4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-367">Une cartouche de nettoyage est présente dans la bibliothèque de bandes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERREUR \_ insertion/éjection \_ complète**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-369">4341 (0x10F5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-370">Impossible d’utiliser le port d’insertion/éjection, car il n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**fichier d’erreur \_ \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-372">4350 (0x10FE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-373">Ce fichier n’est actuellement pas disponible pour être utilisé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERREUR \_ de \_ stockage distant \_ non \_ active**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-375">4351 (0x10FF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-376">Le service de stockage distant n’est pas opérationnel pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**erreur \_ de \_ support de stockage distant \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-379">Le service de stockage étendu a rencontré une erreur de support.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERREUR \_ non \_ un \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-382">Le fichier ou le répertoire n’est pas un point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERREUR lors de l’analyse d’un \_ \_ conflit d’attribut \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-385">L’attribut de point d’analyse ne peut pas être défini, car il est en conflit avec un attribut existant.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERREUR \_ de \_ données d’analyse non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-388">Les données présentes dans la mémoire tampon du point d’analyse ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**balise d’erreur d' \_ analyse \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-391">La balise présente dans la mémoire tampon du point d’analyse n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERREUR d' \_ \_ incompatibilité de la balise d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-393">4394 (0x112A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-394">Il existe une incompatibilité entre la balise spécifiée dans la demande et la balise présente dans le point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**données de l' \_ application erreur \_ \_ \_ introuvables**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-397">Données du cache rapide introuvables.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERREUR lors de l’expiration des données de l' \_ application \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-400">Les données du cache rapide ont expiré.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**données d’application ERRONÉes \_ \_ \_ endommagées**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-403">Données du cache rapide endommagées.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**limite de données d’application d’erreur \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-406">Les données du cache rapide ont dépassé la taille maximale et ne peuvent pas être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERREUR \_ de \_ redémarrage des données de l’application \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-409">Le cache rapide a été réarmé et nécessite un redémarrage jusqu’à ce qu’il puisse être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERREUR \_ SECUREBOOT, \_ restauration \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-412">Le démarrage sécurisé a détecté que la restauration des données protégées a été tentée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERREUR de violation de la \_ \_ stratégie SECUREBOOT \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-415">La valeur est protégée par la stratégie de démarrage sécurisé et ne peut pas être modifiée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERREUR \_ SECUREBOOT \_ , \_ stratégie non valide**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-418">La stratégie de démarrage sécurisé n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERREUR de l' \_ \_ éditeur de stratégie SECUREBOOT \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-421">Une nouvelle stratégie de démarrage sécurisé ne contenait pas le serveur de publication actuel dans sa liste de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERREUR de la \_ \_ stratégie SECUREBOOT \_ non \_ signée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-424">La stratégie de démarrage sécurisé n’est pas signée ou est signée par un signataire non approuvé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERREUR \_ SECUREBOOT \_ non \_ activée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-427">Le démarrage sécurisé n’est pas activé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERREUR \_ \_ fichier SECUREBOOT \_ remplacé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-429">4426 (0x114A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-430">Le démarrage sécurisé nécessite que certains fichiers et pilotes ne soient pas remplacés par d’autres fichiers ou pilotes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERREUR de \_ lecture du déchargement \_ \_ flt \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-433">L’opération de lecture du déchargement de copie n’est pas prise en charge par un filtre.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERREUR de \_ déchargement d' \_ écriture \_ flt \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-436">L’opération d’écriture de déchargement de copie n’est pas prise en charge par un filtre.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERREUR de \_ lecture de fichier de déchargement \_ \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-438">4442 (0x115A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-439">L’opération de lecture du déchargement de copie n’est pas prise en charge pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERREUR lors du \_ déchargement du \_ fichier d’écriture \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-441">4443 (0x115B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-442">L’opération d’écriture de déchargement de copie n’est pas prise en charge pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**le \_ volume d’erreurs \_ n’est pas \_ activé pour SIS \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-445">Le stockage d’instance simple n’est pas disponible sur ce volume.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**la \_ ressource dépendante de l’erreur \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-447">5001 (0x1389)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-448">L’opération ne peut pas être effectuée, car d’autres ressources dépendent de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_dépendance d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-450">5002 (0x138A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-451">La dépendance de ressource de cluster est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**la \_ dépendance d’erreur \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-453">5003 (0x138B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-454">La ressource de cluster ne peut pas être rendue dépendante de la ressource spécifiée, car elle est déjà dépendante.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**la \_ ressource d’erreur \_ n’est pas \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-456">5004 (0x138C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-457">La ressource de cluster n’est pas en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**le \_ nœud d’hôte d’erreur \_ n’est \_ pas \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-459">5005 (0x138D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-460">Un nœud de cluster n’est pas disponible pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ressource d’erreur \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-462">5006 (0x138E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-463">La ressource de cluster n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_ressource d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-465">5007 (0x138F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-466">La ressource de cluster est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERREUR lors de l' \_ arrêt du \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-469">Le cluster est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERREUR \_ Impossible de \_ supprimer le \_ \_ nœud actif**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-472">Un nœud de cluster ne peut pas être expulsé du cluster, sauf si le nœud est en service ou s’il s’agit du dernier nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**l' \_ objet d’erreur \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-475">L'objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_objet \_ d’erreur dans la \_ liste**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-478">L’objet figure déjà dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**Groupe d’erreurs \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-481">Le groupe de clusters n’est pas disponible pour les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_groupe d' \_ Erreurs \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-484">Le groupe de clusters est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**Groupe d’erreurs \_ \_ non \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-487">L’opération n’a pas pu aboutir car le groupe de clusters n’est pas en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERREUR \_ du \_ nœud \_ hôte \_ non \_ propriétaire de la ressource**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-490">L’opération a échoué, car le nœud de cluster spécifié n’est pas le propriétaire de la ressource ou le nœud n’est pas un propriétaire possible de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERREUR \_ le \_ nœud hôte \_ n’est pas \_ propriétaire du groupe \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-493">L’opération a échoué car le nœud de cluster spécifié n’est pas le propriétaire du groupe ou le nœud n’est pas un propriétaire possible du groupe.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERREUR \_ RESMON \_ échec de la création \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-496">Impossible de créer la ressource de cluster dans le moniteur de ressource spécifié.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERREUR \_ RESMON \_ en ligne \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-498">5018 (0x139A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-499">La ressource de cluster n’a pas pu être mise en ligne par le moniteur de ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ressource d’erreur \_ \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-501">5019 (0x139B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-502">L’opération n’a pas pu aboutir car la ressource de cluster est en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**\_ressource de quorum d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-504">5020 (0x139C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-505">La ressource de cluster n’a pas pu être supprimée ou mise hors connexion, car il s’agit de la ressource de quorum.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERREUR \_ non liée au \_ quorum \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-507">5021 (0x139D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-508">Le cluster n’a pas pu transformer la ressource spécifiée en ressource de quorum car elle ne peut pas être une ressource de quorum.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**\_arrêt du cluster d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-510">5022 (0x139E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-511">Le logiciel de cluster est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**État d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-513">5023 (0x139F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-514">Le groupe ou la ressource n’est pas dans l’état correct pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**Propriétés des ressources d’erreur \_ \_ \_ stockées**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-516">5024 (0x13A0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-517">Les propriétés ont été stockées, mais toutes les modifications ne prendront effet qu’à la prochaine mise en ligne de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERREUR \_ non \_ de \_ classe de quorum**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-519">5025 (0x13A1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-520">Le cluster n’a pas pu faire de la ressource spécifiée une ressource de quorum car elle n’appartient pas à une classe de stockage partagée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERREUR \_ de \_ ressource principale**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-522">5026 (0x13A2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-523">La ressource de cluster n’a pas pu être supprimée, car il s’agit d’une ressource principale.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**échec de la ressource de quorum d’erreur \_ \_ \_ en ligne \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-525">5027 (0x13A3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-526">La ressource de quorum n’a pas pu être mise en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**échec de l’ouverture du QUORUMLOG d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-528">5028 (0x13A4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-529">Le journal de quorum n’a pas pu être créé ou monté correctement.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERREUR \_ Clusterlog \_ endommagée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-531">5029 (0x13A5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-532">Le journal de cluster est endommagé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**l’erreur de l' \_ \_ enregistrement Clusterlog \_ dépasse \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-534">5030 (0x13A6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-535">L’enregistrement n’a pas pu être écrit dans le journal du cluster, car il dépasse la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**l’erreur \_ Clusterlog \_ dépasse \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-537">5031 (0x13A7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-538">Le journal du cluster dépasse sa taille maximale.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERREUR \_ Clusterlog \_ CHKPOINT \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-540">5032 (0x13A8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-541">Aucun enregistrement de point de contrôle n’a été trouvé dans le journal de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERREUR \_ Clusterlog \_ \_ espace insuffisant \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-543">5033 (0x13A9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-544">L’espace disque minimal requis pour la journalisation n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**propriétaire du quorum d’erreurs \_ \_ \_ actif**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-546">5034 (0x13AA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-547">Le nœud de cluster n’a pas pu prendre le contrôle de la ressource de quorum, car la ressource est détenue par un autre nœud actif.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERREUR \_ réseau \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-549">5035 (0x13AB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-550">Un réseau de clusters n’est pas disponible pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**nœud d’erreur \_ \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-552">5036 (0x13AC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-553">Un nœud de cluster n’est pas disponible pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERREUR \_ tous les \_ nœuds \_ non \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-555">5037 (0x13AD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-556">Tous les nœuds de cluster doivent être en cours d’exécution pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**échec de la ressource d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-558">5038 (0x13AE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-559">échec d’une ressource de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**nœud d’erreur de \_ cluster \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-561">5039 (0x13AF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-562">Le nœud de cluster n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**le \_ nœud de cluster d’erreurs \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-564">5040 (0x13B0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-565">Le nœud de cluster existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERREUR \_ \_ de jonction \_ de cluster en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-567">5041 (0x13B1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-568">Un nœud est en train de joindre le cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nœud de cluster d’erreurs \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-570">5042 (0x13B2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-571">Le nœud de cluster est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**le \_ nœud local du cluster d’erreurs est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-573">5043 (0x13B3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-574">Les informations du nœud local du cluster sont introuvables.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**le \_ réseau du cluster d’erreurs \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-576">5044 (0x13B4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-577">Le réseau de clusters existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**le réseau du cluster d’erreurs est \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-579">5045 (0x13B5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-580">Le réseau de clusters est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**l’erreur \_ cluster \_ netinterface \_ existe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-582">5046 (0x13B6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-583">L’interface réseau de clusters existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERREUR \_ de \_ netinterface de cluster \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-585">5047 (0x13B7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-586">L’interface réseau du cluster est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**demande de cluster d’erreurs \_ \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-588">5048 (0x13B8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-589">La demande de cluster n’est pas valide pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**\_ \_ fournisseur réseau non valide du cluster d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-591">5049 (0x13B9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-592">Le fournisseur réseau de clusters n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**nœud de cluster d’erreurs \_ \_ \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-594">5050 (0x13BA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-595">Le nœud de cluster est inactif.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERREUR \_ de \_ nœud de cluster \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-597">5051 (0x13BB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-598">Le nœud de cluster n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**nœud de cluster d’erreurs \_ \_ \_ non \_ membre**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-600">5052 (0x13BC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-601">Le nœud de cluster n’est pas membre du cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**la \_ \_ jonction \_ du cluster d’erreurs n’est pas \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-603">5053 (0x13BD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-604">Une opération de jonction de clusters n’est pas en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**réseau d’erreurs \_ \_ réseau non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-606">5054 (0x13BE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-607">Le réseau de clusters n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**nœud de cluster d’erreurs \_ \_ vers le \_ haut**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-609">5056 (0x13C0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-610">Le nœud de cluster est en place.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_ \_ ipaddr du cluster \_ d’erreurs en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-612">5057 (0x13C1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-613">L’adresse IP de cluster est déjà utilisée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**nœud de cluster d’erreurs \_ \_ \_ non \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-615">5058 (0x13C2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-616">Le nœud de cluster n’est pas suspendu.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ contexte de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-618">5059 (0x13C3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-619">Aucun contexte de sécurité de cluster n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERREUR \_ réseau de cluster \_ \_ non \_ interne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-621">5060 (0x13C4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-622">Le réseau de clusters n’est pas configuré pour la communication interne du cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**nœud de cluster d’erreurs \_ \_ déjà en \_ cours \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-624">5061 (0x13C5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-625">Le nœud de cluster est déjà en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**nœud de cluster d’erreurs \_ \_ déjà en cours d' \_ \_ inversion**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-627">5062 (0x13C6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-628">Le nœud de cluster est déjà en cours d’inversion.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERREUR \_ réseau de cluster \_ \_ déjà \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-630">5063 (0x13C7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-631">Le réseau de clusters est déjà en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERREUR \_ réseau de clusters \_ \_ déjà \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-633">5064 (0x13C8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-634">Le réseau de clusters est déjà hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**nœud de cluster d’erreurs \_ \_ \_ déjà \_ membre**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-636">5065 (0x13C9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-637">Le nœud de cluster est déjà membre du cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERREUR \_ du \_ dernier \_ réseau interne du cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-639">5066 (0x13CA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-640">Le réseau de clusters est le seul configuré pour la communication interne du cluster entre deux nœuds de cluster actifs ou plus.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="5cd8f-641">La capacité de communication interne ne peut pas être supprimée du réseau.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERREUR liée au \_ réseau de clusters d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-643">5067 (0x13CB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-644">Une ou plusieurs ressources de cluster dépendent du réseau pour fournir le service aux clients.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="5cd8f-645">La fonctionnalité d’accès client ne peut pas être supprimée du réseau.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERREUR \_ \_ d’opération non valide \_ sur le \_ quorum**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-647">5068 (0x13CC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-648">Cette opération ne peut pas être effectuée sur la ressource de cluster en tant que ressource de quorum.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="5cd8f-649">Vous ne pouvez pas mettre la ressource de quorum hors connexion ou modifier sa liste de propriétaires possibles.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**dépendance d’erreur \_ \_ non \_ autorisée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-651">5069 (0x13CD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-652">La ressource quorum du cluster n’est pas autorisée à avoir des dépendances.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**nœud de cluster d’erreurs \_ \_ \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-654">5070 (0x13CE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-655">Le nœud de cluster est suspendu.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**nœud d’erreur déverser la \_ \_ \_ \_ ressource hôte**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-657">5071 (0x13CF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-658">La ressource de cluster ne peut pas être mise en ligne.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="5cd8f-659">Le nœud propriétaire ne peut pas exécuter cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**le \_ nœud de cluster d’erreur \_ n’est \_ pas \_ prêt**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-661">5072 (0x13D0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-662">Le nœud de cluster n’est pas prêt à effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERREUR lors de l’arrêt du nœud de \_ cluster \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-664">5073 (0x13D1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-665">Le nœud de cluster est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERREUR \_ de \_ jonction de cluster \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-667">5074 (0x13D2)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-668">L’opération de jonction de cluster a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ versions incompatibles du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-670">5075 (0x13D3)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-671">L’opération de jonction de cluster a échoué en raison de versions logicielles incompatibles entre le nœud joint et son sponsor.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ MAXNUM \_ de ressources de cluster d’erreurs \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-673">5076 (0x13D4)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-674">Impossible de créer cette ressource, car le cluster a atteint la limite du nombre de ressources qu’il peut surveiller.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERREUR \_ de \_ configuration du système de cluster \_ \_ modifiée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-676">5077 (0x13D5)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-677">La configuration système a été modifiée lors de la jonction de cluster ou de l’opération de formulaire.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="5cd8f-678">L’opération de jointure ou de formulaire a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERREUR de \_ type de ressource de cluster \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-680">5078 (0x13D6)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-681">Le type de ressource spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**RESTYPE du cluster d’erreurs \_ \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-683">5079 (0x13D7)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-684">Le nœud spécifié ne prend pas en charge une ressource de ce type.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="5cd8f-685">Cela peut être dû à des incohérences de version ou en raison de l’absence de la DLL de ressource sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**RESNAME du cluster d’erreurs \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-687">5080 (0x13D8)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-688">Le nom de ressource spécifié n’est pas pris en charge par cette DLL de ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="5cd8f-689">Cela peut être dû à un nom incorrect (ou modifié) fourni à la DLL de ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ \_ package RPC \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-691">5081 (0x13D9)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-692">Aucun package d’authentification n’a pu être inscrit auprès du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**le \_ \_ propriétaire \_ du cluster d’erreurs n’est pas \_ dans \_ PREFLIST**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-694">5082 (0x13DA)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-695">Vous ne pouvez pas mettre le groupe en ligne, car le propriétaire du groupe n’est pas dans la liste par défaut du groupe.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="5cd8f-696">Pour modifier le nœud propriétaire du groupe, déplacez le groupe.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERREUR \_ \_ de base de données de cluster \_ SEQMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-698">5083 (0x13DB)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-699">L’opération de jointure a échoué, car le numéro de séquence de la base de données de cluster a été modifié ou n’est pas compatible avec le nœud de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="5cd8f-700">Cela peut se produire lors d’une opération de jointure si la base de données de cluster a été modifiée lors de la jointure.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERREUR \_ RESMON \_ État non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-702">5084 (0x13DC)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-703">Le moniteur de ressource n’autorise pas l’exécution de l’opération d’échec tant que la ressource est dans son état actuel.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="5cd8f-704">Cela peut se produire si la ressource est dans un état d’attente.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERREUR de blocage de la \_ gomme du cluster \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-706">5085 (0x13DD)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-707">Un code qui n’a pas de verrou a reçu une demande de réservation du verrou pour la mise à jour globale.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERREUR \_ \_ disque quorum \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-709">5086 (0x13DE)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-710">Le disque quorum n’a pas pu être localisé par le service de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERREUR \_ de sauvegarde de base de données \_ \_ endommagée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-712">5087 (0x13DF)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-713">La base de données de cluster sauvegardée est peut-être endommagée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**le \_ nœud de cluster d’erreurs \_ \_ a déjà une \_ \_ \_ racine DFS**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-715">5088 (0x13E0)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-716">Il existe déjà une racine DFS dans ce nœud de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**propriété de ressource d’erreur non \_ \_ \_ modifiable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-718">5089 (0x13E1)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-719">Une tentative de modification d’une propriété de ressource a échoué, car elle est en conflit avec une autre propriété existante.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**\_État d' \_ appartenance au cluster d’erreurs \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-722">Une opération qui n’est pas compatible avec l’état d’appartenance actuel du nœud a été tentée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**QUORUMLOG du cluster d’erreurs \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-725">La ressource quorum ne contient pas le journal quorum.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERREUR \_ d' \_ arrêt de l’appartenance au cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-728">Le moteur d’appartenance a demandé l’arrêt du service de cluster sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité d’ID d’instance de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-731">L’opération de jointure a échoué, car l’ID d’instance de cluster du nœud joint ne correspond pas à l’ID d’instance de cluster du nœud sponsor.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**le \_ \_ réseau du cluster d’erreurs est \_ \_ introuvable \_ pour l' \_ adresse IP**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-734">Impossible de trouver un réseau de clusters correspondant pour l’adresse IP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**incompatibilité de type de données de propriété de cluster d’erreurs \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-737">Le type de données réel de la propriété ne correspond pas au type de données attendu de la propriété.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**suppression du cluster d’erreurs \_ \_ \_ sans \_ nettoyage**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-740">Le nœud de cluster a été supprimé du cluster avec succès, mais le nœud n’a pas été nettoyé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="5cd8f-741">Pour déterminer les étapes de nettoyage qui ont échoué et comment récupérer, consultez le journal des événements de l’application de clustering de basculement à l’aide de observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**incompatibilité des paramètres de cluster d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-744">Au moins deux valeurs de paramètre spécifiées pour les propriétés d’une ressource sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**le \_ nœud d’erreur \_ ne peut pas \_ être \_ mis en cluster**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-746">5898 (0x170A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-747">Cet ordinateur ne peut pas être membre d’un cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERREUR \_ de \_ \_ version du système d’exploitation incorrecte du cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-749">5899 (0x170B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-750">Cet ordinateur ne peut pas être membre d’un cluster, car il n’a pas la version appropriée de Windows installée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERREUR de \_ cluster \_ Impossible de créer un \_ \_ \_ nom de cluster DUP \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-752">5900 (0x170C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-753">Impossible de créer un cluster avec le nom de cluster spécifié, car ce nom de cluster est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="5cd8f-754">Spécifiez un autre nom pour le cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERREUR \_ CLUSCFG \_ déjà \_ validée**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-756">5901 (0x170D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-757">L’action de configuration du cluster a déjà été validée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERREUR \_ CLUSCFG \_ échec de la restauration \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-759">5902 (0x170E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-760">Impossible de restaurer l’action de configuration du cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERREUR \_ CLUSCFG \_ \_ conflit de \_ lettre de lecteur de disque système \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-762">5903 (0x170F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-763">La lettre de lecteur affectée à un disque système sur un nœud est en conflit avec la lettre de lecteur affectée à un disque d’un autre nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**\_ \_ version antérieure du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-766">Un ou plusieurs nœuds du cluster exécutent une version de Windows qui ne prend pas en charge cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**le cluster d’erreurs ne \_ \_ correspond pas au \_ nom du compte d’ordinateur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-769">Le nom du compte d’ordinateur correspondant ne correspond pas au nom réseau de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERREUR \_ de \_ cluster \_ sans \_ adaptateurs réseau**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-772">Aucune carte réseau n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**CLUSTER d’erreurs \_ \_ incohérent**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-775">Le nœud de cluster a été incohérent.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERREUR \_ de \_ déplacement du groupe de clusters \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-778">Le groupe n’est pas en mesure d’accepter la demande, car elle est déplacée vers un autre nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**TYPE de ressource de cluster d’erreurs \_ \_ \_ \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-781">Le type de ressource ne peut pas accepter la demande, car est trop occupé à effectuer une autre opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**expiration du délai d’attente de l' \_ appel de ressource \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-784">L’appel à la DLL de ressource de cluster a expiré.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERREUR \_ d' \_ \_ adresse IPv6 de cluster non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-787">L’adresse n’est pas valide pour une ressource d’adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="5cd8f-788">Une adresse IPv6 globale est requise et doit correspondre à un réseau de clusters.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="5cd8f-789">Les adresses de compatibilité ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**\_ \_ \_ fonction interne non valide du cluster \_ d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-792">Une erreur de cluster interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-792">An internal cluster error occurred.</span></span> <span data-ttu-id="5cd8f-793">Une tentative d’appel à une fonction non valide a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_ \_ paramètre de cluster \_ d’erreurs hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-796">Une valeur de paramètre est en dehors de la plage acceptable.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**\_ \_ envoi partiel du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-798">5914 (0x171A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-799">Une erreur réseau s’est produite lors de l’envoi de données vers un autre nœud du cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="5cd8f-800">Le nombre d’octets transmis était inférieur au nombre requis.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**\_ \_ \_ fonction non valide du Registre du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-802">5915 (0x171B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-803">Une opération de registre de cluster non valide a été tentée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**\_fin de \_ chaîne non valide du cluster \_ d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-805">5916 (0x171C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-806">Une chaîne d’entrée de caractères n’est pas correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_format de \_ chaîne non valide du cluster \_ d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-808">5917 (0x171D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-809">Une chaîne d’entrée de caractères n’est pas dans un format valide pour les données qu’elle représente.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERREUR \_ de \_ transaction de base de données de cluster \_ \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-811">5918 (0x171E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-812">Une erreur de cluster interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-812">An internal cluster error occurred.</span></span> <span data-ttu-id="5cd8f-813">Une transaction de base de données de cluster a été tentée alors qu’une transaction était déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERREUR \_ \_ de transaction de base de données de cluster \_ \_ non \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-815">5919 (0x171F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-816">Une erreur de cluster interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-816">An internal cluster error occurred.</span></span> <span data-ttu-id="5cd8f-817">Une tentative de validation d’une transaction de base de données de cluster a été effectuée alors qu’aucune transaction n’était en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**\_ \_ données null du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-820">Une erreur de cluster interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-820">An internal cluster error occurred.</span></span> <span data-ttu-id="5cd8f-821">Les données n’ont pas été initialisées correctement.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**\_ \_ lecture partielle du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-824">Une erreur s’est produite lors de la lecture d’un flux de données.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="5cd8f-825">Un nombre inattendu d’octets a été retourné.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**\_ \_ écriture partielle du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-828">Une erreur s’est produite lors de l’écriture dans un flux de données.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="5cd8f-829">Impossible d’écrire le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERREUR \_ de \_ \_ désérialisation des \_ données par le cluster d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-832">Une erreur s’est produite lors de la désérialisation d’un flux de données de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_conflit de \_ propriété de ressource dépendante d' \_ erreur \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-835">Une ou plusieurs valeurs de propriété pour cette ressource sont en conflit avec une ou plusieurs valeurs de propriété associées à ses ressources dépendantes.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ quorum**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-838">Un quorum de nœuds de cluster n’était pas présent pour former un cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERREUR \_ \_ réseau IPv6 non valide du cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-841">Le réseau de clusters n’est pas valide pour une ressource d’adresse IPv6, ou il ne correspond pas à l’adresse configurée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**Erreur \_ de \_ \_ réseau de \_ tunnel \_ IPv6 non valide pour le cluster d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-844">Le réseau de clusters n’est pas valide pour une ressource de tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="5cd8f-845">Vérifiez la configuration de la ressource d’adresse IP dont dépend la ressource de tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_le quorum \_ d’erreur n’est pas \_ autorisé \_ dans \_ ce \_ groupe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-848">La ressource de quorum ne peut pas résider dans le groupe de stockage disponible.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_arborescence de dépendances d’erreur \_ \_ trop \_ complexe**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-851">Les dépendances de cette ressource sont imbriquées trop profondément.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_exception \_ d’erreur dans l’appel de \_ ressource \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-853">5930 (0x172A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-854">L’appel dans la DLL de ressource a levé une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**\_ \_ \_ échec \_ d’initialisation du RHS du cluster d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-856">5931 (0x172B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-857">Échec de l’initialisation du processus RHS.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**le \_ cluster d’erreurs \_ n’est pas \_ installé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-859">5932 (0x172C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-860">La fonctionnalité de clustering de basculement n’est pas installée sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ \_ les ressources de cluster d’erreurs doivent \_ être \_ en ligne \_ sur \_ le \_ même \_ nœud**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-862">5933 (0x172D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-863">Les ressources doivent être en ligne sur le même nœud pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ nombre maximal \_ de nœuds \_ de cluster d’erreurs dans le \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-865">5934 (0x172E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-866">Impossible d’ajouter un nouveau nœud, car ce cluster a déjà un nombre maximal de nœuds.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERREURS \_ de \_ \_ nœud trop nombreux \_ dans le cluster**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-868">5935 (0x172F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-869">Ce cluster ne peut pas être créé, car le nombre de nœuds spécifié dépasse la limite maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**objet de cluster d’erreurs \_ \_ \_ déjà \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-872">Une tentative d’utilisation du nom de cluster spécifié a échoué, car un objet ordinateur activé portant le même nom existe déjà dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERREUR de \_ \_ groupes principaux \_ introuvables**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-875">Ce cluster ne peut pas être détruit.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="5cd8f-876">Il possède des groupes d’applications non centraux qui doivent être supprimés avant que le cluster puisse être détruit.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERREUR \_ de \_ \_ conflit de ressources de partage de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-879">Le partage de fichiers associé à la ressource témoin de partage de fichiers ne peut pas être hébergé par ce cluster ou l’un de ses nœuds.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**\_Suppression de \_ la \_ demande non valide du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-882">L’éviction de ce nœud n’est pas valide pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="5cd8f-883">En raison de l’éviction du nœud exigences de quorum, l’arrêt du cluster se produit.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="5cd8f-884">S’il s’agit du dernier nœud dans le cluster, la commande destroy cluster doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ ressource singleton du cluster d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-887">Une seule instance de ce type de ressource est autorisée dans le cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**\_ \_ ressource singleton du groupe de clusters d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-890">Une seule instance de ce type de ressource est autorisée par groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERREUR lors de l' \_ échec du fournisseur de ressources de cluster \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-893">La ressource n’a pas pu être mise en ligne en raison de l’échec d’une ou de plusieurs ressources du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**erreur de configuration de la \_ ressource de cluster erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-896">La ressource a indiqué qu’elle ne peut pas être mise en ligne sur un nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERREUR du \_ groupe de clusters \_ \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-899">L’opération en cours ne peut pas être effectuée sur ce groupe pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**\_ \_ \_ volume non partagé \_ du cluster d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-902">Le répertoire ou le fichier ne se trouve pas sur un volume partagé de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**descripteur de sécurité de cluster d’erreurs \_ \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-904">5946 (0x173A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-905">Le descripteur de sécurité ne remplit pas les conditions requises pour un cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ \_ volumes partagés de cluster \_ d’erreurs en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-907">5947 (0x173B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-908">Une ou plusieurs ressources de volumes partagés sont configurées dans le cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="5cd8f-909">Ces ressources doivent être déplacées vers le stockage disponible pour que l’opération aboutisse.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**\_ \_ API utiliser des \_ \_ volumes partagés \_ de cluster d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-911">5948 (0x173C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-912">Ce groupe ou cette ressource ne peut pas être manipulé directement.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="5cd8f-913">Utilisez des API de volume partagé pour effectuer l’opération souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERREUR \_ \_ de sauvegarde \_ du cluster en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-915">5949 (0x173D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-916">La sauvegarde est en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-916">Back up is in progress.</span></span> <span data-ttu-id="5cd8f-917">Veuillez attendre la fin de la sauvegarde avant de recommencer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERREUR \_ non \_ CSV \_ path**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-919">5950 (0x173E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-920">Le chemin d’accès n’appartient pas à un volume partagé de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERREUR \_ \_ volume CSV \_ non \_ local**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-922">5951 (0x173F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-923">Le volume partagé de cluster n’est pas monté localement sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**arrêt de la surveillance du cluster d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-926">La surveillance du cluster se termine.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERREUR de \_ ressource de cluster ayant refusé le déplacement des \_ \_ \_ \_ nœuds incompatibles \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-929">Une ressource a refusé un déplacement entre deux nœuds, car ils sont incompatibles.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**poids du nœud de cluster d’erreurs \_ \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-932">La demande n’est pas valide, car la pondération du nœud ne peut pas être modifiée tant que le cluster est en mode de quorum disque uniquement, ou parce que la modification du poids du nœud ne respecte pas les exigences minimales de quorum de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERREUR \_ d' \_ \_ \_ appel refusé de la ressource de cluster**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-935">La ressource a refusé l’appel.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERREUR \_ RESMON \_ \_ ressources système \_ manquantes**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-938">La ressource n’a pas pu démarrer ou s’exécuter car elle n’a pas pu réserver suffisamment de ressources système.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**erreur \_ \_ \_ de refus de la ressource \_ de cluster d’erreurs déplacer les \_ \_ \_ ressources sur la \_ \_ destination**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-941">Une ressource a refusé un déplacement entre deux nœuds, car la destination ne dispose pas actuellement de ressources suffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERREUR \_ \_ \_ de refus de ressource \_ \_ de cluster \_ insuffisante déplacer les \_ ressources \_ sur la \_ source**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-944">Une ressource a refusé un déplacement entre deux nœuds, car la source ne dispose pas actuellement de ressources suffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**\_groupe de clusters d’erreurs en \_ \_ file d’attente**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-947">L’opération demandée ne peut pas être effectuée, car le groupe est mis en file d’attente pour une opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**État du verrouillage de la \_ ressource de cluster d’erreurs \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-950">L’opération demandée ne peut pas être effectuée, car une ressource a l’état verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**\_basculement du volume partagé de cluster d’erreurs \_ \_ \_ \_ non \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-953">La ressource ne peut pas être déplacée vers un autre nœud, car un volume partagé de cluster a refusé l’opération.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERREUR \_ \_ \_ \_ de drainage du nœud de cluster en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-955">5962 (0x174A)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-956">Une vidange de nœud est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-956">A node drain is already in progress.</span></span>

<span data-ttu-id="5cd8f-957">Cette valeur était également nommée **\_ \_ \_ évacuation des nœuds de cluster d’erreur \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERREUR \_ disque de cluster \_ \_ non \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-959">5963 (0x174B)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-960">Le stockage en cluster n’est pas connecté au nœud.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERREUR \_ disque \_ non \_ CSV \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-962">5964 (0x174C)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-963">Le disque n’est pas configuré de manière à être utilisé avec des volumes partagés de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="5cd8f-964">Les disques CSV doivent avoir au moins une partition formatée avec NTFS.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**la \_ ressource \_ d’erreur n’est pas \_ dans le \_ \_ stockage disponible**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-966">5965 (0x174D)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-967">La ressource doit faire partie du groupe de stockage disponible pour effectuer cette action.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERREUR \_ de \_ \_ redirection du volume partagé de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-969">5966 (0x174E)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-970">Échec de l’opération CSVFS car le volume est en mode Redirigé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**\_volume partagé de cluster d’erreurs \_ \_ \_ non \_ Redirigé**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-972">5967 (0x174F)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-973">Échec de l’opération CSVFS car le volume n’est pas en mode Redirigé.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**le \_ cluster d’erreurs \_ ne peut pas \_ retourner les \_ Propriétés**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-976">Les propriétés du cluster ne peuvent pas être retournées pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERREUR \_ la \_ ressource \_ de cluster contient une \_ zone diff non prise en charge \_ \_ \_ pour les \_ \_ volumes partagés**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-979">La ressource de disque en cluster contient une zone diff de capture instantanée logicielle qui n’est pas prise en charge pour les volumes partagés de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**la \_ \_ ressource \_ de cluster d’erreurs est \_ en \_ \_ mode maintenance**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-982">Impossible d’effectuer l’opération, car la ressource est en mode maintenance.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERREUR \_ de \_ conflit d’affinités de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-985">Impossible d’effectuer l’opération en raison de conflits d’affinité de cluster.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5cd8f-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERREUR \_ \_ la ressource de cluster \_ est une \_ \_ machine virtuelle de réplication \_**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cd8f-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="5cd8f-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="5cd8f-988">Impossible d’effectuer l’opération, car la ressource est un ordinateur virtuel de réplication.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="5cd8f-989">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cd8f-989">Requirements</span></span>



| <span data-ttu-id="5cd8f-990">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cd8f-990">Requirement</span></span> | <span data-ttu-id="5cd8f-991">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cd8f-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd8f-992">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cd8f-992">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd8f-993">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cd8f-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5cd8f-994">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cd8f-994">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd8f-995">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cd8f-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cd8f-996">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cd8f-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd8f-997"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cd8f-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd8f-998">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cd8f-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd8f-999">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="5cd8f-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 





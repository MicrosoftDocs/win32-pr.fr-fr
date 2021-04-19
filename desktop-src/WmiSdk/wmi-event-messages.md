---
description: La liste suivante répertorie les événements pris en charge par les journaux WMI dans Windows Vista et les systèmes d’exploitation ultérieurs.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Messages d’événement WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524993"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="f594e-103">Messages d’événement WMI</span><span class="sxs-lookup"><span data-stu-id="f594e-103">WMI Event Messages</span></span>

<span data-ttu-id="f594e-104">La liste suivante répertorie les événements pris en charge par les journaux WMI dans Windows Vista et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="f594e-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="f594e-105">La documentation suivante est conçue pour les développeurs et les administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="f594e-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="f594e-106">Si vous tentez de résoudre un message d’erreur WMI sur votre système d’hébergement, consultez le site Web [support Microsoft](https://support.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="f594e-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="f594e-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_référentiel MC WBEM \_ \_ incohérent**</span><span class="sxs-lookup"><span data-stu-id="f594e-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-108">1073747424 (0x400015E0)</span><span class="sxs-lookup"><span data-stu-id="f594e-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-109">Le service de Windows Management Instrumentation a détecté une incohérence avec l’espace de stockage WMI dans le répertoire *% windir% \\ system32 \\ WBEM \\* et n’a pas pu le récupérer.</span><span class="sxs-lookup"><span data-stu-id="f594e-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="f594e-110">L’espace de stockage WMI sera à présent supprimé. un nouveau référentiel sera créé en fonction du mécanisme de récupération automatique.</span><span class="sxs-lookup"><span data-stu-id="f594e-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_chargement du \_ \_ fournisseur LOCALSYSTEM du sous-système \_ LOCALSYSTEM du \_ fournisseur WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-112">2147483711 (0x8000003F)</span><span class="sxs-lookup"><span data-stu-id="f594e-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-113">Un fournisseur, %1, a été inscrit dans le Windows Management Instrumentation l’espace de noms %2 pour utiliser le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f594e-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="f594e-114">Ce compte est privilégié et le fournisseur peut entraîner une violation de la sécurité s’il n’emprunte pas correctement les demandes des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f594e-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_MOF MD \_ WBEM \_ non \_ chargé \_ lors de la \_ récupération**</span><span class="sxs-lookup"><span data-stu-id="f594e-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-116">3221225476 (0xC0000004)</span><span class="sxs-lookup"><span data-stu-id="f594e-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-117">Erreur %1 rencontrée lors de la tentative de chargement du fichier MOF %2 lors de la récupération. Fichier MOF marqué avec la récupération automatique.</span><span class="sxs-lookup"><span data-stu-id="f594e-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**le \_ filtre MC WBEM \_ ne peut pas \_ activer le \_ filtre**</span><span class="sxs-lookup"><span data-stu-id="f594e-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-119">3221225482 (0xC000000A)</span><span class="sxs-lookup"><span data-stu-id="f594e-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-120">Impossible de réactiver le filtre d’événement avec la requête « %2 » dans l’espace de noms « %1 » en raison de l’erreur %3.</span><span class="sxs-lookup"><span data-stu-id="f594e-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="f594e-121">Les événements ne peuvent pas être remis via ce filtre tant que le problème n’est pas corrigé.</span><span class="sxs-lookup"><span data-stu-id="f594e-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_requête de \_ fournisseur d’événements non valide WBEM MC \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-123">3221225493 (0xC0000015)</span><span class="sxs-lookup"><span data-stu-id="f594e-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-124">Le fournisseur d’événements %1 a tenté d’inscrire une requête syntaxiquement non valide « %2 ».</span><span class="sxs-lookup"><span data-stu-id="f594e-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="f594e-125">La requête sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="f594e-125">The query will be ignored.</span></span> <span data-ttu-id="f594e-126">La requête peut être corrigée en examinant le référentiel WMI avec CIM Studio et en mettant à jour les abonnements permanents pour le fournisseur et la requête listés.</span><span class="sxs-lookup"><span data-stu-id="f594e-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="f594e-127">Si l’abonnement permanent est créé avec un fichier MOF fourni avec un produit installé, le fournisseur de l’application doit être contacté pour corriger l’inscription défectueuse.</span><span class="sxs-lookup"><span data-stu-id="f594e-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ requête intrinsèque de fournisseur d’événements non \_ valide \_ WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="f594e-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-129">3221225494 (0xC0000016)</span><span class="sxs-lookup"><span data-stu-id="f594e-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-130">Le fournisseur d’événements %1 a tenté d’enregistrer une requête d’événement intrinsèque « %2 » dans l’espace de noms %3 pour lequel le jeu de classes d’objets cibles n’a pas pu être déterminé.</span><span class="sxs-lookup"><span data-stu-id="f594e-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="f594e-131">La requête sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="f594e-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_requête du fournisseur d’événement MC WBEM \_ \_ \_ \_ trop \_ large**</span><span class="sxs-lookup"><span data-stu-id="f594e-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-133">3221225495 (0xC0000017)</span><span class="sxs-lookup"><span data-stu-id="f594e-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-134">Le fournisseur d’événements %1 a tenté d’inscrire la requête "%2" dans l’espace de noms %3 qui est trop large.</span><span class="sxs-lookup"><span data-stu-id="f594e-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="f594e-135">Les fournisseurs d’événements ne peuvent pas fournir des événements fournis par le système.</span><span class="sxs-lookup"><span data-stu-id="f594e-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="f594e-136">La requête sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="f594e-136">The query will be ignored.</span></span> <span data-ttu-id="f594e-137">Contactez le fournisseur de l’application.</span><span class="sxs-lookup"><span data-stu-id="f594e-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_requête de fournisseur d’événements WBEM MD \_ \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="f594e-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-139">3221225496 (0xC0000018)</span><span class="sxs-lookup"><span data-stu-id="f594e-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-140">Le fournisseur d’événements %1 a tenté d’inscrire la requête « %2 » dont la classe cible « %3 » dans l’espace de noms %4 n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f594e-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="f594e-141">La requête sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="f594e-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_événement de \_ requête de fournisseur d’événement MC WBEM \_ \_ \_ non \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-143">3221225497 (0xC0000019)</span><span class="sxs-lookup"><span data-stu-id="f594e-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-144">Le fournisseur d’événements %1 a tenté d’inscrire la requête &quot; %2 &quot; dont la classe cible &quot; %3 &quot; n’est pas une classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f594e-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="f594e-145">La requête sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="f594e-145">The query will be ignored.</span></span> <span data-ttu-id="f594e-146">Contactez le fournisseur de l’application.</span><span class="sxs-lookup"><span data-stu-id="f594e-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**échec WBEM du noyau WBEM \_ MD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-148">3221225500 (0xC000001C)</span><span class="sxs-lookup"><span data-stu-id="f594e-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-149">Échec de l’initialisation de WMI Core ou du sous-système du fournisseur ou du sous-système d’événements avec le numéro d’erreur %1.</span><span class="sxs-lookup"><span data-stu-id="f594e-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="f594e-150">Cela peut être dû à une version incorrecte de WMI, à une erreur de mise à niveau du référentiel WMI, à un espace disque insuffisant ou à une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f594e-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_échec de connexion WBEM MC \_ adap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-152">3221225515 (0xC000002B)</span><span class="sxs-lookup"><span data-stu-id="f594e-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-153">Windows Management Instrumentation ADAP n’a pas pu se connecter à l’espace de noms %1 avec l’erreur suivante : %2.</span><span class="sxs-lookup"><span data-stu-id="f594e-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_échec de \_ PUTCLASS WBEM adap \_ PERFLIB \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-155">3221225520 (0xC0000030)</span><span class="sxs-lookup"><span data-stu-id="f594e-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-156">Windows Management Instrumentation ADAP n’a pas pu enregistrer l’objet %1 dans l’espace de noms %2 en raison de l’erreur suivante : %3.</span><span class="sxs-lookup"><span data-stu-id="f594e-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ adap \_ ne peut pas \_ \_ ajouter \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="f594e-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-158">3221225530 (0xC000003A)</span><span class="sxs-lookup"><span data-stu-id="f594e-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-159">Windows Management Instrumentation ADAP n’a pas pu créer la \_ classe de base de performances Win32 dans %1 : résultat = %2.</span><span class="sxs-lookup"><span data-stu-id="f594e-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ adap \_ ne peut pas \_ \_ ajouter \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="f594e-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-161">3221225531 (0xC000003B)</span><span class="sxs-lookup"><span data-stu-id="f594e-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-162">Windows Management Instrumentation ADAP n’a pas pu créer la \_ classe de base Win32 PerfRawData %1.</span><span class="sxs-lookup"><span data-stu-id="f594e-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ échec \_ du démarrage du référentiel \_ MC WBEM**</span><span class="sxs-lookup"><span data-stu-id="f594e-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-164">3221231073 (0xC00015E1)</span><span class="sxs-lookup"><span data-stu-id="f594e-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-165">Le service Windows Management Instrumentation n’a pas pu charger les fichiers du référentiel sous le répertoire *% windir% \\ system32 \\ WBEM \\*.</span><span class="sxs-lookup"><span data-stu-id="f594e-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="f594e-166">Cela peut être dû à un endommagement dans les fichiers de référentiel, aux paramètres de sécurité de ce répertoire, à un manque d’espace disque ou à d’autres problèmes de ressources système tels que l’insuffisance de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f594e-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="f594e-167">Si cette erreur se produit à chaque redémarrage de l’ordinateur, l’administrateur de cet ordinateur devra peut-être arrêter le service WMI, passer en revue le paramètre de sécurité sur ce dossier et les fichiers de ce dossier, puis exécuter WMIDiag pour valider l’intégrité de Windows Management Instrumentation.</span><span class="sxs-lookup"><span data-stu-id="f594e-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**la \_ WBEM MD WBEM \_ \_ requiert un \_ chiffrement \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="f594e-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-169">3221231077 (0xC00015E5)</span><span class="sxs-lookup"><span data-stu-id="f594e-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-170">L’accès à l’espace de noms %1 a été refusé parce que l’espace de noms est marqué avec RequiresEncryption, mais le script ou l’application a tenté de se connecter à cet espace de noms avec un niveau d’authentification inférieur à la **\_ confidentialité PKT**.</span><span class="sxs-lookup"><span data-stu-id="f594e-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="f594e-171">Remplacez le niveau d’authentification par **PKT \_ Privacy** , puis exécutez de nouveau le script ou l’application.</span><span class="sxs-lookup"><span data-stu-id="f594e-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**le \_ WBEM MC WBEM \_ \_ requiert un \_ chiffrement \_ asynchrone \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="f594e-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-173">3221231078 (0xC00015E6)</span><span class="sxs-lookup"><span data-stu-id="f594e-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-174">Windows Management Instrumentation service n’a pas pu fournir de résultats de manière asynchrone pour l’espace de noms %1.</span><span class="sxs-lookup"><span data-stu-id="f594e-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="f594e-175">L’espace de noms est marqué avec RequiresEncryption, mais WinMgmt n’a pas pu établir une connexion sécurisée à l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f594e-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="f594e-176">Assurez-vous qu’il existe une relation d’approbation entre les ordinateurs client et serveur afin que le client reconnaisse le compte de l’ordinateur serveur.</span><span class="sxs-lookup"><span data-stu-id="f594e-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_ \_ hôte WBEM MD \_ WBEM \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="f594e-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-178">3221231084 (0xC00015EC)</span><span class="sxs-lookup"><span data-stu-id="f594e-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-179">Windows Management Instrumentation s’est arrêté WMIPRVSE.EXE, car un quota a atteint une valeur d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="f594e-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="f594e-180">Quota : %1 valeur : %2 valeur maximale : %3 WMIPRVSE PID : %4.</span><span class="sxs-lookup"><span data-stu-id="f594e-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**REPFILESNOTFOUND WBEM WBEM WBEM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-182">3221231086 (0xC00015EE)</span><span class="sxs-lookup"><span data-stu-id="f594e-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-183">Au démarrage du service, le service Windows Management Instrumentation n’a pas pu trouver les fichiers du référentiel.</span><span class="sxs-lookup"><span data-stu-id="f594e-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="f594e-184">Un nouveau référentiel est créé en fonction du mécanisme de récupération automatique.</span><span class="sxs-lookup"><span data-stu-id="f594e-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ lancé avec \_ succès**</span><span class="sxs-lookup"><span data-stu-id="f594e-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-186">3221231087 (0xC00015EF)</span><span class="sxs-lookup"><span data-stu-id="f594e-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-187">Le service de Windows Management Instrumentation a démarré.</span><span class="sxs-lookup"><span data-stu-id="f594e-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**le support technique de la norme WBEM \_ MD \_ WBEM \_ Core ESS a été \_ \_ \_ initialisé**</span><span class="sxs-lookup"><span data-stu-id="f594e-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-189">3221231089 (0xC00015F1)</span><span class="sxs-lookup"><span data-stu-id="f594e-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-190">Les sous-systèmes du service Windows Management Instrumentation correctement initialisés.</span><span class="sxs-lookup"><span data-stu-id="f594e-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**échec de l' \_ \_ \_ initialisation du service WBEM \_ MD WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="f594e-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-192">3221225501 (0xC000001D)</span><span class="sxs-lookup"><span data-stu-id="f594e-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-193">Le numéro d’erreur %1 a été retourné lors de la tentative d’initialisation du service Windows Management Instrumentation.</span><span class="sxs-lookup"><span data-stu-id="f594e-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="f594e-194">Cela peut être dû à une version incorrecte de WMI, à une erreur de mise à niveau du référentiel WMI, à un espace disque insuffisant ou à une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f594e-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f594e-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_ \_ référentiel WBEM WBEM WBEM \_ \_ recréé**</span><span class="sxs-lookup"><span data-stu-id="f594e-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f594e-196">3221231088 (0xC00015F0)</span><span class="sxs-lookup"><span data-stu-id="f594e-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="f594e-197">Windows Management Instrumentation référentiel recréé avec succès à l’aide du mécanisme de récupération automatique.</span><span class="sxs-lookup"><span data-stu-id="f594e-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f594e-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f594e-198">Requirements</span></span>



| <span data-ttu-id="f594e-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f594e-199">Requirement</span></span> | <span data-ttu-id="f594e-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f594e-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f594e-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f594e-201">Minimum supported client</span></span><br/> | <span data-ttu-id="f594e-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f594e-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f594e-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f594e-203">Minimum supported server</span></span><br/> | <span data-ttu-id="f594e-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f594e-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f594e-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f594e-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f594e-206">Événements WMI</span><span class="sxs-lookup"><span data-stu-id="f594e-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

[<span data-ttu-id="f594e-207">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="f594e-207">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> </dl>

 

 





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
# <a name="wmi-event-messages"></a>Messages d’événement WMI

La liste suivante répertorie les événements pris en charge par les journaux WMI dans Windows Vista et les systèmes d’exploitation ultérieurs.

> [!Note]  
> La documentation suivante est conçue pour les développeurs et les administrateurs informatiques. Si vous tentez de résoudre un message d’erreur WMI sur votre système d’hébergement, consultez le site Web [support Microsoft](https://support.microsoft.com/) .

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_référentiel MC WBEM \_ \_ incohérent**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



Le service de Windows Management Instrumentation a détecté une incohérence avec l’espace de stockage WMI dans le répertoire *% windir% \\ system32 \\ WBEM \\* et n’a pas pu le récupérer. L’espace de stockage WMI sera à présent supprimé. un nouveau référentiel sera créé en fonction du mécanisme de récupération automatique.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_chargement du \_ \_ fournisseur LOCALSYSTEM du sous-système \_ LOCALSYSTEM du \_ fournisseur WBEM \_**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Un fournisseur, %1, a été inscrit dans le Windows Management Instrumentation l’espace de noms %2 pour utiliser le compte LocalSystem. Ce compte est privilégié et le fournisseur peut entraîner une violation de la sécurité s’il n’emprunte pas correctement les demandes des utilisateurs.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_MOF MD \_ WBEM \_ non \_ chargé \_ lors de la \_ récupération**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Erreur %1 rencontrée lors de la tentative de chargement du fichier MOF %2 lors de la récupération. Fichier MOF marqué avec la récupération automatique.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**le \_ filtre MC WBEM \_ ne peut pas \_ activer le \_ filtre**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Impossible de réactiver le filtre d’événement avec la requête « %2 » dans l’espace de noms « %1 » en raison de l’erreur %3. Les événements ne peuvent pas être remis via ce filtre tant que le problème n’est pas corrigé.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_requête de \_ fournisseur d’événements non valide WBEM MC \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



Le fournisseur d’événements %1 a tenté d’inscrire une requête syntaxiquement non valide « %2 ». La requête sera ignorée. La requête peut être corrigée en examinant le référentiel WMI avec CIM Studio et en mettant à jour les abonnements permanents pour le fournisseur et la requête listés. Si l’abonnement permanent est créé avec un fichier MOF fourni avec un produit installé, le fournisseur de l’application doit être contacté pour corriger l’inscription défectueuse.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ requête intrinsèque de fournisseur d’événements non \_ valide \_ WBEM MC**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



Le fournisseur d’événements %1 a tenté d’enregistrer une requête d’événement intrinsèque « %2 » dans l’espace de noms %3 pour lequel le jeu de classes d’objets cibles n’a pas pu être déterminé. La requête sera ignorée.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_requête du fournisseur d’événement MC WBEM \_ \_ \_ \_ trop \_ large**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



Le fournisseur d’événements %1 a tenté d’inscrire la requête "%2" dans l’espace de noms %3 qui est trop large. Les fournisseurs d’événements ne peuvent pas fournir des événements fournis par le système. La requête sera ignorée. Contactez le fournisseur de l’application.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_requête de fournisseur d’événements WBEM MD \_ \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



Le fournisseur d’événements %1 a tenté d’inscrire la requête « %2 » dont la classe cible « %3 » dans l’espace de noms %4 n’existe pas. La requête sera ignorée.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_événement de \_ requête de fournisseur d’événement MC WBEM \_ \_ \_ non \_**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



Le fournisseur d’événements %1 a tenté d’inscrire la requête &quot; %2 &quot; dont la classe cible &quot; %3 &quot; n’est pas une classe d’événements. La requête sera ignorée. Contactez le fournisseur de l’application.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**échec WBEM du noyau WBEM \_ MD \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Échec de l’initialisation de WMI Core ou du sous-système du fournisseur ou du sous-système d’événements avec le numéro d’erreur %1. Cela peut être dû à une version incorrecte de WMI, à une erreur de mise à niveau du référentiel WMI, à un espace disque insuffisant ou à une mémoire insuffisante.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_échec de connexion WBEM MC \_ adap \_ \_**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Windows Management Instrumentation ADAP n’a pas pu se connecter à l’espace de noms %1 avec l’erreur suivante : %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_échec de \_ PUTCLASS WBEM adap \_ PERFLIB \_ \_**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Windows Management Instrumentation ADAP n’a pas pu enregistrer l’objet %1 dans l’espace de noms %2 en raison de l’erreur suivante : %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ adap \_ ne peut pas \_ \_ ajouter \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Windows Management Instrumentation ADAP n’a pas pu créer la \_ classe de base de performances Win32 dans %1 : résultat = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ adap \_ ne peut pas \_ \_ ajouter \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Windows Management Instrumentation ADAP n’a pas pu créer la \_ classe de base Win32 PerfRawData %1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ échec \_ du démarrage du référentiel \_ MC WBEM**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



Le service Windows Management Instrumentation n’a pas pu charger les fichiers du référentiel sous le répertoire *% windir% \\ system32 \\ WBEM \\*. Cela peut être dû à un endommagement dans les fichiers de référentiel, aux paramètres de sécurité de ce répertoire, à un manque d’espace disque ou à d’autres problèmes de ressources système tels que l’insuffisance de mémoire. Si cette erreur se produit à chaque redémarrage de l’ordinateur, l’administrateur de cet ordinateur devra peut-être arrêter le service WMI, passer en revue le paramètre de sécurité sur ce dossier et les fichiers de ce dossier, puis exécuter WMIDiag pour valider l’intégrité de Windows Management Instrumentation.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**la \_ WBEM MD WBEM \_ \_ requiert un \_ chiffrement \_ refusé**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



L’accès à l’espace de noms %1 a été refusé parce que l’espace de noms est marqué avec RequiresEncryption, mais le script ou l’application a tenté de se connecter à cet espace de noms avec un niveau d’authentification inférieur à la **\_ confidentialité PKT**. Remplacez le niveau d’authentification par **PKT \_ Privacy** , puis exécutez de nouveau le script ou l’application.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**le \_ WBEM MC WBEM \_ \_ requiert un \_ chiffrement \_ asynchrone \_ refusé**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Windows Management Instrumentation service n’a pas pu fournir de résultats de manière asynchrone pour l’espace de noms %1. L’espace de noms est marqué avec RequiresEncryption, mais WinMgmt n’a pas pu établir une connexion sécurisée à l’ordinateur client. Assurez-vous qu’il existe une relation d’approbation entre les ordinateurs client et serveur afin que le client reconnaisse le compte de l’ordinateur serveur.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_ \_ hôte WBEM MD \_ WBEM \_ supprimé**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Windows Management Instrumentation s’est arrêté WMIPRVSE.EXE, car un quota a atteint une valeur d’avertissement. Quota : %1 valeur : %2 valeur maximale : %3 WMIPRVSE PID : %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**REPFILESNOTFOUND WBEM WBEM WBEM \_ \_ \_**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Au démarrage du service, le service Windows Management Instrumentation n’a pas pu trouver les fichiers du référentiel. Un nouveau référentiel est créé en fonction du mécanisme de récupération automatique.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ lancé avec \_ succès**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Le service de Windows Management Instrumentation a démarré.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**le support technique de la norme WBEM \_ MD \_ WBEM \_ Core ESS a été \_ \_ \_ initialisé**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Les sous-systèmes du service Windows Management Instrumentation correctement initialisés.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**échec de l' \_ \_ \_ initialisation du service WBEM \_ MD WBEM \_**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



Le numéro d’erreur %1 a été retourné lors de la tentative d’initialisation du service Windows Management Instrumentation. Cela peut être dû à une version incorrecte de WMI, à une erreur de mise à niveau du référentiel WMI, à un espace disque insuffisant ou à une mémoire insuffisante.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_ \_ référentiel WBEM WBEM WBEM \_ \_ recréé**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Windows Management Instrumentation référentiel recréé avec succès à l’aide du mécanisme de récupération automatique.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements WMI](wmi-events.md)
</dt> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 





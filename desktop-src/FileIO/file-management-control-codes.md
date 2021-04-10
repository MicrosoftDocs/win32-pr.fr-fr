---
description: Codes de contrôle utilisés dans la gestion des fichiers.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Codes de contrôle de gestion des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868242"
---
# <a name="file-management-control-codes"></a>Codes de contrôle de gestion des fichiers

Les codes de contrôle suivants sont utilisés dans la gestion des fichiers.

## <a name="in-this-section"></a>Dans cette section



| Code de contrôle                                                                                    | Description                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ autoriser \_ les \_ \_ e/s étendues DASD**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Signale au pilote du système de fichiers qu’il n’effectue aucune vérification de la limite d’e/s sur les appels de lecture ou d’écriture de la partition.<br/>                                                                                  |
| [**FSCTL \_ crée \_ ou \_ Obtient \_ l' \_ ID d’objet**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Récupère l’identificateur d’objet pour le fichier ou le répertoire spécifié. S’il n’existe aucun identificateur d’objet, l’utilisation de **FSCTL \_ Create \_ ou de l' \_ \_ \_ ID d’objet** en crée un.<br/>                           |
| [**FSCTL \_ , \_ contrôle CSV**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Récupère les résultats d’une opération de contrôle CSV.<br/>                                                                                                                                        |
| [**ID de suppression de l' \_ \_ objet FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Supprime l’identificateur d’objet d’un fichier ou d’un répertoire spécifié.<br/>                                                                                                                        |
| [**FSCTL \_ les \_ Extensions dupliquées dans le \_ \_ fichier**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Indique au système de fichiers de copier une plage d’octets de fichier pour le compte d’une application.<br/>                                                                                                     |
| [**\_ \_ découpage au niveau du fichier FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Indique au système de stockage les plages du fichier qui ne sont pas nécessaires pour être stockées.<br/>                                                                                                    |
| [**statistiques d’extraction du système de \_ fichiers FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Récupère les informations à partir de différents compteurs de performances du système de fichiers.<br/>                                                                                                                 |
| [**\_statistiques d’extraction du système de fichiers FSCTL \_ \_ \_ ex**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Récupère les informations à partir de différents compteurs de performances du système de fichiers.<br/> Prise en charge de ce code de contrôle démarré avec Windows 10.<br/>                                               |
| [**FSCTL \_ Rechercher les \_ fichiers \_ par \_ sid**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Recherche un fichier dont le propriétaire du créateur correspond au SID spécifié.<br/>                                                                                                           |
| [**FSCTL \_ recevoir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Récupère l’état de compression actuel d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par flux.<br/>                                                            |
| [**FSCTL \_ Obtient \_ un \_ enregistrement de fichier NTFS \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Récupère le premier enregistrement de fichier en cours d’utilisation et est d’une valeur ordinale inférieure ou égale au numéro de référence de fichier demandé.<br/>                                                    |
| [**ID de l' \_ \_ objet FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Récupère l’identificateur d’objet pour le fichier ou le répertoire spécifié.<br/>                                                                                                                     |
| [**réparation de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Récupère des informations sur le mécanisme de réparation automatique du système de fichiers NTFS.<br/>                                                                                                               |
| [**FSCTL \_ lancer la \_ réparation**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Déclenche le système de fichiers NTFS pour démarrer un cycle d’auto-réparation sur un seul fichier.<br/>                                                                                                            |
| [**FSCTL \_ rendre \_ compatible le média \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Ferme une session UDF ouverte sur un média en écriture unique pour rendre la mémoire média compatible.<br/>                                                                                                         |
| [**fermeture de l’accusé de réception FSCTL \_ OPBATCH \_ \_ \_ en attente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Avertit un serveur qu’une application cliente est prête à fermer un fichier.<br/>                                                                                                                    |
| [**FSCTL de \_ rupture de verrou OPLOCK \_ \_ \_ non \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Répond à la notification selon laquelle un verrou opportuniste sur un fichier va être interrompu. Utilisez cette opération pour déverrouiller tous les verrous opportunistes sur le fichier tout en conservant l’ouverture du fichier.<br/>            |
| [**\_accusé de réception FSCTL OPLOCK \_ break \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Répond à la notification selon laquelle un verrou opportuniste exclusif sur un fichier va être interrompu. Utilisez cette opération pour indiquer que le fichier doit recevoir un verrou opportuniste de niveau 2.<br/> |
| [**\_notification de \_ rupture \_ OPLOCK FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Permet à l’application appelante d’attendre la fin d’un arrêt de verrouillage opportuniste.<br/>                                                                                                   |
| [**\_ \_ plages allouées par la requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Analyse un fichier ou un autre flux de données à la recherche de plages pouvant contenir des données différentes de zéro.<br/>                                                                                                       |
| [**\_requête FSCTL \_ sur les informations sur le \_ volume de disque \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Demande des informations sur le volume propres à UDF.<br/>                                                                                                                                                |
| [**\_informations de \_ remplacement de requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Récupère les propriétés de gestion des défauts du volume. Utilisé pour les systèmes de fichiers UDF.<br/>                                                                                                     |
| [**\_fichier de rappel FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Rappelle un fichier à partir du support de stockage géré par le stockage distant, qui est le logiciel de gestion de stockage hiérarchique.<br/>                                                                    |
| [**\_ \_ OPLOCK batch de demande FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Demande un verrou de traitement opportuniste sur un fichier.<br/>                                                                                                                                           |
| [**\_ \_ OPLOCK filtre de requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Demande un verrou opportuniste de filtre sur un fichier.<br/>                                                                                                                                          |
| [**\_OPLOCK Request \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Demande un verrou opportuniste (oplock) sur un fichier et reconnaît qu’une interruption oplock s’est produite.<br/>                                                                                    |
| [**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Demande un verrou opportuniste de niveau 1 sur un fichier.<br/>                                                                                                                                         |
| [**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Demande un verrou opportuniste de niveau 2 sur un fichier.<br/>                                                                                                                                         |
| [**FSCTL \_ définir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Définit l’état de compression d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par fichier et par répertoire.<br/>                                                         |
| [**FSCTL \_ définir \_ la \_ gestion des défauts**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Définit l’état de gestion des défauts logiciels pour le fichier spécifié. Utilisé pour les systèmes de fichiers UDF.<br/>                                                                                             |
| [**\_ID d' \_ objet du jeu de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Définit l’identificateur d’objet pour le fichier ou le répertoire spécifié.<br/>                                                                                                                          |
| [**ID d’objet du jeu de FSCTL \_ \_ \_ \_ étendu**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Modifie les données utilisateur associées à l’identificateur d’objet pour le fichier ou le répertoire spécifié.<br/>                                                                                            |
| [**\_réparation du jeu de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Définit le mode de la fonctionnalité d’auto-réparation d’un système de fichiers NTFS.<br/>                                                                                                                          |
| [**FSCTL \_ Set \_ Sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Marque le fichier indiqué comme étant fragmenté ou non fragmenté. Dans un fichier partiellement alloué, les plages de zéros volumineuses ne peuvent pas nécessiter l’allocation de disque.<br/>                                                               |
| [**FSCTL ne pas \_ définir de \_ \_ données zéro**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Remplit une plage spécifiée d’un fichier avec des zéros (0).<br/>                                                                                                                                        |
| [**FSCTL \_ définie \_ \_ sur zéro à la \_ désallocation**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Indique qu’un descripteur de fichier du système de fichiers NTFS doit avoir ses clusters remplis de zéros lorsqu’il est libéré.<br/>                                                                             |
| [**FSCTL \_ attente \_ de la \_ réparation**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Retourne une valeur lorsque les réparations spécifiées sont terminées.<br/>                                                                                                                                        |



 

Les codes de contrôle suivants sont utilisés avec la [compression et la décompression des fichiers](file-compression-and-decompression.md).

<dl>

[**FSCTL \_ recevoir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**FSCTL \_ définir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Les codes de contrôle suivants sont utilisés avec les [identificateurs d’objet](distributed-link-tracking-and-object-identifiers.md).

<dl>

[**FSCTL \_ crée \_ ou \_ Obtient \_ l' \_ ID d’objet**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**ID de suppression de l' \_ \_ objet FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**ID de l' \_ \_ objet FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**\_ID d' \_ objet du jeu de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**ID d’objet du jeu de FSCTL \_ \_ \_ \_ étendu**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Les codes de contrôle suivants sont utilisés avec des [verrous opportunistes](opportunistic-locks.md).

<dl>

[**fermeture de l’accusé de réception FSCTL \_ OPBATCH \_ \_ \_ en attente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL de \_ rupture de verrou OPLOCK \_ \_ \_ non \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_accusé de réception FSCTL OPLOCK \_ break \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notification de \_ rupture \_ OPLOCK FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ OPLOCK batch de demande FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ OPLOCK filtre de requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_OPLOCK Request \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Les codes de contrôle suivants sont utilisés avec les [fichiers partiellement alloués](sparse-files.md).

<dl>

[**\_ \_ plages allouées par la requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ Set \_ Sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL ne pas \_ définir de \_ \_ données zéro**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

Les codes de contrôle suivants sont utilisés avec le mécanisme de réparation automatique NTFS.

<dl>

[**réparation de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**FSCTL \_ lancer la \_ réparation**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**\_réparation du jeu de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**FSCTL \_ attente \_ de la \_ réparation**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Les codes de contrôle suivants sont utilisés avec UDF.

<dl>

[**FSCTL \_ rendre \_ compatible le média \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**\_requête FSCTL \_ sur les informations sur le \_ volume de disque \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**\_informations de \_ remplacement de requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**FSCTL \_ définir \_ la \_ gestion des défauts**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes de contrôle de gestion d’annuaire](directory-management-control-codes.md)
</dt> <dt>

[Codes de contrôle de gestion des volumes](volume-management-control-codes.md)
</dt> </dl>

 


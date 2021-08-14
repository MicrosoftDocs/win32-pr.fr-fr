---
title: Stockage Fonctions de l’adaptateur
description: Un adaptateur de stockage gère les bases de données de modèles.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911801"
---
# <a name="storage-adapter-functions"></a>Stockage Fonctions de l’adaptateur

Un adaptateur de stockage gère les bases de données de modèles. Les fonctions suivantes doivent être implémentées par le développeur de l’adaptateur. elles sont appelées par le service biométrique Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                         | Description                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | donne à l’adaptateur Stockage la possibilité d’effectuer tout travail nécessaire pour rendre le composant de stockage inactif.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Ajoute un modèle à la base de données.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Ajoute un adaptateur de stockage au pipeline de traitement de l’unité biométrique.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Prépare le pipeline de traitement de l’unité biométrique pour une nouvelle opération.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Ferme la base de données associée au pipeline et libère toutes les ressources associées.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Effectue une opération de contrôle définie par le fournisseur qui ne requiert pas de privilèges élevés.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Effectue une opération de contrôle définie par le fournisseur qui requiert des privilèges élevés.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Crée et configure une nouvelle base de données.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | donne à l’adaptateur Stockage la possibilité d’effectuer les tâches nécessaires pour mettre le composant de stockage en état d’inactivité.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Supprime un ou plusieurs modèles de la base de données.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Libère les ressources spécifiques à l’adaptateur attachées au pipeline.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Efface la base de données et la marque en vue de sa suppression.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Positionne le curseur de jeu de résultats sur le premier enregistrement dans le jeu.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Récupère le contenu de l’enregistrement en cours dans le jeu de résultats du pipeline.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Récupère la taille de la base de données et l’espace disponible.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Récupère les informations relatives au format et à la version utilisées par la base de données actuelle associée au pipeline.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Récupère le nombre d’enregistrements de modèle dans le jeu de résultats du pipeline.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Avance le curseur de jeu de résultats d’un enregistrement.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Reçoit une notification concernant une modification de l’état d’alimentation de l’ordinateur et prépare la carte de stockage en conséquence.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Ouvre une base de données destinée à être utilisée par la carte de stockage.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | donne à l’adaptateur Stockage la possibilité d’effectuer un nettoyage en vue de la fermeture de la base de données du modèle.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | donne à l’adaptateur Stockage la possibilité d’effectuer une initialisation qui reste incomplète.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Interroge la base de données actuellement ouverte pour les modèles associés à un vecteur d’index spécifié.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Interroge la base de données actuellement ouverte pour les modèles associés à une identité et un sous-facteur spécifiés.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Détermine les fonctionnalités et les limitations du composant de stockage biométrique.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Récupère un pointeur vers la structure de l' [**\_ \_ interface de stockage WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) pour l’adaptateur de stockage.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> </dl>

 

 






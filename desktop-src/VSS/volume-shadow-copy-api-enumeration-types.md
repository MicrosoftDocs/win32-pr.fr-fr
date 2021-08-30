---
description: Les énumérations suivantes sont définies dans l’API de cliché instantané des volumes.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Énumérations de l’API de cliché instantané du volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451aec8bf8ef95f8ac86d6a0b496a3205c90d94215cecd044707af5502e50b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866179"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Énumérations de l’API de cliché instantané du volume

Les énumérations suivantes sont définies dans l’API de cliché instantané des volumes.



| Nom                                                                           | Description                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**État de l' \_ enregistreur alternatif VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Définit le jeu d’États valides utilisé pour indiquer si un writer est associé à un autre writer.                                                              |
| [**niveau de l' \_ application VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Définit l’ensemble des niveaux d’application valides.                                                                                                                       |
| [**\_schéma de sauvegarde VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Définit l’ensemble des schémas de sauvegarde (opérations qu’un enregistreur peut participer).                                                                                          |
| [**\_type de sauvegarde VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Définit l’ensemble des types de sauvegarde.                                                                                                                                   |
| [**\_indicateurs du composant VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Indique la prise en charge de la récupération automatique.                                                                                                                               |
| [**\_type de composant VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Définit l’ensemble des types de composants.                                                                                                                                |
| [**\_État de \_ restauration de fichier VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Définit l’ensemble des États d’une opération de restauration de fichiers.                                                                                                           |
| [**\_type de \_ \_ sauvegarde spec de fichier \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Définit le jeu d’opérations de sauvegarde pris en charge par les writers.                                                                                                         |
| [**\_\_options matérielles VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Définit les indicateurs LUN des clichés instantanés.                                                                                                                                     |
| [**\_type d' \_ objet de gestion VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminante pour l’Union d' [**\_ Union d' \_ objets \_ de gestion VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) dans la structure prop de l' [**\_ \_ objet \_ de gestion VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_type d’objet VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Utilisé pour identifier un objet en tant que jeu de clichés instantanés, cliché instantané ou fournisseur.                                                                                         |
| [**\_erreur de protection VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Définit l’ensemble des erreurs de protection contre les clichés instantanés.                                                                                                                  |
| [**\_niveau de protection VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Définit l’ensemble des niveaux de protection du cliché instantané du volume.                                                                                                           |
| [**\_fonctionnalités du fournisseur VSS \_**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Réservé pour un usage futur.                                                                                                                                           |
| [**\_type de fournisseur VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Définit l’ensemble des types de fournisseurs.                                                                                                                                 |
| [**\_options de récupération VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Utilisé par un demandeur pour spécifier le mode d’exécution d’une opération de resynchronisation.                                                                               |
| [**\_cible de restauration VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Définit l’ensemble des cibles de restauration.                                                                                                                                |
| [**\_type de restauration VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Définit l’ensemble des opérations de restauration à effectuer.                                                                                                              |
| [**\_ \_ énumération VSS RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Définit l’ensemble des méthodes de restauration de fichiers par défaut pour un writer.                                                                                                      |
| [**\_type de restauration par progression VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Utilisé par un demandeur pour indiquer le type d’opération de restauration par progression qu’il va effectuer.                                                                         |
| [**\_compatibilité des instantanés VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Définit l’ensemble des opérations de contrôle de volume ou d’e/s de fichier qui peuvent être désactivées pour un volume qui a été copié par des clichés instantanés.                                            |
| [**\_\_contexte de capture instantanée VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Spécifie la manière dont un cliché instantané doit être créé, interrogé ou supprimé, ainsi que le degré d’implication du rédacteur.                                                            |
| [**État de l' \_ instantané VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Définit l’ensemble des États d’une opération de cliché instantané.                                                                                                              |
| [**\_type de source VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Définit l’ensemble des types de données qu’un writer peut gérer.                                                                                                         |
| [**\_masque d’abonnement VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Définit l’ensemble des événements qu’un writer peut recevoir.                                                                                                               |
| [**\_type d’utilisation de VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Spécifie comment le système hôte utilise les données gérées par un enregistreur.                                                                                                   |
| [**\_attributs de l' \_ instantané du volume VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Définit l’ensemble des attributs d’un cliché instantané.                                                                                                                    |
| [**État de l' \_ enregistreur VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Définit l’ensemble des États du writer.                                                                                                                           |
| [**\_ \_ énumération VSS WRITERRESTORE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Définit l’ensemble de conditions sous lequel un writer gère les événements générés au cours d’une opération de restauration.                                                        |



 

 

 




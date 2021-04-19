---
description: Les structures suivantes sont utilisées pour créer et gérer des répertoires et des fichiers d’espace réservé.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Structures de filtre Cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517420"
---
# <a name="cloud-filter-structures"></a>Structures de filtre Cloud

Les structures suivantes sont utilisées pour créer et gérer des répertoires et des fichiers d’espace réservé.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informations de rappel CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contient des informations de rappel courantes.<br/>                                                                                          |
| [**\_paramètres de rappel CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contient des paramètres spécifiques au rappel, tels que le décalage de fichier, la longueur, les indicateurs, etc.<br/>                                                 |
| [**\_inscription de rappel CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Rappels à inscrire par le fournisseur de synchronisation.<br/>                                                                           |
| [**\_plage de fichiers CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Spécifie une plage de données dans un fichier d’espace réservé.<br/>                                                                               |
| [**\_ \_ mémoire tampon des plages de fichiers CF \_**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Structure permettant de décrire l’emplacement et la plage de données dans un fichier.<br/>                                                              |
| [**\_ \_ métadonnées CF FS**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Métadonnées de répertoire ou de fichier d’espace réservé.<br/>                                                                                        |
| [**\_stratégie d’hydratation CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Spécifie la stratégie d’alimentation principale et son modificateur.<br/>                                                                       |
| [**\_informations sur l’opération CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informations sur une opération sur un fichier ou un dossier d’espace réservé.<br/>                                                                |
| [**\_paramètres d’opération CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Paramètres d’une opération sur un fichier ou un dossier d’espace réservé.<br/>                                                                    |
| [**informations de base de l' \_ espace réservé CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Informations d’espace réservé de base.<br/>                                                                                                 |
| [**\_espace réservé CF- \_ créer des \_ informations**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contient des informations d’espace réservé pour la création de nouveaux fichiers ou répertoires d’espaces réservés. <br/>                                           |
| [**INFO standard de l' \_ espace réservé CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Informations d’espace réservé standard.<br/>                                                                                              |
| [**\_informations sur la plateforme CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Retourne des informations pour la plateforme de fichiers Cloud. Cela est destiné aux fournisseurs de synchronisation qui s’exécutent sur plusieurs versions de Windows.<br/> |
| [**\_stratégie de remplissage CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Spécifie la stratégie de remplissage principale et son modificateur.<br/>                                                                      |
| [**\_informations sur le processus CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contient des informations sur un processus utilisateur.<br/>                                                                                     |
| [**\_stratégies de synchronisation CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Définit les stratégies de synchronisation utilisées par une racine de synchronisation.<br/>                                                                                 |
| [**inscription de la \_ synchronisation CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Détails du fournisseur de synchronisation et de la racine de synchronisation à inscrire.<br/>                                                               |
| [**informations de base de la \_ racine CF Sync \_ \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Informations de base sur la racine de synchronisation.<br/>                                                                                                   |
| [**\_ \_ \_ informations sur le fournisseur \_ racine CF Sync**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Synchroniser les informations du fournisseur racine.<br/>                                                                                                |
| [**\_ \_ \_ informations standard de la racine CF Sync \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Informations de racine de synchronisation standard.<br/>                                                                                                |
| [**État de la \_ synchronisation CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Utilisé dans une structure d' [**\_ \_ informations sur l’opération CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) pour décrire l’état d’une racine de synchronisation spécifiée.<br/>     |



 

 


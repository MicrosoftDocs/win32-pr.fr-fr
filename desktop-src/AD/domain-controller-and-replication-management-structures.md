---
title: Structures de contrôleur de domaine et de gestion de la réplication
description: Les fonctions de contrôleur de domaine et de gestion de la réplication utilisent les structures suivantes.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e7ddd37001b3b349159a21137fc1ae7b488c3a4997ac5f406677e3d421969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018250"
---
# <a name="domain-controller-and-replication-management-structures"></a>Structures de contrôleur de domaine et de gestion de la réplication

Les fonctions de contrôleur de domaine et de gestion de la réplication utilisent les structures suivantes :

-   [**\_ \_ \_ Informations 1 sur le contrôleur de domaine DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**\_Informations sur le contrôleur de domaine DS \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**\_Informations sur le contrôleur de domaine DS \_ \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**\_résultat du nom du service de domaine \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**\_élément de \_ résultat de nom de service d’annuaire \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**\_métadonnées de l’attr Directory REPL \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**Métadonnées de l’attr de la \_ REPL DS \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**\_ \_ \_ \_ objet blob de métadonnées de l’attr DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**\_ \_ \_ métadonnées de valeur \_ attr \_ de l’annuaire de réplication**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**\_ \_ \_ Métadonnées de valeur \_ attr \_ de \_ service d’annuaire DS 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**EXT. de \_ \_ \_ \_ métadonnées de la valeur attr \_ de DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**\_curseur de réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**\_Curseur REPL \_ DS \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**\_Curseur REPL \_ DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**\_ \_ objet blob de curseurs REPL DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_ \_ curseurs REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**\_ \_ Curseurs REPL DS \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**\_ \_ Curseurs REPL DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**\_ \_ \_ échec DSA du KCC \_ du service d’annuaire de réplication**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**\_ \_ \_ échecs DSA du KCC \_ du service d’annuaire de réplication**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**\_ \_ \_ \_ objet blob de FAILUREW du \_ KCC de service d’annuaire**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**service de \_ réplication de \_ voisin DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**\_voisins de réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**\_objet blob de réplication de \_ NEIGHBORW DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**métadonnées du service de \_ réplication de \_ \_ \_ données**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**Métadonnées du service de \_ réplication de \_ \_ \_ données \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**réplication DS \_ REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**\_objet blob de réplication de \_ OPW DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**\_opérations de réplication \_ en attente DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**\_STATISTICSW de \_ file d’attente de RÉplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**\_ \_ \_ objet BLOB STATISTICSW de file d’attente de réplication DS \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**\_métadonnées de la valeur de réplication DS \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**\_Métadonnées de valeur de réplication DS \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**\_ext. \_ de \_ métadonnées de valeur de \_ réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**\_ \_ \_ \_ objet blob de métadonnées de valeur de réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**\_ext. \_ blob de \_ métadonnées de valeur de \_ \_ réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**\_REPSYNCALL DS \_ ERRINFO**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**\_synchronisation REPSYNCALL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**\_ \_ mise à jour de REPSYNCALL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**\_mappage du \_ GUID du schéma DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**\_ \_ informations sur le coût du site DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**PROGRAMMATEUR**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**\_en-tête de planification**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Structures dans Active Directory Domain Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 
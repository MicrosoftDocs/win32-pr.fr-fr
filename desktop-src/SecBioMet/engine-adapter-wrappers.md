---
title: Wrappers d’adaptateur de moteur
description: Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de moteur. Ces fonctions sont définies dans WinBio \_ adapter. h.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218100"
---
# <a name="engine-adapter-wrappers"></a>Wrappers d’adaptateur de moteur

Les fonctions wrapper suivantes sont définies dans WinBio \_ adapter. h. Vous pouvez les utiliser pour appeler des fonctions sur votre adaptateur de moteur.



| Fonction                                           | Description                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioEngineAcceptSampleData<br/>              | Appelle la fonction [**EngineAdapterAcceptSampleData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) .<br/>                                                                                                 |
| WbioEngineActivate<br/>                      | Appelle la fonction [**EngineAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                                           |
| WbioEngineAttach<br/>                        | Appelle la fonction [**EngineAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) .<br/>                                                                                                                     |
| WbioEngineCheckForDuplicate<br/>             | Appelle la fonction [**EngineAdapterCheckForDuplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) .<br/>                                                                                               |
| WbioEngineClearContext<br/>                  | Appelle la fonction [**EngineAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) .<br/>                                                                                                         |
| WbioEngineCommitEnrollment<br/>              | Appelle la fonction [**EngineAdapterCommitEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineControlUnit<br/>                   | Appelle la fonction [**EngineAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) .<br/>                                                                                                           |
| WbioEngineControlUnitPrivileged<br/>         | Appelle la fonction [**EngineAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) .<br/>                                                                                       |
| WbioEngineCreateEnrollment<br/>              | Appelle la fonction [**EngineAdapterCreateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineDeactivate<br/>                    | Appelle la fonction [**EngineAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                                       |
| WbioEngineDetach<br/>                        | Appelle la fonction [**EngineAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) .<br/>                                                                                                                     |
| WbioEngineDiscardEnrollment<br/>             | Appelle la fonction [**EngineAdapterDiscardEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) .<br/>                                                                                               |
| WbioEngineExportEngineData<br/>              | Appelle la fonction [**EngineAdapterExportEngineData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) .<br/>                                                                                                 |
| WbioEngineGetEnrollmentHash<br/>             | Appelle la fonction [**EngineAdapterGetEnrollmentHash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) .<br/>                                                                                               |
| WbioEngineGetEnrollmentStatus<br/>           | Appelle la fonction [**EngineAdapterGetEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) .<br/>                                                                                           |
| WbioEngineIdentifyAll<br/>                   | Appelle la fonction [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                                     |
| WbioEngineIdentifyFeatureSet<br/>            | Appelle la fonction [**EngineAdapterIdentifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) .<br/>                                                                                             |
| WbioEngineNotifyPowerChange<br/>             | Appelle la fonction [*EngineAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 8.<br/>                            |
| WbioEnginePipelineCleanup<br/>               | Appelle la fonction [**EngineAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                             |
| WbioEnginePipelineInit<br/>                  | Appelle la fonction [**EngineAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                                   |
| WbioEngineQueryCalibrationData<br/>          | Appelle la fonction [**EngineAdapterQueryCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                   |
| WbioEngineQueryExtendedEnrollmentStatus<br/> | Appelle la fonction [**EngineAdapterQueryExtendedEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/> |
| WbioEngineQueryExtendedInfo<br/>             | Appelle la fonction [**EngineAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                         |
| WbioEngineQueryHashAlgorithms<br/>           | Appelle la fonction [**EngineAdapterQueryHashAlgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) .<br/>                                                                                           |
| WbioEngineQueryIndexVectorSize<br/>          | Appelle la fonction [**EngineAdapterQueryIndexVectorSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) .<br/>                                                                                         |
| WbioEngineQueryPreferredFormat<br/>          | Appelle la fonction [**EngineAdapterQueryPreferredFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) .<br/>                                                                                         |
| WbioEngineQuerySampleHint<br/>               | Appelle la fonction [**EngineAdapterQuerySampleHint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) .<br/>                                                                                                   |
| WbioEngineRefreshCache<br/>                  | Appelle la fonction [**EngineAdapterRefreshCache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                                   |
| WbioEngineSelectCalibrationFormat<br/>       | Appelle la fonction [**EngineAdapterSelectCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>             |
| WbioEngineSetAccountPolicy<br/>              | Appelle la fonction [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                           |
| WbioEngineSetEnrollmentParameters<br/>       | Appelle la fonction [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>             |
| WbioEngineSetEnrollmentSelector<br/>         | Appelle la fonction [**EngineAdapterSetEnrollmentSelector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                 |
| WbioEngineSetHashAlgorithm<br/>              | Appelle la fonction [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .<br/>                                                                                                 |
| WbioEngineUpdateEnrollment<br/>              | Appelle la fonction [**EngineAdapterUpdateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineVerifyFeatureSet<br/>              | Appelle la fonction [**EngineAdapterVerifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) .<br/>                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions d’adaptateur de moteur](engine-adapter-functions.md)
</dt> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> </dl>

 

 






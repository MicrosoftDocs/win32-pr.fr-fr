---
title: Stockage Wrappers d’adaptateur
description: Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de stockage. Ces fonctions sont définies dans WinBio \_ adapter. h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6308dda71cd279ae07e0849c0760526f116de6295bb0555f530f31a0033a5851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911602"
---
# <a name="storage-adapter-wrappers"></a>Stockage Wrappers d’adaptateur

Les fonctions wrapper suivantes sont définies dans WinBio \_ adapter. h. Vous pouvez les utiliser pour appeler des fonctions sur votre adaptateur de stockage.



| Fonction                                    | Description                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Appelle la fonction [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Appelle la fonction [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) .<br/>                                                                                       |
| WbioStorageAttach<br/>                | Appelle la fonction [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) .<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Appelle la fonction [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) .<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Appelle la fonction [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) .<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Appelle la fonction [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) .<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Appelle la fonction [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) .<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Appelle la fonction [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) .<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Appelle la fonction [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Appelle la fonction [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) .<br/>                                                                                 |
| WbioStorageDetach<br/>                | Appelle la fonction [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) .<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Appelle la fonction [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) .<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Appelle la fonction [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) .<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Appelle la fonction [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) .<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Appelle la fonction [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) .<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Appelle la fonction [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) .<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Appelle la fonction [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) .<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Appelle la fonction [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) .<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Appelle la fonction [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Appelle la fonction [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) .<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Appelle la fonction [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Appelle la fonction [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Appelle la fonction [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) .<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Appelle la fonction [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) .<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Appelle la fonction [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Stockage Fonctions de l’adaptateur](storage-adapter-functions.md)
</dt> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> </dl>

 

 






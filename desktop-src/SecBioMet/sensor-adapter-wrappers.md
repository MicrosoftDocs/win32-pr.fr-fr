---
title: Wrappers d’adaptateur de capteur
description: Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de capteur. Ces fonctions sont définies dans WinBio \_ adapter. h.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8887da38a7142c830f19a83b5950abea15791b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100753"
---
# <a name="sensor-adapter-wrappers"></a>Wrappers d’adaptateur de capteur

Les fonctions wrapper suivantes sont définies dans WinBio \_ adapter. h. Vous pouvez les utiliser pour appeler des fonctions sur votre adaptateur de capteur.



| Fonction                                     | Description                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptCalibrationData<br/>   | Appelle la fonction [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>     |
| WbioSensorActivate<br/>                | Appelle la fonction [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                               |
| WbioSensorAttach<br/>                  | Appelle la fonction [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) .<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | Appelle la fonction [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) .<br/>                                                                                                         |
| WbioSensorClearContext<br/>            | Appelle la fonction [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) .<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | Appelle la fonction [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) .<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | Appelle la fonction [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) .<br/>                                                                           |
| WbioSensorDeactivate<br/>              | Appelle la fonction [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                           |
| WbioSensorDetach<br/>                  | Appelle la fonction [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) .<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | Appelle la fonction [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) .<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | Appelle la fonction [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) .<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | Appelle la fonction [**SensorAdapterNotifyPowerChange**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 8.<br/>              |
| WbioSensorPipelineCleanup<br/>         | Appelle la fonction [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                 |
| WbioSensorPipelineInit<br/>            | Appelle la fonction [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>                       |
| WbioSensorPushDataToEngine<br/>        | Appelle la fonction [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) .<br/>                                                                                     |
| WbioSensorQueryCalibrationFormats<br/> | Appelle la fonction [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/> |
| WbioSensorQueryExtendedInfo<br/>       | Appelle la fonction [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>             |
| WbioSensorQueryStatus<br/>             | Appelle la fonction [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) .<br/>                                                                                               |
| WbioSensorReset<br/>                   | Appelle la fonction [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) .<br/>                                                                                                           |
| WbioSensorSetCalibrationFormat<br/>    | Appelle la fonction [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) .<br/> Cette fonction wrapper est prise en charge à partir de Windows 10.<br/>       |
| WbioSensorSetMode<br/>                 | Appelle la fonction [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) .<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | Appelle la fonction [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) .<br/>                                                                                             |



 

Il n’existe aucune fonction wrapper pour les fonctions [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) et [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions d’adaptateur de capteur](sensor-adapter-functions.md)
</dt> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> </dl>

 

 






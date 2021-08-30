---
title: Fonctions d’adaptateur de capteur
description: un adaptateur de capteur encapsule un périphérique biométrique et fournit une interface standard qui permet au service de Windows biométrique de configurer le capteur, de capturer des échantillons et de contrôler le workflow de données biométriques pour le moteur de traitement.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebad4ef849eab4ce0ac2dad110f6272733f1b62da19c47ffc2fe0ec0d3699c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101179"
---
# <a name="sensor-adapter-functions"></a>Fonctions d’adaptateur de capteur

un adaptateur de capteur encapsule un périphérique biométrique et fournit une interface standard qui permet au service de Windows biométrique de configurer le capteur, de capturer des échantillons et de contrôler le workflow de données biométriques pour le moteur de traitement. Les fonctions suivantes doivent être implémentées par le développeur de l’adaptateur. elles sont appelées par le service biométrique Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                           | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Transmet les données d’étalonnage de l’adaptateur du moteur à l’adaptateur du capteur.<br/>                                                                                            |
| [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Donne à l’adaptateur de capteur la possibilité d’effectuer tout travail nécessaire pour rendre le composant de capteur inactif.<br/>                                                |
| [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Ajoute un adaptateur de capteur au pipeline de traitement de l’unité biométrique.<br/>                                                                                           |
| [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Annule toutes les opérations de capteur en attente.<br/>                                                                                                                            |
| [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Prépare le pipeline de traitement de l’unité biométrique pour une nouvelle opération.<br/>                                                                                       |
| [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Effectue une opération de contrôle définie par le fournisseur qui ne requiert pas de privilèges élevés.<br/>                                                                             |
| [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Effectue une opération de contrôle définie par le fournisseur qui requiert des privilèges élevés.<br/>                                                                                     |
| [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Permet à l’adaptateur de capteur d’effectuer les tâches nécessaires pour mettre le composant de capteur dans un état d’inactivité.<br/>                                                    |
| [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Libère les ressources spécifiques à l’adaptateur attachées au pipeline.<br/>                                                                                                     |
| [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Récupère l’exemple biométrique capturé le plus récemment mis en forme en tant que structure [**\_ Bir standard WINBIO**](winbio-bir.md) .<br/>                                        |
| [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | appelée par le Windows Biometric Framework pour attendre la fin d’une opération de capture lancée par la fonction SensorAdapterStartCapture.<br/>                                                                                       |
| [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Récupère une valeur qui indique si l’indicateur de capteur est activé ou désactivé.<br/>                                                                                       |
| [*SensorAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Reçoit une notification concernant une modification de l’état d’alimentation de l’ordinateur et prépare l’adaptateur de capteur en conséquence.<br/>                                                     |
| [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | donne à l’adaptateur de capteur la possibilité d’effectuer un nettoyage dans qui requiert l’aide du moteur ou des composants de l’adaptateur Stockage.<br/>                                   |
| [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | permet à l’adaptateur de capteur d’effectuer toute initialisation qui reste incomplète et qui requiert l’aide du moteur ou Stockage composants de l’adaptateur.<br/> |
| [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Met le contenu actuel de l’exemple de mémoire tampon à la disposition de l’adaptateur du moteur.<br/>                                                                                  |
| [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Détermine l’ensemble des formats d’étalonnage pris en charge par l’adaptateur de capteur.<br/>                                                                                        |
| [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Détermine les fonctionnalités et les limitations du composant de capteur biométrique.<br/>                                                                                    |
| [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Récupère des informations sur l’état actuel de l’appareil capteur.<br/>                                                                                              |
| [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Réinitialise le capteur.<br/>                                                                                                                                         |
| [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Avertit l’adaptateur du capteur qu’un format de données d’étalonnage particulier a été sélectionné par l’adaptateur du moteur.<br/>                                                    |
| [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Active ou désactive l’indicateur de capteur.<br/>                                                                                                                           |
| [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Définit le mode d’adaptateur de capteur.<br/>                                                                                                                                     |
| [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Commence une capture biométrique asynchrone.<br/>                                                                                                                         |
| [**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Récupère un pointeur vers la structure de l' [**\_ \_ interface du capteur WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) pour l’adaptateur du capteur.<br/>                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> </dl>

 

 






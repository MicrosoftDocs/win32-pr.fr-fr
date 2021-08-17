---
description: le capteur de Windows et la plateforme d’emplacement définissent des constantes pour les événements de pilote. Les manfuactureres de capteur peuvent également définir leurs propres constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes d’événement (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b16be770777c8e679e74123ce1c40c385893afee11ff3792dd58df007ae4c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890227"
---
# <a name="event-constants-sensorsh"></a>Constantes d’événement (sensors. h)

le capteur de Windows et la plateforme d’emplacement définissent des constantes pour les événements de pilote. Les manfuactureres de capteur peuvent également définir leurs propres constantes.

**Types d’événements de capteur**

La plateforme définit les identificateurs de type d’événement de capteur suivants.



| Type d’événement de capteur                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**Capteur \_ ÉVÉNEMENT \_ accéléromètre \_ tremble**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indique que l’appareil a été agité.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**Capteur \_ Données d’événement \_ \_ mises à jour**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indique que de nouvelles données sont disponibles.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**Capteur \_ \_ \_ Modification**</dt> de la propriété d’événement <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indique qu’une valeur de propriété a été modifiée. Vérifiez l’interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , transmise via le paramètre *pEventData* à [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), pour déterminer quelle propriété a changé et sa nouvelle valeur.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**Capteur \_ État de l’événement \_ \_ modifié**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Indique une modification de l’état opérationnel, par exemple, de \_ l’état du capteur \_ initialisé à l’état de capteur \_ \_ Ready.<br/>                                                                                                                                                                                            |



**Événement de capteur PROPERTYKEYs**

Les clés de propriété définies par la plateforme pour les événements sont basées sur le GUID suivant :

{64346E30-8728-4B34-BDF6-4F52442C5C28}

La plateforme de capteur définit les **PROPERTYKEY** s suivantes qui identifient les paramètres d’événement de capteur.



| Événement de capteur PROPERTYKEY et PID                                                                                                                                                                                                                                                      | Description                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**Capteur \_ \_ID d' \_ événement \_ du paramètre d’événement**</dt> <dt>(PID = 2)</dt> </dl> | Indique que la valeur **GUID** dans [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) est un ID de type d’événement, comme les données d’événement de capteur \_ \_ \_ mises à jour.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**Capteur \_ \_ \_ État du paramètre d’événement**</dt> <dt>(PID = 3)</dt> </dl>           | Indique que la valeur de l’entier non signé dans **IPortableDeviceValues** est un état de capteur, par exemple l’état du capteur \_ \_ Ready.<br/>                                                  |



**Erreur de capteur PROPERTYKEYs**

Les clés de propriété définies par la plateforme pour les erreurs seront basées sur le GUID suivant :

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

La plateforme de capteur réserve ce GUID pour une utilisation ultérieure.

<dl></dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Capteurs. h</dt> </dl> |



 


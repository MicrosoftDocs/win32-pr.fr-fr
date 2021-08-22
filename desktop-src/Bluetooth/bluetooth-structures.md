---
title: Bluetooth Celles
description: cette section fournit des définitions pour les structures utilisées pour la gestion des appareils et des services Bluetooth.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, référence, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588279"
---
# <a name="bluetooth-structures"></a>Bluetooth Celles

cette section fournit des définitions pour les structures utilisées pour la gestion des appareils et des services Bluetooth.

Bluetooth est également pris en charge à l’aide de l’interface de programmation Windows sockets. pour plus d’informations sur la programmation d’Bluetooth à l’aide de l’interface Windows sockets, consultez [prise en charge de Windows sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                       | Content                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_adresse Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | contient l’adresse d’un appareil Bluetooth.                                                                                      |
| [**\_paramètres de \_ rappel d’authentification Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | contient des informations de configuration spécifiques sur le Bluetooth appareil qui répond à une demande d’authentification.                  |
| [**\_réponse d’authentification Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contient les informations passées en réponse à un \_ événement de demande d’authentification à distance BTH \_ \_ .                                           |
| [**\_paires Bluetooth COD \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | fournit la spécification et la récupération de Bluetooth informations de classe de périphérique (COD).                                         |
| [**\_informations sur l’appareil Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | fournit des informations sur un appareil Bluetooth.                                                                                   |
| [**\_paramètres de \_ recherche de périphérique Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | spécifie des critères de recherche pour Bluetooth les recherches d’appareils.                                                                         |
| [**\_ \_ paramètres radio de recherche Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | facilite l’énumération des Bluetooth les radios installées.                                                                       |
| [**\_ \_ informations sur le service local Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | contient les informations de service local pour un Bluetooth radio.                                                                        |
| [**\_informations de \_ comparaison \_ numériques Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contient la valeur numérique utilisée pour l’authentification via une comparaison numérique.                                                       |
| [**\_ \_ informations sur les données OOB de Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contient les données utilisées pour s’authentifier avant d’établir un jumelage d’appareils hors bande.                                          |
| [**\_informations de clé Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contient la clé de clé utilisée pour l’authentification via une clé de clé.                                                                        |
| [**\_info code confidentiel Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contient des informations utilisées pour l’authentification par le biais du code PIN.                                                                            |
| [**\_informations sur la radio Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | contient des informations sur un Bluetooth radio.                                                                                    |
| [**paramètres de sélection de l' \_ \_ appareil Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | facilite et gère la visibilité, l’authentification et la sélection des appareils et services Bluetooth.                         |
| [**\_informations sur l’appareil BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | stocke les informations relatives à un appareil Bluetooth.                                                                                     |
| [**\_ \_ informations sur l’événement HCI BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Utilisé en relation avec l’obtention \_ des messages WM DEVICECHANGE pour Bluetooth.                                                       |
| [**\_ \_ Informations sur l’événement BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contient des données sur les événements associés à un canal L2CAP.                                                        |
| [**\_périphérique de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | utilisé lors de l’interrogation de la présence d’un appareil Bluetooth.                                                                       |
| [**\_service de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | utilisé pour interroger un service de Bluetooth.                                                                                               |
| [**\_ \_ zone de radio BTH dans la \_ plage**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | stocke les données relatives aux appareils Bluetooth qui se trouvent dans la plage de communication.                                                     |
| [**BTH \_ Set \_ service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | fournit des informations de service pour le service de Bluetooth spécifié.                                                                |
| [**\_données d’élément SDP \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Stocke les données d’élément SDP.                                                                                                         |
| [**\_données de \_ type \_ chaîne SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Stocke des informations sur les types de chaînes SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | utilisé dans une requête Bluetooth pour contraindre l’ensemble d’attributs à retourner dans la requête.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilite la recherche d’UUID.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contient l’UUID sur lequel exécuter une requête SDP. Utilisé conjointement avec la structure [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) . |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | utilisé conjointement avec les opérations de socket de Bluetooth telles que définies par la famille d’adresses de l' \_ adresse BTH.                                   |



 

 

 





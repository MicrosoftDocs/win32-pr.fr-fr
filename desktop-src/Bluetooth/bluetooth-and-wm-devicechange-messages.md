---
title: Messages Bluetooth et WM_DEVICECHANGE
description: Bluetooth comprend des \_ messages DEVICECHANGE WM spécifiques qui permettent aux développeurs d’obtenir des messages lorsque des appareils Bluetooth subissent des modifications d’État.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941078"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Messages Bluetooth et WM \_ DEVICECHANGE

Bluetooth comprend des [**messages \_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) spécifiques qui permettent aux développeurs d’obtenir des messages lorsque des appareils Bluetooth subissent des modifications d’État. Cette rubrique explique comment recevoir des messages **WM \_ DEVICECHANGE** spécifiques à Bluetooth et répertorie les messages spécifiques à Bluetooth.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Réception de messages WM DEVICECHANGE spécifiques à Bluetooth \_

Pour recevoir les messages [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , vous devez d’abord ouvrir un descripteur de la radio locale. Pour ce faire, utilisez l'une des méthodes suivantes :

-   Utilisez la [fonction SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) avec les paramètres suivants : (GUID \_ BTHPORT \_ Device \_ interface,..., DIGCF \_ present \| DIGCF \_ DEVICEINTERFACE), puis utilisez les fonctions [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)et [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .
-   Utilisez les fonctions [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)et [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

Lorsque le handle radio Bluetooth est ouvert, appelez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) et inscrivez-vous aux notifications sur le handle à l’aide du **\_ \_ handle DBT DEVTYP** en tant que DeviceType. Lorsqu’ils sont inscrits, les GUID suivants sont envoyés et le membre de **\_ données** [**\_ \_ handle Broadcast handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: dbch est la mémoire tampon associée.

## <a name="bluetooth-specific-messages"></a>Messages spécifiques à Bluetooth

Le tableau suivant répertorie les messages [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) spécifiques à Bluetooth.

| GUID                                   | BUFFER                                                  | Description                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| événement de GUID \_ Bluetooth \_ HCI \_            | [**\_ \_ informations sur l’événement HCI BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Ce message est envoyé lorsqu’un appareil Bluetooth distant se connecte ou se déconnecte au niveau de la liste de contrôle d’accès.                                                                                                                                                                                                                                                                    |
| \_ \_ Événement L2CAP de GUID Bluetooth \_          | [**\_ \_ Informations sur l’événement BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Ce message est envoyé lorsqu’un canal L2CAP entre la radio locale et un périphérique Bluetooth distant a été établi ou arrêté. Pour les canaux L2CAP qui sont des multiplexeurs, tels que RFCOMM, ce message est envoyé uniquement lorsque le canal sous-jacent est établi, et non lorsque chaque canal multiplexé, tel qu’un canal RFCOMM, est établi ou arrêté. |
| \_demande de \_ code confidentiel Bluetooth GUID \_          | Non applicable.                                         | Ce message doit être ignoré par l’application. Si l’application doit recevoir des demandes de code confidentiel, la fonction [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) doit être utilisée.                                                                                                                                                   |
| \_radio Bluetooth \_ GUID \_ dans la \_ plage      | [**\_ \_ zone de radio BTH dans la \_ plage**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Ce message est envoyé lorsque l’un des attributs suivants d’un appareil Bluetooth distant a changé : l’appareil a été découvert, la classe de l’appareil, le nom, l’état connecté ou l’état de mémorisation de l’appareil. Ce message est également envoyé lorsque ces attributs sont définis ou désactivés.                                                                                  |
| la \_ radio Bluetooth GUID est \_ \_ hors \_ \_ limites | [**\_adresse Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Ce message est envoyé lorsqu’un appareil précédemment détecté n’a pas été trouvé après la dernière recherche. Ce message ne sera pas envoyé pour les appareils mémorisés. La structure d' **\_ adresse BTH** est l’adresse de l’appareil qui n’a pas été trouvée.                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**\_adresse Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**\_ \_ informations sur l’événement HCI BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**\_ \_ Informations sur l’événement BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**\_ \_ zone de radio BTH dans la \_ plage**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**\_handle de diffusion dev \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**\_DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 
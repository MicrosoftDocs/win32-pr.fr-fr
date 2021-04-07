---
title: Rappels Bluetooth
description: Les fonctions de rappel Bluetooth de cette section sont utilisées en association avec les fonctions qui permettent de gérer les appareils et les services Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671609"
---
# <a name="bluetooth-callbacks"></a>Rappels Bluetooth

Les fonctions de rappel Bluetooth de cette section sont utilisées en association avec les fonctions qui permettent de gérer les appareils et les services Bluetooth.

Bluetooth est également pris en charge à l’aide de l’interface de programmation Windows Sockets. Pour plus d’informations sur la programmation de Bluetooth à l’aide de l’interface Windows Sockets, consultez [prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel d’authentification PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Utilisé conjointement avec la fonction [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_rappel d’authentification PFN \_ \_ ex**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Utilisé conjointement avec la fonction [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**\_rappel des \_ attributs d’énumération Bluetooth PFN \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Appelée une fois pour chaque attribut trouvé dans le paramètre *pSDPStream* qui est passé à l’appel de fonction [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**rappel de l' \_ appareil PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Utilisé en association avec la sélection des appareils Bluetooth.                                                                                                                    |



 

 

 





---
title: Fonctions de l’API du périphérique logiciel
description: Cette section décrit les fonctions d’API de périphérique logiciel qu’une application cliente appelle et une fonction de rappel implémentée par une application cliente.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f5d525eb9a4d4bc9af4807a2b3ad069b109b17874040e84cb3a9059d31bb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937089"
---
# <a name="software-device-api-functions"></a>Fonctions de l’API du périphérique logiciel

Cette section décrit les fonctions d’API de périphérique logiciel qu’une application cliente appelle et une fonction de rappel implémentée par une application cliente.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                           | Description                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Ferme le handle de périphérique logiciel. Lorsque le descripteur est fermé, PnP lance le processus de suppression de l’appareil.<br/>                                   |
| [**rappel de création de l' \_ appareil SW \_ \_**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Fournit un périphérique avec la sauvegarde dans le registre et permet à l’appelant de passer des appels aux fonctions de l’API du périphérique logiciel avec le handle *hSwDevice* .<br/> |
| [**SwDeviceCreate**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Lance l’énumération d’un périphérique logiciel.<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Obtient la durée de vie d’un périphérique logiciel. <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Définit des propriétés sur une interface de périphérique logiciel. <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Inscrit une interface d’appareil pour un périphérique logiciel et définit éventuellement des propriétés sur cette interface. <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Active ou désactive une interface d’appareil pour un périphérique logiciel. <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Définit les propriétés d’un périphérique logiciel. <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Gère la durée de vie d’un périphérique logiciel. <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Libère la mémoire allouée par d’autres fonctions de l’API de périphérique logiciel.<br/>                                                                                      |



 

 

 

[Envoyer des commentaires sur cette rubrique à Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Envoyer des commentaires sur cette rubrique à Microsoft")
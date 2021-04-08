---
description: Les \_ \_ constantes de l’état de l’appareil xxx indiquent l’état actuel d’un périphérique de point de terminaison audio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: Constantes DEVICE_STATE_XXX (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747757"
---
# <a name="device_state_xxx-constants"></a>Constantes de l’état de l’appareil \_ \_ xxx

Les \_ \_ constantes de l’état de l’appareil xxx indiquent l’état actuel d’un périphérique de point de terminaison audio.



| Constante/valeur                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**Appareil mobile \_ ÉTAT \_ actif**</dt> <dt>0x00000001</dt> </dl>             | L’appareil de point de terminaison audio est actif. Autrement dit, la carte audio qui se connecte à l’appareil de point de terminaison est présente et activée. En outre, si l’appareil de point de terminaison se connecte à un Jack sur la carte, l’appareil de point de terminaison est branché.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**Appareil mobile \_ ÉTAT \_ désactivé**</dt> <dt>0x00000002</dt> </dl>       | L’appareil de point de terminaison audio est désactivé. L’utilisateur a désactivé l’appareil dans le panneau de configuration multimédia de Windows, Mmsys.cpl. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**Appareil mobile \_ \_Indique absent d’État**</dt> <dt>0x00000004</dt> </dl> | L’appareil de point de terminaison audio n’est pas présent, car la carte audio qui se connecte à l’appareil de point de terminaison a été supprimée du système ou l’utilisateur a désactivé l’appareil de l’adaptateur dans Gestionnaire de périphériques.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**Appareil mobile \_ ÉTAT \_ DÉbranché**</dt> de l’état <dt></dt> </dl>    | L’appareil de point de terminaison audio est débranché. La carte audio qui contient le Jack pour l’appareil de point de terminaison est présente et activée, mais l’appareil de point de terminaison n’est pas branché dans le connecteur. Seul un appareil avec la détection de présence jack-Jack peut être dans cet État. Pour plus d’informations sur la détection de la présence des jacks, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**Appareil mobile \_ STATEMASK \_ tous les**</dt> <dt>0x0000000F</dt> </dl>          | Comprend les appareils de point de terminaison audio dans tous les États actif, désactivé, non présent et débranché.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Notes

Les méthodes [**IMMDeviceEnumerator :: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice :: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)et [**IMMNotificationClient :: OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) utilisent les constantes de l’état de l’appareil \_ \_ xxx. Ces méthodes permettent aux clients d’obtenir des informations sur les appareils de point de terminaison qui se trouvent dans l’un des États représentés par les constantes de l’état de l’appareil \_ \_ xxx.

Toutefois, un client peut ouvrir un flux (par exemple, en obtenant une interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) pour l’appareil) uniquement sur un appareil qui se trouve dans \_ l' \_ état actif de l’appareil.

Le panneau de configuration multimédia de Windows, Mmsys.cpl, affiche les périphériques de point de terminaison audio dans le système. La désactivation d’un appareil dans Mmsys.cpl masque l’appareil des mécanismes de détection des appareils dans les API audio de niveau supérieur, mais il n’invalide pas les objets de flux qu’un client peut avoir instanciés avant la désactivation de l’appareil. Par exemple, si un flux est lu sur l’appareil lorsque l’utilisateur le désactive dans Mmsys.cpl, le flux continue de fonctionner sans interruption.

En revanche, la désactivation d’un appareil dans Gestionnaire de périphériques supprime efficacement l’appareil du système.

Pour utiliser Mmsys.cpl pour afficher les périphériques de rendu, ouvrez une fenêtre d’invite de commandes et entrez la commande suivante :

**mmsys.cpl de contrôle,, 0**

Pour afficher les périphériques de capture, entrez la commande suivante :

**mmsys.cpl de contrôle,, 1**

Vous pouvez également afficher les périphériques de rendu ou les périphériques de capture dans Mmsys.cpl en cliquant avec le bouton droit sur l’icône de haut-parleur dans la zone de notification, située sur le côté droit de la barre des tâches, puis en sélectionnant **périphériques de lecture** ou **périphériques d’enregistrement**.

Mmsys.cpl affiche toujours les appareils de point de terminaison qui sont dans l’état actif de l’appareil \_ \_ . En outre, il peut être configuré pour afficher les appareils désactivés et déconnectés.

Pour afficher les appareils de point de terminaison dont l’état de l’appareil est \_ \_ désactivé et les \_ \_ États indique absent de l’état de l’appareil, cliquez avec le bouton droit dans la fenêtre de Mmsys.cpl et sélectionnez l’option **afficher les périphériques désactivés** .

Pour afficher les appareils de point de terminaison qui sont dans l’État débranché de l’état de l’appareil \_ \_ , cliquez avec le bouton droit dans la fenêtre de Mmsys.cpl et sélectionnez l’option **afficher les appareils déconnectés** .

Pour afficher uniquement les appareils de point de terminaison qui sont dans l’état actif de l’appareil \_ \_ , désélectionnez les options **afficher les périphériques désactivés** et **afficher les appareils déconnectés** .

Pour activer ou désactiver un périphérique de point de terminaison dans Mmsys.cpl, cliquez sur **lecture** ou **enregistrement**, selon que l’appareil est un appareil de lecture ou d’enregistrement. Ensuite, sélectionnez l’appareil et cliquez sur **Propriétés**. Dans la fenêtre **Propriétés** , en regard de **utilisation de l’appareil**, sélectionnez **utiliser ce périphérique (activé)** ou **ne pas utiliser ce périphérique (désactivé)**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes audio principales](core-audio-constants.md)
</dt> <dt>

[**IMMDevice :: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Interface IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 





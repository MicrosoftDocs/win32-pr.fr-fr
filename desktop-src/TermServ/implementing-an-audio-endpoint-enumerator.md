---
title: Implémentation d’un énumérateur de point de terminaison audio personnalisé
description: À partir de Windows Server 2008 R2, vous pouvez implémenter un énumérateur de point de terminaison audio distant personnalisé dans le cadre d’un fournisseur de protocole Bureau à distance.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511520"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implémentation d’un énumérateur de point de terminaison audio personnalisé

À partir de Windows Server 2008 R2, vous pouvez implémenter un énumérateur de point de terminaison audio distant personnalisé dans le cadre d’un fournisseur de protocole Bureau à distance. Un fournisseur de protocole Bureau à distance peut utiliser un énumérateur de point de terminaison audio personnalisé pour récupérer une collection de points de terminaison audio ayant un ensemble spécifique de fonctionnalités.

**Pour implémenter un énumérateur de point de terminaison audio distant personnalisé**

1.  Votre solution d’énumérateur de point de terminaison personnalisée doit implémenter quatre types principaux d’objets : les objets d’énumérateur de périphérique, les objets de collection d’appareils, les objets périphériques et les objets de magasin de propriétés.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Type d’objet</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Objet énumérateur d’appareil<br/></td>
    <td>Un objet énumérateur d’appareil fournit la fonctionnalité d’énumérateur de point de terminaison. Elle expose des méthodes qui retournent un point de terminaison par défaut et des collections spécifiées de points de terminaison. Par exemple, selon les critères spécifiés, l’énumérateur peut retourner des points de terminaison de communication, des points de terminaison de lecture ou des points de terminaison de capture. L’objet énumérateur d’appareil doit implémenter l’interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objet de collection de périphériques<br/></td>
    <td>Un objet collection de périphériques représente une collection de périphériques audio. Il doit implémenter l’interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .<br/></td>
    </tr>
    <tr class="odd">
    <td>Objet d’appareil<br/></td>
    <td>Un objet appareil représente un périphérique audio particulier. Il permet d’accéder à la Banque de propriétés de l’appareil audio et expose la lecture audio et les interfaces de capture disponibles sur l’appareil. L’objet périphérique doit implémenter les interfaces <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> et <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objet de la Banque de propriétés<br/></td>
    <td>Un objet de la Banque de propriétés expose les propriétés associées à un périphérique audio. Certaines de ces propriétés sont utilisées par le système, mais les applications peuvent également stocker des propriétés arbitraires avec le point de terminaison audio.<br/> Tous les périphériques audio ont les trois propriétés suivantes :<br/>
    <ul>
    <li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li>
    </ul>
L’objet de la Banque de propriétés doit implémenter l’interface <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  L’énumérateur de point de terminaison personnalisé doit être implémenté dans une DLL qui peut être chargée dans le système audio et d’autres applications. La DLL doit être signée afin que les processus sécurisés puissent la charger. La DLL doit implémenter et exporter la fonction [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , qui sert de point d’entrée à l’énumérateur de point de terminaison personnalisé.

Le service Services Bureau à distance appelle la méthode [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) et définit le paramètre *QueryType* sur **WTS \_ query \_ AUDIOENUM \_ dll** pour récupérer le nom de l’objet énumérateur.

Les objets énumérateur personnalisés utilisent des interfaces de type COM et un mécanisme de décompte de références COM, mais ce ne sont pas des objets COM véritables. L’énumérateur de point de terminaison personnalisé doit avoir la possibilité d’utiliser des interfaces audio héritées utilisées par les applications qui ne prennent pas en charge COM. Pour cette raison, l’énumérateur de point de terminaison personnalisé ne doit pas reposer sur le mécanisme de gestion du cycle de vie de COM. Les consommateurs de votre énumérateur de point de terminaison audio, tels que MMDevAPI.dll, chargent la DLL d’énumérateur de point de terminaison personnalisée quand ils sont requis par les applications utilisateur, et ils ne déchargent pas l’énumérateur lorsque l’énumérateur contient une référence à un objet d’énumérateur de périphérique, un objet de collection d’appareils, un objet appareil ou un objet de magasin de propriétés. Toutefois, il n’est pas possible pour ces consommateurs de suivre des références à d’autres types d’objets appartenant à l’énumérateur de point de terminaison personnalisé. En conséquence, nous recommandons que votre énumérateur de point de terminaison personnalisé ne crée pas d’objets qui pourraient en surhabiter ces quatre types d’objets.

## <a name="to-implement-a-custom-audio-endpoint"></a>Pour implémenter un point de terminaison audio personnalisé

Pour implémenter un énumérateur de périphérique audio personnalisé, vous devez implémenter un point de terminaison audio personnalisé. La façon dont vos périphériques audio personnalisés sont liés est liée à l’utilisation des deux instructions suivantes :

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Nous ne pensons pas que vous implémentiez la liste complète des interfaces [**IMMDevice :: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) dans votre énumérateur de périphérique audio personnalisé. Au lieu de cela, vous devez implémenter [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) et [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Vous pouvez éventuellement implémenter quelques autres, telles que [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume). Pour toute interface que vous n’implémentez pas, vous devez retourner **E \_ nointerface** (vous devez utiliser ce code d’erreur spécifique). Windows revient ensuite à une implémentation stockée de l’interface (par exemple, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Pour obtenir une documentation de référence supplémentaire sur la façon d’implémenter et d’inscrire des points de terminaison audio, consultez [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Pour obtenir un diagramme illustrant le fonctionnement de WASAPI, consultez [composants audio en mode utilisateur](/windows/desktop/CoreAudio/user-mode-audio-components). Notez que toutes les données audio en mode utilisateur sont nouvelles à partir de Windows Server 2008.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>
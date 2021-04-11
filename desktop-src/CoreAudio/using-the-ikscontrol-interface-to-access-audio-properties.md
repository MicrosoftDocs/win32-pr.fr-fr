---
description: Utilisation de l’interface IKsControl pour accéder aux propriétés audio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Utilisation de l’interface IKsControl pour accéder aux propriétés audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201042"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Utilisation de l’interface IKsControl pour accéder aux propriétés audio

Dans de rares cas, une application audio spécialisée peut nécessiter l’utilisation de l’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) pour accéder à certaines fonctionnalités matérielles d’une carte audio qui ne sont pas exposées par l' [API DEVICETOPOLOGY](devicetopology-api.md) ou l' [API MMDevice](mmdevice-api.md). L’interface **IKsControl** rend les propriétés, les événements et les méthodes des appareils de streaming noyau (KS) disponibles pour les applications en mode utilisateur. L’intérêt principal des applications audio est les propriétés KS. L’interface **IKsControl** peut être utilisée conjointement avec l’API DeviceTopology et l’API MMDevice pour accéder aux propriétés KS des adaptateurs audio.

L’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) est destinée principalement à être utilisée par des fournisseurs de matériel qui écrivent des applications de panneau de contrôle pour gérer leur matériel audio. **IKsControl** est moins utile pour les applications audio à usage général qui ne sont pas liées à des périphériques matériels particuliers. La raison en est que les fournisseurs de matériel implémentent fréquemment des mécanismes propriétaires pour accéder aux propriétés audio de leurs appareils. Contrairement à l’API DeviceTopology, qui masque les caractéristiques des pilotes spécifiques au matériel et fournit une interface relativement uniforme pour accéder aux propriétés audio, les applications utilisent **IKsControl** pour communiquer directement avec les pilotes. Pour plus d’informations sur **IKsControl**, consultez la documentation de Windows DDK.

Comme indiqué dans [topologies d’appareils](device-topologies.md), une sous-unité dans la topologie d’un périphérique d’adaptateur peut prendre en charge une ou plusieurs des interfaces de contrôle spécifiques à la fonction affichées dans la colonne de gauche du tableau suivant. Chaque entrée dans la colonne de droite de la table est la propriété KS qui correspond à l’interface de contrôle à gauche. L’interface de contrôle fournit un accès pratique à la propriété. La plupart des pilotes audio utilisent les propriétés KS pour représenter les fonctionnalités de traitement spécifiques aux fonctions des sous-unités (également appelées nœuds KS) dans les topologies de leurs adaptateurs audio. Pour plus d’informations sur les propriétés KS et les nœuds KS, consultez la documentation de Windows DDK.



| Interface de contrôle                                          | Propriété KS                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | \_AGC audio \_ KSPROPERTY             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | \_basses audio \_ KSPROPERTY            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_configuration du \_ canal \_ audio KSPROPERTY |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | \_ \_ source mux audio \_ KSPROPERTY     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | KSPROPERTY \_ audio \_        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ audio \_ Mid             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | KSPROPERTY \_ audio \_ muet            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ audio \_ DEMUX \_ dest     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ audio \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | \_ \_ aigus audio KSPROPERTY          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ audio \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | \_spécifique au \_ dev \_ audio KSPROPERTY   |



 

Les topologies de certains adaptateurs audio peuvent contenir des sous-unités qui ont des propriétés KS qui ne sont pas répertoriées dans le tableau précédent. Par exemple, supposons qu’un appel à la méthode [**IPart :: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) pour une sous-unité particulière récupère la valeur Guid KSNODETYPE \_ tonal. Ce GUID de sous-type indique que la sous-unité prend en charge une ou plusieurs des propriétés KS suivantes :

-   \_basses audio \_ KSPROPERTY
-   KSPROPERTY \_ audio \_ Mid
-   \_ \_ aigus audio KSPROPERTY
-   KSPROPERTY \_ audio \_ - \_ Booster

Les trois premières propriétés de cette liste sont accessibles par le biais des interfaces de contrôle qui s’affichent dans le tableau précédent, mais la \_ propriété KSPROPERTY audio \_ Bass \_ Boost n’a pas d’interface de contrôle correspondante dans l’API DeviceTopology. Toutefois, une application peut utiliser l’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) pour accéder à cette propriété, si la sous-unité prend en charge la propriété.

Les étapes suivantes sont requises pour accéder à la \_ propriété KSPROPERTY audio \_ Bass \_ Boost d’une sous-unité de sous-type KSNODETYPE \_ tonal :

1.  Appelez la méthode [**IConnector :: GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) ou [**IDeviceTopology :: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) pour obtenir la chaîne d’ID d’appareil qui identifie l’appareil d’adaptateur. Cette chaîne est similaire à une [chaîne d’ID de point de terminaison](endpoint-id-strings.md), à ceci près qu’elle identifie un périphérique d’adaptateur au lieu d’un périphérique de point de terminaison. Pour plus d’informations sur la différence entre un périphérique d’adaptateur et un périphérique de point de terminaison, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).
2.  Obtenez l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de l’adaptateur en appelant la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) avec la chaîne d’ID de l’appareil. Cette interface **IMMDevice** est identique à l’interface décrite dans **interface IMMDevice**, mais elle représente un périphérique adaptateur au lieu d’un périphérique de point de terminaison.
3.  Obtenez l’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) sur la sous-unité en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) avec l' *IID* de paramètre défini sur **REFIID** IID \_ IKsControl. Notez que les interfaces prises en charge par cette méthode **Activate** , qui est destinée à un périphérique d’adaptateur, sont différentes des interfaces prises en charge par la méthode **Activate** pour un appareil de point de terminaison. En particulier, la méthode **Activate** pour un appareil d’adaptateur prend en charge **IKsControl**.
4.  Appelez la méthode [**IPart :: GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) pour obtenir l’ID local de la sous-unité.
5.  Construit une demande de propriété KS. L’ID de nœud KS requis pour la requête est contenu dans les 16 bits les moins significatifs de l’ID local obtenu à l’étape précédente.
6.  Envoyez la demande de propriété KS au pilote audio en appelant la méthode [**IKsControl :: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) . Pour plus d’informations sur cette méthode, consultez la documentation de Windows DDK.

L’exemple de code suivant récupère la valeur de la \_ propriété KSPROPERTY audio \_ Bass \_ Boost à partir d’une sous-unité de sous-type KSNODETYPE \_ Tone :


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



Dans l’exemple de code précédent, la fonction GetBassBoost prend les trois paramètres suivants :

-   `pEnumerator` pointe vers l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) d’un énumérateur de point de terminaison audio.
-   `pPart` pointe vers l’interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) d’une sous-unité qui a un sous-type de KSNODETYPE \_ Tone.
-   `pbValue` pointe vers une variable **booléenne** dans laquelle la fonction écrit la valeur de la propriété.

Un programme appelle GetBassBoost uniquement après avoir appelé [**IPart :: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) et détermine que le sous-type de la sous-unité est KSNODETYPE \_ Tone. La valeur de la propriété est **true** si la Booster est activée. La **valeur est false** si l’augmentation des basses est désactivée.

Au début de la fonction GetBassBoost, l’appel à la méthode [**IPart :: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) obtient l’interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) du périphérique adaptateur qui contient la sous-unité de \_ ton KSNODETYPE. L’appel de la méthode [**IDeviceTopology :: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) récupère la chaîne d’ID de l’appareil qui identifie l’appareil de l’adaptateur. L’appel de la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) prend la chaîne d’ID de l’appareil comme paramètre d’entrée et récupère l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de l’appareil de l’adaptateur. Ensuite, l’appel de la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) récupère l’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) de la sous-unité. Pour plus d’informations sur l’interface **IKsControl** , consultez la documentation de Windows DDK.

Ensuite, l’exemple de code précédent crée une structure de [**\_ \_ canal audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) qui décrit la propriété Bass-Boost. L’exemple de code passe un pointeur vers la structure à la méthode [**IKsControl :: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) , qui utilise les informations de la structure pour récupérer la valeur de la propriété. Pour plus d’informations sur la structure de **\_ \_ canaux audio KSNODEPROPERTY** et la méthode **IKsControl :: KsProperty** , consultez la documentation de Windows DDK.

Le matériel audio affecte généralement un état d’amélioration des basses à chaque canal dans un flux audio. En principe, la Booster de basses peut être activée pour certains canaux et désactivée pour d’autres. La structure de [**\_ \_ canal audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contient un membre de **canal** qui spécifie le numéro de canal. Si un flux contient *n* canaux, les canaux sont numérotés de 0 à *n*— 1. L’exemple de code précédent obtient la valeur de la propriété Bass-Boost pour le canal 0 uniquement. Cette implémentation suppose implicitement que les propriétés d’augmentation des basses pour tous les canaux sont définies uniformément dans le même État. Par conséquent, la lecture de la propriété Bass-Boost pour le canal 0 suffit pour déterminer la valeur de la propriété de l’augmentation du nombre de basses pour le flux. Pour être cohérente avec cette hypothèse, une fonction correspondante permettant de définir la propriété Bass-Boost définit tous les canaux sur la même valeur de propriété Bass-Boost. Il s’agit de conventions raisonnables, mais tous les fournisseurs de matériel ne les suivent pas nécessairement. Par exemple, un fournisseur peut fournir une application de panneau de configuration qui active le suramplificateur de basses uniquement pour les canaux qui dirigent des orateurs à plage complète. (Un conférencier complet est en train de jouer des sons sur toute la plage de basses à des aigus.) Dans ce cas, la valeur de propriété récupérée par l’exemple de code précédent peut ne pas représenter avec précision l’état de booster (Bass-Boost) du flux.

Les clients qui utilisent les interfaces de contrôle figurant dans le tableau précédent peuvent appeler la méthode [**IPart :: RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) pour s’inscrire aux notifications lorsque la valeur d’un paramètre de contrôle change. Notez que l’interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) ne fournit pas un moyen similaire pour que les clients s’inscrivent pour les notifications lorsqu’une valeur de propriété change. Si **IKsControl** prenait en charge les notifications de modification de propriété, il peut informer une application qu’une autre application a modifié une valeur de propriété. Toutefois, contrairement aux contrôles les plus couramment utilisés qui sont surveillés par le biais de notifications [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) , les propriétés gérées par **IKsControl** sont principalement destinées à être utilisées par les fournisseurs de matériel, et ces propriétés sont susceptibles d’être modifiées uniquement par les applications du panneau de configuration écrites par les fournisseurs. Si une application doit détecter les modifications de propriété apportées par une autre application, elle peut détecter les modifications en interrogeant régulièrement la valeur de la propriété par le biais de **IKsControl**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 

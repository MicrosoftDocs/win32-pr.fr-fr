---
description: Topologies d’appareils
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologies d’appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524255"
---
# <a name="device-topologies"></a>Topologies d’appareils

L' [API DeviceTopology](devicetopology-api.md) permet aux clients de contrôler une variété de fonctions internes des adaptateurs audio qu’ils ne peuvent pas accéder via l' [API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)ou l' [API EndpointVolume](endpointvolume-api.md).

Comme expliqué précédemment, l’API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)et l' [API EndpointVolume](endpointvolume-api.md) présentent des microtéléphones, des haut-parleurs, des casques et d’autres périphériques d’entrée et de sortie audio pour les clients en tant qu’appareils de point de [terminaison audio](audio-endpoint-devices.md). Le modèle de périphérique de point de terminaison fournit aux clients un accès pratique aux contrôles de volume et de sourdine des périphériques audio. Les clients qui n’ont besoin que de ces contrôles simples peuvent éviter de traverser les topologies internes des périphériques matériels des adaptateurs audio.

Dans Windows Vista, le moteur audio configure automatiquement les topologies des périphériques audio pour une utilisation par les applications audio. Ainsi, les applications, si jamais, doivent utiliser l’API DeviceTopology à cet effet. Par exemple, supposons qu’une carte audio contient un multiplexeur d’entrée qui peut capturer un flux à partir d’une entrée de ligne ou d’un microphone, mais qui ne peut pas capturer simultanément des flux à partir des deux appareils de point de terminaison. Supposons que l’utilisateur a activé les applications en mode exclusif pour préempter l’utilisation d’un périphérique de point de terminaison audio par des applications en mode partagé, comme décrit dans [flux en mode exclusif](exclusive-mode-streams.md). Si une application en mode partagé enregistre un flux à partir de l’entrée de ligne au moment où une application en mode exclusif commence à enregistrer un flux à partir du microphone, le moteur audio bascule automatiquement le multiplexeur de l’entrée de ligne vers le microphone. En revanche, dans les versions antérieures de Windows, y compris Windows XP, l’application en mode exclusif dans cet exemple utilisait les fonctions **mixerXxx** dans l’API multimédia Windows pour parcourir les topologies des périphériques de l’adaptateur, découvrir le multiplexeur et configurer le multiplexeur pour sélectionner l’entrée microphone. Dans Windows Vista, ces étapes ne sont plus nécessaires.

Toutefois, certains clients peuvent nécessiter un contrôle explicite sur les types de contrôles matériels audio qui ne sont pas accessibles via l’API MMDevice, WASAPI ou l’API EndpointVolume. Pour ces clients, l’API DeviceTopology offre la possibilité de traverser les topologies des périphériques d’adaptateur pour découvrir et gérer les contrôles audio des appareils. Les applications qui utilisent l’API DeviceTopology doivent être conçues avec précaution pour éviter toute interférence avec la stratégie audio Windows et perturber les configurations internes des périphériques audio partagés avec d’autres applications. Pour plus d’informations sur la stratégie audio Windows, consultez [composants audio en mode utilisateur](user-mode-audio-components.md).

L’API DeviceTopology fournit des interfaces pour la découverte et la gestion des types de contrôles audio suivants dans une topologie d’appareil :

-   Contrôle du gain automatique
-   Contrôle des basses
-   Sélecteur d’entrée (multiplexeur)
-   Contrôle du volume
-   Contrôle du milieu de gamme
-   Contrôle muet
-   Sélecteur de sortie (démultiplexeur)
-   Compteur de pic
-   Contrôle des aigus
-   Contrôle du volume

En outre, l’API DeviceTopology permet aux clients d’interroger des périphériques d’adaptateur pour obtenir des informations sur les formats de flux qu’ils prennent en charge. Le fichier d’en-tête Devicetopology. h définit les interfaces dans l’API DeviceTopology.

Le diagramme suivant montre un exemple de plusieurs topologies d’appareils connectées pour la partie d’une carte PCI qui capture l’audio à partir d’un microphone, d’une entrée de ligne et d’un lecteur de CD.

![exemple de quatre topologies d’appareils connectées](images/fig2.jpg)

Le diagramme ci-dessus montre les chemins de données qui mènent aux entrées analogiques vers le bus système. Chacun des appareils suivants est représenté sous la forme d’un objet de topologie d’appareil avec une interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :

-   Périphérique de capture Wave
-   Périphérique multiplexeur d’entrée
-   Appareil de point de terminaison A
-   Périphérique de point de terminaison B

Notez que le diagramme de topologie associe les périphériques d’adaptateur (les périphériques de capture d’onde et de multiplexage d’entrée) aux périphériques de point de terminaison. Via les connexions entre les appareils, les données audio passent d’un appareil à l’autre. À chaque extrémité d’une connexion se trouve un connecteur (intitulé con dans le diagramme) par le biais duquel les données entrent ou quittent un appareil.

Sur le bord gauche du diagramme, les signaux des prises d’entrée et de microphone entrent dans les unités de point de terminaison.

L’intérieur du périphérique de capture Wave et du multiplexeur d’entrée sont des fonctions de traitement de flux, qui, dans la terminologie de l’API DeviceTopology, sont appelées sous-unités. Les types de sous-unités suivants apparaissent dans le diagramme précédent :

-   Contrôle du volume (libellé volume)
-   Contrôle muet (intitulé muet)
-   Multiplexeur (ou sélecteur d’entrée ; appelé MUX)
-   Convertisseur analogique-numérique (étiqueté ADC)

Les paramètres des sous-unités volume, muet et multiplexer peuvent être contrôlés par les clients, et l’API DeviceTopology fournit des interfaces de contrôle aux clients pour les contrôler. Dans cet exemple, la sous-unité ADC n’a aucun paramètre de contrôle. Ainsi, l’API DeviceTopology ne fournit aucune interface de contrôle pour le connecteur Active Directory.

Dans la terminologie de l’API DeviceTopology, les connecteurs et les sous-unités appartiennent à la même catégorie générale, parties. Toutes les parties, qu’il s’agisse de connecteurs ou de sous-unités, fournissent un ensemble commun de fonctions. L’API DeviceTopology implémente une interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) pour représenter les fonctions génériques qui sont communes aux connecteurs et sous-unités. L’API implémente les interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) et [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) pour représenter les aspects spécifiques des connecteurs et des sous-unités.

L’API DeviceTopology construit les topologies du périphérique de capture d’onde et du périphérique multiplexeur d’entrée à partir des filtres de diffusion en continu (KS) du noyau que le pilote audio expose au système d’exploitation pour représenter ces appareils. (Le pilote de carte audio implémente les interfaces **IMiniportWaveXxx** et **IMiniportTopology** pour représenter les parties dépendantes du matériel de ces filtres. pour plus d’informations sur ces interfaces et sur les filtres KS, consultez la documentation de Windows DDK.)

L’API DeviceTopology construit des topologies triviales pour représenter les appareils de point de terminaison A et B dans le diagramme précédent. La topologie de l’appareil d’un appareil de point de terminaison est constituée d’un connecteur unique. Cette topologie est simplement un espace réservé pour l’appareil de point de terminaison et ne contient pas de sous-unités pour le traitement des données audio. En fait, les périphériques d’adaptateur contiennent toutes les sous-unités utilisées par les applications clientes pour contrôler le traitement audio. La topologie d’appareil d’un appareil de point de terminaison sert principalement de point de départ pour l’exploration des topologies d’appareils des périphériques d’adaptateur.

Les connexions internes entre deux parties dans une topologie de périphérique sont appelées liens. L’API DeviceTopology fournit des méthodes pour parcourir les liens d’un composant à l’autre dans une topologie d’appareil. L’API fournit également des méthodes pour parcourir les connexions entre les topologies d’appareils.

Pour commencer l’exploration d’un ensemble de topologies d’appareils connectées, une application cliente active l’interface **IDeviceTopology** d’un périphérique de point de terminaison audio. Le connecteur d’un appareil de point de terminaison se connecte à un connecteur dans une carte audio ou à un réseau. Si le point de terminaison se connecte à un appareil sur une carte audio, les méthodes de l’API DeviceTopology permettent à l’application d’effectuer un pas à pas détaillé de la connexion entre le point de terminaison et l’adaptateur en obtenant une référence à l’interface **IDeviceTopology** du périphérique adaptateur de l’autre côté de la connexion. Un réseau, en revanche, n’a pas de topologie d’appareil. Une connexion réseau canalise un flux audio vers un client qui accède au système à distance.

L’API DeviceTopology fournit un accès uniquement aux topologies des périphériques matériels dans une carte audio. Les périphériques externes situés sur le bord gauche du diagramme et les composants logiciels sur le bord droit n’entrent pas dans le cadre de l’API. Les lignes en pointillés de chaque côté du diagramme représentent les limites de l’API DeviceTopology. Le client peut utiliser l’API pour explorer un chemin de données qui s’étend du jack d’entrée au bus système, mais l’API ne peut pas pénétrer au-delà de ces limites.

Chaque connecteur du diagramme précédent est associé à un type de connexion qui indique le type de connexion que le connecteur effectue. Ainsi, les connecteurs sur les deux côtés d’une connexion ont toujours des types de connexion identiques. Le type de connexion est indiqué par une valeur d’énumération [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) (physique \_ externe, physique \_ interne, logiciel \_ fixe, \_ e/s logiciel ou réseau). Les connexions entre le périphérique multiplexeur d’entrée et les appareils de point de terminaison A et B sont de type externe physique, ce qui \_ signifie que la connexion représente une connexion physique à un périphérique externe (en d’autres termes, une prise jack audio accessible par l’utilisateur). La connexion au signal analogique à partir du lecteur CD interne est de type physique \_ interne, ce qui indique une connexion physique à un appareil auxiliaire installé à l’intérieur du châssis du système. La connexion entre le périphérique de capture d’onde et l’appareil de multiplexage d’entrée est de type logiciel \_ fixe, ce qui indique une connexion permanente qui est fixe et ne peut pas être configurée sous contrôle de logiciel. Enfin, la connexion au bus système sur le côté droit du diagramme est de type logiciel d' \_ e/s, ce qui indique que les e/s de données pour la connexion sont implémentées par un moteur DMA sous contrôle de logiciel. (Le diagramme n’inclut pas d’exemple de type de connexion réseau.)

Le client commence à traverser un chemin de données sur l’appareil de point de terminaison. Tout d’abord, le client obtient une interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui représente l’appareil de point de terminaison, comme expliqué dans [énumération des périphériques audio](enumerating-audio-devices.md). Pour obtenir l’interface **IDeviceTopology** pour l’appareil de point de terminaison, le client appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) avec l' *IID* de paramètre défini sur REFIID IID \_ IDeviceTopology.

Dans l’exemple du diagramme précédent, le périphérique multiplexeur d’entrée contient tous les contrôles matériels (volume, muet et multiplexeur) des flux de capture des prises d’entrée et de microphone. L’exemple de code suivant montre comment obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée à partir de l’interface **IMMDevice** pour l’appareil de point de terminaison pour l’entrée de ligne ou le microphone :


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



La fonction GetHardwareDeviceTopology de l’exemple de code précédent effectue les étapes suivantes pour obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée :

1.  Appelez la méthode **IMMDevice :: Activate** pour obtenir l’interface **IDeviceTopology** pour l’appareil de point de terminaison.
2.  Avec l’interface **IDeviceTopology** obtenue à l’étape précédente, appelez la méthode [**IDeviceTopology :: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) pour obtenir l’interface **IConnector** du connecteur unique (numéro de connecteur 0) dans l’appareil de point de terminaison.
3.  Avec l’interface **IConnector** obtenue à l’étape précédente, appelez la méthode [**IConnector :: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) pour obtenir l’interface **IConnector** du connecteur dans le périphérique multiplexeur d’entrée.
4.  Interrogez l’interface **IConnector** obtenue à l’étape précédente pour son interface **IPart** .
5.  Avec l’interface **IPart** obtenue à l’étape précédente, appelez la méthode [**IPart :: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) pour obtenir l’interface **IDeviceTopology** pour le périphérique multiplexeur d’entrée.

Avant que l’utilisateur puisse enregistrer à partir du microphone dans le diagramme précédent, l’application cliente doit s’assurer que le multiplexeur sélectionne l’entrée microphone. L’exemple de code suivant montre comment un client peut traverser le chemin de données à partir du microphone jusqu’à ce qu’il trouve le multiplexeur, qu’il programme ensuite pour sélectionner l’entrée microphone :


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



L’API DeviceTopology implémente une interface [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) pour encapsuler un multiplexeur, tel que celui du diagramme précédent. (Une interface [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsule un démultiplexeur.) Dans l’exemple de code précédent, la boucle interne de la fonction SelectCaptureDevice interroge chaque sous-unité trouvée pour déterminer si la sous-unité est un multiplexeur. Si la sous-unité est un multiplexeur, la fonction appelle la méthode [**IAudioInputSelector :: SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) pour sélectionner l’entrée qui se connecte au flux de données à partir de l’appareil de point de terminaison.

Dans l’exemple de code précédent, chaque itération de la boucle externe traverse une topologie d’appareil. Lors du parcours des topologies d’appareil dans le diagramme précédent, la première itération traverse l’appareil de multiplexage d’entrée et la deuxième itération traverse l’appareil de capture d’onde. La fonction se termine lorsqu’elle atteint le connecteur sur le bord droit du diagramme. L’arrêt se produit lorsque la fonction détecte un connecteur avec un \_ type de connexion d’e/s logicielles. Ce type de connexion identifie le point auquel l’appareil de l’adaptateur se connecte au bus système.

L’appel à la méthode [**IPart :: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) dans l’exemple de code précédent obtient une valeur d’énumération **IPartType** qui indique si la partie actuelle est un connecteur ou une sous-unité de traitement audio.

La boucle interne dans l’exemple de code précédent suit le lien entre un composant et le suivant en appelant la méthode [**IPart :: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) . (Il existe également une méthode [**IPart :: EnumPartsIncoming pour effectuer**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) un pas à pas détaillé dans le sens inverse.) Cette méthode récupère un objet [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) qui contient une liste de toutes les Parties sortantes. Toutefois, toute partie que la fonction SelectCaptureDevice attend à rencontrer dans un appareil de capture aura toujours une seule partie sortante. Ainsi, l’appel suivant à [**IPartsList :: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) demande toujours la première partie de la liste, la partie numéro 0, car la fonction part du principe qu’il s’agit de la seule partie de la liste.

Si la fonction SelectCaptureDevice rencontre une topologie pour laquelle cette hypothèse n’est pas valide, la fonction peut ne pas réussir à configurer correctement l’appareil. Pour éviter ce type d’échec, une version plus générale de la fonction peut effectuer les opérations suivantes :

-   Appelez la méthode [**IPartsList :: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) pour déterminer le nombre de parties sortantes.
-   Pour chaque partie sortante, appelez **IPartsList :: GetPart** pour commencer à parcourir le chemin de données qui amène le composant.

Certains éléments, mais pas nécessairement tous, ont des contrôles matériels associés que les clients peuvent définir ou obtenir. Une partie particulière peut avoir zéro, un ou plusieurs contrôles matériels. Un contrôle matériel est représenté par les paires d’interfaces suivantes :

-   Interface de contrôle générique, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), qui a des méthodes communes à tous les contrôles matériels.
-   Interface spécifique à une fonction (par exemple, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) qui expose les paramètres de contrôle pour un type particulier de contrôle matériel (par exemple, un contrôle de volume).

Pour énumérer les contrôles matériels d’un composant, le client appelle d’abord la méthode [**IPart :: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) pour déterminer le nombre de contrôles matériels associés à la partie. Ensuite, le client effectue une série d’appels à la méthode [**IPart :: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) pour obtenir l’interface **IControlInterface** pour chaque contrôle matériel. Enfin, le client obtient l’interface spécifique à la fonction pour chaque contrôle matériel en appelant la méthode [**IControlInterface :: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) pour obtenir l’ID d’interface. Le client appelle la méthode [**IPart :: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) avec cet ID pour obtenir l’interface spécifique à la fonction.

Un composant qui est un connecteur peut prendre en charge l’une des interfaces de contrôle spécifiques aux fonctions suivantes :

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Une partie qui est une sous-unité peut prendre en charge une ou plusieurs des interfaces de contrôle spécifiques aux fonctions suivantes :

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Une partie prend en charge l’interface **IDeviceSpecificProperty** uniquement si le contrôle matériel sous-jacent a une valeur de contrôle spécifique à l’appareil et que le contrôle ne peut pas être représenté de manière appropriée par une autre interface spécifique à la fonction dans la liste précédente. En règle générale, une propriété spécifique à un appareil est utile uniquement à un client qui peut déduire la signification de la valeur de propriété à partir d’informations telles que le type de partie, le sous-type de partie et le nom de la partie. Le client peut obtenir ces informations en appelant les méthodes [**IPart :: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart :: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)et [**IPart :: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 

---
description: Événements de l’appareil
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Événements d’appareil (API audio principales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515338"
---
# <a name="device-events-core-audio-apis"></a>Événements d’appareil (API audio principales)

Un événement d’appareil notifie les clients qu’une modification a été apportée à l’état d’un [périphérique de point de terminaison audio](audio-endpoint-devices.md) dans le système. Voici quelques exemples d’événements d’appareil :

-   L’utilisateur active ou désactive un périphérique de point de terminaison audio à partir de Gestionnaire de périphériques ou à partir du panneau de configuration multimédia Windows, Mmsys.cpl.
-   L’utilisateur ajoute un adaptateur audio au système ou supprime un adaptateur audio du système.
-   L’utilisateur connecte un périphérique de point de terminaison audio à une prise jack audio avec la détection de la présence des prises jack ou supprime un périphérique de point de terminaison audio d’une telle Jack.
-   L’utilisateur modifie le [rôle d’appareil](device-roles.md) affecté à un appareil.
-   La valeur d’une [propriété d’un appareil](device-properties.md) change.

L’ajout ou la suppression d’un adaptateur audio génère des événements d’appareil pour tous les périphériques de point de terminaison audio qui se connectent à l’adaptateur. Les quatre premiers éléments de la liste précédente sont des exemples de modifications de l’état de l’appareil. Pour plus d’informations sur les États des appareils de point de terminaison audio, consultez [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx. Pour plus d’informations sur la détection de la présence des jacks, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).

Un client peut s’inscrire pour être averti lorsque des événements d’appareil se produisent. En réponse à ces notifications, le client peut modifier dynamiquement la manière dont il utilise un appareil particulier, ou sélectionner un autre appareil à utiliser dans un but particulier.

Par exemple, si une application lit une piste audio via un ensemble de haut-parleurs USB et que l’utilisateur déconnecte les haut-parleur du connecteur USB, l’application reçoit une notification d’événement d’appareil. En réponse à l’événement, si l’application détecte qu’un ensemble de haut-parleurs de bureau est connecté à la carte audio intégrée sur la carte mère du système, l’application peut reprendre la piste audio via les haut-parleurs du bureau. Dans cet exemple, la transition des haut-parleurs USB aux haut-parleurs de bureau se produit automatiquement, sans que l’utilisateur soit obligé de rediriger explicitement l’application.

Pour s’inscrire afin de recevoir des notifications d’appareils, un client appelle la méthode [**IMMDeviceEnumerator :: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) . Lorsque le client n’a plus besoin de notifications, il l’annule en appelant la méthode [**IMMDeviceEnumerator :: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) . Les deux méthodes acceptent un paramètre d’entrée, nommé *pNotify*, qui est un pointeur vers une instance d’interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .

L’interface **IMMNotificationClient** est implémentée par un client. L’interface contient plusieurs méthodes, chacune servant de routine de rappel pour un type particulier d’événement d’appareil. Lorsqu’un événement d’appareil se produit dans un périphérique de point de terminaison audio, le module MMDevice appelle la méthode appropriée dans l’interface **IMMNotificationClient** de chaque client actuellement inscrit pour recevoir des notifications d’événements d’appareil. Ces appels passent une description de l’événement aux clients. Pour plus d’informations, consultez [**IMMNotificationClient interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).

Un client qui est inscrit pour recevoir des notifications d’événements d’appareil reçoit des notifications de tous les types d’événements d’appareil qui se produisent dans tous les périphériques de point de terminaison audio du système. Si un client s’intéresse uniquement à certains types d’événements ou à certains appareils, les méthodes de son implémentation de **IMMNotificationClient** doivent filtrer les événements de manière appropriée.

Le SDK Windows fournit des exemples qui incluent plusieurs implémentations de l' [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Pour plus d’informations, consultez [les exemples du kit de développement logiciel (SDK) qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md).

L’exemple de code suivant montre une implémentation possible de l’interface **IMMNotificationClient** :


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



La classe CMMNotificationClient de l’exemple de code précédent est une implémentation de l’interface **IMMNotificationClient** . Comme **IMMNotificationClient** hérite de **IUnknown**, la définition de classe contient des implémentations des méthodes **IUnknown** **AddRef**, **Release** et **QueryInterface**. Les autres méthodes publiques de la définition de classe sont spécifiques à l’interface **IMMNotificationClient** . Ces méthodes sont les suivantes :

-   **OnDefaultDeviceChanged**, qui est appelé lorsque l’utilisateur modifie le rôle d’appareil d’un périphérique de point de terminaison audio.
-   **Événements ondeviceadded**, qui est appelé lorsque l’utilisateur ajoute un périphérique de point de terminaison audio au système.
-   **OnDeviceRemoved**, qui est appelé lorsque l’utilisateur supprime un périphérique de point de terminaison audio du système.
-   **OnDeviceStateChanged**, qui est appelé lorsque l’état de l’appareil d’un périphérique de point de terminaison audio change. (Pour plus d’informations sur les États des appareils, consultez [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx.)
-   **OnPropertyValueChanged**, qui est appelé quand la valeur d’une propriété d’un périphérique de point de terminaison audio change.

Chacune de ces méthodes accepte un paramètre d’entrée, *pwstrDeviceId*, qui est un pointeur vers une chaîne d’ID de point de terminaison. La chaîne identifie l’appareil de point de terminaison audio dans lequel l’événement d’appareil s’est produit.

Dans l’exemple de code précédent, \_ PrintDeviceName est une méthode privée dans la classe CMMNotificationClient qui imprime le nom convivial de l’appareil. \_PrintDeviceName prend la chaîne d’ID de point de terminaison en tant que paramètre d’entrée. Elle transmet la chaîne à la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . **GetDevice** crée un objet d’appareil de point de terminaison pour représenter l’appareil et fournit l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) à cet objet. Ensuite, \_ PrintDeviceName appelle la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) pour récupérer l' **interface IPropertyStore** dans la Banque de propriétés de l’appareil. Enfin, \_ PrintDeviceName appelle la méthode **IPropertyStore :: GetItem** pour obtenir la propriété friendly-name de l’appareil. Pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.

En plus des événements d’appareil, les clients peuvent s’inscrire pour recevoir des notifications d’événements de session audio et d’événements de volume de point de terminaison. Pour plus d’informations, consultez [**interface IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) et [**interface IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> </dl>

 

 




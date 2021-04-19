---
description: Gestion des événements à partir de l’appareil
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: Gestion des événements à partir de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524714"
---
# <a name="handling-events-from-the-device"></a>Gestion des événements à partir de l’appareil

Une autre opération accomplie par une application WPD est la gestion des événements déclenchés par l’appareil.

Les opérations de gestion des événements sont accomplies à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                      | Description                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | Permet à l’application de s’inscrire pour recevoir des rappels asynchrones. |
| [**Interface IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | Contient le gestionnaire d’événements de l’application.                        |



 

La classe CPortableDeviceEventsCallback dans le module DeviceEvents. cpp de l’exemple d’application montre comment une application peut implémenter [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback). L’implémentation de la méthode [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) dans cette classe écrit les paramètres de tout événement dans la fenêtre de console de l’application. En plus de la méthode OnEvent, cette classe implémente AddRef et Release, qui sont utilisés pour maintenir le décompte de références de l’objet.


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



L’exemple d’application instancie la classe CPortableDeviceEventsCallback dans sa fonction d’assistance RegisterForEventNotifications. Cette fonction crée une instance de l’objet de rappel à l’aide de l’opérateur New. Il appelle ensuite la méthode [**IPortableDevice :: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) pour inscrire le rappel et commencer à recevoir des événements.


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



Une fois que l’exemple d’application est en recevant des événements, il appelle la fonction d’assistance UnregisterForEventNotifications. Cette fonction appelle à son tour la méthode [**IPortableDevice :: Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) pour annuler l’inscription du rappel lors de la réception des événements.


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




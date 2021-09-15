---
description: Récupération des événements pris en charge par un appareil
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Récupération des événements pris en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522017"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Récupération des événements pris en charge par un appareil

Certains pilotes WPD prennent en charge la notification d’événement. Cela signifie qu’une application peut s’inscrire auprès du pilote pour recevoir une notification lorsqu’une action spécifique se produit. Par exemple, une application peut s’inscrire pour recevoir une notification lors de l’ajout ou de la suppression d’un objet.

Une application peut surveiller dix événements prédéfinis. Ils sont décrits dans le tableau suivant.



| Événement                       | Description                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Fonctionnalités de l’appareil mises à jour | Se produit lorsque les fonctionnalités de l’appareil ont été modifiées.                                                                                      |
| Appareil supprimé              | Se produit lorsque l’appareil est débranché.                                                                                                   |
| Réinitialisation d’appareil                | Se produit lorsque l’appareil a été réinitialisé.                                                                                                 |
| Objet ajouté                | Se produit lorsqu’un nouvel objet est disponible sur l’appareil.                                                                             |
| Objet supprimé              | Se produit après la suppression d’un objet de l’appareil.                                                                               |
| Transfert d’objets demandé   | Indique qu’une demande a été effectuée pour transférer un objet.                                                                          |
| Objet mis à jour              | Se produit après la mise à jour d’un objet ou de ses enfants. (Les clients connectés doivent ensuite mettre à jour leur vue de l’objet donné.) |
| format de Stockage en cours  | Se produit lorsque le stockage de l’appareil est mis en forme.                                                                                     |



 

Pour obtenir la liste des constantes associées à ces événements, consultez la rubrique sur les [constantes d’événement](event-constants.md) .

La fonction ListSupportedEvents dans le module DeviceCapabilities. cpp illustre la récupération des événements pris en charge par un appareil donné.

Votre application peut récupérer les identificateurs des événements pris en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fournit l’accès aux méthodes de récupération d’événements prises en charge. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Permet d’énumérer et de stocker les données de catégorie fonctionnelle.     |



 

La première tâche accomplie par l’exemple d’application est la récupération d’un objet [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , qui est utilisé pour récupérer les événements pris en charge par l’appareil donné.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



Les événements pris en charge sont récupérés en appelant la méthode [**IPortableDeviceCapabilities :: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) . Cette méthode récupère une collection d’identificateurs d’événements pour le périphérique donné et les stocke dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) pointé par l’argument pEvents.


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



L’étape suivante consiste à récupérer le nombre d’événements pris en charge afin que l’application puisse itérer au sein de l’objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) et récupérer l’identificateur pour chacun d’eux.


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes d’événement**](event-constants.md)
</dt> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




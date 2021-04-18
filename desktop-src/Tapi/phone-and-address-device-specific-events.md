---
description: L’exemple de code suivant illustre un gestionnaire d’événements pour les événements d’adresse et d’appareil téléphonique. Le code pour chaque événement montre comment créer l’interface d’événement et comment récupérer les données d’événement.
ms.assetid: 236d4e7f-865f-4b26-8da6-c86476588c47
title: Événements spécifiques au téléphone et à l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cf4c45eb7c7b933a36814f8eba8cd5cc39d8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527585"
---
# <a name="phone-and-address-device-specific-events"></a>Événements spécifiques au téléphone et à l’appareil

L’exemple de code suivant illustre un gestionnaire d’événements pour les événements d’adresse et d’appareil téléphonique. Le code pour chaque événement montre comment créer l’interface d’événement et comment récupérer les données d’événement.

``` syntax
HRESULT STDMETHODCALLTYPE CMyEventNotification::Event(
   TAPI_EVENT TapiEvent,
   IDispatch * pEvent
)
{
    HRESULT hr = S_OK;
    //...
    switch (TapiEvent) 
    {
        case TE_ADDRESSDEVSPECIFIC:
        {
            ITAddressDeviceSpecificEvent* pITADSEvent = NULL;

            hr = pEvent->QueryInterface( 
                               IID_ITAddressDeviceSpecificEvent,
                               (void **)(&pITADSEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITADSEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITADSEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0; 
            hr = pITADSEvent->get_lParam3(&lParam3);
            // If (hr !=S_OK) process the error here...

            // Process the data here.
            // ...
            pITADSEvent->Release();
            break;
        }

        case TE_PHONEDEVSPECIFIC:
        {
            ITPhoneDeviceSpecificEvent* pITPhEvent = NULL;

            hr = pEvent->QueryInterface( 
                            IID_ITPhoneDeviceSpecificEvent,
                            (void **)(&pITPhEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITPhEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITPhEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0;
            hr = pITPhEvent->get_lParam3(&lParam3);
            // If (hr != S_OK) process the error here...

            // Process the data here.
            //...
            pITPhEvent->Release();
            break;
        }
        //...
    } // end of switch 
    //...
}
```

 

 




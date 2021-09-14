---
description: 'utilisez la méthode IWiaDevMgr :: EnumDeviceInfo (ou IWiaDevMgr2 :: EnumDeviceInfo) pour énumérer les périphériques d’Acquisition d’images Windows (WIA) installés sur un système.'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Énumération des périphériques système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231078"
---
# <a name="enumerating-system-devices"></a>Énumération des périphériques système

utilisez la méthode [**IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2 :: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) pour énumérer les périphériques d’Acquisition d’images Windows (WIA) installés sur un système. Cette méthode crée un objet d’énumération pour les propriétés des appareils et retourne un pointeur vers l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) que l’objet d’énumération prend en charge.

Vous pouvez ensuite utiliser les méthodes de l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pour obtenir un pointeur d’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour chaque périphérique installé sur le système.

Le code suivant de l’exemple d’application WiaSSamp montre comment créer un objet d’énumération pour les périphériques sur un système et comment itérer au sein de ces périphériques :


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ DevInfo \_ enum \_ local est une constante WIA qui représente la seule valeur valide pour ce paramètre.

Dans l’exemple, le paramètre **pWiaDevMgr** pointe vers une instance de l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) après un appel précédent à [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

L’application appelle la [**méthode IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2 :: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) [**) du pointeur IWiaDevMgr (**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) qui remplit **pWiaDevMgr** avec l’adresse d' **un pointeur vers** l’interface [**pWiaEnumDevInfo \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

Si l’appel a échoué, l’application appelle ensuite la méthode [**IEnumWIA \_ dev \_ info :: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) du pointeur d' [**\_ \_ informations de développement IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . La variable **pWiaEnumDevInfo** garantit que l’énumération commence au début.

Si cet appel réussit, l’application itère au sein des appareils du système en appelant à plusieurs reprises la méthode [**IEnumWIA \_ dev \_ info :: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) du pointeur [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** jusqu’à ce que la méthode ne retourne plus la valeur \_ OK, indiquant ainsi que l’énumération est terminée.

Chaque appel à **pWiaEnumDevInfo->remplit ensuite** **pWiaPropertyStorage** avec un pointeur vers l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) qui contient les informations de propriété pour un appareil spécifique.

 

 

---
description: Les applications utilisent l’interface IWiaPropertyStorage d’un appareil pour lire et écrire les propriétés de l’appareil. IWiaPropertyStorage hérite de toutes les méthodes de l’interface COM (Component Object Model) IPropertyStorage.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lecture des propriétés de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951213"
---
# <a name="reading-device-properties"></a>Lecture des propriétés de l’appareil

Les applications utilisent l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) d’un appareil pour lire et écrire les propriétés de l’appareil. **IWiaPropertyStorage** hérite de toutes les méthodes de l’interface com (Component Object Model) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).

Les propriétés de l’appareil incluent des informations sur un appareil qui décrivent les fonctionnalités et les paramètres de l’appareil. Pour obtenir la liste de ces propriétés, consultez Propriétés de l' [appareil](-wia-device-properties.md).

Parmi les propriétés d’appareil lues à l’aide de [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , il s’agit de l’ID de l’appareil, qui est ensuite utilisé pour créer un appareil WIA (Windows Image Acquisition). Pour plus d’informations, consultez [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).

L’exemple suivant lit l’ID de l’appareil, le nom de l’appareil et la description de l’appareil à partir du tableau des propriétés de l’appareil, puis imprime ces propriétés sur la console.


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



Dans cet exemple, l’application configure les tableaux [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**PropSpec** et **PropVar**, respectivement) pour contenir les informations de propriété. Ces tableaux sont passés comme paramètres dans l’appel à la méthode [IPropertyStorage :: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) du pointeur [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**. Chaque élément du tableau **PropSpec** contient le type et le nom d’une propriété d’appareil. Lors du retour, chaque élément de la **PropVar** contient la valeur de la propriété de l’appareil représentée par l’élément correspondant du tableau **PropSpec** .

L’application appelle ensuite la propriété [IPropertyStorage :: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) du [](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointeur IWiaPropertyStorage **pWiaPropertyStorage** pour récupérer les informations de propriété.

La technique utilisée pour lire et définir les propriétés de l’appareil est la même que pour les propriétés de l’élément, la seule différence est le type de l’élément WIA sur lequel vous appelez les méthodes appropriées. Pour obtenir la liste des propriétés des éléments, consultez Propriétés de l' [élément](-wia-item-properties.md).

 

 

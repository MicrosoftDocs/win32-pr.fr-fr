---
description: Utilisez les méthodes de l’interface IWiaDataTransfer pour transférer des données d’un appareil WIA (Windows Image Acquisition) 1,0 vers une application.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Transfert de données d’image dans WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113279"
---
# <a name="transferring-image-data-in-wia-10"></a>Transfert de données d’image dans WIA 1,0

> [!Note]  
> Ce didacticiel concerne le transfert de données d’image dans des applications qui exécutent Windows XP ou une version antérieure. Pour plus d’informations sur le transfert de données d’image dans les applications qui s’exécuteront sur Windows Vista ou version ultérieure, consultez [transfert de données d’image dans WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

 

Utilisez les méthodes de l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) pour transférer des données d’un appareil WIA (Windows Image Acquisition) 1,0 vers une application. Cette interface prend en charge une fenêtre de mémoire partagée pour transférer des données de l’objet appareil à l’application et éliminer les copies de données inutiles pendant le marshaling.

Les applications doivent interroger un élément image pour obtenir un pointeur vers son interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , comme dans l’exemple de code suivant :


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



Dans le code précédent, il est supposé que **pWiaItem** est un pointeur valide vers l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . L’appel à [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) remplit **pWiaDataTransfer** avec un pointeur vers l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) de l’élément référencé par **pWiaItem**.

L’application définit ensuite les membres de la structure [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Pour plus d’informations, consultez STGMEDIUM et [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Si vous fournissez un nom de fichier, celui-ci doit inclure l’extension de fichier appropriée ; WIA 1,0 ne fournit pas d’extensions de fichier. Si le membre **lpszFileName** de **StgMedium** a la **valeur null**, WIA 1,0 génère un nom de fichier et un chemin d’accès aléatoires pour les données transférées. Déplacez ou copiez ce fichier avant d’appeler ReleaseStgMedium, car cette fonction supprimera le fichier.

L’application appelle ensuite la méthode [**IWiaDataTransfer :: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) pour exécuter le transfert de données :


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



Dans l’appel à [**IWiaDataTransfer :: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), le deuxième paramètre spécifie un pointeur vers l’interface [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) . Les applications doivent implémenter cette interface pour recevoir des rappels pendant les transferts de données. Pour plus d’informations sur l’implémentation de cette interface, consultez [**IWiaDataCallback :: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

L’application libère ensuite les pointeurs vers l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) et libère toutes les données allouées dans la structure [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

L’application peut également transférer l’image à l’aide de transferts de données en mémoire au lieu de transferts de fichiers. Dans ce cas, l’application utilise la méthode idtGetBandedData à la place de la méthode idtGetData.

Voici l’exemple complet de transfert de données :


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 

---
description: 'Une fois qu’une application a l’ID d’appareil d’un appareil donné, elle peut appeler IWiaDevMgr :: CreateDevice ou IWiaDevMgr2 :: CreateDevicemethod, qui crée une arborescence hiérarchique d’objets IWiaItem ou IWiaItem2 qui représentent un appareil d’imagerie et les lits d’analyse d’image, ainsi que les dossiers contenus sur cet appareil.'
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Création d’un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517864"
---
# <a name="creating-a-device"></a>Création d’un appareil

Une fois qu’une application a l’ID d’appareil d’un appareil donné, elle peut appeler la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) ou [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), qui crée une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) qui représentent un appareil d’imagerie et les lits d’analyse d’image, ainsi que les dossiers contenus sur cet appareil.

L’exemple suivant tiré de l’exemple d’application WiaSSamp implémente une fonction qui prend un ID d’appareil en tant que paramètre. Pour plus d’informations sur l’obtention d’un ID d’appareil pour un appareil particulier, consultez [lecture des propriétés](-wia-reading-device-properties.md)de l’appareil.


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



Dans cet exemple, **pWiaDevMgr** est un pointeur vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , et **ppWiaDevice** est une variable qui, après l’appel à [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou à [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contient l’adresse d’un pointeur vers l’élément racine de l’arborescence qui représente l’appareil nouvellement créé.

 

 




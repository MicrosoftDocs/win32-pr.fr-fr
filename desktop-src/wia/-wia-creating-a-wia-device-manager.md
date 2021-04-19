---
description: La première étape de l’utilisation des services WIA (Windows Image Acquisition) consiste à obtenir un pointeur d’interface IWiaDevMgr (si vous programmez pour Windows XP ou une version antérieure) ou un pointeur d’interface IWiaDevMgr2 (si vous programmez pour Windows Vista ou version ultérieure).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Création d’un Gestionnaire de périphériques WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524236"
---
# <a name="creating-a-wia-device-manager"></a>Création d’un Gestionnaire de périphériques WIA

La première étape de l’utilisation des services WIA (Windows Image Acquisition) consiste à obtenir un pointeur d’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (si vous programmez pour Windows XP ou une version antérieure) ou un pointeur d’interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (si vous programmez pour Windows Vista ou version ultérieure). Pour ce faire, appelez [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec les paramètres appropriés. L’exemple d’application WiaSSamp crée un gestionnaire de périphériques dans une fonction globale implémentée par le code suivant :


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



Dans cet exemple, CLSID \_ WiaDevMgr et IID \_ IWiaDevMgr sont des constantes WIA qui représentent respectivement l’ID de classe et l’ID d’interface de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr). CLSID \_ WiaDevMgr2 et IID \_ IWiaDevMgr2 sont des constantes WIA qui représentent respectivement l’ID de classe et l’ID d’interface de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md).

La valeur de l’argument *dwClsContext* de l’appel [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) doit être CLSCTX \_ local \_ Server. Aucun autre type de serveur n’est pris en charge, et le modèle COM (Component Object Model) rejette toute autre valeur pour ce paramètre.

 

 

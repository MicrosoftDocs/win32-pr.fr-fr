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
# <a name="creating-a-wia-device-manager"></a><span data-ttu-id="920fa-103">Création d’un Gestionnaire de périphériques WIA</span><span class="sxs-lookup"><span data-stu-id="920fa-103">Creating a WIA Device Manager</span></span>

<span data-ttu-id="920fa-104">La première étape de l’utilisation des services WIA (Windows Image Acquisition) consiste à obtenir un pointeur d’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (si vous programmez pour Windows XP ou une version antérieure) ou un pointeur d’interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (si vous programmez pour Windows Vista ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="920fa-104">The first step in using Windows Image Acquisition (WIA) services is to obtain an [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface pointer (if you are programming for Windows XP or earlier) or an [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface pointer (if you are programming for Windows Vista or later).</span></span> <span data-ttu-id="920fa-105">Pour ce faire, appelez [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="920fa-105">To do this, call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the appropriate parameters.</span></span> <span data-ttu-id="920fa-106">L’exemple d’application WiaSSamp crée un gestionnaire de périphériques dans une fonction globale implémentée par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="920fa-106">The sample application WiaSSamp creates a device manager within a global function implemented by the following code:</span></span>


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



<span data-ttu-id="920fa-107">Dans cet exemple, CLSID \_ WiaDevMgr et IID \_ IWiaDevMgr sont des constantes WIA qui représentent respectivement l’ID de classe et l’ID d’interface de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr).</span><span class="sxs-lookup"><span data-stu-id="920fa-107">In this example, CLSID\_WiaDevMgr and IID\_IWiaDevMgr are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectively.</span></span> <span data-ttu-id="920fa-108">CLSID \_ WiaDevMgr2 et IID \_ IWiaDevMgr2 sont des constantes WIA qui représentent respectivement l’ID de classe et l’ID d’interface de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md).</span><span class="sxs-lookup"><span data-stu-id="920fa-108">CLSID\_WiaDevMgr2 and IID\_IWiaDevMgr2 are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectively.</span></span>

<span data-ttu-id="920fa-109">La valeur de l’argument *dwClsContext* de l’appel [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) doit être CLSCTX \_ local \_ Server.</span><span class="sxs-lookup"><span data-stu-id="920fa-109">The value for the *dwClsContext* argument of the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call must be CLSCTX\_LOCAL\_SERVER.</span></span> <span data-ttu-id="920fa-110">Aucun autre type de serveur n’est pris en charge, et le modèle COM (Component Object Model) rejette toute autre valeur pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="920fa-110">No other server type is supported, and Component Object Model (COM) rejects any other value for this parameter.</span></span>

 

 

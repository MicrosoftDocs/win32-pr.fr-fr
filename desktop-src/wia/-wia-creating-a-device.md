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
# <a name="creating-a-device"></a><span data-ttu-id="bdbf8-103">Création d’un appareil</span><span class="sxs-lookup"><span data-stu-id="bdbf8-103">Creating a Device</span></span>

<span data-ttu-id="bdbf8-104">Une fois qu’une application a l’ID d’appareil d’un appareil donné, elle peut appeler la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) ou [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), qui crée une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) qui représentent un appareil d’imagerie et les lits d’analyse d’image, ainsi que les dossiers contenus sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="bdbf8-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="bdbf8-105">L’exemple suivant tiré de l’exemple d’application WiaSSamp implémente une fonction qui prend un ID d’appareil en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="bdbf8-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="bdbf8-106">Pour plus d’informations sur l’obtention d’un ID d’appareil pour un appareil particulier, consultez [lecture des propriétés](-wia-reading-device-properties.md)de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bdbf8-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


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



<span data-ttu-id="bdbf8-107">Dans cet exemple, **pWiaDevMgr** est un pointeur vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , et **ppWiaDevice** est une variable qui, après l’appel à [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou à [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contient l’adresse d’un pointeur vers l’élément racine de l’arborescence qui représente l’appareil nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="bdbf8-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 




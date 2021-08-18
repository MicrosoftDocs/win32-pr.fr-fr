---
description: 'l’exemple suivant utilise la méthode wia (Windows image acquisition) 1,0 IWiaDevMgr :: RegisterEventCallbackCLSID pour s’inscrire à une notification quand un appareil wia (Windows image acquisition) est connecté au système.'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Inscription pour des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965548"
---
# <a name="registering-for-events"></a>Inscription pour des événements

l’exemple suivant utilise la méthode wia (Windows image acquisition) 1,0 [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) pour s’inscrire à une notification quand un appareil wia (Windows image acquisition) est connecté au système. Les applications peuvent également utiliser WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) et WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) pour s’inscrire aux événements. avec Windows Vista et versions ultérieures, vous pouvez utiliser les méthodes d’Acquisition d’Image Windows (WIA) 2,0 [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)ou [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) pour vous inscrire aux événements.

Il est supposé que l’exemple provient d’une application inscrite en tant qu’objet serveur COM (Component Object Model) hors processus.

L’appel à [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (ou [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) se présente comme suit :


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



Dans le code précédent, **pWiaDevMgr** est un pointeur valide vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ( [**ou IWiaDevMgr2**](-wia-iwiadevmgr2.md)), WIA \_ Register \_ Event \_ callback est une constante qui spécifie que cet appel doit s’inscrire pour l’événement par opposition à l’annulation de l’inscription de l’événement. WIA \_ Event \_ Device \_ Connected est une constante qui spécifie que l’application est inscrite pour être notifiée quand un appareil est connecté à l’ordinateur **pCLSID** est un pointeur vers le CLSID inscrit de l’application, **bstrName** est le nom de l’application, **bstrDescription** est une description textuelle de l’application et **bstrIcon** est le nom d’un fichier image à utiliser pour l’icône de l’inscription de l’application pour l’événement.

L’application doit ensuite implémenter la méthode [**IWiaEventCallback :: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , qui est appelée chaque fois qu’un événement se produit pour lequel l’application est inscrite.

Une application peut utiliser la méthode [**IWiaItem :: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (ou [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) pour énumérer les informations sur les événements pour lesquels elle est inscrite.

 

 




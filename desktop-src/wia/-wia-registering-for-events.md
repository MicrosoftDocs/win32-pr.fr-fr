---
description: 'L’exemple suivant utilise la méthode WIA (Windows Image Acquisition) 1,0 IWiaDevMgr :: RegisterEventCallbackCLSID pour s’inscrire à une notification quand un appareil WIA (Windows Image Acquisition) est connecté au système.'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Inscription pour des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113283"
---
# <a name="registering-for-events"></a>Inscription pour des événements

L’exemple suivant utilise la méthode WIA (Windows Image Acquisition) 1,0 [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) pour s’inscrire à une notification quand un appareil WIA (Windows Image Acquisition) est connecté au système. Les applications peuvent également utiliser WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) et WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) pour s’inscrire aux événements. Avec Windows Vista et versions ultérieures, vous pouvez utiliser les méthodes WIA (Windows Image Acquisition) 2,0 [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)ou [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) pour vous inscrire aux événements.

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

 

 




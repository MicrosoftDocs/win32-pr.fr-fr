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
# <a name="registering-for-events"></a><span data-ttu-id="2845f-103">Inscription pour des événements</span><span class="sxs-lookup"><span data-stu-id="2845f-103">Registering for Events</span></span>

<span data-ttu-id="2845f-104">L’exemple suivant utilise la méthode WIA (Windows Image Acquisition) 1,0 [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) pour s’inscrire à une notification quand un appareil WIA (Windows Image Acquisition) est connecté au système.</span><span class="sxs-lookup"><span data-stu-id="2845f-104">The following example uses the Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) method to register for notification when any Windows Image Acquisition (WIA) device is connected to the system.</span></span> <span data-ttu-id="2845f-105">Les applications peuvent également utiliser WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) et WIA 1,0 [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) pour s’inscrire aux événements.</span><span class="sxs-lookup"><span data-stu-id="2845f-105">Applications can also use WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) and WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register for events.</span></span> <span data-ttu-id="2845f-106">Avec Windows Vista et versions ultérieures, vous pouvez utiliser les méthodes WIA (Windows Image Acquisition) 2,0 [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)ou [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) pour vous inscrire aux événements.</span><span class="sxs-lookup"><span data-stu-id="2845f-106">With Windows Vista and later, you can use the Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md), or [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) methods to register for events.</span></span>

<span data-ttu-id="2845f-107">Il est supposé que l’exemple provient d’une application inscrite en tant qu’objet serveur COM (Component Object Model) hors processus.</span><span class="sxs-lookup"><span data-stu-id="2845f-107">It is assumed that the example is taken from an application that is registered as a Component Object Model (COM) out-of-process server object.</span></span>

<span data-ttu-id="2845f-108">L’appel à [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (ou [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="2845f-108">The call to [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) is as follows:</span></span>


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



<span data-ttu-id="2845f-109">Dans le code précédent, **pWiaDevMgr** est un pointeur valide vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ( [**ou IWiaDevMgr2**](-wia-iwiadevmgr2.md)), WIA \_ Register \_ Event \_ callback est une constante qui spécifie que cet appel doit s’inscrire pour l’événement par opposition à l’annulation de l’inscription de l’événement. WIA \_ Event \_ Device \_ Connected est une constante qui spécifie que l’application est inscrite pour être notifiée quand un appareil est connecté à l’ordinateur **pCLSID** est un pointeur vers le CLSID inscrit de l’application, **bstrName** est le nom de l’application, **bstrDescription** est une description textuelle de l’application et **bstrIcon** est le nom d’un fichier image à utiliser pour l’icône de l’inscription de l’application pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="2845f-109">In the previous code, **pWiaDevMgr** is a valid pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface, WIA\_REGISTER\_EVENT\_CALLBACK is a constant that specifies that this call is to register for the event as opposed to unregistering for the event, WIA\_EVENT\_DEVICE\_CONNECTED is a constant that specifies that the application is registering to be notified whenever a device is connected to the user's computer, **pCLSID** is a pointer to the registered CLSID of the application, **bstrName** is the name of the application, **bstrDescription** is a text description of the application, and **bstrIcon** is the name of an image file to be used for the icon for the application registering for the event.</span></span>

<span data-ttu-id="2845f-110">L’application doit ensuite implémenter la méthode [**IWiaEventCallback :: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , qui est appelée chaque fois qu’un événement se produit pour lequel l’application est inscrite.</span><span class="sxs-lookup"><span data-stu-id="2845f-110">The application must then implement the [**IWiaEventCallback::ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method, which is called whenever an event occurs for which the application is registered.</span></span>

<span data-ttu-id="2845f-111">Une application peut utiliser la méthode [**IWiaItem :: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (ou [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) pour énumérer les informations sur les événements pour lesquels elle est inscrite.</span><span class="sxs-lookup"><span data-stu-id="2845f-111">An application can use the [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) method to enumerate the information about events for which it is registered.</span></span>

 

 




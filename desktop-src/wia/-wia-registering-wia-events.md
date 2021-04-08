---
description: 'Les applications peuvent s’inscrire pour être avertis des événements d’appareil matériel WIA (Windows Image Acquisition) en appelant l’une des méthodes d’interface IWiaDevMgr ou IWiaDevMgr2 suivantes : IWiaDevMgr :: RegisterEventCallbackCLSID ou IWiaDevMgr2 :: RegisterEventCallbackCLSIDIWiaDevMgr :: RegisterEventCallbackInterface ou IWiaDevMgr2 :: RegisterEventCallbackInterfaceIWiaDevMgr :: RegisterEventCallbackProgram ou IWiaDevMgr2 :: RegisterEventCallbackProgram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Inscription des événements WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951212"
---
# <a name="registering-wia-events"></a>Inscription des événements WIA

Les applications peuvent s’inscrire pour être avertis des événements de périphérique matériel WIA (Windows Image Acquisition) en appelant l’une des méthodes d’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) suivantes :

-   [**IWiaDevMgr :: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) ou [ **IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) ou [ **IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) ou [ **IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Toutes ces méthodes acceptent les paramètres qui spécifient l’événement et le périphérique matériel pour lequel l’application doit être notifiée. Les applications s’inscrivent pour recevoir un événement pour tous les appareils WIA en passant une valeur **null** pour le paramètre qui spécifie le périphérique matériel.

La méthode **RegisterEventCallbackInterface** inscrit une application pour recevoir un événement de périphérique matériel WIA si l’application est en cours d’exécution au moment où l’événement se produit. Lorsque l’événement pour lequel l’application est inscrite se produit, WIA appelle la méthode [**IWiaEventCallback :: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) de l’objet fourni par l’application pour transmettre les informations sur l’événement.

La méthode **RegisterEventCallbackCLSID** inscrit une application qui est un composant COM (Component Object Model) inscrit pour recevoir un événement de périphérique matériel WIA, même si l’application n’est pas en cours d’exécution. En plus des paramètres mentionnés précédemment, cette méthode prend un paramètre, *pClsID*, qui spécifie l’ID de classe de l’application. Lorsque l’événement spécifié se produit, le système WIA utilise la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et l’ID de classe spécifié par *pClsID* pour créer une nouvelle instance de l’application, puis appelle la méthode [**IWiaEventCallback :: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) de cette application pour transmettre les informations sur l’événement.

La méthode **RegisterEventCallbackProgram** inscrit une application pour recevoir un événement de périphérique matériel WIA, même si l’application n’est pas en cours d’exécution lorsque l’événement se produit. L’application n’a pas besoin d’être un composant COM inscrit. WIA lance l’application avec une instruction de ligne de commande. **RegisterEventCallbackProgram** prend un paramètre, *bstrCommandline*, qui spécifie le chemin d’accès complet et le nom de fichier de l’application exécutable. **RegisterEventCallbackProgram** existe pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour WIA et qui doivent être évitées. Utilisez **RegisterEventCallbackInterface** ou **RegisterEventCallbackCLSID** à la place.

Pour déterminer quels gestionnaires sont inscrits pour les événements sur un appareil WIA spécifique, une application appelle une méthode [**IWiaItem :: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) d’un élément racine. Cette méthode crée un objet d’énumération pour les informations d’inscription. L’application peut ensuite utiliser l’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) de cet objet pour énumérer les informations sur les gestionnaires inscrits pour recevoir des événements pour cet appareil.

Si un événement se produit pour lequel une application en cours d’exécution est inscrite via **RegisterEventCallbackInterface** et **RegisterEventCallbackCLSID** ou **RegisterEventCallbackProgram**, WIA notifie l’application en cours d’exécution et n’essaie pas de lancer une nouvelle instance de l’application, car l’inscription des événements via **RegisterEventCallbackInterface** est prioritaire sur **RegisterEventCallbackCLSID** et **RegisterEventCallbackProgram**.

> [!Note]  
> Dans une application multithread, il n’y a aucune garantie que le thread sur lequel le rappel de notification d’événements retourne est le même thread que celui qui a enregistré le rappel.

 

 

 

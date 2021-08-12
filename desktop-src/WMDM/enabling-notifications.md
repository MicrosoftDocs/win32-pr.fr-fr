---
title: Activation des notifications
description: Activation des notifications
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Gestionnaire de périphériques de média, notifications
- Gestionnaire de périphériques, notifications
- Guide de programmation, notifications
- applications de bureau, notifications
- création d’applications de Gestionnaire de périphériques Windows Media, notifications
- Notifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585062"
---
# <a name="enabling-notifications"></a>Activation des notifications

Windows Le Gestionnaire de périphériques de média déclare quatre interfaces qu’une application peut implémenter dans une classe COM pour recevoir des notifications d’événements. Ces interfaces se répartissent en deux groupes, comme indiqué dans le tableau suivant.



| Interfaces                                                                                                                                                | Description                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Avertit l’application lorsque des appareils ou un média de stockage sont connectés ou déconnectés.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Système de notification très simple pour avertir une application de la progression d’un événement. L’application n’est pas tenue d’effectuer des actions en réponse à ces messages. |



 

**IWMDMNotification**

**IWMDMNotification** alerte l’application lorsque plug-and-Play appareils sont connectés ou déconnectés de l’ordinateur, ainsi que lorsque plug-and-Play support de stockage (comme les cartes Flash) sont insérés ou supprimés de l’appareil. Ces notifications peuvent aider l’application à mettre à jour son interface utilisateur pour refléter les modifications.

Pour recevoir ces notifications, votre application doit s’inscrire pour les recevoir à l’aide des interfaces **IConnectionPointContainer** et **IConnectionPoint** du kit de développement logiciel (SDK) de plateforme. Votre application doit s’inscrire pour recevoir des événements lors de son démarrage, et annuler son inscription lorsqu’elle se ferme. Suivez ces étapes pour vous inscrire afin de recevoir ces notifications.

1.  Interrogez l’interface **IWMDeviceManager** principale que vous avez reçue lorsque vous avez authentifié votre application pour **IConnectionPointContainer**.
2.  Appelez **IConnectionPointContainer :: FindConnectionPoint** pour récupérer un point de connexion de conteneur pour les interfaces **IWMDMNotification** .
3.  Inscrivez-vous pour recevoir des événements en appelant **IConnectionPoint :: Advise**. Transmettez la classe qui implémente **IWMDMNotification** et récupérez un cookie, un ID unique qui identifie votre point de connexion. Celui-ci doit être stocké et utilisé ultérieurement pour annuler l’inscription aux notifications d’événements.

Le code C++ suivant montre comment vous pouvez vous inscrire pour recevoir des notifications de **IWMDMNotification**.


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



Lorsque votre application se ferme, vous devez annuler l’inscription à **IConnectionPoint** pour indiquer qu’elle ne doit plus envoyer de notifications. Pour annuler l’inscription aux notifications, procédez comme suit :

1.  Interrogez l’interface **IWMDeviceManager** principale pour **IConnectionPointContainer**.
2.  Obtient un point de connexion pour les interfaces **IWMDMNotification** .
3.  Annulez l’inscription de votre application pour les notifications d’événements en appelant **IConnectionPoint :: Unadvise**, en transmettant l’ID unique reçu quand vous vous êtes inscrit pour recevoir des événements.

Le code C++ suivant montre comment annuler l’inscription des événements **IWMDMNotification** lorsque votre application se ferme.


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



**Utilisation de IWMDMProgress**

Windows Les Gestionnaire de périphériques de média peuvent envoyer les messages d’état de votre application lorsque des actions spécifiques, telles que le transfert de contenu, l’acquisition d’horloge sécurisée et les informations de fichier DRM, se produisent. Votre application peut utiliser ces messages pour surveiller l’état de l’événement ou pour annuler un événement. Pour utiliser cette interface, implémentez [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)ou [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), puis transmettez-la en tant que paramètre à une méthode qui accepte un message de progression. Notez que **IWMDMProgress3** est l’interface supérieure, car elle fournit un GUID d’identification qui spécifie l’action faisant l’objet d’un suivi. Les méthodes d’application suivantes acceptent une interface de progression (les méthodes de fournisseur de service correspondantes doivent être en mesure d’envoyer des notifications à une interface envoyée) :

[**IWMDMStorageControl ::D supprim**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl :: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl :: Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl :: lecture**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl :: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals :: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Des exemples de passage d’une interface dans une méthode sont fournis dans la documentation relative à ces méthodes. Pour obtenir des exemples d’implémentation des interfaces de rappel, consultez la documentation pour les méthodes de **IWMDMProgress**, **IWMDMProgress2** ou **IWMDMProgress3**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 






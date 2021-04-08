---
title: Activation des notifications
description: Activation des notifications
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Gestionnaire de périphériques Windows Media, notifications
- Gestionnaire de périphériques, notifications
- Guide de programmation, notifications
- applications de bureau, notifications
- création d’applications Windows Media Gestionnaire de périphériques, notifications
- Notifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672665"
---
# <a name="enabling-notifications"></a><span data-ttu-id="b58b1-109">Activation des notifications</span><span class="sxs-lookup"><span data-stu-id="b58b1-109">Enabling Notifications</span></span>

<span data-ttu-id="b58b1-110">Windows Media Gestionnaire de périphériques déclare quatre interfaces qu’une application peut implémenter dans une classe COM pour recevoir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="b58b1-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="b58b1-111">Ces interfaces se répartissent en deux groupes, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b58b1-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="b58b1-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b58b1-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="b58b1-113">Description</span><span class="sxs-lookup"><span data-stu-id="b58b1-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b58b1-114">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="b58b1-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="b58b1-115">Avertit l’application lorsque des appareils ou un média de stockage sont connectés ou déconnectés.</span><span class="sxs-lookup"><span data-stu-id="b58b1-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="b58b1-116">**IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="b58b1-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="b58b1-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="b58b1-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="b58b1-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="b58b1-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="b58b1-119">Système de notification très simple pour avertir une application de la progression d’un événement.</span><span class="sxs-lookup"><span data-stu-id="b58b1-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="b58b1-120">L’application n’est pas tenue d’effectuer des actions en réponse à ces messages.</span><span class="sxs-lookup"><span data-stu-id="b58b1-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="b58b1-121">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="b58b1-121">**IWMDMNotification**</span></span>

<span data-ttu-id="b58b1-122">**IWMDMNotification** alerte l’application lorsque plug-and-Play appareils sont connectés ou déconnectés de l’ordinateur, ainsi que lorsque plug-and-Play support de stockage (comme les cartes Flash) sont insérés ou supprimés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b58b1-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="b58b1-123">Ces notifications peuvent aider l’application à mettre à jour son interface utilisateur pour refléter les modifications.</span><span class="sxs-lookup"><span data-stu-id="b58b1-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="b58b1-124">Pour recevoir ces notifications, votre application doit s’inscrire pour les recevoir à l’aide des interfaces **IConnectionPointContainer** et **IConnectionPoint** du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="b58b1-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="b58b1-125">Votre application doit s’inscrire pour recevoir des événements lors de son démarrage, et annuler son inscription lorsqu’elle se ferme.</span><span class="sxs-lookup"><span data-stu-id="b58b1-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="b58b1-126">Suivez ces étapes pour vous inscrire afin de recevoir ces notifications.</span><span class="sxs-lookup"><span data-stu-id="b58b1-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="b58b1-127">Interrogez l’interface **IWMDeviceManager** principale que vous avez reçue lorsque vous avez authentifié votre application pour **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="b58b1-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="b58b1-128">Appelez **IConnectionPointContainer :: FindConnectionPoint** pour récupérer un point de connexion de conteneur pour les interfaces **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="b58b1-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="b58b1-129">Inscrivez-vous pour recevoir des événements en appelant **IConnectionPoint :: Advise**.</span><span class="sxs-lookup"><span data-stu-id="b58b1-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="b58b1-130">Transmettez la classe qui implémente **IWMDMNotification** et récupérez un cookie, un ID unique qui identifie votre point de connexion.</span><span class="sxs-lookup"><span data-stu-id="b58b1-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="b58b1-131">Celui-ci doit être stocké et utilisé ultérieurement pour annuler l’inscription aux notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="b58b1-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="b58b1-132">Le code C++ suivant montre comment vous pouvez vous inscrire pour recevoir des notifications de **IWMDMNotification**.</span><span class="sxs-lookup"><span data-stu-id="b58b1-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


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



<span data-ttu-id="b58b1-133">Lorsque votre application se ferme, vous devez annuler l’inscription à **IConnectionPoint** pour indiquer qu’elle ne doit plus envoyer de notifications.</span><span class="sxs-lookup"><span data-stu-id="b58b1-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="b58b1-134">Pour annuler l’inscription aux notifications, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b58b1-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="b58b1-135">Interrogez l’interface **IWMDeviceManager** principale pour **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="b58b1-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="b58b1-136">Obtient un point de connexion pour les interfaces **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="b58b1-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="b58b1-137">Annulez l’inscription de votre application pour les notifications d’événements en appelant **IConnectionPoint :: Unadvise**, en transmettant l’ID unique reçu quand vous vous êtes inscrit pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="b58b1-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="b58b1-138">Le code C++ suivant montre comment annuler l’inscription des événements **IWMDMNotification** lorsque votre application se ferme.</span><span class="sxs-lookup"><span data-stu-id="b58b1-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


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



<span data-ttu-id="b58b1-139">**Utilisation de IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="b58b1-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="b58b1-140">Les Gestionnaire de périphériques Windows Media peuvent envoyer les messages d’état de votre application lorsque des actions spécifiques, telles que le transfert de contenu, l’acquisition d’horloge sécurisée et les informations de fichier DRM, se produisent.</span><span class="sxs-lookup"><span data-stu-id="b58b1-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="b58b1-141">Votre application peut utiliser ces messages pour surveiller l’état de l’événement ou pour annuler un événement.</span><span class="sxs-lookup"><span data-stu-id="b58b1-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="b58b1-142">Pour utiliser cette interface, implémentez [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)ou [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), puis transmettez-la en tant que paramètre à une méthode qui accepte un message de progression.</span><span class="sxs-lookup"><span data-stu-id="b58b1-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="b58b1-143">Notez que **IWMDMProgress3** est l’interface supérieure, car elle fournit un GUID d’identification qui spécifie l’action faisant l’objet d’un suivi.</span><span class="sxs-lookup"><span data-stu-id="b58b1-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="b58b1-144">Les méthodes d’application suivantes acceptent une interface de progression (les méthodes de fournisseur de service correspondantes doivent être en mesure d’envoyer des notifications à une interface envoyée) :</span><span class="sxs-lookup"><span data-stu-id="b58b1-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="b58b1-145">**IWMDMStorageControl ::D supprim**</span><span class="sxs-lookup"><span data-stu-id="b58b1-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="b58b1-146">**IWMDMStorageControl :: Insert**</span><span class="sxs-lookup"><span data-stu-id="b58b1-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="b58b1-147">**IWMDMStorageControl :: Move**</span><span class="sxs-lookup"><span data-stu-id="b58b1-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="b58b1-148">**IWMDMStorageControl :: lecture**</span><span class="sxs-lookup"><span data-stu-id="b58b1-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="b58b1-149">**IWMDMStorageControl :: Rename**</span><span class="sxs-lookup"><span data-stu-id="b58b1-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="b58b1-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="b58b1-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="b58b1-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="b58b1-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="b58b1-152">**IWMDMStorageGlobals :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="b58b1-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="b58b1-153">**IWMDRMDeviceApp::AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="b58b1-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="b58b1-154">Des exemples de passage d’une interface dans une méthode sont fournis dans la documentation relative à ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b58b1-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="b58b1-155">Pour obtenir des exemples d’implémentation des interfaces de rappel, consultez la documentation pour les méthodes de **IWMDMProgress**, **IWMDMProgress2** ou **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="b58b1-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b58b1-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b58b1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b58b1-157">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="b58b1-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 






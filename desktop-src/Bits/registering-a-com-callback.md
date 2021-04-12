---
title: Inscription d’un rappel COM
description: Au lieu d’interroger les modifications de l’état d’un travail, vous pouvez vous inscrire pour recevoir une notification en cas de modification de l’état du travail.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- BITS de tâche de transfert, notification d’événement
- inscription pour les BITS de notification d’événements
- BITS de notification d’événement
- BITS de notification d’événements, rappels
- BITS des événements de notification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315695"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="e34d8-108">Inscription d’un rappel COM</span><span class="sxs-lookup"><span data-stu-id="e34d8-108">Registering a COM Callback</span></span>

<span data-ttu-id="e34d8-109">Au lieu d' [interroger](polling-for-the-status-of-the-job.md) les modifications de l’état d’un travail, vous pouvez vous inscrire pour recevoir une notification en cas de modification de l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="e34d8-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="e34d8-110">Pour recevoir une notification, vous devez implémenter l’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="e34d8-111">L’interface contient les méthodes suivantes que BITS appelle, en fonction de votre inscription :</span><span class="sxs-lookup"><span data-stu-id="e34d8-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="e34d8-112">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="e34d8-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="e34d8-113">**JobError**</span><span class="sxs-lookup"><span data-stu-id="e34d8-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="e34d8-114">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="e34d8-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="e34d8-115">**FileTransferred**</span><span class="sxs-lookup"><span data-stu-id="e34d8-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="e34d8-116">Pour obtenir un exemple qui implémente l’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , consultez l’exemple de code dans la rubrique de l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="e34d8-117">L’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fournit une notification lorsqu’un fichier est transféré.</span><span class="sxs-lookup"><span data-stu-id="e34d8-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="e34d8-118">En général, vous utilisez cette méthode pour valider le fichier, afin que le fichier soit disponible pour le téléchargement des homologues. dans le cas contraire, le fichier n’est pas disponible pour les homologues tant que vous n’appelez pas la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="e34d8-119">Pour valider le fichier, appelez la méthode [**IBackgroundCopyFile3 :: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="e34d8-120">Il existe deux méthodes pour inscrire un rappel COM : l’inscription d’un objet de rappel ou l’inscription d’un ID de classe de rappel.</span><span class="sxs-lookup"><span data-stu-id="e34d8-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="e34d8-121">L’utilisation d’un objet de rappel est plus simple et moins lourde. l’utilisation d’un CLSID de rappel est plus fiable, mais plus complexe.</span><span class="sxs-lookup"><span data-stu-id="e34d8-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="e34d8-122">Vous pouvez inscrire l’un ou l’autre, ou aucun des deux : BITS utilisera un objet de rappel s’il en existe un et peut encore être appelé, et reviendra à l’instanciation d’un nouvel objet basé sur un ID de classe fourni si cette opération échoue.</span><span class="sxs-lookup"><span data-stu-id="e34d8-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="e34d8-123">Inscription d’un objet de rappel</span><span class="sxs-lookup"><span data-stu-id="e34d8-123">Registering a Callback Object</span></span>

<span data-ttu-id="e34d8-124">Pour inscrire votre implémentation avec BITS, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="e34d8-125">Pour spécifier les méthodes que BITS appelle, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).</span><span class="sxs-lookup"><span data-stu-id="e34d8-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="e34d8-126">L’interface de notification n’est plus valide quand votre application se termine ; BITS ne rend pas persistant l’interface Notify.</span><span class="sxs-lookup"><span data-stu-id="e34d8-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="e34d8-127">Par conséquent, le processus d’initialisation de votre application doit enregistrer les tâches existantes pour lesquelles vous souhaitez recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="e34d8-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="e34d8-128">Si vous avez besoin de capturer l’État et les informations de progression qui se sont produites depuis la dernière exécution de votre application, interrogez les informations d’État et de progression pendant l’initialisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="e34d8-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="e34d8-129">Avant de quitter, votre application doit effacer le pointeur d’interface de rappel (**SetNotifyInterface (null)**).</span><span class="sxs-lookup"><span data-stu-id="e34d8-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="e34d8-130">Il est plus efficace d’effacer le pointeur de rappel que de laisser les BITS découvrir qu’il n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="e34d8-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="e34d8-131">Notez que si plusieurs applications appellent la méthode [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour définir l’interface de notification pour le travail, la dernière application à appeler la méthode **SetNotifyInterface** est celle qui recevra les notifications ; les autres applications ne recevront pas de notifications.</span><span class="sxs-lookup"><span data-stu-id="e34d8-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="e34d8-132">L’exemple suivant montre comment s’inscrire pour les notifications.</span><span class="sxs-lookup"><span data-stu-id="e34d8-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="e34d8-133">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.</span><span class="sxs-lookup"><span data-stu-id="e34d8-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="e34d8-134">Pour plus d’informations sur l’exemple de classe CNotifyInterface utilisé dans l’exemple suivant, consultez l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="e34d8-135">Inscription d’un CLSID de rappel</span><span class="sxs-lookup"><span data-stu-id="e34d8-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="e34d8-136">Pour inscrire un CLSID de rappel avec BITS, appelez la méthode [**IBackgroundCopyJob5 :: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) avec l' **\_ \_ \_ \_ identificateur de propriété de la tâche bits** PropertyId.</span><span class="sxs-lookup"><span data-stu-id="e34d8-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="e34d8-137">Pour spécifier les méthodes que BITS appelle, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="e34d8-138">Vous devez vous assurer que le CLSID de notification est inscrit sur un serveur COM hors processus avant d’inscrire le CLSID avec un travail BITS.</span><span class="sxs-lookup"><span data-stu-id="e34d8-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="e34d8-139">L’implémentation d’un [serveur com](/windows/desktop/com/com-server-responsibilities) est beaucoup plus compliquée que la définition et la transmission d’un objet de rappel, mais offre plusieurs avantages importants.</span><span class="sxs-lookup"><span data-stu-id="e34d8-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="e34d8-140">Un serveur COM permet à BITS de maintenir l’association entre un travail BITS et le code de votre application entre les redémarrages du système et les tâches de longue durée ou durables.</span><span class="sxs-lookup"><span data-stu-id="e34d8-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="e34d8-141">Un serveur COM permet également à votre application de s’arrêter complètement alors que BITS continue d’exécuter les transferts en arrière-plan, ce qui peut améliorer l’utilisation de la batterie, du processeur et de la mémoire du système.</span><span class="sxs-lookup"><span data-stu-id="e34d8-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="e34d8-142">Pour fournir une notification que vous avez enregistrée pour la réception, BITS tente d’abord d’appeler la méthode correspondante d’un objet de rappel existant que vous avez peut-être attaché.</span><span class="sxs-lookup"><span data-stu-id="e34d8-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="e34d8-143">S’il n’existe aucun objet, ou si cet objet existant a été déconnecté (généralement suite à l’arrêt de votre application), BITS appelle CoCreateInstance en utilisant le CLSID de notification pour instancier un nouvel objet de rappel et utilise cet objet pour tous les rappels ultérieurs jusqu’à ce qu’il soit déconnecté ou remplacé par un nouvel appel à [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span><span class="sxs-lookup"><span data-stu-id="e34d8-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="e34d8-144">Contrairement aux objets de rappel, le CLSID de rappel est conservé avec leurs travaux BITS correspondants si le service BITS ou le système sont arrêtés et redémarrés.</span><span class="sxs-lookup"><span data-stu-id="e34d8-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="e34d8-145">Votre application peut effacer tout CLSID de notification précédemment défini avant de quitter (ou à tout autre moment) en passant un nouveau CLSID de notification de GUID \_ null, mais votre application peut préférer laisser le CLSID de notification inscrit si votre application s’est inscrite pour que com la démarre en réponse à des demandes CoCreateInstance pour votre CLSID.</span><span class="sxs-lookup"><span data-stu-id="e34d8-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="e34d8-146">Notez que si plusieurs applications définissent les appels à la propriété **CLSID de notification de \_ propriété de tâche \_ \_ \_ bits** , le dernier CLSID à définir est celui utilisé par bits pour instancier les objets de rappel. les autres CLSID ne seront pas instanciés.</span><span class="sxs-lookup"><span data-stu-id="e34d8-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="e34d8-147">De même, si une application inscrit un CLSID et qu’un autre inscrit un objet de rappel, les règles habituelles pour l’objet de rappel qui prend la priorité s’appliquent et le CLSID n’est pas utilisé à moins que l’objet de rappel soit effacé ou déconnecté.</span><span class="sxs-lookup"><span data-stu-id="e34d8-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="e34d8-148">L’exemple suivant montre comment s’inscrire pour les notifications CLSID.</span><span class="sxs-lookup"><span data-stu-id="e34d8-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="e34d8-149">L’exemple suppose que le pointeur d’interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) est valide et que votre application est déjà inscrite en tant que serveur com hors processus qui implémente la classe CNotifyInterface.</span><span class="sxs-lookup"><span data-stu-id="e34d8-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="e34d8-150">Pour plus d’informations sur l’exemple de classe CNotifyInterface utilisé dans l’exemple suivant, consultez l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="e34d8-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 
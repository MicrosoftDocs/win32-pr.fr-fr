---
description: Contrôle d’un périphérique externe
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Contrôle d’un périphérique externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520724"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="e039d-103">Contrôle d’un périphérique externe</span><span class="sxs-lookup"><span data-stu-id="e039d-103">Controlling an External Device</span></span>

<span data-ttu-id="e039d-104">Pour contrôler un appareil magnétoscope, utilisez la méthode [**IAMExtTransport ::p ut \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="e039d-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="e039d-105">Spécifiez le nouvel État en utilisant l’une des constantes listées dans [État du transport](device-transport-state.md)de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e039d-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="e039d-106">Par exemple, pour arrêter l’appareil, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e039d-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="e039d-107">Étant donné que le magnétoscope est un appareil physique, il y a généralement un décalage entre l’émission de la commande et la fin de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="e039d-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="e039d-108">Votre application doit créer un deuxième thread de travail qui attend la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="e039d-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="e039d-109">Une fois la commande terminée, le thread peut mettre à jour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e039d-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="e039d-110">Utilisez une section critique pour sérialiser le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="e039d-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="e039d-111">Certains magnétoscopes peuvent notifier l’application lorsque l’état du transport de l’appareil a changé.</span><span class="sxs-lookup"><span data-stu-id="e039d-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="e039d-112">Si l’appareil prend en charge cette fonctionnalité, le thread de travail peut attendre la notification.</span><span class="sxs-lookup"><span data-stu-id="e039d-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="e039d-113">Toutefois, conformément à la spécification de la sous-unité « lecteur/enregistreur de bandes AV/C de l’Association 1394 », la commande de notification d’état de transport est facultative, ce qui signifie que les appareils ne sont pas requis pour la prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="e039d-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="e039d-114">Si un appareil ne prend pas en charge la notification, vous devez interroger l’appareil à intervalles réguliers pour son état actuel.</span><span class="sxs-lookup"><span data-stu-id="e039d-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="e039d-115">Cette section décrit tout d’abord le mécanisme de notification, puis décrit l’interrogation des appareils.</span><span class="sxs-lookup"><span data-stu-id="e039d-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="e039d-116">Utilisation de la notification d’état de transport</span><span class="sxs-lookup"><span data-stu-id="e039d-116">Using Transport State Notification</span></span>

<span data-ttu-id="e039d-117">La notification d’état de transport fonctionne en faisant en sorte que le pilote signale un événement lorsque le transport bascule vers un nouvel État.</span><span class="sxs-lookup"><span data-stu-id="e039d-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="e039d-118">Dans votre application, déclarez une section critique, un événement et un handle de thread.</span><span class="sxs-lookup"><span data-stu-id="e039d-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="e039d-119">La section critique est utilisée pour synchroniser l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e039d-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="e039d-120">L’événement est utilisé pour arrêter le thread de travail lorsque l’application se ferme :</span><span class="sxs-lookup"><span data-stu-id="e039d-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="e039d-121">Après avoir créé une instance du filtre de capture, créez le thread de travail :</span><span class="sxs-lookup"><span data-stu-id="e039d-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="e039d-122">Dans le thread de travail, commencez par appeler la méthode [**IAMExtTransport :: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) avec la valeur Ed \_ Notify \_ HEVENT \_ .</span><span class="sxs-lookup"><span data-stu-id="e039d-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="e039d-123">Cet appel retourne un handle à un événement qui est signalé lorsqu’une opération se termine :</span><span class="sxs-lookup"><span data-stu-id="e039d-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="e039d-124">Ensuite, appelez à nouveau **GetState** et passez la valeur du \_ mode de modification du mode Ed \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="e039d-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="e039d-125">Si l’appareil prend en charge la notification, la méthode retourne la valeur E \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="e039d-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="e039d-126">(Dans le cas contraire, vous devez interroger l’appareil, comme décrit dans la section suivante.) En supposant que l’appareil prend en charge la notification, l’événement est signalé chaque fois que l’état du transport VTR change.</span><span class="sxs-lookup"><span data-stu-id="e039d-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="e039d-127">À ce stade, vous pouvez mettre à jour l’interface utilisateur pour refléter le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="e039d-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="e039d-128">Pour recevoir la notification suivante, réinitialisez le descripteur d’événement et appelez **GetStatus** avec le \_ mode Ed \_ modifier \_ notifier.</span><span class="sxs-lookup"><span data-stu-id="e039d-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="e039d-129">Avant de quitter le thread de travail, libérez le descripteur d’événement en appelant **GetStatus** avec l’indicateur Ed \_ Notify \_ HEVENT \_ et l’adresse du descripteur :</span><span class="sxs-lookup"><span data-stu-id="e039d-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="e039d-130">Le code suivant illustre la procédure de thread complète.</span><span class="sxs-lookup"><span data-stu-id="e039d-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="e039d-131">La fonction UpdateTransportState est supposée être une fonction d’application qui met à jour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e039d-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="e039d-132">Notez que le thread attend deux événements : l’événement de notification (*hNotify*) et l’événement de fin de thread (*hThreadEnd*).</span><span class="sxs-lookup"><span data-stu-id="e039d-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="e039d-133">Notez également que la section critique est utilisée pour protéger la variable d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e039d-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="e039d-134">Utilisez également la section critique lorsque vous émettez des commandes sur l’appareil, comme suit :</span><span class="sxs-lookup"><span data-stu-id="e039d-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="e039d-135">Avant la fermeture de l’application, arrêtez le thread secondaire en définissant l’événement de fin de thread :</span><span class="sxs-lookup"><span data-stu-id="e039d-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="e039d-136">Interrogation de l’état du transport</span><span class="sxs-lookup"><span data-stu-id="e039d-136">Polling the Transport State</span></span>

<span data-ttu-id="e039d-137">Si vous appelez **IAMExtTransport :: GetStatus** avec l' \_ indicateur de notification de modification du mode Ed et que \_ \_ la valeur de retour n’est pas \_ en attente, cela signifie que l’appareil ne prend pas en charge la notification.</span><span class="sxs-lookup"><span data-stu-id="e039d-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="e039d-138">Dans ce cas, vous devez interroger l’appareil pour déterminer son état.</span><span class="sxs-lookup"><span data-stu-id="e039d-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="e039d-139">L' *interrogation* consiste simplement à appeler le **\_ mode d’extraction** à intervalles réguliers pour vérifier l’état du transport.</span><span class="sxs-lookup"><span data-stu-id="e039d-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="e039d-140">Vous devez toujours utiliser un thread secondaire et une section critique, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="e039d-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="e039d-141">Le thread interroge l’appareil à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="e039d-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="e039d-142">L’exemple suivant montre une façon d’implémenter le thread :</span><span class="sxs-lookup"><span data-stu-id="e039d-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="e039d-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e039d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e039d-144">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="e039d-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




---
description: Contrôle d’un périphérique externe
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Contrôle d’un périphérique externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f530bb48f35a6e35a0ab75d0559cc3c6770c4d0d1dfb2948f871982f70eb0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652129"
---
# <a name="controlling-an-external-device"></a>Contrôle d’un périphérique externe

Pour contrôler un appareil magnétoscope, utilisez la méthode [**IAMExtTransport ::p ut \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) . Spécifiez le nouvel État en utilisant l’une des constantes listées dans [État du transport](device-transport-state.md)de l’appareil. Par exemple, pour arrêter l’appareil, utilisez la commande suivante :


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Étant donné que le magnétoscope est un appareil physique, il y a généralement un décalage entre l’émission de la commande et la fin de l’exécution de la commande. Votre application doit créer un deuxième thread de travail qui attend la fin de la commande. Une fois la commande terminée, le thread peut mettre à jour l’interface utilisateur. Utilisez une section critique pour sérialiser le changement d’État.

Certains magnétoscopes peuvent notifier l’application lorsque l’état du transport de l’appareil a changé. Si l’appareil prend en charge cette fonctionnalité, le thread de travail peut attendre la notification. Toutefois, conformément à la spécification de la sous-unité « lecteur/enregistreur de bandes AV/C de l’Association 1394 », la commande de notification d’état de transport est facultative, ce qui signifie que les appareils ne sont pas requis pour la prendre en charge. Si un appareil ne prend pas en charge la notification, vous devez interroger l’appareil à intervalles réguliers pour son état actuel.

Cette section décrit tout d’abord le mécanisme de notification, puis décrit l’interrogation des appareils.

Utilisation de la notification d’état de transport

La notification d’état de transport fonctionne en faisant en sorte que le pilote signale un événement lorsque le transport bascule vers un nouvel État. Dans votre application, déclarez une section critique, un événement et un handle de thread. La section critique est utilisée pour synchroniser l’état de l’appareil. L’événement est utilisé pour arrêter le thread de travail lorsque l’application se ferme :


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



Après avoir créé une instance du filtre de capture, créez le thread de travail :


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



Dans le thread de travail, commencez par appeler la méthode [**IAMExtTransport :: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) avec la valeur Ed \_ Notify \_ HEVENT \_ . Cet appel retourne un handle à un événement qui est signalé lorsqu’une opération se termine :


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Ensuite, appelez à nouveau **GetState** et passez la valeur du \_ mode de modification du mode Ed \_ \_ :


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Si l’appareil prend en charge la notification, la méthode retourne la valeur E \_ en attente. (Dans le cas contraire, vous devez interroger l’appareil, comme décrit dans la section suivante.) En supposant que l’appareil prend en charge la notification, l’événement est signalé chaque fois que l’état du transport VTR change. À ce stade, vous pouvez mettre à jour l’interface utilisateur pour refléter le nouvel État. Pour recevoir la notification suivante, réinitialisez le descripteur d’événement et appelez **GetStatus** avec le \_ mode Ed \_ modifier \_ notifier.

Avant de quitter le thread de travail, libérez le descripteur d’événement en appelant **GetStatus** avec l’indicateur Ed \_ Notify \_ HEVENT \_ et l’adresse du descripteur :


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



Le code suivant illustre la procédure de thread complète. La fonction UpdateTransportState est supposée être une fonction d’application qui met à jour l’interface utilisateur. Notez que le thread attend deux événements : l’événement de notification (*hNotify*) et l’événement de fin de thread (*hThreadEnd*). Notez également que la section critique est utilisée pour protéger la variable d’état de l’appareil.


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



Utilisez également la section critique lorsque vous émettez des commandes sur l’appareil, comme suit :


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Avant la fermeture de l’application, arrêtez le thread secondaire en définissant l’événement de fin de thread :


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



Interrogation de l’état du transport

Si vous appelez **IAMExtTransport :: GetStatus** avec l' \_ indicateur de notification de modification du mode Ed et que \_ \_ la valeur de retour n’est pas \_ en attente, cela signifie que l’appareil ne prend pas en charge la notification. Dans ce cas, vous devez interroger l’appareil pour déterminer son état. L' *interrogation* consiste simplement à appeler le **\_ mode d’extraction** à intervalles réguliers pour vérifier l’état du transport. Vous devez toujours utiliser un thread secondaire et une section critique, comme décrit précédemment. Le thread interroge l’appareil à intervalles réguliers. L’exemple suivant montre une façon d’implémenter le thread :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




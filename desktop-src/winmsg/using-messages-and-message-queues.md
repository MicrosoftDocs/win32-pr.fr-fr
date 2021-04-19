---
description: Les exemples de code suivants montrent comment effectuer les tâches suivantes associées aux messages Windows et aux files d’attente de messages.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Utilisation des messages et des files d’attente de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527905"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="c05c1-103">Utilisation des messages et des files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="c05c1-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="c05c1-104">Les exemples de code suivants montrent comment effectuer les tâches suivantes associées aux messages Windows et aux files d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="c05c1-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="c05c1-105">Création d’une boucle de message</span><span class="sxs-lookup"><span data-stu-id="c05c1-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="c05c1-106">Examen d’une file d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="c05c1-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="c05c1-107">Publication d’un message</span><span class="sxs-lookup"><span data-stu-id="c05c1-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="c05c1-108">Envoi d’un message</span><span class="sxs-lookup"><span data-stu-id="c05c1-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="c05c1-109">Création d’une boucle de message</span><span class="sxs-lookup"><span data-stu-id="c05c1-109">Creating a Message Loop</span></span>

<span data-ttu-id="c05c1-110">Le système ne crée pas automatiquement une file d’attente de messages pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="c05c1-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="c05c1-111">Au lieu de cela, le système crée une file d’attente de messages uniquement pour les threads qui effectuent des opérations qui nécessitent une file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="c05c1-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="c05c1-112">Si le thread crée une ou plusieurs fenêtres, une boucle de message doit être fournie. Cette boucle de messages récupère les messages de la file d’attente de messages du thread et les distribue aux procédures de fenêtre appropriées.</span><span class="sxs-lookup"><span data-stu-id="c05c1-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="c05c1-113">Étant donné que le système dirige les messages vers des fenêtres individuelles dans une application, un thread doit créer au moins une fenêtre avant de démarrer sa boucle de message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="c05c1-114">La plupart des applications contiennent un seul thread qui crée des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="c05c1-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="c05c1-115">Une application classique inscrit la classe de fenêtre pour sa fenêtre principale, crée et affiche la fenêtre principale, puis démarre sa boucle de messages, le tout dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="c05c1-116">Vous créez une boucle de messages à l’aide des fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) et [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="c05c1-117">Si votre application doit obtenir une entrée de caractères de la part de l’utilisateur, incluez la fonction [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) dans la boucle.</span><span class="sxs-lookup"><span data-stu-id="c05c1-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="c05c1-118">**TranslateMessage** traduit les messages de clé virtuelle en messages de caractères.</span><span class="sxs-lookup"><span data-stu-id="c05c1-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="c05c1-119">L’exemple suivant illustre la boucle de message dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) d’une application simple basée sur Windows.</span><span class="sxs-lookup"><span data-stu-id="c05c1-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="c05c1-120">L’exemple suivant montre une boucle de messages pour un thread qui utilise des accélérateurs et affiche une boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="c05c1-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="c05c1-121">Lorsque [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) ou [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) retourne **true** (indiquant que le message a été traité), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) et [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) ne sont pas appelés.</span><span class="sxs-lookup"><span data-stu-id="c05c1-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="c05c1-122">Cela est dû au fait que **TranslateAccelerator** et **IsDialogMessage** effectuent la traduction et la distribution des messages nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c05c1-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="c05c1-123">Examen d’une file d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="c05c1-123">Examining a Message Queue</span></span>

<span data-ttu-id="c05c1-124">Parfois, une application doit examiner le contenu de la file d’attente de messages d’un thread à partir de l’extérieur de la boucle de message du thread.</span><span class="sxs-lookup"><span data-stu-id="c05c1-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="c05c1-125">Par exemple, si la procédure de fenêtre d’une application exécute une longue opération de dessin, vous souhaiterez peut-être que l’utilisateur soit en mesure d’interrompre l’opération.</span><span class="sxs-lookup"><span data-stu-id="c05c1-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="c05c1-126">À moins que votre application n’examine régulièrement la file d’attente de messages pendant l’opération pour les messages de souris et de clavier, elle ne répond pas à l’entrée d’utilisateur tant que l’opération n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="c05c1-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="c05c1-127">Cela est dû au fait que la fonction [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) dans la boucle de message du thread ne retourne pas de réponse tant que la procédure de fenêtre n’a pas terminé le traitement d’un message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="c05c1-128">Vous pouvez utiliser la fonction [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pour examiner une file d’attente de messages pendant une opération de longue durée.</span><span class="sxs-lookup"><span data-stu-id="c05c1-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="c05c1-129">**PeekMessage** est similaire à la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ; Vérifiez une file d’attente de messages pour un message qui correspond aux critères de filtre, puis copiez le message dans une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="c05c1-130">La principale différence entre les deux fonctions est que **GetMessage** ne retourne aucun résultat tant qu’un message correspondant aux critères de filtre n’a pas été placé dans la file d’attente, tandis que **PeekMessage** est retourné immédiatement, qu’un message se trouve dans la file d’attente ou non.</span><span class="sxs-lookup"><span data-stu-id="c05c1-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="c05c1-131">L’exemple suivant montre comment utiliser [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pour examiner une file d’attente de messages pour les clics de souris et l’entrée au clavier pendant une longue opération.</span><span class="sxs-lookup"><span data-stu-id="c05c1-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="c05c1-132">D’autres fonctions, notamment [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) et [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), vous permettent également d’examiner le contenu de la file d’attente de messages d’un thread.</span><span class="sxs-lookup"><span data-stu-id="c05c1-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="c05c1-133">**GetQueueStatus** retourne un tableau d’indicateurs qui indique les types de messages dans la file d’attente ; son utilisation est le moyen le plus rapide de déterminer si la file d’attente contient des messages.</span><span class="sxs-lookup"><span data-stu-id="c05c1-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="c05c1-134">**GetInputState** retourne la **valeur true** si la file d’attente contient des messages de souris ou de clavier.</span><span class="sxs-lookup"><span data-stu-id="c05c1-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="c05c1-135">Ces deux fonctions peuvent être utilisées pour déterminer si la file d’attente contient des messages qui doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="c05c1-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="c05c1-136">Publication d’un message</span><span class="sxs-lookup"><span data-stu-id="c05c1-136">Posting a Message</span></span>

<span data-ttu-id="c05c1-137">Vous pouvez poster un message dans une file d’attente de messages à l’aide de la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="c05c1-138">**PostMessage** place un message à la fin de la file d’attente de messages d’un thread et le retourne immédiatement, sans attendre que le thread traite le message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="c05c1-139">Les paramètres de la fonction incluent un handle de fenêtre, un identificateur de message et deux paramètres de message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="c05c1-140">Le système copie ces paramètres dans une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , remplit les membres **Time** et **PT** de la structure et place la structure dans la file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="c05c1-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="c05c1-141">Le système utilise le handle de fenêtre passé avec la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) pour déterminer quelle file d’attente de messages de thread doit recevoir le message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="c05c1-142">Si le handle est **le \_ plus HWND**, le système publie le message dans les files d’attente de messages de thread de toutes les fenêtres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="c05c1-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="c05c1-143">Vous pouvez utiliser la fonction [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) pour envoyer un message à une file d’attente de messages de thread spécifique.</span><span class="sxs-lookup"><span data-stu-id="c05c1-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="c05c1-144">**PostThreadMessage** est similaire à [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), sauf que le premier paramètre est un identificateur de thread plutôt qu’un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c05c1-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="c05c1-145">Vous pouvez récupérer l’identificateur de thread en appelant la fonction [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="c05c1-146">Utilisez la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) pour quitter une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="c05c1-147">**PostQuitMessage** publie le message [**WM \_ Quit**](wm-quit.md) sur le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c05c1-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="c05c1-148">La boucle de message du thread se termine et retourne le contrôle au système lorsqu’il rencontre le message **WM \_ Quit** .</span><span class="sxs-lookup"><span data-stu-id="c05c1-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="c05c1-149">Une application appelle généralement **PostQuitMessage** en réponse au message [**WM \_ Destroy**](wm-destroy.md) , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c05c1-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="c05c1-150">Envoi d’un message</span><span class="sxs-lookup"><span data-stu-id="c05c1-150">Sending a Message</span></span>

<span data-ttu-id="c05c1-151">La fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) est utilisée pour envoyer un message directement à une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c05c1-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="c05c1-152">**SendMessage** appelle une procédure de fenêtre et attend que cette procédure traite le message et retourne un résultat.</span><span class="sxs-lookup"><span data-stu-id="c05c1-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="c05c1-153">Un message peut être envoyé à n’importe quelle fenêtre du système ; tout ce qui est obligatoire est un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c05c1-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="c05c1-154">Le système utilise le handle pour déterminer la procédure de fenêtre qui doit recevoir le message.</span><span class="sxs-lookup"><span data-stu-id="c05c1-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="c05c1-155">Avant de traiter un message qui a pu être envoyé à partir d’un autre thread, une procédure de fenêtre doit d’abord appeler la fonction [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) .</span><span class="sxs-lookup"><span data-stu-id="c05c1-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="c05c1-156">Si cette fonction retourne la **valeur true**, la procédure de fenêtre doit appeler [**replyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) avant toute fonction qui amène le thread à donner le contrôle, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c05c1-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="c05c1-157">Un certain nombre de messages peuvent être envoyés à des contrôles dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c05c1-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="c05c1-158">Ces messages de contrôle définissent l’apparence, le comportement et le contenu des contrôles ou récupèrent des informations sur les contrôles.</span><span class="sxs-lookup"><span data-stu-id="c05c1-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="c05c1-159">Par exemple, le message [**CB \_ ADDSTRING**](../controls/cb-addstring.md) peut ajouter une chaîne à une zone de liste déroulante, et le message [**\_ SETCHECK BM**](../controls/bm-setcheck.md) peut définir l’état d’activation d’une case à cocher ou d’une case d’option.</span><span class="sxs-lookup"><span data-stu-id="c05c1-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="c05c1-160">Utilisez la fonction [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) pour envoyer un message à un contrôle, en spécifiant l’identificateur du contrôle et le handle de la fenêtre de la boîte de dialogue qui contient le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c05c1-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="c05c1-161">L’exemple suivant, extrait d’une procédure de boîte de dialogue, copie une chaîne du contrôle d’édition d’une zone de liste déroulante dans sa zone de liste.</span><span class="sxs-lookup"><span data-stu-id="c05c1-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="c05c1-162">L’exemple utilise **SendDlgItemMessage** pour envoyer un message [**CB \_ ADDSTRING**](../controls/cb-addstring.md) à la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c05c1-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 

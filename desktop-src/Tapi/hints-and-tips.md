---
description: Vous trouverez ci-dessous des conseils et des conseils à prendre en compte lors de l’écriture d’une application pour TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Conseils et astuces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537195"
---
# <a name="hints-and-tips"></a><span data-ttu-id="51f28-103">Conseils et astuces</span><span class="sxs-lookup"><span data-stu-id="51f28-103">Hints and Tips</span></span>

<span data-ttu-id="51f28-104">Vous trouverez ci-dessous des conseils et des conseils à prendre en compte lors de l’écriture d’une application pour TAPI 3 :</span><span class="sxs-lookup"><span data-stu-id="51f28-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="51f28-105">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com crée indirectement des fenêtres ; Cela est particulièrement important pour les threads cloisonnés.</span><span class="sxs-lookup"><span data-stu-id="51f28-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="51f28-106">Si un thread crée des fenêtres, il doit traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="51f28-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="51f28-107">Si vos threads appellent **CoInitialize**, exécutez une pompe de messages pour éviter tout problème.</span><span class="sxs-lookup"><span data-stu-id="51f28-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="51f28-108">Par exemple, COM peut cesser de marshaler correctement, ou les méthodes sur les interfaces COM, telles que **IGlobalInterfaceTable** , peuvent se bloquer.</span><span class="sxs-lookup"><span data-stu-id="51f28-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="51f28-109">Dans le cas d’un thread cloisonné, vous devez disposer d’une pompe de messages, que vous attendiez ou non des objets de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="51f28-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="51f28-110">Cela est particulièrement important si vous disposez d’une application console ou si vous écrivez un objet serveur local/distant COM qui est un thread cloisonné (où vous ne disposez pas d’une console ou d’une interface utilisateur graphique, mais le contrôle s’exécute simplement dans le système).</span><span class="sxs-lookup"><span data-stu-id="51f28-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="51f28-111">Lors de l’appel des fonctions Wait et Synchronization, telles que [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), etc.</span><span class="sxs-lookup"><span data-stu-id="51f28-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="51f28-112">À la place, utilisez [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) et traitez les messages, ou utilisez [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), qui détecte automatiquement le type de cloisonnement dans lequel se trouve le thread (STA ou MTA) et attend dans une boucle modale com (si STA) ou un bloc sur **WAITFORMULTIPLEOBJECTS** (s’il est MTA).</span><span class="sxs-lookup"><span data-stu-id="51f28-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="51f28-113">**MsgWaitForMultipleObjects** et **CoWaitForMultipleHandles** traitent également les messages Windows en fonction des règles com.</span><span class="sxs-lookup"><span data-stu-id="51f28-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="51f28-114">Par exemple, à la place de :</span><span class="sxs-lookup"><span data-stu-id="51f28-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="51f28-115">Utilisez :</span><span class="sxs-lookup"><span data-stu-id="51f28-115">Use:</span></span>

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  <span data-ttu-id="51f28-116">**ITTAPIEventNotification :: Event** est la fonction d’événement Apps appelée sur un thread de rappel TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="51f28-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="51f28-117">Effectuez le minimum dans la routine d’événement ; Utilisez plutôt votre propre thread dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="51f28-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="51f28-118">N’oubliez pas que l’exemple de code suivant est fourni, mais n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="51f28-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  <span data-ttu-id="51f28-119">Ne manipulez pas les objets COM après avoir appelé [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="51f28-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="51f28-120">Les résultats sont imprévisibles et défavorables à une application saine.</span><span class="sxs-lookup"><span data-stu-id="51f28-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="51f28-121">Voici quelques exemples de threads de travail et de destructeurs C++ qui peuvent s’exécuter après qu’une application a appelé **CoUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="51f28-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 

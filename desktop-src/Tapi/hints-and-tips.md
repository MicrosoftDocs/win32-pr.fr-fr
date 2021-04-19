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
# <a name="hints-and-tips"></a>Conseils et astuces

Vous trouverez ci-dessous des conseils et des conseils à prendre en compte lors de l’écriture d’une application pour TAPI 3 :

1.  [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com crée indirectement des fenêtres ; Cela est particulièrement important pour les threads cloisonnés. Si un thread crée des fenêtres, il doit traiter les messages. Si vos threads appellent **CoInitialize**, exécutez une pompe de messages pour éviter tout problème. Par exemple, COM peut cesser de marshaler correctement, ou les méthodes sur les interfaces COM, telles que **IGlobalInterfaceTable** , peuvent se bloquer.

    Dans le cas d’un thread cloisonné, vous devez disposer d’une pompe de messages, que vous attendiez ou non des objets de synchronisation. Cela est particulièrement important si vous disposez d’une application console ou si vous écrivez un objet serveur local/distant COM qui est un thread cloisonné (où vous ne disposez pas d’une console ou d’une interface utilisateur graphique, mais le contrôle s’exécute simplement dans le système).

    > [!Caution]  
    > Lors de l’appel des fonctions Wait et Synchronization, telles que [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), etc. À la place, utilisez [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) et traitez les messages, ou utilisez [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), qui détecte automatiquement le type de cloisonnement dans lequel se trouve le thread (STA ou MTA) et attend dans une boucle modale com (si STA) ou un bloc sur **WAITFORMULTIPLEOBJECTS** (s’il est MTA). **MsgWaitForMultipleObjects** et **CoWaitForMultipleHandles** traitent également les messages Windows en fonction des règles com.

     

    Par exemple, à la place de :

    `Sleep (5000);`

    Utilisez :

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

2.  **ITTAPIEventNotification :: Event** est la fonction d’événement Apps appelée sur un thread de rappel TAPI 3.

    Effectuez le minimum dans la routine d’événement ; Utilisez plutôt votre propre thread dans la mesure du possible.

    N’oubliez pas que l’exemple de code suivant est fourni, mais n’est pas obligatoire.

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

3.  Ne manipulez pas les objets COM après avoir appelé [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Les résultats sont imprévisibles et défavorables à une application saine. Voici quelques exemples de threads de travail et de destructeurs C++ qui peuvent s’exécuter après qu’une application a appelé **CoUninitialize**.

 

 

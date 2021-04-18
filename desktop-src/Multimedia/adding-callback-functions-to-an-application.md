---
title: Ajout de fonctions de rappel à une application
description: Ajout de fonctions de rappel à une application
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507251"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="17d08-103">Ajout de fonctions de rappel à une application</span><span class="sxs-lookup"><span data-stu-id="17d08-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="17d08-104">Une application peut enregistrer des fonctions de rappel avec la fenêtre de capture afin qu’elle envoie une notification à l’application dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="17d08-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="17d08-105">L’état change</span><span class="sxs-lookup"><span data-stu-id="17d08-105">The status changes</span></span>
-   <span data-ttu-id="17d08-106">Des erreurs se produisent</span><span class="sxs-lookup"><span data-stu-id="17d08-106">Errors occur</span></span>
-   <span data-ttu-id="17d08-107">Les mémoires tampons audio et les images vidéo deviennent disponibles</span><span class="sxs-lookup"><span data-stu-id="17d08-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="17d08-108">L’application doit se produire pendant la capture en continu</span><span class="sxs-lookup"><span data-stu-id="17d08-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="17d08-109">L’exemple suivant crée une fenêtre de capture et enregistre les fonctions d’État, d’erreur, de flux vidéo et de rappel de frame dans la boucle de traitement de message d’une application.</span><span class="sxs-lookup"><span data-stu-id="17d08-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="17d08-110">Il comprend également un exemple d’instruction pour la désactivation d’une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="17d08-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="17d08-111">Les exemples suivants illustrent des fonctions d’État, d’erreur et de rappel d’image simples.</span><span class="sxs-lookup"><span data-stu-id="17d08-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="17d08-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17d08-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d08-113">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="17d08-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 





---
title: Création de fonctions de rappel d’État
description: Ce didacticiel explique comment créer une fonction de rappel d’état utilisée pour surveiller l’état d’une demande Internet.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106511525"
---
# <a name="creating-status-callback-functions"></a><span data-ttu-id="5959b-103">Création de fonctions de rappel d’État</span><span class="sxs-lookup"><span data-stu-id="5959b-103">Creating Status Callback Functions</span></span>

<span data-ttu-id="5959b-104">Ce didacticiel explique comment créer une fonction de rappel d’état utilisée pour surveiller l’état d’une demande Internet.</span><span class="sxs-lookup"><span data-stu-id="5959b-104">This tutorial describes how to create a status callback function used to monitor the status of an Internet request.</span></span>

<span data-ttu-id="5959b-105">Les fonctions de rappel d’État reçoivent des rappels d’État sur toutes les requêtes Internet provenant de toute fonction WinINet à laquelle une valeur de contexte différente de zéro a été passée.</span><span class="sxs-lookup"><span data-stu-id="5959b-105">Status callback functions receive status callbacks on any Internet requests that originated from any WinINet function that was passed a nonzero context value.</span></span>


<span data-ttu-id="5959b-106">Les étapes suivantes sont nécessaires pour créer une fonction de rappel d’État :</span><span class="sxs-lookup"><span data-stu-id="5959b-106">The following steps are necessary for creating a status callback function:</span></span>

1.  [<span data-ttu-id="5959b-107">Définissez la valeur de contexte.</span><span class="sxs-lookup"><span data-stu-id="5959b-107">Define the context value.</span></span>](#defining-the-context-value)
2.  [<span data-ttu-id="5959b-108">Créez la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-108">Create the status callback function.</span></span>](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a><span data-ttu-id="5959b-109">Définition de la valeur de contexte</span><span class="sxs-lookup"><span data-stu-id="5959b-109">Defining the Context Value</span></span>

<span data-ttu-id="5959b-110">La valeur de contexte peut être n’importe quelle valeur d’entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="5959b-110">The context value can be any unsigned long integer value.</span></span> <span data-ttu-id="5959b-111">Dans l’idéal, la valeur de contexte doit identifier la demande qui vient d’être terminée et l’emplacement de toutes les ressources associées, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5959b-111">Ideally, the context value should identify what request has just been completed and the location of any associated resources, if needed.</span></span>

<span data-ttu-id="5959b-112">L’une des méthodes les plus utiles pour utiliser la valeur de contexte consiste à passer l’adresse d’une structure et à la convertir en **\_ ptr DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5959b-112">One of the most useful ways to use the context value is to pass the address of a structure and cast it to a **DWORD\_PTR**.</span></span> <span data-ttu-id="5959b-113">La structure peut être utilisée pour stocker des informations sur la demande, afin qu’elle soit passée à la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-113">The structure can be used to store information about the request, so that it is passed to the status callback function.</span></span>

<span data-ttu-id="5959b-114">La structure suivante est un exemple de valeur de contexte possible.</span><span class="sxs-lookup"><span data-stu-id="5959b-114">The following structure is an example of a possible context value.</span></span> <span data-ttu-id="5959b-115">Les membres de la structure sont choisis avec la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="5959b-115">The members of the structure are chosen with the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function in mind.</span></span>


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



<span data-ttu-id="5959b-116">Dans cet exemple, la fonction de rappel d’État aurait accès au handle de fenêtre, ce qui lui permettrait d’afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5959b-116">In this example, the status callback function would have access to the window handle, which would allow it to display a user interface.</span></span> <span data-ttu-id="5959b-117">Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être passé à une autre fonction qui peut télécharger la ressource et un tableau de caractères qui peut être utilisé pour transmettre des informations sur la demande.</span><span class="sxs-lookup"><span data-stu-id="5959b-117">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) could be passed to another function that can download the resource and an array of characters that can be used to pass information about the request.</span></span>

<span data-ttu-id="5959b-118">Les membres de la structure peuvent être modifiés en fonction des besoins d’une application particulière, donc ne vous contentez pas d’utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="5959b-118">The members of the structure can be changed to fit the needs of a particular application, so do not feel constrained by this example.</span></span>

### <a name="creating-the-status-callback-function"></a><span data-ttu-id="5959b-119">Création de la fonction de rappel d’État</span><span class="sxs-lookup"><span data-stu-id="5959b-119">Creating the Status Callback Function</span></span>

<span data-ttu-id="5959b-120">La fonction de rappel d’État doit respecter le format [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="5959b-120">The status callback function must follow the format of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span> <span data-ttu-id="5959b-121">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="5959b-121">To do this:</span></span>

1.  <span data-ttu-id="5959b-122">Écrivez une déclaration de fonction pour votre fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-122">Write a function declaration for your status callback function.</span></span>

    <span data-ttu-id="5959b-123">L’exemple suivant illustre un exemple de déclaration.</span><span class="sxs-lookup"><span data-stu-id="5959b-123">The following example shows a sample declaration.</span></span>

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  <span data-ttu-id="5959b-124">Déterminez ce que fera la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-124">Determine what your status callback function will do.</span></span> <span data-ttu-id="5959b-125">Pour les applications qui effectuent des appels asynchrones, la fonction de rappel d’État doit gérer la valeur de la \_ \_ demande d’État Internet \_ Complete, qui indique qu’une demande asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="5959b-125">For applications that are making asynchronous calls, the status callback function must handle the INTERNET\_STATUS\_REQUEST\_COMPLETE value, which indicates an asynchronous request is complete.</span></span> <span data-ttu-id="5959b-126">La fonction de rappel d’État peut également être utilisée pour suivre la progression d’une demande Internet.</span><span class="sxs-lookup"><span data-stu-id="5959b-126">The status callback function can also be used to track the progress of an Internet request.</span></span>

    <span data-ttu-id="5959b-127">En général, il est préférable d’utiliser une instruction switch avec *dwInternetStatus* comme valeur de commutateur et les valeurs d’État pour les instructions case.</span><span class="sxs-lookup"><span data-stu-id="5959b-127">In general, it works best to use a switch statement with *dwInternetStatus* as the switch value and the status values for the case statements.</span></span> <span data-ttu-id="5959b-128">Selon les types de fonctions que votre application appelle, vous pouvez ignorer certaines des valeurs d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-128">Depending on the types of functions your application is calling, you can ignore some of the status values.</span></span> <span data-ttu-id="5959b-129">Pour obtenir une définition des différentes valeurs d’État, consultez la liste sous le paramètre *dwInternetStatus* de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="5959b-129">For a definition of the different status values, see the listing under the *dwInternetStatus* parameter of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span>

    <span data-ttu-id="5959b-130">L’instruction switch suivante est un exemple de gestion des rappels d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-130">The following switch statement is an example of how to handle status callbacks.</span></span>

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  <span data-ttu-id="5959b-131">Créez le code pour gérer les valeurs d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-131">Create the code to handle the status values.</span></span>

    <span data-ttu-id="5959b-132">Le code permettant de gérer chacune des valeurs d’état dépend fortement de l’utilisation prévue de la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-132">The code to handle each of the status values depends heavily on your intended use of the status callback function.</span></span> <span data-ttu-id="5959b-133">Pour les applications qui effectuent simplement le suivi de la progression d’une demande, l’écriture d’une chaîne dans une zone de liste peut être tout ce dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="5959b-133">For applications that are just tracking the progress of a request, writing a string to a list box might be all you need.</span></span> <span data-ttu-id="5959b-134">Pour les opérations asynchrones, le code doit gérer certaines des données retournées dans le rappel.</span><span class="sxs-lookup"><span data-stu-id="5959b-134">For asynchronous operations, the code must handle some of the data returned in the callback.</span></span>

    <span data-ttu-id="5959b-135">La fonction de rappel d’État suivante utilise une fonction Switch pour déterminer la valeur d’État et crée une chaîne qui comprend le nom de la valeur d’État et la fonction précédente appelée, qui est stockée dans le membre szMemo de la structure de contexte de la requête \_ .</span><span class="sxs-lookup"><span data-stu-id="5959b-135">The following status callback function uses a switch function to determine what the status value is and creates a string that includes the name of the status value and the previous function called, which is stored in the szMemo member of the REQUEST\_CONTEXT structure.</span></span>

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  <span data-ttu-id="5959b-136">Utilisez la fonction [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) pour définir la fonction de rappel d’État sur le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) pour lequel vous souhaitez recevoir des rappels d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-136">Use the [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) function to set the status callback function on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle for which you want to receive status callbacks.</span></span>

    <span data-ttu-id="5959b-137">L’exemple suivant montre comment définir une fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="5959b-137">The following example demonstrates how to set a status callback function.</span></span>

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> <span data-ttu-id="5959b-138">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="5959b-138">WinINet does not support server implementations.</span></span> <span data-ttu-id="5959b-139">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="5959b-139">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5959b-140">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5959b-140">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5959b-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5959b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5959b-142">Création de fonctions de rappel d’État</span><span class="sxs-lookup"><span data-stu-id="5959b-142">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="5959b-143">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="5959b-143">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[<span data-ttu-id="5959b-144">*InternetStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="5959b-144">*InternetStatusCallback*</span></span>](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 
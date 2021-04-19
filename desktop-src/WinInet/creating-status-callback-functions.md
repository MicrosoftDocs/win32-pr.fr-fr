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
# <a name="creating-status-callback-functions"></a>Création de fonctions de rappel d’État

Ce didacticiel explique comment créer une fonction de rappel d’état utilisée pour surveiller l’état d’une demande Internet.

Les fonctions de rappel d’État reçoivent des rappels d’État sur toutes les requêtes Internet provenant de toute fonction WinINet à laquelle une valeur de contexte différente de zéro a été passée.


Les étapes suivantes sont nécessaires pour créer une fonction de rappel d’État :

1.  [Définissez la valeur de contexte.](#defining-the-context-value)
2.  [Créez la fonction de rappel d’État.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Définition de la valeur de contexte

La valeur de contexte peut être n’importe quelle valeur d’entier long non signé. Dans l’idéal, la valeur de contexte doit identifier la demande qui vient d’être terminée et l’emplacement de toutes les ressources associées, si nécessaire.

L’une des méthodes les plus utiles pour utiliser la valeur de contexte consiste à passer l’adresse d’une structure et à la convertir en **\_ ptr DWORD**. La structure peut être utilisée pour stocker des informations sur la demande, afin qu’elle soit passée à la fonction de rappel d’État.

La structure suivante est un exemple de valeur de contexte possible. Les membres de la structure sont choisis avec la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) à l’esprit.


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



Dans cet exemple, la fonction de rappel d’État aurait accès au handle de fenêtre, ce qui lui permettrait d’afficher une interface utilisateur. Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être passé à une autre fonction qui peut télécharger la ressource et un tableau de caractères qui peut être utilisé pour transmettre des informations sur la demande.

Les membres de la structure peuvent être modifiés en fonction des besoins d’une application particulière, donc ne vous contentez pas d’utiliser cet exemple.

### <a name="creating-the-status-callback-function"></a>Création de la fonction de rappel d’État

La fonction de rappel d’État doit respecter le format [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback). Pour ce faire :

1.  Écrivez une déclaration de fonction pour votre fonction de rappel d’État.

    L’exemple suivant illustre un exemple de déclaration.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Déterminez ce que fera la fonction de rappel d’État. Pour les applications qui effectuent des appels asynchrones, la fonction de rappel d’État doit gérer la valeur de la \_ \_ demande d’État Internet \_ Complete, qui indique qu’une demande asynchrone est terminée. La fonction de rappel d’État peut également être utilisée pour suivre la progression d’une demande Internet.

    En général, il est préférable d’utiliser une instruction switch avec *dwInternetStatus* comme valeur de commutateur et les valeurs d’État pour les instructions case. Selon les types de fonctions que votre application appelle, vous pouvez ignorer certaines des valeurs d’État. Pour obtenir une définition des différentes valeurs d’État, consultez la liste sous le paramètre *dwInternetStatus* de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    L’instruction switch suivante est un exemple de gestion des rappels d’État.

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

3.  Créez le code pour gérer les valeurs d’État.

    Le code permettant de gérer chacune des valeurs d’état dépend fortement de l’utilisation prévue de la fonction de rappel d’État. Pour les applications qui effectuent simplement le suivi de la progression d’une demande, l’écriture d’une chaîne dans une zone de liste peut être tout ce dont vous avez besoin. Pour les opérations asynchrones, le code doit gérer certaines des données retournées dans le rappel.

    La fonction de rappel d’État suivante utilise une fonction Switch pour déterminer la valeur d’État et crée une chaîne qui comprend le nom de la valeur d’État et la fonction précédente appelée, qui est stockée dans le membre szMemo de la structure de contexte de la requête \_ .

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

    

4.  Utilisez la fonction [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) pour définir la fonction de rappel d’État sur le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) pour lequel vous souhaitez recevoir des rappels d’État.

    L’exemple suivant montre comment définir une fonction de rappel d’État.

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
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fonctions de rappel d’État](creating-status-callback-functions.md)
</dt> <dt>

[**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 
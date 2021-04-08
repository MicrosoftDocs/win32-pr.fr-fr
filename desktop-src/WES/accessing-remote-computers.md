---
title: Accès aux ordinateurs distants
description: Vous pouvez utiliser l’API du journal des événements Windows pour accéder aux données sur l’ordinateur local ou sur un ordinateur distant.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0063238560ddd7f1613e94b83ecc7f27900bb3
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101365"
---
# <a name="accessing-remote-computers"></a><span data-ttu-id="691f6-103">Accès aux ordinateurs distants</span><span class="sxs-lookup"><span data-stu-id="691f6-103">Accessing Remote Computers</span></span>

<span data-ttu-id="691f6-104">Vous pouvez utiliser l’API du journal des événements Windows pour accéder aux données sur l’ordinateur local ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="691f6-104">You can use the Windows Event Log API to access data on the local computer or on a remote computer.</span></span> <span data-ttu-id="691f6-105">Pour accéder aux données d’un ordinateur distant, vous devez appeler la fonction [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) pour créer un contexte de session à distance.</span><span class="sxs-lookup"><span data-stu-id="691f6-105">To access data on a remote computer, you need to call the [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) function to create a remote session context.</span></span> <span data-ttu-id="691f6-106">Lorsque vous appelez cette fonction, vous spécifiez le nom de l’ordinateur distant auquel vous souhaitez vous connecter, les informations d’identification de l’utilisateur à utiliser pour établir la connexion, ainsi que le type d’authentification à utiliser pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="691f6-106">When you call this function, you specify the name of the remote computer that you want to connect to, the user credentials to use to make the connection, and the type of authentication to use to authenticate the user.</span></span> <span data-ttu-id="691f6-107">Pour spécifier l’utilisateur actuel, définissez les membres du domaine, de l’utilisateur et du mot de passe sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="691f6-107">To specify the current user, set the Domain, User, and Password members to **NULL**.</span></span>

<span data-ttu-id="691f6-108">Lorsque vous appelez l’API du journal des événements Windows, vous transmettez le descripteur au contexte de session à distance retourné par la fonction [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) .</span><span class="sxs-lookup"><span data-stu-id="691f6-108">When you call Windows Event Log API, you pass the handle to the remote session context that the [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) function returns.</span></span> <span data-ttu-id="691f6-109">(Pour accéder aux données sur l’ordinateur local, transmettez la **valeur null** pour spécifier la session par défaut.) Pour accéder aux données sur l’ordinateur distant, l’ordinateur distant doit activer l’exception de pare-feu Windows « gestion des journaux des événements à distance ». dans le cas contraire, lorsque vous tentez d’utiliser le descripteur de session, l’appel est erroné avec le \_ serveur RPC S \_ \_ non disponible.</span><span class="sxs-lookup"><span data-stu-id="691f6-109">(To access data on the local computer, pass **NULL** to specify the default session.) To access data on the remote computer, the remote computer must enable the "Remote Event Log Management" Windows Firewall exception; otherwise, when you try to use the session handle, the call will error with RPC\_S\_SERVER\_UNAVAILABLE.</span></span> <span data-ttu-id="691f6-110">L’ordinateur auquel vous vous connectez doit exécuter Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="691f6-110">The computer to which you are connecting must be running Windows Vista or later.</span></span>

<span data-ttu-id="691f6-111">L’exemple suivant montre comment se connecter à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="691f6-111">The following example shows how to connect to a remote computer.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```

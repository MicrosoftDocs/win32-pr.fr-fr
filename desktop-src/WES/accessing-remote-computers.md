---
title: Accès aux ordinateurs distants
description: vous pouvez utiliser l’API du journal des événements Windows pour accéder aux données sur l’ordinateur local ou sur un ordinateur distant.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a64bf1b3bded6ba1c72231e85bc78fa7f486739741fea1391c869ad79b457e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032579"
---
# <a name="accessing-remote-computers"></a>Accès aux ordinateurs distants

vous pouvez utiliser l’API du journal des événements Windows pour accéder aux données sur l’ordinateur local ou sur un ordinateur distant. Pour accéder aux données d’un ordinateur distant, vous devez appeler la fonction [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) pour créer un contexte de session à distance. Lorsque vous appelez cette fonction, vous spécifiez le nom de l’ordinateur distant auquel vous souhaitez vous connecter, les informations d’identification de l’utilisateur à utiliser pour établir la connexion, ainsi que le type d’authentification à utiliser pour authentifier l’utilisateur. Pour spécifier l’utilisateur actuel, définissez les membres du domaine, de l’utilisateur et du mot de passe sur la **valeur null**.

lorsque vous appelez Windows API du journal des événements, vous transmettez le descripteur au contexte de session à distance retourné par la fonction [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) . (Pour accéder aux données sur l’ordinateur local, transmettez la **valeur null** pour spécifier la session par défaut.) pour accéder aux données sur l’ordinateur distant, l’ordinateur distant doit activer la « gestion des journaux des événements à distance » Windows exception de pare-feu ; dans le cas contraire, lorsque vous tentez d’utiliser le descripteur de session, l’appel est erroné avec le \_ serveur RPC S \_ \_ non disponible. l’ordinateur auquel vous vous connectez doit exécuter Windows Vista ou version ultérieure.

L’exemple suivant montre comment se connecter à un ordinateur distant.


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

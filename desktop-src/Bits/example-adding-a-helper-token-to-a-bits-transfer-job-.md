---
title: Exemple d’ajout d’un jeton d’assistance à une tâche de transfert BITS
description: Vous pouvez configurer une tâche de transfert Service de transfert intelligent en arrière-plan (BITS) avec un jeton de sécurité supplémentaire. La tâche de transfert BITS utilise ce jeton d’assistance pour l’authentification et pour accéder aux ressources.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031788"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Exemple : ajout d’un jeton d’assistance à une tâche de transfert BITS

Vous pouvez configurer une tâche de transfert Service de transfert intelligent en arrière-plan (BITS) avec un jeton de sécurité supplémentaire. La tâche de transfert BITS utilise ce jeton d’assistance pour l’authentification et pour accéder aux ressources.

Pour plus d’informations, consultez [jetons d’assistance pour les tâches de transfert bits](helper-tokens-for-bits-transfer-jobs.md).

La procédure suivante crée une tâche de transfert BITS dans le contexte de l’utilisateur local, obtient les informations d’identification d’un deuxième utilisateur, crée un jeton d’assistance avec ces informations d’identification, puis définit le jeton d’assistance sur la tâche de transfert BITS.

Cet exemple utilise l’en-tête et l’implémentation définis dans [exemple : classes communes](common-classes.md).

**Pour ajouter un jeton d’assistance à une tâche de transfert BITS**

1.  Initialisez les paramètres COM en appelant la fonction CCoInitializer. Pour plus d’informations sur la fonction CCoInitializer, consultez [exemple : classes communes](common-classes.md).
2.  Obtient un pointeur vers l’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) . Cet exemple utilise la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) pour gérer les pointeurs d’interface com.
3.  Initialisez la sécurité des processus COM en appelant [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requiert au moins le niveau d’emprunt d’identité d’emprunt d’identité. BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini.
4.  Obtenez un pointeur vers l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) et obtenez le localisateur initial pour bits en appelant la fonction [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
5.  Créez une tâche de transfert BITS en appelant la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
6.  Obtenez un pointeur vers l’interface de rappel CNotifyInterface et appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour recevoir la notification des événements liés aux travaux. Pour plus d’informations sur CNotifyInterface, consultez [exemple : classes communes](common-classes.md).
7.  Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour définir les types de notifications à recevoir. Dans cet exemple, les indicateurs d' **\_ \_ \_ erreur** du **\_ travail de notification \_ \_ BG** et du travail de notification BG sont définis.
8.  Obtenir un pointeur vers l’interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) en appelant la méthode **méthode ibackgroundcopyjob :: QueryInterface** avec l’identificateur d’interface approprié.
9.  Tente d’ouvrir une session sur l’utilisateur du jeton d’assistance. Créez un descripteur d’emprunt d’identité et appelez la [fonction LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) pour remplir le descripteur d’emprunt d’identité. En cas de réussite, appelez la [fonction ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser). En cas d’échec, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté, une erreur est générée et le descripteur est fermé.
10. Appelez la méthode [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) pour emprunter l’identité du jeton de l’utilisateur connecté. Si cette méthode échoue, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté, une erreur est générée et le descripteur est fermé.
    > [!Note]
    >
    > Dans les versions prises en charge de Windows antérieures à Windows 10, la version 1607, le propriétaire du travail doit disposer d’informations d’identification d’administration pour appeler la méthode [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .
    >
    > À compter de Windows 10, version 1607, les propriétaires de travaux non-administrateurs peuvent définir des jetons d’assistance non-administrateur sur les travaux BITS qu’ils possèdent. Les propriétaires de travaux doivent toujours disposer d’informations d’identification administratives pour définir des jetons d’assistance avec des privilèges d’administrateur.

     

11. Appelez la méthode [**IBitsTokenOptions :: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) pour spécifier les ressources auxquelles accéder à l’aide du contexte de sécurité du jeton d’assistance.
12. Une fois l’emprunt d’identité terminé, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté et le descripteur est fermé.
13. Ajoutez des fichiers à la tâche de transfert BITS en appelant [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).
14. Une fois le fichier ajouté, appelez [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour reprendre la tâche.
15. Configurez une boucle while pour attendre le message Quit de l’interface de rappel pendant le transfert du travail. La boucle while utilise la fonction [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) pour récupérer le nombre de millisecondes qui se sont écoulées depuis le début du transfert du travail.
16. Une fois la tâche de transfert BITS terminée, supprimez la tâche de la file d’attente en appelant [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

L’exemple de code suivant ajoute un jeton d’assistance à une tâche de transfert BITS.


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(
            NULL,
            -1,
            NULL,
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL,
            EOAC_DYNAMIC_CLOAKING,
            0
            );

        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
            throw MyException(hr, L"Resume");
        }    
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jetons d’assistance pour les tâches de transfert BITS](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Exemple : classes communes](common-classes.md)
</dt> </dl>

 

 
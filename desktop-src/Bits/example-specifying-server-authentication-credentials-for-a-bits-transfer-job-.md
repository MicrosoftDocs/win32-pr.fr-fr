---
title: Spécifier les informations d’identification d’authentification du serveur pour une tâche de transfert BITS
description: Vous pouvez spécifier des schémas d’authentification différents pour une tâche de transfert Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031840"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Spécifier les informations d’identification d’authentification du serveur pour une tâche de transfert BITS

Vous pouvez spécifier des schémas d’authentification différents pour une tâche de transfert Service de transfert intelligent en arrière-plan (BITS).

La procédure suivante permet d’obtenir un schéma d’authentification et de créer une structure d’identité d’authentification. L’application crée ensuite une tâche de téléchargement BITS et définit les informations d’identification du travail. Une fois la tâche créée, l’application obtient un pointeur vers une interface de rappel et interroge l’état de la tâche de transfert BITS. Une fois la tâche terminée, elle est supprimée de la file d’attente.

Cet exemple utilise l’en-tête et l’implémentation définis dans [exemple : classes communes](common-classes.md).

**Pour spécifier les informations d’authentification du serveur pour une tâche de transfert BITS**

1.  Créer une structure de conteneur qui mappe les valeurs du [**\_ \_ schéma d’authentification BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) aux noms de schémas.

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  Initialisez les paramètres COM en appelant la fonction CCoInitializer. Pour plus d’informations sur la fonction CCoInitializer, consultez [exemple : classes communes](common-classes.md).
3.  Préparez une [**structure \_ \_ d’informations d’identification d’authentification BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) . L’exemple utilise la fonction [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) pour effacer les emplacements de mémoire associés aux informations sensibles. La fonction [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) est définie dans WinBase. h.
4.  Utilisez la fonction GetScheme pour récupérer le schéma d’authentification à utiliser pour se connecter au serveur.

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  Renseignez la structure des [**\_ \_ informations d’identification d’authentification BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) avec le schéma d’authentification retourné par la fonction GetScheme et le nom d’utilisateur et le mot de passe passés dans la fonction ServerAuthentication.
6.  Obtient un pointeur vers l’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).
7.  Initialisez la sécurité des processus COM en appelant [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requiert au moins le niveau d’emprunt d’identité d’emprunt d’identité. BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini.
8.  Obtenez un pointeur vers l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) et obtenez le localisateur initial pour bits en appelant la fonction [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
9.  Créez une tâche de transfert BITS en appelant la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
10. Obtenez un pointeur vers l’interface de rappel CNotifyInterface et appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour recevoir la notification des événements liés au travail. Pour plus d’informations sur CNotifyInterface, consultez [exemple : classes communes](common-classes.md).
11. Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour définir les types de notifications à recevoir. Dans cet exemple, les indicateurs d' **\_ \_ \_ erreur** du **\_ travail de notification \_ \_ BG** et du travail de notification BG sont définis.
12. Obtient un pointeur vers l’interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Utilisez le pointeur **IBackgroundCopyJob2** pour définir des propriétés supplémentaires sur le travail. Ce programme utilise la méthode [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) pour définir les informations d’identification de la tâche de transfert bits.
13. Ajoutez des fichiers à la tâche de transfert BITS en appelant [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile). Dans cet exemple, la méthode **méthode ibackgroundcopyjob :: AddFile** utilise les variables RemoteFile et fichier_local qui ont été passées à la fonction ServerAuthentication.
14. Une fois le fichier ajouté, appelez [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour reprendre la tâche.
15. Configurez une boucle while pour attendre le message Quit de l’interface de rappel pendant le transfert du travail.

    > [!Note]  
    > Cette étape est nécessaire uniquement si le cloisonnement COM est un cloisonnement à thread unique. Pour plus d’informations, consultez [cloisonnements à thread unique](../com/single-threaded-apartments.md).

     

    ```C++
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
    ```

    

    La boucle ci-dessus utilise la fonction [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) pour récupérer le nombre de millisecondes qui se sont écoulées depuis le début du transfert du travail.

16. Une fois la tâche de transfert BITS terminée, supprimez la tâche de la file d’attente en appelant [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

L’exemple de code suivant spécifie les informations d’identification d’authentification du serveur pour une tâche de transfert BITS.


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

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
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
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
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
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Exemple : classes communes](common-classes.md)
</dt> </dl>

 

 
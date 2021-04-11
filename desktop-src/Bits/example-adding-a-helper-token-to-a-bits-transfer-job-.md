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
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="74df5-104">Exemple : ajout d’un jeton d’assistance à une tâche de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="74df5-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="74df5-105">Vous pouvez configurer une tâche de transfert Service de transfert intelligent en arrière-plan (BITS) avec un jeton de sécurité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="74df5-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="74df5-106">La tâche de transfert BITS utilise ce jeton d’assistance pour l’authentification et pour accéder aux ressources.</span><span class="sxs-lookup"><span data-stu-id="74df5-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="74df5-107">Pour plus d’informations, consultez [jetons d’assistance pour les tâches de transfert bits](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="74df5-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="74df5-108">La procédure suivante crée une tâche de transfert BITS dans le contexte de l’utilisateur local, obtient les informations d’identification d’un deuxième utilisateur, crée un jeton d’assistance avec ces informations d’identification, puis définit le jeton d’assistance sur la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="74df5-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="74df5-109">Cet exemple utilise l’en-tête et l’implémentation définis dans [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="74df5-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="74df5-110">**Pour ajouter un jeton d’assistance à une tâche de transfert BITS**</span><span class="sxs-lookup"><span data-stu-id="74df5-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="74df5-111">Initialisez les paramètres COM en appelant la fonction CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="74df5-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="74df5-112">Pour plus d’informations sur la fonction CCoInitializer, consultez [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="74df5-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="74df5-113">Obtient un pointeur vers l’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="74df5-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="74df5-114">Cet exemple utilise la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) pour gérer les pointeurs d’interface com.</span><span class="sxs-lookup"><span data-stu-id="74df5-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="74df5-115">Initialisez la sécurité des processus COM en appelant [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="74df5-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="74df5-116">BITS requiert au moins le niveau d’emprunt d’identité d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="74df5-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="74df5-117">BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="74df5-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="74df5-118">Obtenez un pointeur vers l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) et obtenez le localisateur initial pour bits en appelant la fonction [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="74df5-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="74df5-119">Créez une tâche de transfert BITS en appelant la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="74df5-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="74df5-120">Obtenez un pointeur vers l’interface de rappel CNotifyInterface et appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour recevoir la notification des événements liés aux travaux.</span><span class="sxs-lookup"><span data-stu-id="74df5-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="74df5-121">Pour plus d’informations sur CNotifyInterface, consultez [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="74df5-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="74df5-122">Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour définir les types de notifications à recevoir.</span><span class="sxs-lookup"><span data-stu-id="74df5-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="74df5-123">Dans cet exemple, les indicateurs d' **\_ \_ \_ erreur** du **\_ travail de notification \_ \_ BG** et du travail de notification BG sont définis.</span><span class="sxs-lookup"><span data-stu-id="74df5-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="74df5-124">Obtenir un pointeur vers l’interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) en appelant la méthode **méthode ibackgroundcopyjob :: QueryInterface** avec l’identificateur d’interface approprié.</span><span class="sxs-lookup"><span data-stu-id="74df5-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="74df5-125">Tente d’ouvrir une session sur l’utilisateur du jeton d’assistance.</span><span class="sxs-lookup"><span data-stu-id="74df5-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="74df5-126">Créez un descripteur d’emprunt d’identité et appelez la [fonction LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) pour remplir le descripteur d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="74df5-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="74df5-127">En cas de réussite, appelez la [fonction ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span><span class="sxs-lookup"><span data-stu-id="74df5-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="74df5-128">En cas d’échec, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté, une erreur est générée et le descripteur est fermé.</span><span class="sxs-lookup"><span data-stu-id="74df5-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="74df5-129">Appelez la méthode [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) pour emprunter l’identité du jeton de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="74df5-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="74df5-130">Si cette méthode échoue, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté, une erreur est générée et le descripteur est fermé.</span><span class="sxs-lookup"><span data-stu-id="74df5-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="74df5-131">Dans les versions prises en charge de Windows antérieures à Windows 10, la version 1607, le propriétaire du travail doit disposer d’informations d’identification d’administration pour appeler la méthode [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .</span><span class="sxs-lookup"><span data-stu-id="74df5-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="74df5-132">À compter de Windows 10, version 1607, les propriétaires de travaux non-administrateurs peuvent définir des jetons d’assistance non-administrateur sur les travaux BITS qu’ils possèdent.</span><span class="sxs-lookup"><span data-stu-id="74df5-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="74df5-133">Les propriétaires de travaux doivent toujours disposer d’informations d’identification administratives pour définir des jetons d’assistance avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="74df5-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="74df5-134">Appelez la méthode [**IBitsTokenOptions :: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) pour spécifier les ressources auxquelles accéder à l’aide du contexte de sécurité du jeton d’assistance.</span><span class="sxs-lookup"><span data-stu-id="74df5-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="74df5-135">Une fois l’emprunt d’identité terminé, l’exemple appelle la [fonction RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour mettre fin à l’emprunt d’identité de l’utilisateur connecté et le descripteur est fermé.</span><span class="sxs-lookup"><span data-stu-id="74df5-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="74df5-136">Ajoutez des fichiers à la tâche de transfert BITS en appelant [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="74df5-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="74df5-137">Une fois le fichier ajouté, appelez [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour reprendre la tâche.</span><span class="sxs-lookup"><span data-stu-id="74df5-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="74df5-138">Configurez une boucle while pour attendre le message Quit de l’interface de rappel pendant le transfert du travail.</span><span class="sxs-lookup"><span data-stu-id="74df5-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="74df5-139">La boucle while utilise la fonction [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) pour récupérer le nombre de millisecondes qui se sont écoulées depuis le début du transfert du travail.</span><span class="sxs-lookup"><span data-stu-id="74df5-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="74df5-140">Une fois la tâche de transfert BITS terminée, supprimez la tâche de la file d’attente en appelant [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="74df5-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="74df5-141">L’exemple de code suivant ajoute un jeton d’assistance à une tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="74df5-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="74df5-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74df5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74df5-143">Jetons d’assistance pour les tâches de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="74df5-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="74df5-144">**IBitsTokenOptions**</span><span class="sxs-lookup"><span data-stu-id="74df5-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="74df5-145">Exemple : classes communes</span><span class="sxs-lookup"><span data-stu-id="74df5-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 
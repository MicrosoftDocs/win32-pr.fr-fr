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
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="cb600-103">Spécifier les informations d’identification d’authentification du serveur pour une tâche de transfert BITS</span><span class="sxs-lookup"><span data-stu-id="cb600-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="cb600-104">Vous pouvez spécifier des schémas d’authentification différents pour une tâche de transfert Service de transfert intelligent en arrière-plan (BITS).</span><span class="sxs-lookup"><span data-stu-id="cb600-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="cb600-105">La procédure suivante permet d’obtenir un schéma d’authentification et de créer une structure d’identité d’authentification.</span><span class="sxs-lookup"><span data-stu-id="cb600-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="cb600-106">L’application crée ensuite une tâche de téléchargement BITS et définit les informations d’identification du travail.</span><span class="sxs-lookup"><span data-stu-id="cb600-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="cb600-107">Une fois la tâche créée, l’application obtient un pointeur vers une interface de rappel et interroge l’état de la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="cb600-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="cb600-108">Une fois la tâche terminée, elle est supprimée de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cb600-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="cb600-109">Cet exemple utilise l’en-tête et l’implémentation définis dans [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="cb600-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="cb600-110">**Pour spécifier les informations d’authentification du serveur pour une tâche de transfert BITS**</span><span class="sxs-lookup"><span data-stu-id="cb600-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="cb600-111">Créer une structure de conteneur qui mappe les valeurs du [**\_ \_ schéma d’authentification BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) aux noms de schémas.</span><span class="sxs-lookup"><span data-stu-id="cb600-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

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

    

2.  <span data-ttu-id="cb600-112">Initialisez les paramètres COM en appelant la fonction CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="cb600-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="cb600-113">Pour plus d’informations sur la fonction CCoInitializer, consultez [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="cb600-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="cb600-114">Préparez une [**structure \_ \_ d’informations d’identification d’authentification BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="cb600-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="cb600-115">L’exemple utilise la fonction [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) pour effacer les emplacements de mémoire associés aux informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="cb600-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="cb600-116">La fonction [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) est définie dans WinBase. h.</span><span class="sxs-lookup"><span data-stu-id="cb600-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="cb600-117">Utilisez la fonction GetScheme pour récupérer le schéma d’authentification à utiliser pour se connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="cb600-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

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

    

5.  <span data-ttu-id="cb600-118">Renseignez la structure des [**\_ \_ informations d’identification d’authentification BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) avec le schéma d’authentification retourné par la fonction GetScheme et le nom d’utilisateur et le mot de passe passés dans la fonction ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cb600-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="cb600-119">Obtient un pointeur vers l’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).</span><span class="sxs-lookup"><span data-stu-id="cb600-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="cb600-120">Initialisez la sécurité des processus COM en appelant [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="cb600-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="cb600-121">BITS requiert au moins le niveau d’emprunt d’identité d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="cb600-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="cb600-122">BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb600-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="cb600-123">Obtenez un pointeur vers l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) et obtenez le localisateur initial pour bits en appelant la fonction [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="cb600-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="cb600-124">Créez une tâche de transfert BITS en appelant la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="cb600-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="cb600-125">Obtenez un pointeur vers l’interface de rappel CNotifyInterface et appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour recevoir la notification des événements liés au travail.</span><span class="sxs-lookup"><span data-stu-id="cb600-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="cb600-126">Pour plus d’informations sur CNotifyInterface, consultez [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="cb600-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="cb600-127">Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour définir les types de notifications à recevoir.</span><span class="sxs-lookup"><span data-stu-id="cb600-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="cb600-128">Dans cet exemple, les indicateurs d' **\_ \_ \_ erreur** du **\_ travail de notification \_ \_ BG** et du travail de notification BG sont définis.</span><span class="sxs-lookup"><span data-stu-id="cb600-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="cb600-129">Obtient un pointeur vers l’interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="cb600-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="cb600-130">Utilisez le pointeur **IBackgroundCopyJob2** pour définir des propriétés supplémentaires sur le travail.</span><span class="sxs-lookup"><span data-stu-id="cb600-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="cb600-131">Ce programme utilise la méthode [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) pour définir les informations d’identification de la tâche de transfert bits.</span><span class="sxs-lookup"><span data-stu-id="cb600-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="cb600-132">Ajoutez des fichiers à la tâche de transfert BITS en appelant [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="cb600-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="cb600-133">Dans cet exemple, la méthode **méthode ibackgroundcopyjob :: AddFile** utilise les variables RemoteFile et fichier_local qui ont été passées à la fonction ServerAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cb600-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="cb600-134">Une fois le fichier ajouté, appelez [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour reprendre la tâche.</span><span class="sxs-lookup"><span data-stu-id="cb600-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="cb600-135">Configurez une boucle while pour attendre le message Quit de l’interface de rappel pendant le transfert du travail.</span><span class="sxs-lookup"><span data-stu-id="cb600-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="cb600-136">Cette étape est nécessaire uniquement si le cloisonnement COM est un cloisonnement à thread unique.</span><span class="sxs-lookup"><span data-stu-id="cb600-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="cb600-137">Pour plus d’informations, consultez [cloisonnements à thread unique](../com/single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="cb600-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

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

    

    <span data-ttu-id="cb600-138">La boucle ci-dessus utilise la fonction [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) pour récupérer le nombre de millisecondes qui se sont écoulées depuis le début du transfert du travail.</span><span class="sxs-lookup"><span data-stu-id="cb600-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="cb600-139">Une fois la tâche de transfert BITS terminée, supprimez la tâche de la file d’attente en appelant [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="cb600-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="cb600-140">L’exemple de code suivant spécifie les informations d’identification d’authentification du serveur pour une tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="cb600-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cb600-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb600-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb600-142">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="cb600-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="cb600-143">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="cb600-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="cb600-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="cb600-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="cb600-145">Exemple : classes communes</span><span class="sxs-lookup"><span data-stu-id="cb600-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 
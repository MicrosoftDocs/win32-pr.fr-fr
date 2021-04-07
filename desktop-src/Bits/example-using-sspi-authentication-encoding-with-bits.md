---
title: Exemple utilisant l’encodage d’authentification SSPI avec BITS
description: Vous pouvez utiliser l’authentification SSPI (Security Support Provider Interface) et les méthodes Service de transfert intelligent en arrière-plan (BITS) pour obtenir les informations d’identification d’un utilisateur, encoder les informations d’identification et définir les informations d’identification encodées pour une tâche de transfert BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730164"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="90128-103">Exemple : utilisation de l’encodage d’authentification SSPI avec BITS</span><span class="sxs-lookup"><span data-stu-id="90128-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="90128-104">Vous pouvez utiliser l’authentification SSPI (Security Support Provider Interface) et les méthodes Service de transfert intelligent en arrière-plan (BITS) pour obtenir les informations d’identification d’un utilisateur, encoder les informations d’identification et définir les informations d’identification encodées pour une tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="90128-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="90128-105">L’encodage est nécessaire pour convertir la structure des informations d’identification en chaînes qui peuvent être passées à une tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="90128-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="90128-106">Pour plus d’informations sur l’authentification et les méthodes SSPI, consultez [SSPI](../secauthn/sspi.md).</span><span class="sxs-lookup"><span data-stu-id="90128-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="90128-107">La procédure suivante vous invite à entrer les informations d’identification de l’utilisateur à l’aide du package de sécurité Negotiate.</span><span class="sxs-lookup"><span data-stu-id="90128-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="90128-108">Le programme crée une structure d’identité d’authentification et remplit la structure avec les chaînes encodées qui représentent le nom d’utilisateur, le domaine et le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="90128-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="90128-109">Ensuite, le programme crée une tâche de téléchargement BITS et définit le nom d’utilisateur et le mot de passe codés en tant qu’informations d’identification pour le travail.</span><span class="sxs-lookup"><span data-stu-id="90128-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="90128-110">Le programme libère la structure d’identité d’authentification une fois qu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="90128-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="90128-111">Cet exemple utilise l’en-tête et l’implémentation définis dans [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="90128-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="90128-112">**Pour utiliser l’encodage d’authentification SSPI avec les tâches de transfert BITS**</span><span class="sxs-lookup"><span data-stu-id="90128-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="90128-113">Initialisez les paramètres COM en appelant la fonction CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="90128-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="90128-114">Pour plus d’informations sur la fonction CCoInitializer, consultez [exemple : classes communes](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="90128-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="90128-115">Obtient des pointeurs pour les interfaces [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)et [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="90128-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="90128-116">Cet exemple utilise la [classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) pour gérer les pointeurs d’interface com.</span><span class="sxs-lookup"><span data-stu-id="90128-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="90128-117">Créez une structure [CREDUI \_ info](/windows/win32/api/wincred/ns-wincred-credui_infoa) qui contient des informations sur la personnalisation de l’apparence de la boîte de dialogue pour la [fonction SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="90128-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="90128-118">Ensuite, demander les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="90128-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="90128-119">Pour plus d’informations, consultez la [fonction SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="90128-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="90128-120">Encodez la structure des informations d’identification en tant que chaînes qui peuvent être passées à une tâche de transfert BITS à l’aide de la fonction [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .</span><span class="sxs-lookup"><span data-stu-id="90128-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="90128-121">Préparez une [**structure \_ \_ d’informations d’identification d’authentification BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="90128-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="90128-122">Initialisez la sécurité des processus COM en appelant [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="90128-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="90128-123">BITS requiert au moins le niveau d’emprunt d’identité d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="90128-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="90128-124">BITS échoue avec **E \_ ACCESSDENIED** si le niveau d’emprunt d’identité correct n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="90128-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="90128-125">Obtenez le localisateur initial pour BITS en appelant la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="90128-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="90128-126">Créez une tâche de transfert BITS en appelant la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="90128-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="90128-127">Récupérez l’identificateur de l’interface [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) et appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="90128-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="90128-128">Renseignez la structure des [**\_ \_ informations d’identification d’authentification BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) avec les chaînes de nom d’utilisateur et de mot de passe encodées, puis définissez le schéma d’authentification sur Negotiate (**BG \_ auth \_ Scheme \_ Negotiate**).</span><span class="sxs-lookup"><span data-stu-id="90128-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="90128-129">Utilisez le pointeur [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pour effectuer des demandes à bits.</span><span class="sxs-lookup"><span data-stu-id="90128-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="90128-130">Ce programme utilise la méthode [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) pour définir les informations d’identification de la tâche de transfert bits.</span><span class="sxs-lookup"><span data-stu-id="90128-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="90128-131">Ajoutez des fichiers, modifiez les propriétés ou reprenez la tâche de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="90128-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="90128-132">Une fois la tâche de transfert BITS terminée, supprimez la tâche de la file d’attente en appelant [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="90128-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="90128-133">Enfin, libérez la structure d’identité d’authentification en appelant la fonction [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .</span><span class="sxs-lookup"><span data-stu-id="90128-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="90128-134">L’exemple de code suivant montre comment utiliser l’encodage d’authentification SSPI avec les tâches de transfert BITS.</span><span class="sxs-lookup"><span data-stu-id="90128-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

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
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a><span data-ttu-id="90128-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90128-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90128-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="90128-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="90128-137">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="90128-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="90128-138">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="90128-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="90128-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="90128-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="90128-140">Exemple : classes communes</span><span class="sxs-lookup"><span data-stu-id="90128-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 
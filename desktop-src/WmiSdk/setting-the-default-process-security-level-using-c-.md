---
description: Lorsqu’une application cliente se connecte à Windows Management Instrumentation (WMI) pour la première fois, elle doit définir le niveau de sécurité de processus par défaut à l’aide d’un appel à CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Définition du niveau de sécurité de processus par défaut à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530135"
---
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="fb19e-103">Définition du niveau de sécurité de processus par défaut à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="fb19e-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="fb19e-104">Lorsqu’une application cliente se connecte à Windows Management Instrumentation (WMI) pour la première fois, elle doit définir le niveau de sécurité de processus par défaut à l’aide d’un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="fb19e-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="fb19e-105">COM utilise les informations de l’appel pour déterminer la sécurité qu’un autre processus doit avoir pour accéder au processus de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="fb19e-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="fb19e-106">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="fb19e-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="fb19e-107">Modification des informations d’authentification par défaut à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="fb19e-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="fb19e-108">Modification des niveaux d’emprunt d’identité par défaut à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="fb19e-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="fb19e-109">Pour la plupart des applications clientes, les arguments indiqués dans l’exemple suivant définissent la sécurité par défaut pour WMI.</span><span class="sxs-lookup"><span data-stu-id="fb19e-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



<span data-ttu-id="fb19e-110">Le code requiert les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="fb19e-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="fb19e-111">La définition du niveau d’authentification à la **\_ \_ \_ \_ valeur par défaut** du niveau d’authentification RPC C permet à DCOM de négocier le niveau d’authentification pour répondre aux demandes de sécurité de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="fb19e-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="fb19e-112">Pour plus d’informations, consultez [modification des informations d’authentification par défaut à l’aide de c++](#changing-the-default-authentication-credentials-using-c) et [modification des paramètres d’emprunt d’identité par défaut à l’aide de c++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="fb19e-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="fb19e-113">Modification des informations d’authentification par défaut à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="fb19e-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="fb19e-114">Les informations d’identification d’authentification par défaut fonctionnent dans la plupart des cas, mais vous devrez peut-être utiliser des informations d’identification d’authentification différentes dans différentes situations.</span><span class="sxs-lookup"><span data-stu-id="fb19e-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="fb19e-115">Par exemple, vous souhaiterez peut-être ajouter un chiffrement aux procédures d’authentification.</span><span class="sxs-lookup"><span data-stu-id="fb19e-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="fb19e-116">Le tableau suivant répertorie et décrit les différents niveaux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="fb19e-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="fb19e-117">Niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="fb19e-117">Authentication level</span></span>                 | <span data-ttu-id="fb19e-118">Description</span><span class="sxs-lookup"><span data-stu-id="fb19e-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb19e-119">\_ \_ \_ valeur par défaut du niveau d’authentification RPC C \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="fb19e-120">Authentification de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb19e-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="fb19e-121">RPC \_ C \_ Authn \_ niveau \_ aucun</span><span class="sxs-lookup"><span data-stu-id="fb19e-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="fb19e-122">Aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="fb19e-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="fb19e-123">\_ \_ \_ connexion au niveau AUTHn C RPC \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="fb19e-124">Authentification uniquement lorsque le client crée une relation avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="fb19e-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="fb19e-125">\_ \_ \_ appel au niveau d’authentification RPC C \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="fb19e-126">Authentification chaque fois que le serveur reçoit un RPC.</span><span class="sxs-lookup"><span data-stu-id="fb19e-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="fb19e-127">protocole d’authentification de l' \_ authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="fb19e-128">Authentification chaque fois que le serveur reçoit des données d’un client.</span><span class="sxs-lookup"><span data-stu-id="fb19e-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="fb19e-129">\_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="fb19e-130">Authentification pour laquelle aucune donnée du paquet n’a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="fb19e-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="fb19e-131">\_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="fb19e-132">Comprend tous les niveaux d’authentification précédents et chiffre la valeur de chaque appel RPC.</span><span class="sxs-lookup"><span data-stu-id="fb19e-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="fb19e-133">Vous pouvez spécifier les informations d’authentification par défaut pour plusieurs utilisateurs à l’aide d’une seule structure de **\_ \_ liste d’authentification** dans le paramètre *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="fb19e-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="fb19e-134">L’exemple de code suivant montre comment modifier les informations d’identification d’authentification.</span><span class="sxs-lookup"><span data-stu-id="fb19e-134">The following code example shows how to change the authentication credentials.</span></span>


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="fb19e-135">Modification des niveaux d’emprunt d’identité par défaut à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="fb19e-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="fb19e-136">COM fournit des niveaux de sécurité par défaut lus à partir du Registre système.</span><span class="sxs-lookup"><span data-stu-id="fb19e-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="fb19e-137">Toutefois, à moins d’être spécifiquement modifiées, les paramètres du registre définissent le niveau d’emprunt d’identité trop faible pour fonctionner avec WMI.</span><span class="sxs-lookup"><span data-stu-id="fb19e-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="fb19e-138">En règle générale, le niveau d’emprunt d’identité par défaut est **RPC \_ c \_ IMP \_ Level \_ identifier**, mais WMI a besoin d’au moins le niveau d’identification **RPC \_ c \_ IMP \_ \_** pour fonctionner avec la plupart des fournisseurs, et vous pouvez rencontrer une situation dans laquelle vous devez définir un niveau d’emprunt d’identité plus élevé.</span><span class="sxs-lookup"><span data-stu-id="fb19e-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="fb19e-139">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fb19e-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="fb19e-140">Le tableau suivant répertorie les différents niveaux d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="fb19e-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="fb19e-141">Level</span><span class="sxs-lookup"><span data-stu-id="fb19e-141">Level</span></span>                           | <span data-ttu-id="fb19e-142">Description</span><span class="sxs-lookup"><span data-stu-id="fb19e-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb19e-143">\_ \_ \_ valeur par défaut du niveau d’IMP RPC C \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="fb19e-144">Le système d’exploitation choisit le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="fb19e-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="fb19e-145">\_niveau d' \_ IMP \_ \_ anonyme du C RPC</span><span class="sxs-lookup"><span data-stu-id="fb19e-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="fb19e-146">Le serveur peut emprunter l’identité du client, mais le jeton d’emprunt d’identité ne peut pas être utilisé pour quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="fb19e-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="fb19e-147">\_identification du \_ niveau d’IMP RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="fb19e-148">Le serveur peut obtenir l’identité du client et emprunter l’identité du client pour la vérification de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="fb19e-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="fb19e-149">\_emprunt d' \_ identité du niveau d’IMP RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="fb19e-150">Le serveur peut emprunter l’identité du client sur une limite d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fb19e-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="fb19e-151">\_délégué de \_ \_ niveau IMP RPC C \_</span><span class="sxs-lookup"><span data-stu-id="fb19e-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="fb19e-152">Le serveur peut emprunter l’identité du client à travers plusieurs limites et peut effectuer des appels pour le compte du client.</span><span class="sxs-lookup"><span data-stu-id="fb19e-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 

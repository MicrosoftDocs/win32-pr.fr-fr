---
description: Une vérification d’accès détermine si un descripteur de sécurité accorde un ensemble spécifié de droits d’accès au client ou au thread identifié par un jeton d’accès.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Exécution des vérifications d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521073"
---
# <a name="performing-access-checks"></a><span data-ttu-id="95a6d-103">Exécution des vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="95a6d-103">Performing Access Checks</span></span>

<span data-ttu-id="95a6d-104">Une vérification d’accès détermine si un descripteur de sécurité accorde un ensemble spécifié de droits d’accès au client ou au thread identifié par un jeton d’accès.</span><span class="sxs-lookup"><span data-stu-id="95a6d-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="95a6d-105">Vous pouvez appeler la fonction de sécurité [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) à partir des applications clientes WMI ou des fournisseurs écrits en C++ ou en C#.</span><span class="sxs-lookup"><span data-stu-id="95a6d-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="95a6d-106">Les scripts et les applications de Visual Basic ne peuvent pas effectuer des vérifications d’accès à l’aide de la méthode décrite ici.</span><span class="sxs-lookup"><span data-stu-id="95a6d-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="95a6d-107">Les applications clientes doivent effectuer une vérification d’accès pour déterminer l’identité du rappel lors du retour des résultats au récepteur fourni par l’appel asynchrone du client.</span><span class="sxs-lookup"><span data-stu-id="95a6d-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="95a6d-108">Lorsque les fournisseurs ne peuvent pas emprunter l’identité de l’application cliente ou du script qui demande des données, ils doivent effectuer des vérifications d’accès pour les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="95a6d-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="95a6d-109">Lors de l’accès à des ressources qui ne sont pas protégées par des listes de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="95a6d-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="95a6d-110">Lorsque le client s’est connecté au niveau **RPC, \_ \_ \_ Identifiez** le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="95a6d-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="95a6d-111">Les applications C++ et C# peuvent contrôler si les contrôles d’accès sont exécutés par un processus distinct.</span><span class="sxs-lookup"><span data-stu-id="95a6d-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="95a6d-112">Les scripts et les applications de Visual Basic peuvent lire ou modifier une clé de Registre pour s’assurer que WMI effectue des vérifications d’accès.</span><span class="sxs-lookup"><span data-stu-id="95a6d-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="95a6d-113">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="95a6d-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="95a6d-114">L’exemple de code de cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="95a6d-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



<span data-ttu-id="95a6d-115">L’exemple de code suivant montre comment vérifier que le jeton de sécurité d’un thread d’application cliente contient des autorisations appropriées à un descripteur de sécurité spécifié.</span><span class="sxs-lookup"><span data-stu-id="95a6d-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="95a6d-116">La fonction prend la chaîne « utilisateur de domaine \\ » et retourne le SID.</span><span class="sxs-lookup"><span data-stu-id="95a6d-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="95a6d-117">Si l’appel échoue, la fonction retourne la **valeur null**, sinon l’appelant doit libérer le pointeur retourné.</span><span class="sxs-lookup"><span data-stu-id="95a6d-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="95a6d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95a6d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95a6d-119">Choix de l’inscription correcte</span><span class="sxs-lookup"><span data-stu-id="95a6d-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="95a6d-120">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="95a6d-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="95a6d-121">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="95a6d-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="95a6d-122">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="95a6d-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

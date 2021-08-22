---
description: Une vérification d’accès détermine si un descripteur de sécurité accorde un ensemble spécifié de droits d’accès au client ou au thread identifié par un jeton d’accès.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Exécution des vérifications d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e06f2bccab886b38b53ecc3592371555b8c93a0ed12cdad0a4f039b62d62752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050507"
---
# <a name="performing-access-checks"></a>Exécution des vérifications d’accès

Une vérification d’accès détermine si un descripteur de sécurité accorde un ensemble spécifié de droits d’accès au client ou au thread identifié par un jeton d’accès. Vous pouvez appeler la fonction de sécurité [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) à partir des applications clientes WMI ou des fournisseurs écrits en C++ ou en C#. les Scripts et les applications de Visual Basic ne peuvent pas effectuer des vérifications d’accès à l’aide de la méthode décrite ici.

Les applications clientes doivent effectuer une vérification d’accès pour déterminer l’identité du rappel lors du retour des résultats au récepteur fourni par l’appel asynchrone du client.

Lorsque les fournisseurs ne peuvent pas emprunter l’identité de l’application cliente ou du script qui demande des données, ils doivent effectuer des vérifications d’accès pour les situations suivantes :

-   Lors de l’accès à des ressources qui ne sont pas protégées par des listes de contrôle d’accès (ACL).
-   Lorsque le client s’est connecté au niveau **RPC, \_ \_ \_ Identifiez** le niveau d’emprunt d’identité.

> [!Note]  
> Les applications C++ et C# peuvent contrôler si les contrôles d’accès sont exécutés par un processus distinct. les Scripts et les applications de Visual Basic peuvent lire ou modifier une clé de registre pour s’assurer que WMI effectue des vérifications d’accès. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

 

L’exemple de code de cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.


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



L’exemple de code suivant montre comment vérifier que le jeton de sécurité d’un thread d’application cliente contient des autorisations appropriées à un descripteur de sécurité spécifié. La fonction prend la chaîne « utilisateur de domaine \\ » et retourne le SID. Si l’appel échoue, la fonction retourne la **valeur null**, sinon l’appelant doit libérer le pointeur retourné.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Choix de l’inscription correcte](choosing-correct-registration.md)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

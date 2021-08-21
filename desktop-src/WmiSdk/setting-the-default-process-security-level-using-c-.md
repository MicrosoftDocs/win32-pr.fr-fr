---
description: lorsqu’une application cliente se connecte à Windows Management Instrumentation (WMI) pour la première fois, elle doit définir le niveau de sécurité de processus par défaut à l’aide d’un appel à CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Définition du niveau de sécurité de processus par défaut à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050287"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Définition du niveau de sécurité de processus par défaut à l’aide de C++

lorsqu’une application cliente se connecte à Windows Management Instrumentation (WMI) pour la première fois, elle doit définir le niveau de sécurité de processus par défaut à l’aide d’un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM utilise les informations de l’appel pour déterminer la sécurité qu’un autre processus doit avoir pour accéder au processus de l’application cliente.

Les sections suivantes sont présentées dans cette rubrique :

-   [Modification des informations d’authentification par défaut à l’aide de C++](#changing-the-default-authentication-credentials-using-c)
-   [Modification des niveaux d’emprunt d’identité par défaut à l’aide de C++](#changing-the-default-impersonation-levels-using-c)

Pour la plupart des applications clientes, les arguments indiqués dans l’exemple suivant définissent la sécurité par défaut pour WMI.


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



Le code requiert les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



La définition du niveau d’authentification à la **\_ \_ \_ \_ valeur par défaut** du niveau d’authentification RPC C permet à DCOM de négocier le niveau d’authentification pour répondre aux demandes de sécurité de l’ordinateur cible. pour plus d’informations, consultez [modification des informations d’authentification par défaut à l’aide de c++](#changing-the-default-authentication-credentials-using-c) et [modification de l’emprunt d’identité par défaut Paramètres à l’aide de c++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Modification des informations d’authentification par défaut à l’aide de C++

Les informations d’identification d’authentification par défaut fonctionnent dans la plupart des cas, mais vous devrez peut-être utiliser des informations d’identification d’authentification différentes dans différentes situations. Par exemple, vous souhaiterez peut-être ajouter un chiffrement aux procédures d’authentification.

Le tableau suivant répertorie et décrit les différents niveaux d’authentification.



| Niveau d’authentification                 | Description                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ valeur par défaut du niveau d’authentification RPC C \_        | Authentification de sécurité par défaut.                                                      |
| RPC \_ C \_ Authn \_ niveau \_ aucun           | Aucune authentification.                                                                    |
| \_ \_ \_ connexion au niveau AUTHn C RPC \_        | Authentification uniquement lorsque le client crée une relation avec le serveur.           |
| \_ \_ \_ appel au niveau d’authentification RPC C \_           | Authentification chaque fois que le serveur reçoit un RPC.                                  |
| protocole d’authentification de l' \_ authentification RPC C \_ \_ \_            | Authentification chaque fois que le serveur reçoit des données d’un client.                      |
| \_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_ | Authentification pour laquelle aucune donnée du paquet n’a été modifiée.                        |
| \_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_   | Comprend tous les niveaux d’authentification précédents et chiffre la valeur de chaque appel RPC. |



 

Vous pouvez spécifier les informations d’authentification par défaut pour plusieurs utilisateurs à l’aide d’une seule structure de **\_ \_ liste d’authentification** dans le paramètre *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

L’exemple de code suivant montre comment modifier les informations d’identification d’authentification.


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



## <a name="changing-the-default-impersonation-levels-using-c"></a>Modification des niveaux d’emprunt d’identité par défaut à l’aide de C++

COM fournit des niveaux de sécurité par défaut lus à partir du Registre système. Toutefois, à moins d’être spécifiquement modifiées, les paramètres du registre définissent le niveau d’emprunt d’identité trop faible pour fonctionner avec WMI. En règle générale, le niveau d’emprunt d’identité par défaut est **RPC \_ c \_ IMP \_ Level \_ identifier**, mais WMI a besoin d’au moins le niveau d’identification **RPC \_ c \_ IMP \_ \_** pour fonctionner avec la plupart des fournisseurs, et vous pouvez rencontrer une situation dans laquelle vous devez définir un niveau d’emprunt d’identité plus élevé. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md). Le tableau suivant répertorie les différents niveaux d’emprunt d’identité.



| Niveau                           | Description                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ valeur par défaut du niveau d’IMP RPC C \_     | Le système d’exploitation choisit le niveau d’emprunt d’identité.                                                      |
| \_niveau d' \_ IMP \_ \_ anonyme du C RPC   | Le serveur peut emprunter l’identité du client, mais le jeton d’emprunt d’identité ne peut pas être utilisé pour quoi que ce soit.               |
| \_identification du \_ niveau d’IMP RPC C \_ \_    | Le serveur peut obtenir l’identité du client et emprunter l’identité du client pour la vérification de la liste de contrôle d’accès.                 |
| \_emprunt d' \_ identité du niveau d’IMP RPC C \_ \_ | Le serveur peut emprunter l’identité du client sur une limite d’ordinateur.                                           |
| \_délégué de \_ \_ niveau IMP RPC C \_    | Le serveur peut emprunter l’identité du client à travers plusieurs limites et peut effectuer des appels pour le compte du client. |



 

 

 

---
description: Les applications clientes spéciales peuvent appeler des opérations privilégiées.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Exécution d’opérations privilégiées à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318942"
---
# <a name="executing-privileged-operations-using-c"></a>Exécution d’opérations privilégiées à l’aide de C++

Les applications clientes spéciales peuvent appeler des opérations privilégiées. Par exemple, une application peut permettre à un gestionnaire de redémarrer un ordinateur Office qui ne répond pas. À l’aide de Windows Management Instrumentation (WMI), vous pouvez exécuter une opération privilégiée en appelant le fournisseur WMI pour l’opération privilégiée.

La procédure suivante décrit comment appeler un fournisseur pour une opération privilégiée.

**Pour appeler un fournisseur pour une opération privilégiée**

1.  Obtenez des autorisations pour que le processus client exécute l’opération privilégiée.

    En règle générale, un administrateur définit les autorisations à l’aide des outils d’administration système, avant d’exécuter le processus.

2.  Obtenez l’autorisation pour le processus du fournisseur afin d’activer l’opération privilégiée.

    En règle générale, vous pouvez définir des autorisations de fournisseur avec un appel à la fonction [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .

3.  Obtenez l’autorisation pour le processus client pour activer l’opération privilégiée.

    Cette étape est nécessaire uniquement si le fournisseur est local pour le client. Si le client et le fournisseur existent sur le même ordinateur, le client doit activer spécifiquement l’opération privilégiée à l’aide de l’une des techniques suivantes :

    -   Si le client possède le processus, le client peut utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour ajuster le jeton de processus avant d’appeler WMI. Dans ce cas, vous n’avez pas besoin de coder davantage.
    -   Si le client ne peut pas accéder au jeton client, le client peut utiliser la procédure suivante pour créer un jeton de thread et utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur ce jeton.

La procédure suivante décrit comment créer un jeton de thread et utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur ce jeton.

**Pour créer un jeton de thread et utiliser AdjustTokenPrivileges sur ce jeton**

1.  Créez une copie du jeton de processus en appelant [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).
2.  Récupérez le jeton de thread nouvellement créé en appelant [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).
3.  Activez l’opération privilégiée avec un appel à [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur le nouveau jeton.
4.  Obtient un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).
5.  Voilez le pointeur sur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) avec un appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
6.  Répétez les étapes 1 à 5 lors de chaque appel à WMI.

    > [!Note]  
    > Vous devez répéter les étapes, car COM met en cache les jetons de manière incorrecte.

     

L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.


```C++
#include <wbemidl.h>
```



L’exemple de code suivant montre comment activer des privilèges sur un ordinateur local.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 

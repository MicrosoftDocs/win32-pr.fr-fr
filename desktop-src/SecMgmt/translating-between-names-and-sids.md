---
description: L’autorité de sécurité locale (LSA, Local Security Authority) fournit des fonctions pour effectuer la conversion entre les noms d’utilisateurs, de groupes et de groupes locaux, ainsi que les valeurs d’identificateur de sécurité (SID) correspondantes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Conversion entre les noms et les sid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f67bd95e41a9813522d635e737f4fc528a61aebceeab205a2d40e1f44d7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004807"
---
# <a name="translating-between-names-and-sids"></a>Conversion entre les noms et les sid

L' [*autorité de sécurité locale (LSA, Local Security Authority*](/windows/desktop/SecGloss/l-gly) ) fournit des fonctions pour effectuer la conversion entre les noms d’utilisateurs, de groupes et de groupes locaux, ainsi que les valeurs d' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) correspondantes. Pour localiser les noms de compte, appelez la fonction [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) . Cette fonction retourne le SID sous la forme d’une paire d’index RID/domaine. Pour obtenir le SID en tant qu’élément unique, appelez la fonction [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) . Pour rechercher des SID, appelez [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Ces fonctions peuvent traduire les informations de nom et de SID de n’importe quel domaine approuvé par le système local.

Avant de pouvoir passer d’un nom de compte à un autre, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) local, comme le montre l' [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).

L’exemple suivant recherche le SID d’un compte, en fonction du nom du compte.


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



Dans l’exemple précédent, la fonction **InitLsaString** convertit une chaîne Unicode en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Ces fonctions de traduction sont principalement fournies pour une utilisation par les éditeurs d’autorisations pour afficher les informations de [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL). Un éditeur d’autorisations doit toujours appeler ces fonctions à l’aide de l’objet de [**stratégie**](policy-object.md) pour le système où se trouve le nom ou le SID de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) . Cela permet de garantir que l’ensemble approprié de domaines approuvés est référencé au cours de la traduction.

 

Windows Access Control fournit également des fonctions qui effectuent des traductions entre les SID et les noms de comptes : [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) et [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). si votre application doit rechercher un nom de compte ou un SID et n’utilise pas de fonctionnalité de stratégie lsa supplémentaire, utilisez les fonctions Windows Access Control à la place des fonctions de stratégie lsa. Pour plus d’informations sur ces fonctions, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

 

 

---
description: Le LSA fournit plusieurs fonctions que les applications peuvent appeler pour énumérer ou définir des privilèges pour les comptes d’utilisateurs, de groupes et de groupes locaux.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Gestion des autorisations de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5424d43424b067bc4771bd687c287e05e195f3e807a2db64bebaed4ece049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894069"
---
# <a name="managing-account-permissions"></a>Gestion des autorisations de compte

Le LSA fournit plusieurs fonctions que les applications peuvent appeler pour énumérer ou définir [*des privilèges*](/windows/desktop/SecGloss/p-gly) pour les comptes d’utilisateurs, de groupes et de groupes locaux.

Avant de pouvoir gérer les informations de compte, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) locale, comme indiqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md). En outre, pour énumérer ou modifier des autorisations pour un compte, vous devez disposer de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) de ce compte. Votre application peut localiser un SID en fonction du nom du compte, comme décrit dans [traduction entre les noms et les SID](translating-between-names-and-sids.md).

Pour accéder à tous les comptes qui ont une autorisation particulière, appelez [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Cette fonction remplit un tableau avec les SID de tous les comptes qui disposent de l’autorisation spécifiée.

Une fois que vous avez obtenu le SID d’un compte, vous pouvez modifier ses autorisations. Appelez [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) pour ajouter des autorisations au compte. Si le compte spécifié n’existe pas, **LsaAddAccountRights** le crée. Pour supprimer des autorisations d’un compte, appelez [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Si vous supprimez toutes les autorisations d’un compte, **LsaRemoveAccountRights** supprime également le compte.

Votre application peut vérifier les autorisations actuellement affectées à un compte en appelant [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Cette fonction remplit un tableau de structures [**de \_ \_ chaînes Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Chaque structure contient le nom d’un privilège détenu par le compte spécifié.

L’exemple suivant ajoute l’autorisation SeServiceLogonRight à un compte. Dans cet exemple, la variable AccountSID spécifie le SID du compte. Pour plus d’informations sur la recherche d’un SID de compte, consultez [conversion entre les noms et les SID](translating-between-names-and-sids.md).


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



Dans l’exemple précédent, la fonction InitLsaString convertit une chaîne [*Unicode*](/windows/desktop/SecGloss/u-gly) en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).

 

 

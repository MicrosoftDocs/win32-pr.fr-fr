---
description: La stratégie LSA fournit deux fonctions que vous pouvez utiliser pour définir et récupérer des données privées.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Stockage des données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009020"
---
# <a name="storing-private-data"></a>Stockage des données privées

La stratégie LSA fournit deux fonctions que vous pouvez utiliser pour définir et récupérer des données privées. Ces données sont stockées sous la forme d’une chaîne chiffrée dans le registre. Par exemple, vous pouvez utiliser ces fonctions pour stocker des mots de passe de compte de serveur et d’autres informations sensibles.

Appelez la fonction [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) pour stocker et chiffrer les données privées. Comme décrit dans [objet de données privées](private-data-object.md), les objets de données privés incluent trois types spécialisés : local, global et machine. Pour créer un objet spécialisé, ajoutez un préfixe au nom de clé passé à **LsaStorePrivateData**: « L $ » pour les objets locaux, « G $ » pour les objets globaux et « M $ » pour les objets ordinateur. Si vous ne créez pas l’un de ces types spécialisés, vous n’avez pas besoin de spécifier un préfixe de nom de clé.

Pour récupérer et décoder des données privées précédemment stockées, appelez [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Notez que vous ne pouvez pas récupérer les objets de données privées de l’ordinateur ; les objets ordinateur ne peuvent être récupérés que par le système d’exploitation.

Avant de pouvoir stocker ou récupérer des données privées, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) local, comme indiqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).

L’exemple suivant crée un objet de données privées locales. Notez que la fonction InitLsaString convertit une chaîne [*Unicode*](/windows/desktop/SecGloss/u-gly) en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> Les données stockées par la fonction [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) ne sont pas entièrement protégées. Toutefois, la clé a une liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) qui permet uniquement au créateur et aux administrateurs de lire les données.

 

 

 

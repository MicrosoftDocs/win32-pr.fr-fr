---
description: La plupart des fonctions de stratégie LSA requièrent un handle vers l’objet de stratégie que le système doit interroger ou modifier. Pour obtenir un handle d’objet de stratégie, appelez LsaOpenPolicy et spécifiez le nom du système auquel vous souhaitez accéder et le jeu d’autorisations d’accès requis.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Ouverture d’un handle d’objet de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521973"
---
# <a name="opening-a-policy-object-handle"></a>Ouverture d’un handle d’objet de stratégie

La plupart des fonctions de stratégie LSA requièrent un handle vers l’objet de [**stratégie**](policy-object.md) que le système doit interroger ou modifier. Pour obtenir un handle d’objet de **stratégie** , appelez [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) et spécifiez le nom du système auquel vous souhaitez accéder et le jeu d’autorisations d’accès requis.

Les autorisations d’accès requises pour votre application dépendent des actions qu’elle effectue. Pour plus d’informations sur les autorisations requises pour chaque fonction, consultez la description de cette fonction dans [fonctions de stratégie LSA](management-functions.md).

Si l’appel à [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) réussit, il retourne un handle vers l’objet de [**stratégie**](policy-object.md) pour le système spécifié. Votre application passe ensuite ce handle dans les appels de fonction de stratégie LSA suivants. Lorsque votre application n’a plus besoin du descripteur, elle doit appeler [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) pour la libérer.

L’exemple suivant montre comment ouvrir un handle d’objet de [**stratégie**](policy-object.md) .


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



Dans l’exemple précédent, l’application a demandé \_ \_ [*des privilèges*](/windows/desktop/SecGloss/p-gly)d’accès à la stratégie. Pour plus d’informations sur les autorisations que votre application doit demander lors de l’appel de [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consultez les descriptions des fonctions auxquelles votre application passera le descripteur d’objet de [**stratégie**](policy-object.md) .

Pour ouvrir un handle vers l’objet de [**stratégie**](policy-object.md) d’un domaine approuvé, appelez [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (pour créer une relation d’approbation avec un domaine) ou appelez [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (pour accéder à un domaine approuvé existant). Ces deux fonctions définissent un pointeur vers [**un \_ handle LSA**](lsa-handle.md), que vous pouvez ensuite spécifier dans les appels de fonction de stratégie LSA ultérieurs. Comme avec [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), votre application doit appeler [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quand elle n’a plus besoin du descripteur de l’objet de **stratégie** du domaine approuvé.

 

 

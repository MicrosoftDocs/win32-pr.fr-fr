---
description: Le LSA fournit des fonctions que les administrateurs peuvent utiliser pour interroger et définir des informations de stratégie globale pour l’ordinateur local et le domaine.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Gestion des informations de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521909"
---
# <a name="managing-policy-information"></a>Gestion des informations de stratégie

Le LSA fournit des fonctions que les administrateurs peuvent utiliser pour interroger et définir des informations de stratégie globale pour l’ordinateur local et le domaine.

Avant de pouvoir gérer les informations de stratégie, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) locale, comme indiqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md). Ce handle est requis par les fonctions qui gèrent les informations de stratégie.

Pour récupérer des informations sur la stratégie de sécurité locale, appelez [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy). Pour définir la stratégie de sécurité locale, appelez [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy). La description de l’énumération de la [**\_ \_ classe d’informations de stratégie**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) détaille les types d’informations de stratégie qui peuvent être interrogées ou définies.

L’exemple suivant montre comment obtenir les informations de domaine du compte d’un système, en fonction d’un handle de l’objet de [**stratégie**](policy-object.md) du système.


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 

---
description: La stratégie LSA fournit plusieurs fonctions que vous pouvez utiliser pour créer, énumérer et supprimer des domaines approuvés, ainsi que pour définir et récupérer des informations de domaine approuvé.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Gestion des informations de domaine approuvé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a945705efaedf56920ee2170deeab9da0d01802259a57aca5cda2fac9d531aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894089"
---
# <a name="managing-trusted-domain-information"></a>Gestion des informations de domaine approuvé

La stratégie LSA fournit plusieurs fonctions que vous pouvez utiliser pour créer, énumérer et supprimer des domaines approuvés, ainsi que pour définir et récupérer des informations de domaine approuvé.

Avant de pouvoir gérer les informations de domaine approuvé, votre application doit obtenir un handle vers un objet de [**stratégie**](policy-object.md) , comme expliqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).

Vous pouvez énumérer les domaines approuvés en appelant [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).

Pour récupérer les informations relatives à un domaine approuvé, appelez [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) ou [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname). Les deux fonctions retournent les mêmes informations ; Toutefois, **LsaQueryTrustedDomainInfo** identifie le domaine approuvé par SID et **LsaQueryTrustedDomainInfoByName** identifie le domaine approuvé par son nom.

Pour définir des informations pour un domaine approuvé, appelez [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) ou [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname). Comme avec les fonctions de requête, **LsaSetTrustedDomainInformation** identifie le domaine approuvé par SID, tandis que **LsaSetTrustedDomainInfoByName** identifie le domaine approuvé par son nom.

Votre application peut révoquer une relation d’approbation pour un domaine approuvé en appelant [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).

L’exemple suivant énumère les domaines approuvés pour le système local.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 




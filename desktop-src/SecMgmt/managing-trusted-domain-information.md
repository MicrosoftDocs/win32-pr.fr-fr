---
description: La stratégie LSA fournit plusieurs fonctions que vous pouvez utiliser pour créer, énumérer et supprimer des domaines approuvés, ainsi que pour définir et récupérer des informations de domaine approuvé.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Gestion des informations de domaine approuvé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209864"
---
# <a name="managing-trusted-domain-information"></a><span data-ttu-id="9d29d-103">Gestion des informations de domaine approuvé</span><span class="sxs-lookup"><span data-stu-id="9d29d-103">Managing Trusted Domain Information</span></span>

<span data-ttu-id="9d29d-104">La stratégie LSA fournit plusieurs fonctions que vous pouvez utiliser pour créer, énumérer et supprimer des domaines approuvés, ainsi que pour définir et récupérer des informations de domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="9d29d-104">LSA Policy provides several functions that you can use to create, enumerate, and delete trusted domains and to set and retrieve trusted domain information.</span></span>

<span data-ttu-id="9d29d-105">Avant de pouvoir gérer les informations de domaine approuvé, votre application doit obtenir un handle vers un objet de [**stratégie**](policy-object.md) , comme expliqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="9d29d-105">Before you can manage trusted domain information, your application must get a handle to a [**Policy**](policy-object.md) object, as explained in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="9d29d-106">Vous pouvez énumérer les domaines approuvés en appelant [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="9d29d-106">You can enumerate the trusted domains by calling [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span>

<span data-ttu-id="9d29d-107">Pour récupérer les informations relatives à un domaine approuvé, appelez [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) ou [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="9d29d-107">To retrieve information about a trusted domain, call either [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) or [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span></span> <span data-ttu-id="9d29d-108">Les deux fonctions retournent les mêmes informations ; Toutefois, **LsaQueryTrustedDomainInfo** identifie le domaine approuvé par SID et **LsaQueryTrustedDomainInfoByName** identifie le domaine approuvé par son nom.</span><span class="sxs-lookup"><span data-stu-id="9d29d-108">Both functions return the same information; however, **LsaQueryTrustedDomainInfo** identifies the trusted domain by SID, and **LsaQueryTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="9d29d-109">Pour définir des informations pour un domaine approuvé, appelez [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) ou [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="9d29d-109">To set information for a trusted domain, call either [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) or [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span></span> <span data-ttu-id="9d29d-110">Comme avec les fonctions de requête, **LsaSetTrustedDomainInformation** identifie le domaine approuvé par SID, tandis que **LsaSetTrustedDomainInfoByName** identifie le domaine approuvé par son nom.</span><span class="sxs-lookup"><span data-stu-id="9d29d-110">As with the query functions, **LsaSetTrustedDomainInformation** identifies the trusted domain by SID, while **LsaSetTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="9d29d-111">Votre application peut révoquer une relation d’approbation pour un domaine approuvé en appelant [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span><span class="sxs-lookup"><span data-stu-id="9d29d-111">Your application can revoke a trust relationship for a trusted domain by calling [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span></span>

<span data-ttu-id="9d29d-112">L’exemple suivant énumère les domaines approuvés pour le système local.</span><span class="sxs-lookup"><span data-stu-id="9d29d-112">The following example enumerates the trusted domains for the local system.</span></span>


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



 

 




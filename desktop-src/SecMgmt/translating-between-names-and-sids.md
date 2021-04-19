---
description: L’autorité de sécurité locale (LSA, Local Security Authority) fournit des fonctions pour effectuer la conversion entre les noms d’utilisateurs, de groupes et de groupes locaux, ainsi que les valeurs d’identificateur de sécurité (SID) correspondantes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Conversion entre les noms et les sid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532082"
---
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="ce7de-103">Conversion entre les noms et les sid</span><span class="sxs-lookup"><span data-stu-id="ce7de-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="ce7de-104">L' [*autorité de sécurité locale (LSA, Local Security Authority*](/windows/desktop/SecGloss/l-gly) ) fournit des fonctions pour effectuer la conversion entre les noms d’utilisateurs, de groupes et de groupes locaux, ainsi que les valeurs d' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) correspondantes.</span><span class="sxs-lookup"><span data-stu-id="ce7de-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="ce7de-105">Pour localiser les noms de compte, appelez la fonction [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) .</span><span class="sxs-lookup"><span data-stu-id="ce7de-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="ce7de-106">Cette fonction retourne le SID sous la forme d’une paire d’index RID/domaine.</span><span class="sxs-lookup"><span data-stu-id="ce7de-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="ce7de-107">Pour obtenir le SID en tant qu’élément unique, appelez la fonction [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) .</span><span class="sxs-lookup"><span data-stu-id="ce7de-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="ce7de-108">Pour rechercher des SID, appelez [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="ce7de-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="ce7de-109">Ces fonctions peuvent traduire les informations de nom et de SID de n’importe quel domaine approuvé par le système local.</span><span class="sxs-lookup"><span data-stu-id="ce7de-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="ce7de-110">Avant de pouvoir passer d’un nom de compte à un autre, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) local, comme le montre l' [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ce7de-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="ce7de-111">L’exemple suivant recherche le SID d’un compte, en fonction du nom du compte.</span><span class="sxs-lookup"><span data-stu-id="ce7de-111">The following example looks up the SID for an account, given the account name.</span></span>


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



<span data-ttu-id="ce7de-112">Dans l’exemple précédent, la fonction **InitLsaString** convertit une chaîne Unicode en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="ce7de-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="ce7de-113">Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="ce7de-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="ce7de-114">Ces fonctions de traduction sont principalement fournies pour une utilisation par les éditeurs d’autorisations pour afficher les informations de [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="ce7de-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="ce7de-115">Un éditeur d’autorisations doit toujours appeler ces fonctions à l’aide de l’objet de [**stratégie**](policy-object.md) pour le système où se trouve le nom ou le SID de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="ce7de-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="ce7de-116">Cela permet de garantir que l’ensemble approprié de domaines approuvés est référencé au cours de la traduction.</span><span class="sxs-lookup"><span data-stu-id="ce7de-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="ce7de-117">Windows Access Control fournit également des fonctions qui effectuent des traductions entre les SID et les noms de comptes : [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) et [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="ce7de-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="ce7de-118">Si votre application doit rechercher un nom de compte ou un SID et n’utilise pas de fonctionnalité de stratégie LSA supplémentaire, utilisez les fonctions de Access Control de Windows au lieu des fonctions de stratégie LSA.</span><span class="sxs-lookup"><span data-stu-id="ce7de-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="ce7de-119">Pour plus d’informations sur ces fonctions, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="ce7de-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 

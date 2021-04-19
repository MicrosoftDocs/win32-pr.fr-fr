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
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="3cbec-104">Ouverture d’un handle d’objet de stratégie</span><span class="sxs-lookup"><span data-stu-id="3cbec-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="3cbec-105">La plupart des fonctions de stratégie LSA requièrent un handle vers l’objet de [**stratégie**](policy-object.md) que le système doit interroger ou modifier.</span><span class="sxs-lookup"><span data-stu-id="3cbec-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="3cbec-106">Pour obtenir un handle d’objet de **stratégie** , appelez [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) et spécifiez le nom du système auquel vous souhaitez accéder et le jeu d’autorisations d’accès requis.</span><span class="sxs-lookup"><span data-stu-id="3cbec-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="3cbec-107">Les autorisations d’accès requises pour votre application dépendent des actions qu’elle effectue.</span><span class="sxs-lookup"><span data-stu-id="3cbec-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="3cbec-108">Pour plus d’informations sur les autorisations requises pour chaque fonction, consultez la description de cette fonction dans [fonctions de stratégie LSA](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="3cbec-109">Si l’appel à [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) réussit, il retourne un handle vers l’objet de [**stratégie**](policy-object.md) pour le système spécifié.</span><span class="sxs-lookup"><span data-stu-id="3cbec-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="3cbec-110">Votre application passe ensuite ce handle dans les appels de fonction de stratégie LSA suivants.</span><span class="sxs-lookup"><span data-stu-id="3cbec-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="3cbec-111">Lorsque votre application n’a plus besoin du descripteur, elle doit appeler [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) pour la libérer.</span><span class="sxs-lookup"><span data-stu-id="3cbec-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="3cbec-112">L’exemple suivant montre comment ouvrir un handle d’objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3cbec-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


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



<span data-ttu-id="3cbec-113">Dans l’exemple précédent, l’application a demandé \_ \_ [*des privilèges*](/windows/desktop/SecGloss/p-gly)d’accès à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3cbec-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="3cbec-114">Pour plus d’informations sur les autorisations que votre application doit demander lors de l’appel de [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consultez les descriptions des fonctions auxquelles votre application passera le descripteur d’objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3cbec-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="3cbec-115">Pour ouvrir un handle vers l’objet de [**stratégie**](policy-object.md) d’un domaine approuvé, appelez [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (pour créer une relation d’approbation avec un domaine) ou appelez [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (pour accéder à un domaine approuvé existant).</span><span class="sxs-lookup"><span data-stu-id="3cbec-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="3cbec-116">Ces deux fonctions définissent un pointeur vers [**un \_ handle LSA**](lsa-handle.md), que vous pouvez ensuite spécifier dans les appels de fonction de stratégie LSA ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="3cbec-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="3cbec-117">Comme avec [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), votre application doit appeler [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quand elle n’a plus besoin du descripteur de l’objet de **stratégie** du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="3cbec-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 

---
description: "Le type de données du handle de l' \\_ énumération LSA \\_ est utilisé par la fonction LSA qui énumère les objets trustedDomain : LsaEnumerateTrustedDomainsEx."
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538681"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="e413f-103">\_handle d’énumération LSA \_</span><span class="sxs-lookup"><span data-stu-id="e413f-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="e413f-104">Le type de données du handle de l' **\_ énumération \_ LSA** est utilisé par la fonction LSA qui énumère les objets [**trustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="e413f-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="e413f-105">Cette fonction est conçue afin que vous puissiez effectuer plusieurs appels pour énumérer tous les objets d’un type donné dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e413f-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="e413f-106">Lors de l’appel initial de la fonction d’énumération, vous transmettez un pointeur vers une variable de **\_ \_ handle d’énumération LSA** qui est initialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="e413f-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="e413f-107">La fonction met à jour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e413f-107">The function updates this value.</span></span> <span data-ttu-id="e413f-108">Si la fonction retourne une valeur qui indique qu’il y a plus d’objets à énumérer, appelez à nouveau la fonction et transmettez la valeur de **\_ \_ handle d’énumération LSA** mise à jour pour obtenir une énumération qui continue à partir du point où l’énumération précédente s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="e413f-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="e413f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e413f-109">Requirements</span></span>



| <span data-ttu-id="e413f-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e413f-110">Requirement</span></span> | <span data-ttu-id="e413f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e413f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e413f-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e413f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e413f-113">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e413f-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e413f-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e413f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e413f-115">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e413f-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e413f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e413f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e413f-117"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e413f-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e413f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e413f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e413f-119">**LsaEnumerateTrustedDomainsEx**</span><span class="sxs-lookup"><span data-stu-id="e413f-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 





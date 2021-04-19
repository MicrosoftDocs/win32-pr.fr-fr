---
description: Ajoute un autre nom de réseau local pour l’ordinateur à partir duquel il est appelé.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543287"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="a1046-103">AddLocalAlternateComputerName fonction)</span><span class="sxs-lookup"><span data-stu-id="a1046-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="a1046-104">Ajoute un autre nom de réseau local pour l’ordinateur à partir duquel il est appelé.</span><span class="sxs-lookup"><span data-stu-id="a1046-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1046-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1046-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a1046-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1046-107">*lpDnsFQHostname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1046-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1046-108">Autre nom à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a1046-108">The alternate name to be added.</span></span> <span data-ttu-id="a1046-109">Le nom doit être au format **ComputerNameDnsFullyQualified** , tel que défini dans l’énumération de [**\_ \_ format de nom d’ordinateur**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , et la fonction [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) doit être en mesure de la valider avec son format défini sur **DnsNameHostnameFull**.</span><span class="sxs-lookup"><span data-stu-id="a1046-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="a1046-110">*ulFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1046-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1046-111">Ce paramètre est réservé et doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a1046-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1046-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1046-112">Return value</span></span>

<span data-ttu-id="a1046-113">Si la fonction réussit, la fonction retourne une **erreur de \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="a1046-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="a1046-114">Si la fonction échoue, elle retourne un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="a1046-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="a1046-115">Parmi les codes d’erreur qu’elle retourne, citons les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1046-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="a1046-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a1046-116">Return code</span></span>                                                                                               | <span data-ttu-id="a1046-117">Description</span><span class="sxs-lookup"><span data-stu-id="a1046-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1046-118"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1046-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="a1046-119">Indique que le paramètre *lpDnsFQHostname* ne pointe pas vers un nom DNS valide ou que le paramètre *ulFlags* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a1046-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="a1046-120"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1046-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="a1046-121">La mémoire disponible est insuffisante pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="a1046-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="a1046-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1046-122">Requirements</span></span>



| <span data-ttu-id="a1046-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1046-123">Requirement</span></span> | <span data-ttu-id="a1046-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1046-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1046-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a1046-125">Library</span></span><br/>                | <dl> <span data-ttu-id="a1046-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1046-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="a1046-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a1046-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="a1046-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1046-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="a1046-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a1046-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="a1046-130">**AddLocalAlternateComputerNameW** (Unicode) et **AddLocalAlternateComputerNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a1046-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1046-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1046-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1046-132">**\_format du nom de l’ordinateur \_**</span><span class="sxs-lookup"><span data-stu-id="a1046-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="a1046-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="a1046-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 

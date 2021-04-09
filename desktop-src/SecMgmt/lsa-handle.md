---
description: Handle de l’objet de stratégie locale.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034567"
---
# <a name="lsa_handle"></a><span data-ttu-id="9371d-103">\_handle LSA</span><span class="sxs-lookup"><span data-stu-id="9371d-103">LSA\_HANDLE</span></span>

<span data-ttu-id="9371d-104">Le type de données du **\_ handle LSA** est un descripteur de l’objet de [**stratégie**](policy-object.md) locale.</span><span class="sxs-lookup"><span data-stu-id="9371d-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="9371d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9371d-105">Remarks</span></span>

<span data-ttu-id="9371d-106">Avant de pouvoir utiliser l’API de stratégie locale, votre application doit ouvrir un handle vers un objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9371d-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="9371d-107">Pour ce faire, appelez [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="9371d-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="9371d-108">Cette fonction retourne un handle que votre application peut ensuite spécifier dans les appels de fonction de stratégie LSA suivants.</span><span class="sxs-lookup"><span data-stu-id="9371d-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="9371d-109">Chaque handle possède un ensemble d’autorisations associées qui déterminent les opérations que votre application peut effectuer sur l’objet de [**stratégie**](policy-object.md) à l’aide du descripteur.</span><span class="sxs-lookup"><span data-stu-id="9371d-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="9371d-110">Votre application peut ouvrir plusieurs descripteurs à la fois sur l’objet de **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="9371d-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="9371d-111">Lorsqu’un descripteur n’est plus nécessaire, votre application doit la fermer en appelant [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span><span class="sxs-lookup"><span data-stu-id="9371d-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="9371d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9371d-112">Requirements</span></span>



| <span data-ttu-id="9371d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9371d-113">Requirement</span></span> | <span data-ttu-id="9371d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9371d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9371d-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9371d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9371d-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9371d-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9371d-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9371d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9371d-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9371d-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9371d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9371d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9371d-120"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9371d-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9371d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9371d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9371d-122">**LsaClose**</span><span class="sxs-lookup"><span data-stu-id="9371d-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="9371d-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="9371d-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 


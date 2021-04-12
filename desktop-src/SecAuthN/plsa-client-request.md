---
description: Type de données opaque.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203045"
---
# <a name="plsa_client_request"></a><span data-ttu-id="3e918-103">\_demande du client PLSA \_</span><span class="sxs-lookup"><span data-stu-id="3e918-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="3e918-104">Le type de données de la **\_ \_ demande du client PLSA** est un type de données opaque.</span><span class="sxs-lookup"><span data-stu-id="3e918-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="3e918-105">L' [*autorité de sécurité locale (LSA, Local Security Authority*](../secgloss/l-gly.md) ) l’utilise en interne pour gérer les informations du client relatives aux demandes individuelles.</span><span class="sxs-lookup"><span data-stu-id="3e918-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="3e918-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e918-106">Requirements</span></span>



| <span data-ttu-id="3e918-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e918-107">Requirement</span></span> | <span data-ttu-id="3e918-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e918-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e918-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e918-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3e918-110">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e918-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e918-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e918-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3e918-112">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e918-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e918-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e918-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e918-114"><dt>Ntsecpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e918-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 

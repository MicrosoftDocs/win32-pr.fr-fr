---
description: Le type de données TimeStamp contient des informations sur la durée de validité des jetons de sécurité. Le format de la valeur du type de données TimeStamp est le même que celui de la structure FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Horodateur (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527832"
---
# <a name="timestamp"></a><span data-ttu-id="78bd6-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="78bd6-104">TimeStamp</span></span>

<span data-ttu-id="78bd6-105">Le type de données **timestamp** contient des informations sur la durée de validité des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="78bd6-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="78bd6-106">Le format de la valeur du type de données **timestamp** est le même que celui de la structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="78bd6-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="78bd6-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78bd6-107">Requirements</span></span>



| <span data-ttu-id="78bd6-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78bd6-108">Requirement</span></span> | <span data-ttu-id="78bd6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="78bd6-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bd6-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78bd6-110">Minimum supported client</span></span><br/> | <span data-ttu-id="78bd6-111">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78bd6-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="78bd6-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78bd6-112">Minimum supported server</span></span><br/> | <span data-ttu-id="78bd6-113">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78bd6-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="78bd6-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="78bd6-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="78bd6-115"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78bd6-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 

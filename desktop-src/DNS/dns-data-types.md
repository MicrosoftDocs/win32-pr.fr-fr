---
title: Types de données DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: En savoir plus sur les types de données DNS
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202877"
---
# <a name="dns-data-types"></a><span data-ttu-id="9d0e8-104">Types de données DNS</span><span class="sxs-lookup"><span data-stu-id="9d0e8-104">DNS Data Types</span></span>

<span data-ttu-id="9d0e8-105">Les types de données suivants sont définis pour DNS :</span><span class="sxs-lookup"><span data-stu-id="9d0e8-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="9d0e8-106">**\_Adresse adresse IP4**</span><span class="sxs-lookup"><span data-stu-id="9d0e8-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="9d0e8-107">Valeur qui représente une adresse IPv4 (Internet Protocol version 4).</span><span class="sxs-lookup"><span data-stu-id="9d0e8-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="9d0e8-108">Par exemple, l’adresse IPv4 décimale séparée par des points, **127.0.0.1**, est représentée dans l’ordre d’octet de l’hôte en tant que **0x7F000001**.</span><span class="sxs-lookup"><span data-stu-id="9d0e8-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d0e8-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d0e8-109">Requirements</span></span>



| <span data-ttu-id="9d0e8-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d0e8-110">Requirement</span></span> | <span data-ttu-id="9d0e8-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d0e8-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0e8-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d0e8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0e8-113">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d0e8-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9d0e8-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d0e8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0e8-115">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d0e8-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d0e8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d0e8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d0e8-117"><dt>Windns. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0e8-117"><dt>Windns.h</dt></span></span> </dl> |



 

 






---
description: L' \_ énumération de type KEYSVC définit si une clé s’applique à un ordinateur ou à un service.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Énumération KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953152"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="90303-103">\_Énumération de type KEYSVC</span><span class="sxs-lookup"><span data-stu-id="90303-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="90303-104">L’énumération de **\_ type KEYSVC** définit si une clé s’applique à un ordinateur ou à un service.</span><span class="sxs-lookup"><span data-stu-id="90303-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="90303-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90303-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="90303-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="90303-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90303-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span><span class="sxs-lookup"><span data-stu-id="90303-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="90303-108">La clé est destinée à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="90303-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="90303-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span><span class="sxs-lookup"><span data-stu-id="90303-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="90303-110">La clé concerne un service.</span><span class="sxs-lookup"><span data-stu-id="90303-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90303-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90303-111">Requirements</span></span>



| <span data-ttu-id="90303-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90303-112">Requirement</span></span> | <span data-ttu-id="90303-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="90303-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90303-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90303-114">Minimum supported client</span></span><br/> | <span data-ttu-id="90303-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="90303-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="90303-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90303-116">Minimum supported server</span></span><br/> | <span data-ttu-id="90303-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90303-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90303-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="90303-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="90303-119"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="90303-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90303-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90303-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90303-121">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="90303-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 





---
description: Le \_ type de données handle KEYSVCC définit un handle de service de clé. Un \_ handle de handle KEYSVCC est utilisé par les fonctions RKeyOpenKeyService et RKeyCloseKeyService.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530187"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="55b8a-104">\_handle KEYSVCC</span><span class="sxs-lookup"><span data-stu-id="55b8a-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="55b8a-105">Le type de données **\_ handle KEYSVCC** définit un handle de service de clé.</span><span class="sxs-lookup"><span data-stu-id="55b8a-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="55b8a-106">Un handle de **\_ handle KEYSVCC** est utilisé par les fonctions [**RKeyOpenKeyService**](rkeyopenkeyservice.md) et [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="55b8a-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="55b8a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55b8a-107">Requirements</span></span>



| <span data-ttu-id="55b8a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55b8a-108">Requirement</span></span> | <span data-ttu-id="55b8a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="55b8a-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55b8a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b8a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="55b8a-111">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b8a-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="55b8a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b8a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="55b8a-113">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55b8a-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55b8a-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="55b8a-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b8a-115"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b8a-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b8a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55b8a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b8a-117">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="55b8a-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="55b8a-118">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="55b8a-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 





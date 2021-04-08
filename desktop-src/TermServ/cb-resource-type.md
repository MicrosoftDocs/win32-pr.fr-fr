---
title: Énumération CB_RESOURCE_TYPE (Cbclient. h)
description: Spécifie le type de ressource auquel la connexion entrante est connectée.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Énumération CB_RESOURCE_TYPE Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740581"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="60b74-104">\_Énumération de type de ressource CB \_</span><span class="sxs-lookup"><span data-stu-id="60b74-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="60b74-105">Spécifie le type de ressource auquel la connexion entrante est connectée.</span><span class="sxs-lookup"><span data-stu-id="60b74-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="60b74-106">Cette énumération est utilisée avec la structure d' [**\_ \_ informations de connexion CB**](cb-connection-info.md) .</span><span class="sxs-lookup"><span data-stu-id="60b74-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b74-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60b74-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="60b74-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="60b74-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="60b74-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**\_ressource CB \_ non définie**</span><span class="sxs-lookup"><span data-stu-id="60b74-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="60b74-110">Le type de ressource n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="60b74-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="60b74-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_session de ressources CB \_**</span><span class="sxs-lookup"><span data-stu-id="60b74-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="60b74-112">La ressource est une session à distance.</span><span class="sxs-lookup"><span data-stu-id="60b74-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="60b74-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_ \_ machine virtuelle de la ressource CB**</span><span class="sxs-lookup"><span data-stu-id="60b74-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="60b74-114">La ressource est une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="60b74-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60b74-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60b74-115">Requirements</span></span>



| <span data-ttu-id="60b74-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b74-116">Requirement</span></span> | <span data-ttu-id="60b74-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b74-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b74-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60b74-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60b74-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="60b74-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60b74-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60b74-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="60b74-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="60b74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b74-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b74-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b74-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b74-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b74-125">**\_informations de connexion CB \_**</span><span class="sxs-lookup"><span data-stu-id="60b74-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 






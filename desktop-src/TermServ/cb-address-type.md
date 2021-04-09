---
title: Énumération CB_ADDRESS_TYPE (Cbclient. h)
description: Spécifie le type d’adresse.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Énumération CB_ADDRESS_TYPE Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740588"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="2cf4f-104">\_Énumération de type d’adresse CB \_</span><span class="sxs-lookup"><span data-stu-id="2cf4f-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="2cf4f-105">Spécifie le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf4f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cf4f-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2cf4f-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="2cf4f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2cf4f-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB \_ addr \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="2cf4f-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2cf4f-109">Le type d’adresse n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="2cf4f-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**\_Adresse CB \_ IPv4**</span><span class="sxs-lookup"><span data-stu-id="2cf4f-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="2cf4f-111">L’adresse est une adresse IPv4.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="2cf4f-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**Bloc d' \_ adresse CB \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="2cf4f-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="2cf4f-113">L’adresse est une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cf4f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cf4f-114">Requirements</span></span>



| <span data-ttu-id="2cf4f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cf4f-115">Requirement</span></span> | <span data-ttu-id="2cf4f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cf4f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf4f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf4f-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2cf4f-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="2cf4f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf4f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cf4f-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="2cf4f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cf4f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf4f-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4f-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 






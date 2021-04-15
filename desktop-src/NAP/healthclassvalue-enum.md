---
title: Énumération HealthClassValue (NapProtocol. h)
description: Indique la valeur de la classe d’intégrité TLV.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue de l’énumération NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464210"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="de02e-104">Énumération HealthClassValue</span><span class="sxs-lookup"><span data-stu-id="de02e-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="de02e-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="de02e-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="de02e-106">Le type d’énumération **HealthClassValue** indique la valeur de la classe d’intégrité TLV.</span><span class="sxs-lookup"><span data-stu-id="de02e-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="de02e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de02e-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="de02e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="de02e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="de02e-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span><span class="sxs-lookup"><span data-stu-id="de02e-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="de02e-110">La classe d’intégrité TLV est le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="de02e-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="de02e-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span><span class="sxs-lookup"><span data-stu-id="de02e-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="de02e-112">La classe d’intégrité TLV est un niveau de correctif.</span><span class="sxs-lookup"><span data-stu-id="de02e-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="de02e-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span><span class="sxs-lookup"><span data-stu-id="de02e-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="de02e-114">La classe d’intégrité TLV est un antivirus.</span><span class="sxs-lookup"><span data-stu-id="de02e-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="de02e-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span><span class="sxs-lookup"><span data-stu-id="de02e-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="de02e-116">La classe d’intégrité TLV est une mise à jour critique.</span><span class="sxs-lookup"><span data-stu-id="de02e-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="de02e-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span><span class="sxs-lookup"><span data-stu-id="de02e-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="de02e-118">Réservé à l’usage du système uniquement.</span><span class="sxs-lookup"><span data-stu-id="de02e-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de02e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de02e-119">Requirements</span></span>



| <span data-ttu-id="de02e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de02e-120">Requirement</span></span> | <span data-ttu-id="de02e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="de02e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="de02e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de02e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de02e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de02e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de02e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de02e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de02e-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de02e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="de02e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="de02e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="de02e-127"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="de02e-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="de02e-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="de02e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de02e-129"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de02e-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 






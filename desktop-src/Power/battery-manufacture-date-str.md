---
description: Contient la date de fabrication d’une batterie.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Structure BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519703"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="04ba6-103">Structure de date de la fabrication de la batterie \_ \_</span><span class="sxs-lookup"><span data-stu-id="04ba6-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="04ba6-104">Contient la date de fabrication d’une batterie.</span><span class="sxs-lookup"><span data-stu-id="04ba6-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="04ba6-105">Cette structure est utilisée par la structure d' [**\_ \_ informations sur les requêtes de batterie**](battery-query-information-str.md) lorsque le niveau d’information BatteryManufactureDate est demandé.</span><span class="sxs-lookup"><span data-stu-id="04ba6-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ba6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04ba6-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="04ba6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="04ba6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="04ba6-108">**Jour**</span><span class="sxs-lookup"><span data-stu-id="04ba6-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="04ba6-109">Jour du mois de fabrication, compris entre 1 et 31.</span><span class="sxs-lookup"><span data-stu-id="04ba6-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="04ba6-110">En dépit du type de données, il ne s’agit pas d’une valeur encodée en ASCII.</span><span class="sxs-lookup"><span data-stu-id="04ba6-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="04ba6-111">Il s’agit d’un octet non signé.</span><span class="sxs-lookup"><span data-stu-id="04ba6-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="04ba6-112">**Chronique**</span><span class="sxs-lookup"><span data-stu-id="04ba6-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="04ba6-113">Mois de fabrication, dans la plage comprise entre 1 (janvier) et 12 (décembre).</span><span class="sxs-lookup"><span data-stu-id="04ba6-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="04ba6-114">En dépit du type de données, il ne s’agit pas d’une valeur encodée en ASCII.</span><span class="sxs-lookup"><span data-stu-id="04ba6-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="04ba6-115">Il s’agit d’un octet non signé.</span><span class="sxs-lookup"><span data-stu-id="04ba6-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="04ba6-116">**Year**</span><span class="sxs-lookup"><span data-stu-id="04ba6-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="04ba6-117">Année de fabrication.</span><span class="sxs-lookup"><span data-stu-id="04ba6-117">The year of manufacture.</span></span> <span data-ttu-id="04ba6-118">Il se trouve généralement dans la plage 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="04ba6-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04ba6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="04ba6-119">Remarks</span></span>

<span data-ttu-id="04ba6-120">La date est encodée au format grégorien ou occidental.</span><span class="sxs-lookup"><span data-stu-id="04ba6-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ba6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04ba6-121">Requirements</span></span>



| <span data-ttu-id="04ba6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04ba6-122">Requirement</span></span> | <span data-ttu-id="04ba6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="04ba6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ba6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ba6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="04ba6-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ba6-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="04ba6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ba6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="04ba6-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ba6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="04ba6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="04ba6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ba6-129"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="04ba6-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ba6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04ba6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ba6-131">**\_informations sur la requête de batterie \_**</span><span class="sxs-lookup"><span data-stu-id="04ba6-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="04ba6-132">**\_ \_ informations sur les requêtes de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="04ba6-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 





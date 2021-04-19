---
description: Contient l’état actuel de la batterie.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Structure BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524219"
---
# <a name="battery_status-structure"></a><span data-ttu-id="edf6f-103">Structure d’état de la batterie \_</span><span class="sxs-lookup"><span data-stu-id="edf6f-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="edf6f-104">Contient l’état actuel de la batterie.</span><span class="sxs-lookup"><span data-stu-id="edf6f-104">Contains the current state of the battery.</span></span> <span data-ttu-id="edf6f-105">Cette structure est utilisée par le code de contrôle de l’état de la [**\_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="edf6f-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf6f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edf6f-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="edf6f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="edf6f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="edf6f-108">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="edf6f-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="edf6f-109">État de la batterie.</span><span class="sxs-lookup"><span data-stu-id="edf6f-109">The battery state.</span></span> <span data-ttu-id="edf6f-110">Ce membre peut être égal à zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="edf6f-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="edf6f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf6f-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="edf6f-112">Signification</span><span class="sxs-lookup"><span data-stu-id="edf6f-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="edf6f-113"><dt>**Batterie \_ CHARGEMENT**</dt> de <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="edf6f-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="edf6f-114">Indique que la batterie est en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="edf6f-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="edf6f-115"><dt>**Batterie \_**</dt> <dt>0x00000008</dt> critique</span><span class="sxs-lookup"><span data-stu-id="edf6f-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="edf6f-116">Indique que la défaillance de la batterie est imminente.</span><span class="sxs-lookup"><span data-stu-id="edf6f-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="edf6f-117">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="edf6f-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="edf6f-118"><dt>**Batterie \_ Déchargement**</dt> de <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="edf6f-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="edf6f-119">Indique que la batterie est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="edf6f-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="edf6f-120"><dt>**Batterie \_ METTRE \_ sous \_ tension**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="edf6f-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="edf6f-121">Indique que le système a accès à l’alimentation secteur, donc aucune batterie n’est en cours de défacturation.</span><span class="sxs-lookup"><span data-stu-id="edf6f-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="edf6f-122">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="edf6f-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="edf6f-123">Capacité actuelle de la batterie, en mWh (ou relatif).</span><span class="sxs-lookup"><span data-stu-id="edf6f-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="edf6f-124">Cette valeur peut être utilisée pour générer un affichage de « jauge de gaz » en le divisant par le membre **FullChargedCapacity** de la structure d' [**\_ informations sur la batterie**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="edf6f-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="edf6f-125">Si la capacité n’est pas disponible, il s’agit de la capacité inconnue de la batterie \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="edf6f-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="edf6f-126">**Voltage**</span><span class="sxs-lookup"><span data-stu-id="edf6f-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="edf6f-127">Tension actuelle de la batterie sur les bornes de la batterie, en millivolts (MV).</span><span class="sxs-lookup"><span data-stu-id="edf6f-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="edf6f-128">Si la tension n’est pas disponible, il s’agit d’une tension de batterie \_ inconnue \_ .</span><span class="sxs-lookup"><span data-stu-id="edf6f-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="edf6f-129">**Tarif**</span><span class="sxs-lookup"><span data-stu-id="edf6f-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="edf6f-130">Taux actuel de charge ou de décharge de la batterie.</span><span class="sxs-lookup"><span data-stu-id="edf6f-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="edf6f-131">Cette valeur sera en milliwatts, sauf si les informations relatives au taux de batterie sont relatives, auquel cas elle sera en unités arbitraires par heure.</span><span class="sxs-lookup"><span data-stu-id="edf6f-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="edf6f-132">Pour déterminer si les informations sur la batterie sont relatives, examinez l' \_ indicateur relatif à la capacité de la batterie \_ dans le membre **capacités** de la structure d' [**\_ informations sur la batterie**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="edf6f-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="edf6f-133">Un taux positif différent de zéro indique une charge ; un taux négatif indique un déchargement.</span><span class="sxs-lookup"><span data-stu-id="edf6f-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="edf6f-134">Certaines batteries signalent uniquement des taux de rejet.</span><span class="sxs-lookup"><span data-stu-id="edf6f-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="edf6f-135">Si le taux n’est pas disponible, la fréquence de la batterie est inconnue pour ce membre \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="edf6f-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="edf6f-136">Si l’état de la batterie ou de la source d’alimentation change, le taux peut devenir disponible.</span><span class="sxs-lookup"><span data-stu-id="edf6f-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edf6f-137">Notes</span><span class="sxs-lookup"><span data-stu-id="edf6f-137">Remarks</span></span>

<span data-ttu-id="edf6f-138">L' \_ indicateur critique de la batterie dans le membre **PowerState** de cette structure indique une condition matérielle « critique pour la batterie ».</span><span class="sxs-lookup"><span data-stu-id="edf6f-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="edf6f-139">Ce niveau critique est défini par le fabricant de la batterie, et non par l’utilisateur dans la « alarme de batterie critique ».</span><span class="sxs-lookup"><span data-stu-id="edf6f-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="edf6f-140">Cela signifie généralement que le système de batterie a calculé que la batterie est entièrement drainée et que toute puissance dessinée dépasse ce qui est attendu.</span><span class="sxs-lookup"><span data-stu-id="edf6f-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf6f-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edf6f-141">Requirements</span></span>



| <span data-ttu-id="edf6f-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edf6f-142">Requirement</span></span> | <span data-ttu-id="edf6f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf6f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf6f-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf6f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="edf6f-145">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edf6f-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="edf6f-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf6f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="edf6f-147">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edf6f-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="edf6f-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="edf6f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="edf6f-149"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="edf6f-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edf6f-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf6f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf6f-151">**\_informations sur la batterie**</span><span class="sxs-lookup"><span data-stu-id="edf6f-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="edf6f-152">**État de la \_ requête de batterie IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="edf6f-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 





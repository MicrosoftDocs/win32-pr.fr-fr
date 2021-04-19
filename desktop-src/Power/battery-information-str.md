---
description: Contient des informations sur la batterie.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Structure BATTERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527641"
---
# <a name="battery_information-structure"></a><span data-ttu-id="50c56-103">\_Structure d’informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="50c56-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="50c56-104">Contient des informations sur la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-104">Contains battery information.</span></span> <span data-ttu-id="50c56-105">Cette structure est retournée par le code de contrôle des informations de requête de la [**\_ batterie \_ \_ IOCTL**](ioctl-battery-query-information.md) lorsque le niveau d’information BatteryInformation est demandé.</span><span class="sxs-lookup"><span data-stu-id="50c56-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c56-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50c56-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="50c56-107">Membres</span><span class="sxs-lookup"><span data-stu-id="50c56-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="50c56-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="50c56-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-109">Capacités de la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-109">The battery capabilities.</span></span> <span data-ttu-id="50c56-110">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="50c56-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="50c56-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c56-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="50c56-112">Signification</span><span class="sxs-lookup"><span data-stu-id="50c56-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="50c56-113"><dt>**Batterie \_ 0x40000000 \_ relative**</dt> à la capacité <dt></dt></span><span class="sxs-lookup"><span data-stu-id="50c56-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="50c56-114">Indique que les informations relatives à la capacité et au taux de la batterie sont relatives, et non dans des unités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="50c56-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="50c56-115">Si ce bit n’est pas défini, les unités de rapport sont milliwatts heure-Hours (mWh) pour Capacity et milliwatts (mW) pour rate.</span><span class="sxs-lookup"><span data-stu-id="50c56-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="50c56-116">Si ce bit est défini, toutes les références aux unités dans la documentation de l’autre batterie peuvent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="50c56-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="50c56-117">Toutes les informations sur les taux sont signalées en unités par heure.</span><span class="sxs-lookup"><span data-stu-id="50c56-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="50c56-118">Par exemple, si la capacité entièrement facturée est signalée comme 100, un taux de 200 indique que la batterie utilise toute sa capacité en une demi-heure.</span><span class="sxs-lookup"><span data-stu-id="50c56-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="50c56-119"><dt>**Batterie \_ EST 0x20000000 à \_ bref \_ terme**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="50c56-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="50c56-120">Indique que l’opération normale est destinée à une fonction de prévention de défaillance.</span><span class="sxs-lookup"><span data-stu-id="50c56-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="50c56-121">Si ce bit n’est pas défini, la batterie est censée être utilisée lors de l’utilisation normale du système.</span><span class="sxs-lookup"><span data-stu-id="50c56-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="50c56-122"><dt>**Batterie \_ DÉFINIR les \_ frais \_ pris en charge**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="50c56-123">Indique que les demandes d’informations set du type BatteryCharge sont prises en charge par ce périphérique de batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="50c56-124"><dt>**Batterie \_ DÉFINIR un \_ rejet \_ pris en charge**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="50c56-125">Indique que les demandes d’informations set du type BatteryDischarge sont prises en charge par ce périphérique de batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="50c56-126"><dt>**Batterie \_ \_Batterie système**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="50c56-127">Indique que la batterie peut fournir une alimentation générale pour l’exécution du système.</span><span class="sxs-lookup"><span data-stu-id="50c56-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="50c56-128">**Technology**</span><span class="sxs-lookup"><span data-stu-id="50c56-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-129">La technologie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-129">The battery technology.</span></span> <span data-ttu-id="50c56-130">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="50c56-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="50c56-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c56-131">Value</span></span>                                                                        | <span data-ttu-id="50c56-132">Signification</span><span class="sxs-lookup"><span data-stu-id="50c56-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="50c56-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="50c56-134">Batterie Nonrechargeable, par exemple, alcaline.</span><span class="sxs-lookup"><span data-stu-id="50c56-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="50c56-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="50c56-136">Batterie refacturable, par exemple, l’acide de leads.</span><span class="sxs-lookup"><span data-stu-id="50c56-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="50c56-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="50c56-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="50c56-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-139">**Chimique**</span><span class="sxs-lookup"><span data-stu-id="50c56-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-140">Chaîne de caractères abrégée qui indique la chimie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="50c56-141">Cette chaîne ne se termine pas nécessairement par zéro.</span><span class="sxs-lookup"><span data-stu-id="50c56-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="50c56-142">Voici une liste partielle des abréviations qui peuvent être retournées et des Chemistries associés.</span><span class="sxs-lookup"><span data-stu-id="50c56-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="50c56-143">chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="50c56-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="50c56-144">Signification</span><span class="sxs-lookup"><span data-stu-id="50c56-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="50c56-145"><dt>**PbAc**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="50c56-146">Acidité</span><span class="sxs-lookup"><span data-stu-id="50c56-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="50c56-147"><dt>**LION**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="50c56-148">Lithium-ion</span><span class="sxs-lookup"><span data-stu-id="50c56-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="50c56-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="50c56-150">Lithium-ion</span><span class="sxs-lookup"><span data-stu-id="50c56-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="50c56-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="50c56-152">Nickel cadmium</span><span class="sxs-lookup"><span data-stu-id="50c56-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="50c56-153"><dt>**NiMH**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="50c56-154">Nickel metal-hydrure</span><span class="sxs-lookup"><span data-stu-id="50c56-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="50c56-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="50c56-156">Nickel-zinc</span><span class="sxs-lookup"><span data-stu-id="50c56-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="50c56-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="50c56-158">Alkaline-Manganese refacturable</span><span class="sxs-lookup"><span data-stu-id="50c56-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="50c56-159">D’autres Chemistries peuvent apparaître à l’avenir et votre code doit être en mesure de les gérer.</span><span class="sxs-lookup"><span data-stu-id="50c56-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-160">**DesignedCapacity**</span><span class="sxs-lookup"><span data-stu-id="50c56-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-161">Capacité théorique de la batterie lorsqu’elle est nouvelle, dans mWh, sauf si la capacité de la batterie \_ \_ est définie.</span><span class="sxs-lookup"><span data-stu-id="50c56-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="50c56-162">Dans ce cas, les unités ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="50c56-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-163">**FullChargedCapacity**</span><span class="sxs-lookup"><span data-stu-id="50c56-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-164">Capacité totale actuelle de la batterie dans mWh (ou relative).</span><span class="sxs-lookup"><span data-stu-id="50c56-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="50c56-165">Comparez cette valeur à **DesignedCapacity** pour estimer l’usure de la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="50c56-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-167">Capacité suggérée par le fabricant, en mWh, à laquelle une alerte de batterie faible doit se produire.</span><span class="sxs-lookup"><span data-stu-id="50c56-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="50c56-168">Les définitions de faible varient d’un fabricant au fabricant.</span><span class="sxs-lookup"><span data-stu-id="50c56-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="50c56-169">En général, un état d’avertissement se produit avant un État faible, mais vous ne devez pas supposer qu’il le sera toujours.</span><span class="sxs-lookup"><span data-stu-id="50c56-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="50c56-170">Pour réduire les risques de perte de données, cette valeur est généralement utilisée comme paramètre par défaut pour l’alarme de batterie critique.</span><span class="sxs-lookup"><span data-stu-id="50c56-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="50c56-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-172">Capacité suggérée par le fabricant, en mWh, à laquelle une alerte de batterie d’avertissement doit se produire.</span><span class="sxs-lookup"><span data-stu-id="50c56-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="50c56-173">Les définitions d’avertissement varient d’un fabricant à l’autres.</span><span class="sxs-lookup"><span data-stu-id="50c56-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="50c56-174">En général, un état d’avertissement se produit avant un État faible, mais vous ne devez pas supposer qu’il le sera toujours.</span><span class="sxs-lookup"><span data-stu-id="50c56-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="50c56-175">Pour réduire les risques de perte de données, cette valeur est généralement utilisée comme paramètre par défaut pour l’alerte de batterie faible.</span><span class="sxs-lookup"><span data-stu-id="50c56-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-176">**CriticalBias**</span><span class="sxs-lookup"><span data-stu-id="50c56-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-177">Biais de zéro, dans mWh, qui est appliqué à la création de rapports de batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="50c56-178">Certaines batteries réservent une petite charge qui est écartée des valeurs de capacité de la batterie pour afficher « 0 » comme niveau de batterie critique.</span><span class="sxs-lookup"><span data-stu-id="50c56-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="50c56-179">Le décalage critique est similaire à la définition d’une jauge de carburant pour afficher « vide » lorsqu’il existe plusieurs litres de carburant.</span><span class="sxs-lookup"><span data-stu-id="50c56-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="50c56-180">**CycleCount**</span><span class="sxs-lookup"><span data-stu-id="50c56-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="50c56-181">Nombre de cycles de charge/décharge que la batterie a rencontrés.</span><span class="sxs-lookup"><span data-stu-id="50c56-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="50c56-182">Cela permet de déterminer l’usure de la batterie.</span><span class="sxs-lookup"><span data-stu-id="50c56-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="50c56-183">Si la batterie ne prend pas en charge un compteur de cycles, ce membre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="50c56-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50c56-184">Notes</span><span class="sxs-lookup"><span data-stu-id="50c56-184">Remarks</span></span>

<span data-ttu-id="50c56-185">En règle générale, un état d’avertissement se produit avant un État faible, mais vous ne devez pas le supposer.</span><span class="sxs-lookup"><span data-stu-id="50c56-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="50c56-186">Il est possible d’interroger une batterie et de constater qu’aucun niveau d’alerte ne s’est produit, et d’interroger à nouveau la batterie et de la trouver déductible dans la mesure où les deux niveaux ont été atteints.</span><span class="sxs-lookup"><span data-stu-id="50c56-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="50c56-187">Cela peut indiquer que vous n’êtes pas assez souvent interrogé.</span><span class="sxs-lookup"><span data-stu-id="50c56-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="50c56-188">Cela peut également indiquer que la batterie ne peut pas être facturée pendant très longtemps et qu’elle est en train de se décharger plus rapidement que prévu.</span><span class="sxs-lookup"><span data-stu-id="50c56-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="50c56-189">Une batterie de ce type est proche de la fin de sa durée de vie utile, ou elle est peut-être endommagée.</span><span class="sxs-lookup"><span data-stu-id="50c56-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c56-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50c56-190">Requirements</span></span>



| <span data-ttu-id="50c56-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50c56-191">Requirement</span></span> | <span data-ttu-id="50c56-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c56-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c56-193">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50c56-193">Minimum supported client</span></span><br/> | <span data-ttu-id="50c56-194">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50c56-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="50c56-195">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50c56-195">Minimum supported server</span></span><br/> | <span data-ttu-id="50c56-196">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50c56-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="50c56-197">En-tête</span><span class="sxs-lookup"><span data-stu-id="50c56-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="50c56-198"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="50c56-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c56-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c56-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c56-200">**\_ \_ informations sur les requêtes de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="50c56-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 





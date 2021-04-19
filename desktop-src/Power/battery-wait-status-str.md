---
description: Contient des informations sur les conditions dans lesquelles l’état de la batterie doit être récupéré.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Structure BATTERY_WAIT_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517080"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="cda1a-103">Structure d’état d' \_ attente de la batterie \_</span><span class="sxs-lookup"><span data-stu-id="cda1a-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="cda1a-104">Contient des informations sur les conditions dans lesquelles l’état de la batterie doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="cda1a-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="cda1a-105">Cette structure est utilisée par le code de contrôle de l’état de la [**\_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="cda1a-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda1a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cda1a-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="cda1a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cda1a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cda1a-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="cda1a-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-109">La balise de batterie actuelle pour la batterie.</span><span class="sxs-lookup"><span data-stu-id="cda1a-109">The current battery tag for the battery.</span></span> <span data-ttu-id="cda1a-110">Seules les informations relatives à une batterie correspondant à la balise peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="cda1a-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="cda1a-111">Chaque fois que cette valeur ne correspond pas à la balise active de la batterie, l’opération [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) échoue avec le code d’erreur fichier d’erreur \_ \_ \_ introuvable, qui indique à l’appelant que la batterie pour laquelle il a une balise n’est plus installée. l’appelant peut choisir d’utiliser l’opération d' [**étiquette de \_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-tag.md) pour déterminer l’étiquette de la batterie nouvellement installée, le cas</span><span class="sxs-lookup"><span data-stu-id="cda1a-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="cda1a-112">En outre, si la demande est en cours lors de la suppression de la batterie ou si la balise change, l’opération est abandonnée avec l’État fichier d’erreur \_ \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="cda1a-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="cda1a-113">(Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="cda1a-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-114">**Délai d'expiration**</span><span class="sxs-lookup"><span data-stu-id="cda1a-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-115">Nombre de millisecondes pendant lesquelles la requête attendra la condition spécifiée par les membres **PowerState**, **LowCapacity** et **HighCapacity** avant de se terminer.</span><span class="sxs-lookup"><span data-stu-id="cda1a-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="cda1a-116">La valeur-1 indique que la demande attend indéfiniment que les conditions soient satisfaites.</span><span class="sxs-lookup"><span data-stu-id="cda1a-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="cda1a-117">La valeur zéro indique que les informations sur la batterie demandées doivent être retournées immédiatement, indépendamment des autres conditions.</span><span class="sxs-lookup"><span data-stu-id="cda1a-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="cda1a-118">Toute autre valeur indique que la requête doit attendre ce laps de temps, ou jusqu’à ce que l’une des autres conditions soit satisfaite.</span><span class="sxs-lookup"><span data-stu-id="cda1a-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="cda1a-119">Si l’ordinateur est passé en mode veille, l’horloge continue à s’exécuter, mais le fait d’épuiser le nombre n’est pas mis en éveil par l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cda1a-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="cda1a-120">Si le nombre est épuisé lorsque l’ordinateur est activé et que d’autres conditions sont satisfaites, l’appel est immédiatement retourné en cas de réveil.</span><span class="sxs-lookup"><span data-stu-id="cda1a-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-121">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="cda1a-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-122">Zéro, un ou plusieurs des bits d’état suivants, qui indiquent l’état de la batterie.</span><span class="sxs-lookup"><span data-stu-id="cda1a-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="cda1a-123">Il est identique au membre **PowerState** de la structure [**d' \_ État**](battery-status-str.md) de la batterie.</span><span class="sxs-lookup"><span data-stu-id="cda1a-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="cda1a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cda1a-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="cda1a-125">Signification</span><span class="sxs-lookup"><span data-stu-id="cda1a-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="cda1a-126"><dt>**Batterie \_ CHARGEMENT**</dt> de <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="cda1a-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="cda1a-127">Indique que la batterie est en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="cda1a-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="cda1a-128"><dt>**Batterie \_**</dt> <dt>0x00000008</dt> critique</span><span class="sxs-lookup"><span data-stu-id="cda1a-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="cda1a-129">Indique que la défaillance de la batterie est imminente.</span><span class="sxs-lookup"><span data-stu-id="cda1a-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="cda1a-130">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cda1a-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="cda1a-131"><dt>**Batterie \_ Déchargement**</dt> de <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cda1a-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="cda1a-132">Indique que la batterie est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="cda1a-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="cda1a-133"><dt>**Batterie \_ METTRE \_ sous \_ tension**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cda1a-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="cda1a-134">Indique que la batterie a accès à l’alimentation secteur.</span><span class="sxs-lookup"><span data-stu-id="cda1a-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="cda1a-135">**LowCapacity**</span><span class="sxs-lookup"><span data-stu-id="cda1a-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-136">Capacité actuelle de la batterie, en mWh (ou relatif).</span><span class="sxs-lookup"><span data-stu-id="cda1a-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="cda1a-137">Cette valeur est identique à la **capacité** membre de la structure d' [**\_ État**](battery-status-str.md) de la batterie.</span><span class="sxs-lookup"><span data-stu-id="cda1a-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-138">**HighCapacity**</span><span class="sxs-lookup"><span data-stu-id="cda1a-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-139">Capacité actuelle de la batterie, en mWh (ou relatif).</span><span class="sxs-lookup"><span data-stu-id="cda1a-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="cda1a-140">Cette valeur est identique à la **capacité** membre de la structure d' [**\_ État**](battery-status-str.md) de la batterie.</span><span class="sxs-lookup"><span data-stu-id="cda1a-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cda1a-141">Notes</span><span class="sxs-lookup"><span data-stu-id="cda1a-141">Remarks</span></span>

<span data-ttu-id="cda1a-142">Les demandes d’informations sur la batterie sont reportées jusqu’à ce que l’un des éléments suivants se produise :</span><span class="sxs-lookup"><span data-stu-id="cda1a-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="cda1a-143">Le délai d’attente expire (en supposant que le **délai d’expiration** n’est pas-1).</span><span class="sxs-lookup"><span data-stu-id="cda1a-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="cda1a-144">L’état actuel de la batterie ne correspond pas à **PowerState**.</span><span class="sxs-lookup"><span data-stu-id="cda1a-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="cda1a-145">La capacité de la batterie est inférieure à **LowCapacity**.</span><span class="sxs-lookup"><span data-stu-id="cda1a-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="cda1a-146">La capacité de la batterie est supérieure à **HighCapacity**.</span><span class="sxs-lookup"><span data-stu-id="cda1a-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="cda1a-147">La balise de batterie change.</span><span class="sxs-lookup"><span data-stu-id="cda1a-147">The battery tag changes.</span></span>

<span data-ttu-id="cda1a-148">Quand l’une de ces conditions est satisfaite, les données sont collectées et l’opération est retournée.</span><span class="sxs-lookup"><span data-stu-id="cda1a-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="cda1a-149">Cela permet aux applications de surveiller les informations de batterie dynamique classiques sans interroger l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cda1a-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="cda1a-150">Avant d’utiliser l’une des deux conditions de capacité, assurez-vous que la batterie les prend en charge en utilisant le code de contrôle d' [**\_ \_ \_ État de la batterie IOCTL**](ioctl-battery-query-status.md) avec un délai d’expiration de zéro.</span><span class="sxs-lookup"><span data-stu-id="cda1a-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="cda1a-151">Examinez les résultats pour déterminer si le membre de **capacité** est pris en charge (c’est-à-dire, pas de capacité de batterie \_ inconnue \_ ).</span><span class="sxs-lookup"><span data-stu-id="cda1a-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda1a-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cda1a-152">Requirements</span></span>



| <span data-ttu-id="cda1a-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cda1a-153">Requirement</span></span> | <span data-ttu-id="cda1a-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="cda1a-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda1a-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cda1a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cda1a-156">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cda1a-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="cda1a-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cda1a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cda1a-158">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cda1a-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="cda1a-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="cda1a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda1a-160"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="cda1a-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda1a-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda1a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda1a-162">**État de la batterie \_**</span><span class="sxs-lookup"><span data-stu-id="cda1a-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="cda1a-163">**État de la \_ requête de batterie IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cda1a-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="cda1a-164">**\_ \_ balise de requête de batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="cda1a-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 


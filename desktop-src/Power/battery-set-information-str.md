---
description: Contient les informations sur la batterie à définir.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Structure BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115558"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="ca754-103">Structure des informations du \_ jeu de batteries \_</span><span class="sxs-lookup"><span data-stu-id="ca754-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="ca754-104">Contient les informations sur la batterie à définir.</span><span class="sxs-lookup"><span data-stu-id="ca754-104">Contains battery information to be set.</span></span> <span data-ttu-id="ca754-105">Cette structure est utilisée avec le code de contrôle d' [**\_ informations du \_ jeu \_ de batteries IOCTL**](ioctl-battery-set-information.md) .</span><span class="sxs-lookup"><span data-stu-id="ca754-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca754-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca754-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="ca754-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ca754-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca754-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="ca754-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="ca754-109">La balise de batterie actuelle pour la batterie.</span><span class="sxs-lookup"><span data-stu-id="ca754-109">The current battery tag for the battery.</span></span> <span data-ttu-id="ca754-110">Les informations relatives à une batterie correspondant à la balise peuvent uniquement être retournées.</span><span class="sxs-lookup"><span data-stu-id="ca754-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="ca754-111">Chaque fois que cette valeur ne correspond pas à la balise active de la batterie, la requête IOCTL se termine avec le fichier d’erreur \_ \_ \_ introuvable, ce qui indique à l’appelant que la batterie pour laquelle il a une balise n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="ca754-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="ca754-112">L’appelant peut choisir d’utiliser l’opération de [**\_ \_ \_ balises de requête de batterie IOCTL**](ioctl-battery-query-tag.md) pour déterminer la balise de la batterie nouvellement installée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ca754-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="ca754-113">(Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="ca754-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="ca754-114">Quand une demande d’informations sur une requête est effectuée, cette valeur est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="ca754-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="ca754-115">En outre, si la demande est en cours alors que cette valeur change, la demande est abandonnée avec l’état \_ fichier d' \_ erreur \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="ca754-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="ca754-116">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="ca754-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="ca754-117">Informations sur la batterie à définir.</span><span class="sxs-lookup"><span data-stu-id="ca754-117">The battery information to be set.</span></span> <span data-ttu-id="ca754-118">Le type de données dans le membre de la **mémoire tampon** dépend de la valeur de ce membre.</span><span class="sxs-lookup"><span data-stu-id="ca754-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="ca754-119">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca754-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="ca754-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca754-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ca754-121">Signification</span><span class="sxs-lookup"><span data-stu-id="ca754-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="ca754-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="ca754-123">Indique à l’appareil de batterie que l’utilisateur a demandé que la batterie soit chargée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="ca754-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="ca754-124">Par exemple, avec un sélecteur/batterie intelligent, l’application peut charger une batterie à la fois.</span><span class="sxs-lookup"><span data-stu-id="ca754-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="ca754-125">Le membre de la **mémoire tampon** de cette structure est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ca754-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="ca754-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="ca754-127">Définit le réglage de décalage critique de la batterie.</span><span class="sxs-lookup"><span data-stu-id="ca754-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="ca754-128">Notez qu’il n’est pas prévu que cette valeur soit normalement modifiée par le logiciel et qu’elle soit présente dans les interfaces uniquement en tant que fonctionnalité de maintenance.</span><span class="sxs-lookup"><span data-stu-id="ca754-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="ca754-129">Toutes les batteries ne peuvent pas gérer ce type de paramètre et les informations sur la batterie doivent être lues pour confirmer que la batterie a accepté le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca754-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="ca754-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="ca754-131">Indique à l’appareil de batterie que l’utilisateur a demandé le déchargement de la batterie à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="ca754-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="ca754-132">Par exemple, cela peut être utilisé pour indiquer la batterie que l’utilisateur veut actuellement alimenter sur le système.</span><span class="sxs-lookup"><span data-stu-id="ca754-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="ca754-133">Le membre de la **mémoire tampon** de cette structure est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ca754-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="ca754-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="ca754-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="ca754-135">Informations sur la batterie à définir.</span><span class="sxs-lookup"><span data-stu-id="ca754-135">The battery information to be set.</span></span> <span data-ttu-id="ca754-136">Les données dépendent de la valeur de **InformationLevel**.</span><span class="sxs-lookup"><span data-stu-id="ca754-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca754-137">Notes</span><span class="sxs-lookup"><span data-stu-id="ca754-137">Remarks</span></span>

<span data-ttu-id="ca754-138">La structure d' **\_ \_ informations sur l’ensemble de batteries** est une structure de longueur variable et vous devez allouer une mémoire tampon de taille appropriée pour les informations à inclure dans la structure.</span><span class="sxs-lookup"><span data-stu-id="ca754-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca754-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca754-139">Requirements</span></span>



| <span data-ttu-id="ca754-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca754-140">Requirement</span></span> | <span data-ttu-id="ca754-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca754-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca754-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca754-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ca754-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca754-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="ca754-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca754-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ca754-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca754-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="ca754-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca754-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca754-147"><dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca754-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca754-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca754-149">**\_ \_ informations sur le jeu de batteries IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="ca754-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 





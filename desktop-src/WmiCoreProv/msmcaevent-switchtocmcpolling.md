---
description: Représente la gestion de la vérification de l’ordinateur (CMC) corrigée pour passer du pilote d’interruption à l’interrogation. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318354"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="39824-104">MSMCAEvent \_ SwitchToCMCPolling, classe</span><span class="sxs-lookup"><span data-stu-id="39824-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="39824-105">La classe **MSMCAEvent \_ SwitchToCMCPolling** représente la gestion des machines (CMC) corrigée pour passer du pilote d’interruption à l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="39824-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="39824-106">Dans certains cas, le noyau interroge la couche d’abstraction système (SAL) pour toute erreur CMC ou une erreur de plateforme corrigée (CPE) qui s’est produite au cours de l’intervalle d’interrogation précédent.</span><span class="sxs-lookup"><span data-stu-id="39824-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="39824-107">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="39824-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="39824-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="39824-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39824-109">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="39824-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39824-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39824-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="39824-111">Membres</span><span class="sxs-lookup"><span data-stu-id="39824-111">Members</span></span>

<span data-ttu-id="39824-112">La classe **MSMCAEvent \_ SwitchToCMCPolling** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="39824-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="39824-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39824-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39824-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39824-114">Properties</span></span>

<span data-ttu-id="39824-115">La classe **MSMCAEvent \_ SwitchToCMCPolling** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="39824-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39824-116">**Actif**</span><span class="sxs-lookup"><span data-stu-id="39824-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39824-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="39824-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39824-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39824-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39824-119">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="39824-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="39824-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="39824-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39824-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39824-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39824-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39824-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39824-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39824-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39824-124">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="39824-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39824-125">Notes</span><span class="sxs-lookup"><span data-stu-id="39824-125">Remarks</span></span>

<span data-ttu-id="39824-126">La classe **MSMCAEvent \_ SwitchToCMCPolling** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="39824-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="39824-127">La couche d’abstraction système (SAL) est du code gravé sur la ROM que le système d’exploitation appelle pour effectuer des opérations dépendantes de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="39824-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="39824-128">Il est similaire au BIOS sur une plateforme x86.</span><span class="sxs-lookup"><span data-stu-id="39824-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="39824-129">Dans les cas où la plateforme ne prend pas en charge les interruptions pour l’interrogation CMC ou CPE, le système d’exploitation interroge toutes les minutes, en vérifiant si une erreur s’est produite précédemment.</span><span class="sxs-lookup"><span data-stu-id="39824-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="39824-130">Si la plateforme prend en charge les interruptions et que le système d’exploitation reçoit une quantité définie par l’utilisateur d’interrogations CMC ou CPE pendant une minute, elle désactive l’interruption et l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="39824-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="39824-131">Si l’utilisateur ne définit pas le nombre d’interrogations au bout d’une minute, le système définit une valeur par défaut de 10 interrogations par minute.</span><span class="sxs-lookup"><span data-stu-id="39824-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="39824-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39824-132">Requirements</span></span>



| <span data-ttu-id="39824-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39824-133">Requirement</span></span> | <span data-ttu-id="39824-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="39824-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39824-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39824-135">Minimum supported client</span></span><br/> | <span data-ttu-id="39824-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="39824-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="39824-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39824-137">Minimum supported server</span></span><br/> | <span data-ttu-id="39824-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39824-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="39824-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39824-139">Namespace</span></span><br/>                | <span data-ttu-id="39824-140">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="39824-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="39824-141">MOF</span><span class="sxs-lookup"><span data-stu-id="39824-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39824-142"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39824-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="39824-143">DLL</span><span class="sxs-lookup"><span data-stu-id="39824-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39824-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39824-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39824-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39824-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39824-146">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="39824-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="39824-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="39824-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


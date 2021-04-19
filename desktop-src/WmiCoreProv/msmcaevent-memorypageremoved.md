---
description: Indique qu’une page de mémoire a été supprimée de l’utilisation du système en raison d’erreurs de vérification et de correction d’erreurs matérielles (ECC) excessives. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: Classe MSMCAEvent_MemoryPageRemoved
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521124"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="c7924-104">MSMCAEvent \_ MemoryPageRemoved, classe</span><span class="sxs-lookup"><span data-stu-id="c7924-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="c7924-105">La classe **MSMCAEvent \_ MemoryPageRemoved** indique qu’une page de mémoire a été supprimée de l’utilisation du système en raison d’erreurs de vérification et de correction d’erreurs matérielles (ECC) excessives.</span><span class="sxs-lookup"><span data-stu-id="c7924-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="c7924-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c7924-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="c7924-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c7924-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c7924-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c7924-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7924-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7924-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="c7924-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c7924-110">Members</span></span>

<span data-ttu-id="c7924-111">La classe **MSMCAEvent \_ MemoryPageRemoved** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7924-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="c7924-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7924-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7924-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7924-113">Properties</span></span>

<span data-ttu-id="c7924-114">La classe **MSMCAEvent \_ MemoryPageRemoved** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7924-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7924-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="c7924-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7924-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c7924-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7924-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7924-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7924-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c7924-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c7924-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c7924-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7924-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7924-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7924-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7924-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7924-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7924-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7924-123">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="c7924-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c7924-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="c7924-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7924-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7924-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7924-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7924-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7924-127">Adresse de la page de mémoire qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="c7924-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="c7924-128">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7924-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7924-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c7924-129">Remarks</span></span>

<span data-ttu-id="c7924-130">La classe **MSMCAEvent \_ MemoryPageRemoved** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="c7924-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7924-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7924-131">Requirements</span></span>



| <span data-ttu-id="c7924-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7924-132">Requirement</span></span> | <span data-ttu-id="c7924-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7924-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7924-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7924-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c7924-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7924-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c7924-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7924-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c7924-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7924-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c7924-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7924-138">Namespace</span></span><br/>                | <span data-ttu-id="c7924-139">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="c7924-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c7924-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c7924-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7924-141"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7924-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7924-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c7924-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7924-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7924-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7924-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7924-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7924-145">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="c7924-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="c7924-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="c7924-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


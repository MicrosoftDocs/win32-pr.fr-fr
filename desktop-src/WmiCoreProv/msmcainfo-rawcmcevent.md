---
description: Contient un événement de vérification de l’ordinateur (CMC) corrigé. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: Classe MSMCAInfo_RawCMCEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536573"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="d8ff8-104">MSMCAInfo \_ RawCMCEvent, classe</span><span class="sxs-lookup"><span data-stu-id="d8ff8-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="d8ff8-105">La classe **MSMCAInfo \_ RawCMCEvent** contient un événement de vérification de l’ordinateur (CMC) corrigé.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="d8ff8-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="d8ff8-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d8ff8-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ff8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8ff8-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="d8ff8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d8ff8-110">Members</span></span>

<span data-ttu-id="d8ff8-111">La classe **MSMCAInfo \_ RawCMCEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8ff8-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d8ff8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8ff8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8ff8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8ff8-113">Properties</span></span>

<span data-ttu-id="d8ff8-114">La classe **MSMCAInfo \_ RawCMCEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8ff8-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ff8-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8ff8-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ff8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ff8-118">TRUE si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d8ff8-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ff8-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8ff8-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ff8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ff8-122">Nombre d’enregistrements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="d8ff8-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ff8-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ff8-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ff8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ff8-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d8ff8-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d8ff8-127">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="d8ff8-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d8ff8-128">**Enregistrements**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ff8-129">Type de données : tableau d' **\_ entrée MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="d8ff8-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ff8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8ff8-131">Tableau des enregistrements d’erreurs MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="d8ff8-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="d8ff8-132">Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="d8ff8-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8ff8-133">Notes</span><span class="sxs-lookup"><span data-stu-id="d8ff8-133">Remarks</span></span>

<span data-ttu-id="d8ff8-134">La classe **MSMCAInfo \_ RawCMCEvent** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="d8ff8-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ff8-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8ff8-135">Requirements</span></span>



| <span data-ttu-id="d8ff8-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8ff8-136">Requirement</span></span> | <span data-ttu-id="d8ff8-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8ff8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ff8-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ff8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ff8-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8ff8-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d8ff8-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ff8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ff8-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8ff8-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d8ff8-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8ff8-142">Namespace</span></span><br/>                | <span data-ttu-id="d8ff8-143">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="d8ff8-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d8ff8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d8ff8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8ff8-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8ff8-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8ff8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ff8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ff8-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ff8-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ff8-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8ff8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ff8-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="d8ff8-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="d8ff8-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="d8ff8-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


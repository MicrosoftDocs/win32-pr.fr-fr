---
description: Contient un événement de plateforme corrigé (CPE). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536398"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="b09a2-104">MSMCAInfo \_ RawCorrectedPlatformEvent, classe</span><span class="sxs-lookup"><span data-stu-id="b09a2-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="b09a2-105">La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** contient un événement de plateforme corrigé (CPE).</span><span class="sxs-lookup"><span data-stu-id="b09a2-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="b09a2-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b09a2-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b09a2-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b09a2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b09a2-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b09a2-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09a2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b09a2-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="b09a2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b09a2-110">Members</span></span>

<span data-ttu-id="b09a2-111">La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b09a2-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b09a2-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b09a2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b09a2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b09a2-113">Properties</span></span>

<span data-ttu-id="b09a2-114">La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b09a2-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b09a2-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="b09a2-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b09a2-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b09a2-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b09a2-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b09a2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b09a2-118">TRUE si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b09a2-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b09a2-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="b09a2-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b09a2-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09a2-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b09a2-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b09a2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b09a2-122">Nombre d’enregistrements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b09a2-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="b09a2-123">**Enregistrements**</span><span class="sxs-lookup"><span data-stu-id="b09a2-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b09a2-124">Type de données : tableau d' **\_ entrée MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="b09a2-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="b09a2-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b09a2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b09a2-126">Tableau d’enregistrements d’erreurs MCA.</span><span class="sxs-lookup"><span data-stu-id="b09a2-126">Array of MCA error records.</span></span> <span data-ttu-id="b09a2-127">Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="b09a2-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b09a2-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b09a2-128">Remarks</span></span>

<span data-ttu-id="b09a2-129">La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="b09a2-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b09a2-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b09a2-130">Requirements</span></span>



| <span data-ttu-id="b09a2-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b09a2-131">Requirement</span></span> | <span data-ttu-id="b09a2-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b09a2-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b09a2-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b09a2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b09a2-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b09a2-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b09a2-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b09a2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b09a2-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b09a2-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b09a2-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b09a2-137">Namespace</span></span><br/>                | <span data-ttu-id="b09a2-138">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="b09a2-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b09a2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b09a2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b09a2-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b09a2-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b09a2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b09a2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b09a2-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b09a2-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09a2-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b09a2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09a2-144">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="b09a2-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b09a2-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="b09a2-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 





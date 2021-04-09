---
description: Contient un événement MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Classe MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952687"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="7ba24-104">MSMCAInfo \_ RawMCAEvent, classe</span><span class="sxs-lookup"><span data-stu-id="7ba24-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="7ba24-105">La classe **MSMCAInfo \_ RawMCAEvent** contient un événement MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="7ba24-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="7ba24-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7ba24-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="7ba24-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7ba24-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7ba24-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7ba24-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba24-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ba24-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="7ba24-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7ba24-110">Members</span></span>

<span data-ttu-id="7ba24-111">La classe **MSMCAInfo \_ RawMCAEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7ba24-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="7ba24-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ba24-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ba24-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ba24-113">Properties</span></span>

<span data-ttu-id="7ba24-114">La classe **MSMCAInfo \_ RawMCAEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ba24-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ba24-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="7ba24-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba24-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7ba24-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba24-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ba24-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba24-118">TRUE si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7ba24-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7ba24-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="7ba24-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba24-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ba24-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba24-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ba24-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba24-122">Nombre d’enregistrements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7ba24-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="7ba24-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7ba24-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba24-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ba24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba24-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ba24-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba24-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7ba24-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7ba24-127">Chaîne qui identifie de façon unique cette instance de la classe **MSMCAInfo \_ RawMCAEvent** .</span><span class="sxs-lookup"><span data-stu-id="7ba24-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="7ba24-128">**Enregistrements**</span><span class="sxs-lookup"><span data-stu-id="7ba24-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba24-129">Type de données : tableau d' **\_ entrée MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="7ba24-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="7ba24-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ba24-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba24-131">Tableau d’enregistrements d’erreurs MCA.</span><span class="sxs-lookup"><span data-stu-id="7ba24-131">Array of MCA error records.</span></span> <span data-ttu-id="7ba24-132">Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="7ba24-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ba24-133">Notes</span><span class="sxs-lookup"><span data-stu-id="7ba24-133">Remarks</span></span>

<span data-ttu-id="7ba24-134">La classe **MSMCAInfo \_ RawMCAEvent** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="7ba24-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba24-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ba24-135">Requirements</span></span>



| <span data-ttu-id="7ba24-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ba24-136">Requirement</span></span> | <span data-ttu-id="7ba24-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ba24-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba24-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ba24-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba24-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ba24-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7ba24-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ba24-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba24-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ba24-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7ba24-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ba24-142">Namespace</span></span><br/>                | <span data-ttu-id="7ba24-143">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="7ba24-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7ba24-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7ba24-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ba24-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ba24-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ba24-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba24-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba24-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba24-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ba24-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ba24-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba24-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="7ba24-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="7ba24-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="7ba24-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


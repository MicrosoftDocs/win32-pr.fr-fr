---
description: Spécifie les journaux MCA (machine Check architecture) bruts. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Classe MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526103"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="b2830-104">MSMCAInfo \_ RawMCAData, classe</span><span class="sxs-lookup"><span data-stu-id="b2830-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="b2830-105">**MSMCAInfo \_ RawMCAData** spécifie les journaux MCA (machine Check architecture) bruts.</span><span class="sxs-lookup"><span data-stu-id="b2830-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="b2830-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b2830-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b2830-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b2830-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b2830-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b2830-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2830-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2830-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="b2830-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b2830-110">Members</span></span>

<span data-ttu-id="b2830-111">La classe **MSMCAInfo \_ RawMCAData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2830-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2830-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2830-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2830-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2830-113">Properties</span></span>

<span data-ttu-id="b2830-114">La classe **MSMCAInfo \_ RawMCAData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2830-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2830-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="b2830-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2830-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b2830-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2830-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2830-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2830-118">TRUE si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b2830-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b2830-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="b2830-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2830-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2830-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2830-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2830-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2830-122">Nombre d’enregistrements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b2830-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="b2830-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b2830-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2830-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2830-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2830-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2830-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2830-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2830-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2830-127">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="b2830-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="b2830-128">**Enregistrements**</span><span class="sxs-lookup"><span data-stu-id="b2830-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2830-129">Type de données : tableau d' **\_ entrée MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="b2830-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="b2830-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2830-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2830-131">Tableau d’enregistrements d’erreurs MCA.</span><span class="sxs-lookup"><span data-stu-id="b2830-131">Array of MCA error records.</span></span> <span data-ttu-id="b2830-132">Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .</span><span class="sxs-lookup"><span data-stu-id="b2830-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2830-133">Notes</span><span class="sxs-lookup"><span data-stu-id="b2830-133">Remarks</span></span>

<span data-ttu-id="b2830-134">La classe **MSMCAInfo \_ RawMCAData** est dérivée de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="b2830-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2830-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2830-135">Requirements</span></span>



| <span data-ttu-id="b2830-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2830-136">Requirement</span></span> | <span data-ttu-id="b2830-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2830-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2830-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2830-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b2830-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2830-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b2830-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2830-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b2830-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2830-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b2830-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2830-142">Namespace</span></span><br/>                | <span data-ttu-id="b2830-143">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="b2830-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b2830-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b2830-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2830-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2830-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2830-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b2830-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2830-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2830-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2830-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2830-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2830-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="b2830-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b2830-150">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="b2830-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 


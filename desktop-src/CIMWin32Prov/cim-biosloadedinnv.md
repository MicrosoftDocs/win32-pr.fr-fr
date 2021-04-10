---
description: La \_ classe CIM BIOSLoadedInNV associe un élément BIOS et le stockage non volatile dans lequel elle est chargée.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: Classe CIM_BIOSLoadedInNV
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950707"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="e1109-103">\_Classe CIM BIOSLoadedInNV</span><span class="sxs-lookup"><span data-stu-id="e1109-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="e1109-104">La classe **CIM \_ BIOSLoadedInNV** associe un élément BIOS et le stockage non volatile dans lequel elle est chargée.</span><span class="sxs-lookup"><span data-stu-id="e1109-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1109-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e1109-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1109-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1109-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e1109-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e1109-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e1109-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e1109-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1109-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1109-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="e1109-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e1109-110">Members</span></span>

<span data-ttu-id="e1109-111">La classe **CIM \_ BIOSLoadedInNV** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e1109-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="e1109-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1109-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1109-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1109-113">Properties</span></span>

<span data-ttu-id="e1109-114">La classe **CIM \_ BIOSLoadedInNV** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1109-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1109-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e1109-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1109-116">Type de données : **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="e1109-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="e1109-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1109-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1109-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e1109-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e1109-119">[**\_ NonVolatileStorage CIM**](cim-nonvolatilestorage.md) qui décrit le stockage non volatile.</span><span class="sxs-lookup"><span data-stu-id="e1109-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="e1109-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e1109-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1109-121">Type de données : **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="e1109-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="e1109-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1109-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1109-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e1109-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e1109-124">[**\_ BIOSElement CIM**](cim-bioselement.md) qui décrit le BIOS stocké dans l’étendue non volatile.</span><span class="sxs-lookup"><span data-stu-id="e1109-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="e1109-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="e1109-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1109-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1109-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1109-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1109-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1109-128">Adresse de fin où le BIOS se trouve dans un stockage non volatile.</span><span class="sxs-lookup"><span data-stu-id="e1109-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="e1109-129">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e1109-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e1109-130">**De la**</span><span class="sxs-lookup"><span data-stu-id="e1109-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1109-131">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1109-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1109-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1109-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1109-133">Adresse de départ où le BIOS se trouve dans un stockage non volatile.</span><span class="sxs-lookup"><span data-stu-id="e1109-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="e1109-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e1109-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1109-135">Notes</span><span class="sxs-lookup"><span data-stu-id="e1109-135">Remarks</span></span>

<span data-ttu-id="e1109-136">La classe **CIM \_ BIOSLoadedInNV** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e1109-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e1109-137">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e1109-137">WMI does not implement this class.</span></span>

<span data-ttu-id="e1109-138">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1109-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1109-139">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e1109-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1109-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1109-140">Requirements</span></span>



| <span data-ttu-id="e1109-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1109-141">Requirement</span></span> | <span data-ttu-id="e1109-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1109-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1109-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1109-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e1109-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1109-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1109-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1109-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e1109-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1109-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1109-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1109-147">Namespace</span></span><br/>                | <span data-ttu-id="e1109-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e1109-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1109-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e1109-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1109-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1109-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1109-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e1109-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1109-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1109-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1109-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1109-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1109-154">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e1109-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


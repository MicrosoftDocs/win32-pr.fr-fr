---
description: La \_ classe d’association CIM DeviceAccessedByFile spécifie l’appareil logique accessible à l’aide de la classe CIM DeviceFile référencée \_ .
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: Classe CIM_DeviceAccessedByFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861269"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="51b6e-103">\_Classe CIM DeviceAccessedByFile</span><span class="sxs-lookup"><span data-stu-id="51b6e-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="51b6e-104">La classe d’association **CIM \_ DeviceAccessedByFile** spécifie l’appareil logique accessible à l’aide de la classe [**CIM \_ DeviceFile**](cim-devicefile.md) référencée.</span><span class="sxs-lookup"><span data-stu-id="51b6e-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51b6e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="51b6e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="51b6e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="51b6e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="51b6e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="51b6e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51b6e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="51b6e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b6e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51b6e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="51b6e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="51b6e-110">Members</span></span>

<span data-ttu-id="51b6e-111">La classe **CIM \_ DeviceAccessedByFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="51b6e-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="51b6e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51b6e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51b6e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51b6e-113">Properties</span></span>

<span data-ttu-id="51b6e-114">La classe **CIM \_ DeviceAccessedByFile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="51b6e-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51b6e-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="51b6e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51b6e-116">Type de données : **CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="51b6e-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="51b6e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51b6e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51b6e-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="51b6e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="51b6e-119">[**\_ DeviceFile CIM**](cim-devicefile.md) qui décrit le fichier de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="51b6e-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="51b6e-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="51b6e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51b6e-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="51b6e-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="51b6e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51b6e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51b6e-123">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="51b6e-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="51b6e-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil accessible à l’aide du fichier d’appareil.</span><span class="sxs-lookup"><span data-stu-id="51b6e-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51b6e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="51b6e-125">Remarks</span></span>

<span data-ttu-id="51b6e-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="51b6e-126">WMI does not implement this class.</span></span>

<span data-ttu-id="51b6e-127">La classe **CIM \_ DeviceAccessedByFile** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="51b6e-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="51b6e-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="51b6e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="51b6e-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="51b6e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b6e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51b6e-130">Requirements</span></span>



| <span data-ttu-id="51b6e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51b6e-131">Requirement</span></span> | <span data-ttu-id="51b6e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="51b6e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51b6e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51b6e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="51b6e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51b6e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51b6e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51b6e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="51b6e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51b6e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51b6e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="51b6e-137">Namespace</span></span><br/>                | <span data-ttu-id="51b6e-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="51b6e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51b6e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="51b6e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51b6e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51b6e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51b6e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="51b6e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51b6e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51b6e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b6e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51b6e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b6e-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="51b6e-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


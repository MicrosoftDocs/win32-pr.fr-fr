---
description: La \_ classe CIM DeviceSAPImplementation représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: CIM_DeviceSAPImplementation, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748700"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="545af-103">CIM_DeviceSAPImplementation, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="545af-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="545af-104">La classe **CIM \_ DeviceSAPImplementation** représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté.</span><span class="sxs-lookup"><span data-stu-id="545af-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="545af-105">Lorsque de nombreux périphériques logiques sont associés à un SAP, les éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="545af-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="545af-106">Si différentes implémentations d’un SAP existent, chaque implémentation entraîne des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="545af-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="545af-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="545af-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="545af-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="545af-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="545af-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="545af-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="545af-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="545af-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="545af-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="545af-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="545af-112">Membres</span><span class="sxs-lookup"><span data-stu-id="545af-112">Members</span></span>

<span data-ttu-id="545af-113">La classe **CIM \_ DeviceSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="545af-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="545af-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="545af-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="545af-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="545af-115">Properties</span></span>

<span data-ttu-id="545af-116">La classe **CIM \_ DeviceSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="545af-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="545af-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="545af-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545af-118">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="545af-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="545af-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545af-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545af-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="545af-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="545af-121">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="545af-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="545af-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="545af-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545af-123">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="545af-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="545af-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545af-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545af-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="545af-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="545af-126">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service implémenté à l’aide de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="545af-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="545af-127">Notes</span><span class="sxs-lookup"><span data-stu-id="545af-127">Remarks</span></span>

<span data-ttu-id="545af-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="545af-128">WMI does not implement this class.</span></span>

<span data-ttu-id="545af-129">La classe **CIM \_ DeviceSAPImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="545af-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="545af-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="545af-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="545af-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="545af-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="545af-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="545af-132">Requirements</span></span>



| <span data-ttu-id="545af-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="545af-133">Requirement</span></span> | <span data-ttu-id="545af-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="545af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="545af-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="545af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="545af-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="545af-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="545af-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="545af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="545af-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="545af-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="545af-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="545af-139">Namespace</span></span><br/>                | <span data-ttu-id="545af-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="545af-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="545af-141">MOF</span><span class="sxs-lookup"><span data-stu-id="545af-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="545af-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="545af-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="545af-143">DLL</span><span class="sxs-lookup"><span data-stu-id="545af-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="545af-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="545af-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545af-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="545af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545af-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="545af-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


---
description: La \_ classe CIM DeviceServiceImplementation représente une association entre un service et la manière dont il est implémenté.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: Classe CIM_DeviceServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950725"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="4b887-103">\_Classe CIM DeviceServiceImplementation</span><span class="sxs-lookup"><span data-stu-id="4b887-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="4b887-104">La classe **CIM \_ DeviceServiceImplementation** représente une association entre un service et la manière dont il est implémenté.</span><span class="sxs-lookup"><span data-stu-id="4b887-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="4b887-105">Lorsque plusieurs appareils sont associés à un service, les éléments fonctionnent conjointement pour fournir le service.</span><span class="sxs-lookup"><span data-stu-id="4b887-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="4b887-106">Si différentes implémentations d’un service existent, chaque implémentation produit des instanciations individuelles de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="4b887-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b887-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4b887-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b887-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b887-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b887-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4b887-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b887-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4b887-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b887-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b887-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4b887-112">Membres</span><span class="sxs-lookup"><span data-stu-id="4b887-112">Members</span></span>

<span data-ttu-id="4b887-113">La classe **CIM \_ DeviceServiceImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b887-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="4b887-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b887-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b887-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b887-115">Properties</span></span>

<span data-ttu-id="4b887-116">La classe **CIM \_ DeviceServiceImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b887-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b887-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4b887-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b887-118">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="4b887-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4b887-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b887-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b887-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4b887-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4b887-121">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4b887-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4b887-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4b887-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b887-123">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="4b887-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="4b887-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b887-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b887-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4b887-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4b887-126">[**\_ Service CIM**](cim-service.md) qui décrit le service implémenté à l’aide de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4b887-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b887-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4b887-127">Remarks</span></span>

<span data-ttu-id="4b887-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4b887-128">WMI does not implement this class.</span></span>

<span data-ttu-id="4b887-129">La classe **CIM \_ DeviceServiceImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4b887-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4b887-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b887-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b887-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4b887-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b887-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b887-132">Requirements</span></span>



| <span data-ttu-id="4b887-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b887-133">Requirement</span></span> | <span data-ttu-id="4b887-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b887-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b887-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b887-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4b887-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b887-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b887-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b887-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4b887-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b887-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b887-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b887-139">Namespace</span></span><br/>                | <span data-ttu-id="4b887-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4b887-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b887-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4b887-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b887-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b887-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b887-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4b887-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b887-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b887-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b887-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b887-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b887-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="4b887-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


---
description: La \_ classe CIM AllocatedResource représente une association entre les unités logiques et les ressources système et indique que la ressource est affectée à l’appareil.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: Classe CIM_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111102"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="7153d-103">\_Classe CIM AllocatedResource</span><span class="sxs-lookup"><span data-stu-id="7153d-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="7153d-104">La classe **CIM \_ AllocatedResource** représente une association entre les unités logiques et les ressources système et indique que la ressource est affectée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7153d-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7153d-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="7153d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7153d-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7153d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7153d-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7153d-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7153d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7153d-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7153d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7153d-109">Members</span></span>

<span data-ttu-id="7153d-110">La classe **CIM \_ AllocatedResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7153d-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="7153d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7153d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7153d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7153d-112">Properties</span></span>

<span data-ttu-id="7153d-113">La classe **CIM \_ AllocatedResource** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7153d-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7153d-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7153d-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7153d-115">Type de données : **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="7153d-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="7153d-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7153d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7153d-117">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7153d-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7153d-118">[**\_ SystemResource CIM**](cim-systemresource.md) qui décrit la ressource.</span><span class="sxs-lookup"><span data-stu-id="7153d-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7153d-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7153d-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7153d-120">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="7153d-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7153d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7153d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7153d-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="7153d-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7153d-123">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui contient l’unité logique à laquelle la ressource est affectée.</span><span class="sxs-lookup"><span data-stu-id="7153d-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7153d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7153d-124">Remarks</span></span>

<span data-ttu-id="7153d-125">La classe **CIM \_ AllocatedResource** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7153d-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7153d-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="7153d-126">WMI does not implement this class.</span></span> <span data-ttu-id="7153d-127">Pour plus d’informations sur les classes dérivées de **CIM \_ AllocatedResource**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7153d-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7153d-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="7153d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7153d-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7153d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7153d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7153d-130">Requirements</span></span>



| <span data-ttu-id="7153d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7153d-131">Requirement</span></span> | <span data-ttu-id="7153d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7153d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7153d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7153d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7153d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7153d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7153d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7153d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7153d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7153d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7153d-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7153d-137">Namespace</span></span><br/>                | <span data-ttu-id="7153d-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7153d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7153d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7153d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7153d-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7153d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7153d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7153d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7153d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7153d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7153d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7153d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7153d-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="7153d-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


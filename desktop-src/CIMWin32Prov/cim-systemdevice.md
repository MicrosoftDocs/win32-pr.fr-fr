---
description: L' \_ Association CIM SystemDevice représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: CIM_SystemDevice, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516383"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="9068f-103">CIM_SystemDevice, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9068f-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9068f-104">L’Association **CIM \_ SystemDevice** représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.</span><span class="sxs-lookup"><span data-stu-id="9068f-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9068f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9068f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9068f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9068f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9068f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9068f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9068f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9068f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9068f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9068f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9068f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9068f-110">Members</span></span>

<span data-ttu-id="9068f-111">La classe **CIM \_ SystemDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9068f-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="9068f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9068f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9068f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9068f-113">Properties</span></span>

<span data-ttu-id="9068f-114">La classe **CIM \_ SystemDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9068f-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9068f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9068f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9068f-116">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="9068f-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="9068f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9068f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9068f-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9068f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9068f-119">[**\_ Système CIM**](cim-system.md) qui décrit le système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9068f-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="9068f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9068f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9068f-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="9068f-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9068f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9068f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9068f-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9068f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9068f-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil logique qui est un composant d’un système.</span><span class="sxs-lookup"><span data-stu-id="9068f-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9068f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9068f-125">Remarks</span></span>

<span data-ttu-id="9068f-126">La classe **CIM \_ SystemDevice** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9068f-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="9068f-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9068f-127">WMI does not implement this class.</span></span> <span data-ttu-id="9068f-128">Pour les classes WMI dérivées de **CIM \_ SystemDevice**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9068f-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9068f-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9068f-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9068f-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9068f-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9068f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9068f-131">Requirements</span></span>



| <span data-ttu-id="9068f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9068f-132">Requirement</span></span> | <span data-ttu-id="9068f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9068f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9068f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9068f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9068f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9068f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9068f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9068f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9068f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9068f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9068f-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9068f-138">Namespace</span></span><br/>                | <span data-ttu-id="9068f-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9068f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9068f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9068f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9068f-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9068f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9068f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9068f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9068f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9068f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9068f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9068f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9068f-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9068f-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


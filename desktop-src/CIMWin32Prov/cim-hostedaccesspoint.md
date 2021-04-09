---
description: La \_ classe CIM HostedAccessPoint représente une association entre un point d’accès de service (SAP) et le système sur lequel il est fourni. Chaque système peut héberger de nombreuses SAP.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: CIM_HostedAccessPoint, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110858"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="0bd28-104">CIM_HostedAccessPoint, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0bd28-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0bd28-105">La classe **CIM \_ HostedAccessPoint** représente une association entre un point d’accès de service (SAP) et le système sur lequel il est fourni.</span><span class="sxs-lookup"><span data-stu-id="0bd28-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="0bd28-106">Chaque système peut héberger de nombreuses SAP.</span><span class="sxs-lookup"><span data-stu-id="0bd28-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bd28-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0bd28-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0bd28-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0bd28-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0bd28-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0bd28-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0bd28-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0bd28-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd28-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd28-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0bd28-112">Membres</span><span class="sxs-lookup"><span data-stu-id="0bd28-112">Members</span></span>

<span data-ttu-id="0bd28-113">La classe **CIM \_ HostedAccessPoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0bd28-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="0bd28-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bd28-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bd28-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bd28-115">Properties</span></span>

<span data-ttu-id="0bd28-116">La classe **CIM \_ HostedAccessPoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0bd28-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bd28-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="0bd28-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bd28-118">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="0bd28-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="0bd28-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bd28-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bd28-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0bd28-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0bd28-121">[**\_ Système CIM**](cim-system.md) qui décrit le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="0bd28-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="0bd28-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="0bd28-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bd28-123">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="0bd28-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="0bd28-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bd28-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bd28-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bd28-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bd28-126">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le ou les SAP qui sont hébergés sur ce système.</span><span class="sxs-lookup"><span data-stu-id="0bd28-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bd28-127">Notes</span><span class="sxs-lookup"><span data-stu-id="0bd28-127">Remarks</span></span>

<span data-ttu-id="0bd28-128">**CIM \_ HostedAccessPoint** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0bd28-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0bd28-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0bd28-129">WMI does not implement this class.</span></span>

<span data-ttu-id="0bd28-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0bd28-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0bd28-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0bd28-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd28-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bd28-132">Requirements</span></span>



| <span data-ttu-id="0bd28-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bd28-133">Requirement</span></span> | <span data-ttu-id="0bd28-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd28-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd28-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bd28-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd28-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bd28-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bd28-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bd28-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd28-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bd28-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bd28-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0bd28-139">Namespace</span></span><br/>                | <span data-ttu-id="0bd28-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0bd28-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bd28-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0bd28-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bd28-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bd28-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bd28-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0bd28-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bd28-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bd28-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd28-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bd28-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd28-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="0bd28-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


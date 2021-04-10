---
description: La \_ classe CIM HostedBootSAP définit le système informatique unitaire d’hébergement pour une \_ classe CIM BootSAP.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: Classe CIM_HostedBootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950650"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="2e397-103">\_Classe CIM HostedBootSAP</span><span class="sxs-lookup"><span data-stu-id="2e397-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="2e397-104">La classe **CIM \_ HostedBootSAP** définit le système informatique unitaire d’hébergement pour une classe [**CIM \_ BootSAP**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="2e397-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="2e397-105">Étant donné que cette relation est sous-classée à partir de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md), où un point d’accès défère au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="2e397-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="2e397-106">Dans ce cas, **le \_ BootSAP CIM** doit être différé à sa classe [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="2e397-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e397-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2e397-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e397-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e397-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e397-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2e397-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2e397-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2e397-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e397-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e397-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2e397-112">Membres</span><span class="sxs-lookup"><span data-stu-id="2e397-112">Members</span></span>

<span data-ttu-id="2e397-113">La classe **CIM \_ HostedBootSAP** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e397-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="2e397-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e397-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e397-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e397-115">Properties</span></span>

<span data-ttu-id="2e397-116">La classe **CIM \_ HostedBootSAP** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e397-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e397-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2e397-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e397-118">Type de données : **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="2e397-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2e397-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e397-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e397-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2e397-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2e397-121">[**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) qui décrit le système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="2e397-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2e397-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2e397-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e397-123">Type de données : **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="2e397-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="2e397-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e397-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e397-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="2e397-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2e397-126">[**\_ BootSAP CIM**](cim-bootsap.md) qui décrit le démarrage de SAP hébergé sur le système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="2e397-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e397-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2e397-127">Remarks</span></span>

<span data-ttu-id="2e397-128">La classe **CIM \_ HostedBootSAP** est dérivée de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="2e397-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="2e397-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2e397-129">WMI does not implement this class.</span></span>

<span data-ttu-id="2e397-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e397-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e397-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2e397-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e397-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e397-132">Requirements</span></span>



| <span data-ttu-id="2e397-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e397-133">Requirement</span></span> | <span data-ttu-id="2e397-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e397-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e397-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e397-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2e397-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e397-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e397-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e397-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2e397-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e397-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e397-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e397-139">Namespace</span></span><br/>                | <span data-ttu-id="2e397-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2e397-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e397-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2e397-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e397-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e397-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e397-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2e397-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e397-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e397-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e397-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e397-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e397-146">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="2e397-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 


---
description: La \_ classe SAPSAPDEPENDENCY CIM est une association entre deux points d’accès de service (SAP), qui indique que le deuxième SAP est requis pour que le premier SAP se connecte à son service.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: CIM_SAPSAPDependency, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950518"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="adc22-103">CIM_SAPSAPDependency, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="adc22-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="adc22-104">La **classe \_ SAPSAPDependency CIM** est une association entre deux points d’accès de service (SAP), qui indique que le deuxième SAP est requis pour que le premier SAP se connecte à son service.</span><span class="sxs-lookup"><span data-stu-id="adc22-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="adc22-105">Par exemple, pour imprimer sur une imprimante réseau, les points d’accès de l’imprimante locale doivent utiliser des SAP liés au réseau sous-jacents ou des points de terminaison de protocole pour envoyer la demande d’impression.</span><span class="sxs-lookup"><span data-stu-id="adc22-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adc22-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="adc22-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="adc22-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="adc22-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="adc22-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="adc22-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="adc22-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="adc22-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc22-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adc22-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="adc22-111">Membres</span><span class="sxs-lookup"><span data-stu-id="adc22-111">Members</span></span>

<span data-ttu-id="adc22-112">La classe **CIM \_ SAPSAPDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="adc22-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="adc22-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="adc22-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adc22-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="adc22-114">Properties</span></span>

<span data-ttu-id="adc22-115">La classe **CIM \_ SAPSAPDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="adc22-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adc22-116">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="adc22-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc22-117">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="adc22-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="adc22-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adc22-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc22-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="adc22-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="adc22-120">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service requis.</span><span class="sxs-lookup"><span data-stu-id="adc22-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="adc22-121">**Charge**</span><span class="sxs-lookup"><span data-stu-id="adc22-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc22-122">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="adc22-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="adc22-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adc22-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc22-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="adc22-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="adc22-125">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service qui dépend d’un SAP sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="adc22-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adc22-126">Notes</span><span class="sxs-lookup"><span data-stu-id="adc22-126">Remarks</span></span>

<span data-ttu-id="adc22-127">La classe **CIM \_ SAPSAPDependency** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="adc22-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="adc22-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="adc22-128">WMI does not implement this class.</span></span>

<span data-ttu-id="adc22-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="adc22-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="adc22-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="adc22-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc22-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adc22-131">Requirements</span></span>



| <span data-ttu-id="adc22-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adc22-132">Requirement</span></span> | <span data-ttu-id="adc22-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="adc22-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adc22-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adc22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="adc22-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adc22-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="adc22-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adc22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="adc22-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adc22-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="adc22-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="adc22-138">Namespace</span></span><br/>                | <span data-ttu-id="adc22-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="adc22-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="adc22-140">MOF</span><span class="sxs-lookup"><span data-stu-id="adc22-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adc22-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adc22-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="adc22-142">DLL</span><span class="sxs-lookup"><span data-stu-id="adc22-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adc22-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc22-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc22-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adc22-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc22-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="adc22-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


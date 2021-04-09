---
description: La \_ classe CIM ServiceSAPDependency représente une association entre un service et un point d’accès au service (SAP), qui indique que le SAP référencé est utilisé par le service pour fournir ses fonctionnalités.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: CIM_ServiceSAPDependency, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110610"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="fd0ae-103">CIM_ServiceSAPDependency, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="fd0ae-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fd0ae-104">La classe **CIM \_ ServiceSAPDependency** représente une association entre un service et un point d’accès au service (SAP), qui indique que le SAP référencé est utilisé par le service pour fournir ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="fd0ae-105">Par exemple, les services de démarrage peuvent appeler des services de disque BIOS (interruptions) pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd0ae-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd0ae-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd0ae-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd0ae-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fd0ae-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0ae-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd0ae-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fd0ae-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fd0ae-111">Members</span></span>

<span data-ttu-id="fd0ae-112">La classe **CIM \_ ServiceSAPDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd0ae-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="fd0ae-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd0ae-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd0ae-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd0ae-114">Properties</span></span>

<span data-ttu-id="fd0ae-115">La classe **CIM \_ ServiceSAPDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd0ae-116">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fd0ae-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd0ae-117">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="fd0ae-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="fd0ae-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd0ae-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd0ae-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fd0ae-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fd0ae-120">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service requis.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="fd0ae-121">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fd0ae-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd0ae-122">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="fd0ae-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="fd0ae-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd0ae-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd0ae-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="fd0ae-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fd0ae-125">[**\_ Service CIM**](cim-service.md) qui décrit le service qui dépend d’un SAP sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd0ae-126">Notes</span><span class="sxs-lookup"><span data-stu-id="fd0ae-126">Remarks</span></span>

<span data-ttu-id="fd0ae-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-127">WMI does not implement this class.</span></span>

<span data-ttu-id="fd0ae-128">La classe **CIM \_ ServiceSAPDependency** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fd0ae-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fd0ae-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fd0ae-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fd0ae-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0ae-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd0ae-131">Requirements</span></span>



| <span data-ttu-id="fd0ae-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd0ae-132">Requirement</span></span> | <span data-ttu-id="fd0ae-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd0ae-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0ae-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0ae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0ae-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd0ae-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd0ae-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0ae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0ae-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd0ae-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd0ae-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd0ae-138">Namespace</span></span><br/>                | <span data-ttu-id="fd0ae-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fd0ae-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd0ae-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fd0ae-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd0ae-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ae-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd0ae-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fd0ae-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd0ae-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ae-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0ae-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd0ae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0ae-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="fd0ae-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


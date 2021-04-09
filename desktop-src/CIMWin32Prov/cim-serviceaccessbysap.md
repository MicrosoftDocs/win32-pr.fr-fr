---
description: La \_ classe d’association CIM ServiceAccessBySAP représente les points d’accès pour un service. Par exemple, il est possible d’accéder à une imprimante par des points d’accès SAP, Macintosh ou de service Windows, qui sont potentiellement hébergés sur différents systèmes.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950590"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="d026e-104">\_Classe CIM ServiceAccessBySAP</span><span class="sxs-lookup"><span data-stu-id="d026e-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="d026e-105">La classe d’association **CIM \_ ServiceAccessBySAP** représente les points d’accès pour un service.</span><span class="sxs-lookup"><span data-stu-id="d026e-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="d026e-106">Par exemple, il est possible d’accéder à une imprimante par des points d’accès SAP, Macintosh ou de service Windows, qui sont potentiellement hébergés sur différents systèmes.</span><span class="sxs-lookup"><span data-stu-id="d026e-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d026e-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d026e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d026e-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d026e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d026e-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d026e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d026e-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d026e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d026e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d026e-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d026e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="d026e-112">Members</span></span>

<span data-ttu-id="d026e-113">La classe **CIM \_ ServiceAccessBySAP** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d026e-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="d026e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d026e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d026e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d026e-115">Properties</span></span>

<span data-ttu-id="d026e-116">La classe **CIM \_ ServiceAccessBySAP** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d026e-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d026e-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d026e-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d026e-118">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="d026e-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d026e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d026e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d026e-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d026e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d026e-121">[**\_ Service CIM**](cim-service.md) qui décrit le service.</span><span class="sxs-lookup"><span data-stu-id="d026e-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="d026e-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d026e-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d026e-123">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="d026e-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d026e-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d026e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d026e-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="d026e-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d026e-126">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit un point d’accès pour un service.</span><span class="sxs-lookup"><span data-stu-id="d026e-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="d026e-127">Les points d’accès sont dépendants de cette relation, car ils n’ont aucune fonction sans service correspondant.</span><span class="sxs-lookup"><span data-stu-id="d026e-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d026e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d026e-128">Remarks</span></span>

<span data-ttu-id="d026e-129">La classe **CIM \_ ServiceAccessBySAP** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d026e-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d026e-130">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d026e-130">WMI does not implement this class.</span></span> <span data-ttu-id="d026e-131">Pour les classes WMI dérivées de **CIM \_ ServiceAccessBySAP**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d026e-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d026e-132">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d026e-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d026e-133">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d026e-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d026e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d026e-134">Requirements</span></span>



| <span data-ttu-id="d026e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d026e-135">Requirement</span></span> | <span data-ttu-id="d026e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d026e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d026e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d026e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d026e-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d026e-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d026e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d026e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d026e-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d026e-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d026e-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d026e-141">Namespace</span></span><br/>                | <span data-ttu-id="d026e-142">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d026e-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d026e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d026e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d026e-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d026e-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d026e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d026e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d026e-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d026e-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d026e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d026e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d026e-148">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="d026e-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


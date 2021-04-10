---
description: La \_ classe CIM ClusterServiceAccessBySAP représente la relation entre un service de clustering et ses points d’accès.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: Classe CIM_ClusterServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950702"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="67313-103">\_Classe CIM ClusterServiceAccessBySAP</span><span class="sxs-lookup"><span data-stu-id="67313-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="67313-104">La classe **CIM \_ ClusterServiceAccessBySAP** représente la relation entre un service de clustering et ses points d’accès.</span><span class="sxs-lookup"><span data-stu-id="67313-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67313-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="67313-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="67313-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="67313-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="67313-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="67313-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="67313-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="67313-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67313-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67313-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="67313-110">Membres</span><span class="sxs-lookup"><span data-stu-id="67313-110">Members</span></span>

<span data-ttu-id="67313-111">La classe **CIM \_ ClusterServiceAccessBySAP** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67313-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="67313-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67313-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67313-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67313-113">Properties</span></span>

<span data-ttu-id="67313-114">La classe **CIM \_ ClusterServiceAccessBySAP** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="67313-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67313-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="67313-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67313-116">Type de données : **CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="67313-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="67313-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67313-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67313-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="67313-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="67313-119">[**\_ ClusteringService CIM**](cim-clusteringservice.md) qui décrit le service de clustering.</span><span class="sxs-lookup"><span data-stu-id="67313-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="67313-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="67313-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67313-121">Type de données : **CIM \_ ClusteringSAP**</span><span class="sxs-lookup"><span data-stu-id="67313-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="67313-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67313-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67313-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="67313-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="67313-124">[**\_ ClusteringSAP CIM**](cim-clusteringsap.md) qui décrit un point d’accès pour le service de clustering.</span><span class="sxs-lookup"><span data-stu-id="67313-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67313-125">Notes</span><span class="sxs-lookup"><span data-stu-id="67313-125">Remarks</span></span>

<span data-ttu-id="67313-126">La classe **CIM \_ ClusterServiceAccessBySAP** est dérivée de [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="67313-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="67313-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="67313-127">WMI does not implement this class.</span></span>

<span data-ttu-id="67313-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="67313-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="67313-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="67313-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67313-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67313-130">Requirements</span></span>



| <span data-ttu-id="67313-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67313-131">Requirement</span></span> | <span data-ttu-id="67313-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="67313-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67313-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67313-133">Minimum supported client</span></span><br/> | <span data-ttu-id="67313-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67313-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67313-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67313-135">Minimum supported server</span></span><br/> | <span data-ttu-id="67313-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67313-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67313-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="67313-137">Namespace</span></span><br/>                | <span data-ttu-id="67313-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="67313-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67313-139">MOF</span><span class="sxs-lookup"><span data-stu-id="67313-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67313-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67313-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67313-141">DLL</span><span class="sxs-lookup"><span data-stu-id="67313-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67313-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67313-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67313-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67313-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67313-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="67313-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 


---
description: Représente une association dans laquelle un \_ objet CIM BaseMetricDefinition définit des métriques pour un élément managé.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: Classe CIM_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866418"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="7b296-103">\_Classe CIM MetricDefForME</span><span class="sxs-lookup"><span data-stu-id="7b296-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="7b296-104">Représente une association dans laquelle un objet [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) définit des métriques pour un élément managé.</span><span class="sxs-lookup"><span data-stu-id="7b296-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b296-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b296-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="7b296-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7b296-106">Members</span></span>

<span data-ttu-id="7b296-107">La classe **CIM \_ MetricDefForME** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b296-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="7b296-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b296-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b296-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b296-109">Properties</span></span>

<span data-ttu-id="7b296-110">La classe **CIM \_ MetricDefForME** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b296-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b296-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7b296-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b296-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="7b296-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="7b296-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b296-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b296-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7b296-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7b296-115">Élément managé associé à la définition de métrique.</span><span class="sxs-lookup"><span data-stu-id="7b296-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="7b296-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7b296-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b296-117">Type de données : **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="7b296-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="7b296-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b296-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b296-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="7b296-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7b296-120">Définition de métrique associée à l’élément géré.</span><span class="sxs-lookup"><span data-stu-id="7b296-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="7b296-121">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="7b296-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b296-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b296-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b296-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b296-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b296-124">Indique si la mesure est collectée pour l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="7b296-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7b296-125">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="7b296-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7b296-126">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="7b296-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="7b296-127">**Réservé** (4)</span><span class="sxs-lookup"><span data-stu-id="7b296-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7b296-128">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7b296-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7b296-129">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7b296-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="7b296-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7b296-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7b296-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b296-131">Requirements</span></span>



| <span data-ttu-id="7b296-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b296-132">Requirement</span></span> | <span data-ttu-id="7b296-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b296-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b296-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b296-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b296-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b296-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7b296-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b296-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b296-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b296-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7b296-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b296-138">Namespace</span></span><br/>                | <span data-ttu-id="7b296-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b296-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b296-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7b296-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b296-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b296-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b296-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7b296-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b296-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b296-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b296-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b296-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b296-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="7b296-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


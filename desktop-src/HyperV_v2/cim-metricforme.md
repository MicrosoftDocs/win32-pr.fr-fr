---
description: Représente une association dans laquelle des valeurs de métriques sont collectées pour un élément managé.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: Classe CIM_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530877"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="fc65e-103">\_Classe CIM MetricForME</span><span class="sxs-lookup"><span data-stu-id="fc65e-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="fc65e-104">Représente une association dans laquelle des valeurs de métriques sont collectées pour un élément managé.</span><span class="sxs-lookup"><span data-stu-id="fc65e-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc65e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc65e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fc65e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fc65e-106">Members</span></span>

<span data-ttu-id="fc65e-107">La classe **CIM \_ MetricForME** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fc65e-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="fc65e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc65e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc65e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc65e-109">Properties</span></span>

<span data-ttu-id="fc65e-110">La classe **CIM \_ MetricForME** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc65e-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc65e-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fc65e-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc65e-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fc65e-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fc65e-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc65e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc65e-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fc65e-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fc65e-115">Élément managé dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="fc65e-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="fc65e-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fc65e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc65e-117">Type de données : **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="fc65e-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="fc65e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc65e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc65e-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="fc65e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fc65e-120">Valeur de métrique dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="fc65e-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc65e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc65e-121">Requirements</span></span>



| <span data-ttu-id="fc65e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc65e-122">Requirement</span></span> | <span data-ttu-id="fc65e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc65e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc65e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc65e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc65e-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fc65e-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fc65e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc65e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc65e-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fc65e-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fc65e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fc65e-128">Namespace</span></span><br/>                | <span data-ttu-id="fc65e-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc65e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc65e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fc65e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc65e-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc65e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc65e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fc65e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc65e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc65e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc65e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc65e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc65e-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="fc65e-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


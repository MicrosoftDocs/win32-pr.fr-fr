---
description: Représente une association d’objets de valeur de métrique à leurs définitions de métriques.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Classe Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518671"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="b8377-103">MSVM \_ MetricInstance, classe</span><span class="sxs-lookup"><span data-stu-id="b8377-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="b8377-104">Représente une association d’objets de valeur de métrique à leurs définitions de métriques.</span><span class="sxs-lookup"><span data-stu-id="b8377-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="b8377-105">Cette association lie une instance de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) à son [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b8377-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="b8377-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b8377-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8377-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8377-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b8377-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b8377-108">Members</span></span>

<span data-ttu-id="b8377-109">La classe **MSVM \_ MetricInstance** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8377-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="b8377-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8377-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8377-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8377-111">Properties</span></span>

<span data-ttu-id="b8377-112">La classe **MSVM \_ MetricInstance** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8377-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8377-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b8377-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8377-114">Type de données : \* \* \* \* CIM \_ propriété ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b8377-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="b8377-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8377-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8377-116">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b8377-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8377-117">Référence à une instance de la classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui représente les définitions de métriques.</span><span class="sxs-lookup"><span data-stu-id="b8377-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="b8377-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b8377-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8377-119">Type de données : \* \* \* \* CIM \_ propriété ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b8377-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="b8377-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8377-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8377-121">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b8377-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8377-122">Référence à une instance de la classe [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) qui représente les métriques qui dépendent de l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="b8377-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8377-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8377-123">Requirements</span></span>



| <span data-ttu-id="b8377-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8377-124">Requirement</span></span> | <span data-ttu-id="b8377-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8377-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8377-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8377-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b8377-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8377-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8377-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8377-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b8377-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8377-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8377-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b8377-130">Namespace</span></span><br/>                | <span data-ttu-id="b8377-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8377-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8377-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b8377-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8377-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8377-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8377-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b8377-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8377-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8377-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 





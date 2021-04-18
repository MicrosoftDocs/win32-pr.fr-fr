---
description: Cette association lie un élément géré aux valeurs de mesure conservées pour celui-ci.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Classe Msvm_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522736"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="2e817-103">MSVM \_ MetricForME, classe</span><span class="sxs-lookup"><span data-stu-id="2e817-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="2e817-104">Cette association lie un élément géré aux valeurs de mesure conservées pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2e817-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="2e817-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2e817-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e817-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e817-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2e817-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2e817-107">Members</span></span>

<span data-ttu-id="2e817-108">La classe **MSVM \_ MetricForME** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e817-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="2e817-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e817-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e817-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e817-110">Properties</span></span>

<span data-ttu-id="2e817-111">La classe **MSVM \_ MetricForME** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e817-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e817-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2e817-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e817-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2e817-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2e817-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e817-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e817-115">Référence à une instance de la classe [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente l’élément managé dont les métriques sont définies par le **dépendant** maintenu.</span><span class="sxs-lookup"><span data-stu-id="2e817-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="2e817-116">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="2e817-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="2e817-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2e817-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e817-118">Type de données : \* \* \* \* CIM \_ BaseMetricValue \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2e817-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="2e817-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e817-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e817-120">Référence à une instance de la classe **\_ BaseMetricValue CIM** qui représente la mesure que l' **antécédent** a collectée pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2e817-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="2e817-121">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="2e817-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e817-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e817-122">Requirements</span></span>



| <span data-ttu-id="2e817-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e817-123">Requirement</span></span> | <span data-ttu-id="2e817-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e817-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e817-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e817-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e817-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e817-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e817-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e817-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e817-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e817-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e817-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e817-129">Namespace</span></span><br/>                | <span data-ttu-id="2e817-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e817-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e817-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2e817-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e817-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e817-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e817-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e817-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e817-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e817-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


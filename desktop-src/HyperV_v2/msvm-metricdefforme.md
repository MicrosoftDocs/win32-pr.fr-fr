---
description: Définit l’association entre un \_ BaseMetricDefinition MSVM et un \_ propriété ManagedElement CIM pour définir des mesures pour ce dernier. La définition des métriques est donnée au contexte par propriété ManagedElement, ce qui explique pourquoi la définition dépend de l’élément.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Classe Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525049"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="81bb0-104">MSVM \_ MetricDefForME, classe</span><span class="sxs-lookup"><span data-stu-id="81bb0-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="81bb0-105">Définit l’association entre un [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) et un [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) pour définir des mesures pour ce dernier.</span><span class="sxs-lookup"><span data-stu-id="81bb0-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="81bb0-106">La définition des métriques est donnée au contexte par propriété ManagedElement, ce qui explique pourquoi la définition dépend de l’élément.</span><span class="sxs-lookup"><span data-stu-id="81bb0-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="81bb0-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="81bb0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bb0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81bb0-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="81bb0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="81bb0-109">Members</span></span>

<span data-ttu-id="81bb0-110">La classe **MSVM \_ MetricDefForME** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="81bb0-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="81bb0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81bb0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81bb0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81bb0-112">Properties</span></span>

<span data-ttu-id="81bb0-113">La classe **MSVM \_ MetricDefForME** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="81bb0-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81bb0-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="81bb0-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bb0-115">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="81bb0-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="81bb0-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81bb0-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bb0-117">Référence à une instance de la classe [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente l’élément managé qui peut avoir des métriques du type défini par **dépendant** qui lui sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="81bb0-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="81bb0-118">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="81bb0-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="81bb0-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="81bb0-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bb0-120">Type de données : **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="81bb0-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="81bb0-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81bb0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bb0-122">Référence à une instance de la classe [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de la métrique à laquelle l' **antécédent** peut s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="81bb0-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="81bb0-123">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="81bb0-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="81bb0-124">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="81bb0-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bb0-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bb0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bb0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81bb0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bb0-127">Indique si la mesure définie par **Dependent** est collectée pour l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="81bb0-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="81bb0-128">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="81bb0-128">This will be one of the following values.</span></span>



| <span data-ttu-id="81bb0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="81bb0-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="81bb0-130">Signification</span><span class="sxs-lookup"><span data-stu-id="81bb0-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="81bb0-131"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="81bb0-132">La mesure est collectée.</span><span class="sxs-lookup"><span data-stu-id="81bb0-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="81bb0-133"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="81bb0-134">La mesure n’est pas collectée.</span><span class="sxs-lookup"><span data-stu-id="81bb0-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="81bb0-135"><dt>**Réservé**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="81bb0-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="81bb0-137">La métrique est collectée pour certains périphériques, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="81bb0-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81bb0-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81bb0-138">Requirements</span></span>



| <span data-ttu-id="81bb0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81bb0-139">Requirement</span></span> | <span data-ttu-id="81bb0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="81bb0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81bb0-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81bb0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="81bb0-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81bb0-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81bb0-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81bb0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="81bb0-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81bb0-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81bb0-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81bb0-145">Namespace</span></span><br/>                | <span data-ttu-id="81bb0-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="81bb0-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81bb0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="81bb0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81bb0-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81bb0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="81bb0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81bb0-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81bb0-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


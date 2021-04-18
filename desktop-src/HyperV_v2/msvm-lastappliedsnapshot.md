---
description: Représente une association entre un système virtuel et les données de paramètre de l’instantané qui a été appliqué en dernier au système virtuel.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Classe Msvm_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536367"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="34a3d-103">MSVM \_ LastAppliedSnapshot, classe</span><span class="sxs-lookup"><span data-stu-id="34a3d-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="34a3d-104">Représente une association entre un système virtuel et les données de paramètre de l’instantané qui a été appliqué en dernier au système virtuel.</span><span class="sxs-lookup"><span data-stu-id="34a3d-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="34a3d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="34a3d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a3d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34a3d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="34a3d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="34a3d-107">Members</span></span>

<span data-ttu-id="34a3d-108">La classe **MSVM \_ LastAppliedSnapshot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="34a3d-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="34a3d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34a3d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34a3d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34a3d-110">Properties</span></span>

<span data-ttu-id="34a3d-111">La classe **MSVM \_ LastAppliedSnapshot** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="34a3d-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34a3d-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="34a3d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a3d-113">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="34a3d-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="34a3d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="34a3d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a3d-115">Qualificateurs : **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="34a3d-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="34a3d-116">Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané du système virtuel qui a été appliqué en dernier au système virtuel.</span><span class="sxs-lookup"><span data-stu-id="34a3d-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="34a3d-117">Cette propriété est héritée de la **\_ dépendance CIM**.</span><span class="sxs-lookup"><span data-stu-id="34a3d-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="34a3d-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="34a3d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a3d-119">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="34a3d-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="34a3d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="34a3d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a3d-121">Qualificateurs : **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="34a3d-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="34a3d-122">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système virtuel sur lequel l’instantané de système virtuel représenté par la propriété **Antecedent** a été appliqué en dernier.</span><span class="sxs-lookup"><span data-stu-id="34a3d-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="34a3d-123">Cette propriété est héritée de la **\_ dépendance CIM**.</span><span class="sxs-lookup"><span data-stu-id="34a3d-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34a3d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34a3d-124">Requirements</span></span>



| <span data-ttu-id="34a3d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34a3d-125">Requirement</span></span> | <span data-ttu-id="34a3d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a3d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a3d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34a3d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="34a3d-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34a3d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34a3d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34a3d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="34a3d-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34a3d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34a3d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="34a3d-131">Namespace</span></span><br/>                | <span data-ttu-id="34a3d-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="34a3d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34a3d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="34a3d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34a3d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34a3d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34a3d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="34a3d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a3d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34a3d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 





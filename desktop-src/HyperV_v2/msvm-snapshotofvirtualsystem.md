---
description: Associe un système virtuel à un instantané qui a été capturé à partir du système virtuel.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Classe Msvm_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951525"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="fc57e-103">MSVM \_ SnapshotOfVirtualSystem, classe</span><span class="sxs-lookup"><span data-stu-id="fc57e-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="fc57e-104">Associe un système virtuel à un instantané qui a été capturé à partir du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc57e-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="fc57e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fc57e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc57e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc57e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fc57e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fc57e-107">Members</span></span>

<span data-ttu-id="fc57e-108">La classe **MSVM \_ SnapshotOfVirtualSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fc57e-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="fc57e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc57e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc57e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc57e-110">Properties</span></span>

<span data-ttu-id="fc57e-111">La classe **MSVM \_ SnapshotOfVirtualSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc57e-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc57e-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fc57e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc57e-113">Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="fc57e-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fc57e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc57e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc57e-115">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="fc57e-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="fc57e-116">Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="fc57e-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="fc57e-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fc57e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc57e-118">Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="fc57e-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fc57e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc57e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc57e-120">Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané.</span><span class="sxs-lookup"><span data-stu-id="fc57e-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="fc57e-121">Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="fc57e-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc57e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc57e-122">Requirements</span></span>



| <span data-ttu-id="fc57e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc57e-123">Requirement</span></span> | <span data-ttu-id="fc57e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc57e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc57e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc57e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fc57e-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc57e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc57e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc57e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fc57e-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc57e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc57e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fc57e-129">Namespace</span></span><br/>                | <span data-ttu-id="fc57e-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc57e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc57e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fc57e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc57e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc57e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc57e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fc57e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc57e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc57e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc57e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc57e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc57e-136">**\_SNAPSHOTOFVIRTUALSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fc57e-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="fc57e-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="fc57e-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 


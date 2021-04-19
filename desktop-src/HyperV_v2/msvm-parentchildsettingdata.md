---
description: Association entre une instance de MSVM \_ VirtualSystemSettingData et l' \_ instance VirtualSystemSettingData MSVM qui représente l’instantané le plus récent sur lequel cet objet est basé.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Classe Msvm_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534124"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="43a47-103">MSVM \_ ParentChildSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="43a47-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="43a47-104">Association entre une instance de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) et l’instance **\_ VirtualSystemSettingData MSVM** qui représente l’instantané le plus récent sur lequel cet objet est basé.</span><span class="sxs-lookup"><span data-stu-id="43a47-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="43a47-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="43a47-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a47-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43a47-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="43a47-107">Membres</span><span class="sxs-lookup"><span data-stu-id="43a47-107">Members</span></span>

<span data-ttu-id="43a47-108">La classe **MSVM \_ ParentChildSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="43a47-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="43a47-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43a47-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43a47-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43a47-110">Properties</span></span>

<span data-ttu-id="43a47-111">La classe **MSVM \_ ParentChildSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="43a47-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43a47-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="43a47-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43a47-113">Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="43a47-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43a47-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43a47-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43a47-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="43a47-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="43a47-116">Données de paramètre d’instantané sur lesquelles les données de paramètres enfants sont basées.</span><span class="sxs-lookup"><span data-stu-id="43a47-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="43a47-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="43a47-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43a47-118">Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="43a47-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43a47-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43a47-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43a47-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="43a47-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="43a47-121">Données de paramètre de l’ordinateur virtuel qui représente l’enfant du parent.</span><span class="sxs-lookup"><span data-stu-id="43a47-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43a47-122">Notes</span><span class="sxs-lookup"><span data-stu-id="43a47-122">Remarks</span></span>

<span data-ttu-id="43a47-123">L’accès à la classe **MSVM \_ ParentChildSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="43a47-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="43a47-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="43a47-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="43a47-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43a47-125">Requirements</span></span>



| <span data-ttu-id="43a47-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43a47-126">Requirement</span></span> | <span data-ttu-id="43a47-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a47-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a47-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a47-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43a47-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43a47-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43a47-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a47-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43a47-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43a47-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43a47-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43a47-132">Namespace</span></span><br/>                | <span data-ttu-id="43a47-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="43a47-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43a47-134">MOF</span><span class="sxs-lookup"><span data-stu-id="43a47-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43a47-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43a47-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43a47-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43a47-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a47-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43a47-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43a47-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43a47-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a47-139">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="43a47-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="43a47-140">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="43a47-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="43a47-141">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="43a47-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


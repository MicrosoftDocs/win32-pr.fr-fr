---
description: Association utilisée pour représenter les paramètres réseau de migration de système virtuel du service de migration de système virtuel.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Classe Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516419"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="66bc3-103">MSVM \_ VirtualSystemMigrationServiceSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="66bc3-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="66bc3-104">Association utilisée pour représenter les paramètres réseau de migration de système virtuel du service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bc3-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="66bc3-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="66bc3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bc3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66bc3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="66bc3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="66bc3-107">Members</span></span>

<span data-ttu-id="66bc3-108">La classe **MSVM \_ VirtualSystemMigrationServiceSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66bc3-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="66bc3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66bc3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66bc3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66bc3-110">Properties</span></span>

<span data-ttu-id="66bc3-111">La classe **MSVM \_ VirtualSystemMigrationServiceSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="66bc3-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66bc3-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="66bc3-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bc3-113">Type de données : **MSVM \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="66bc3-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="66bc3-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bc3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bc3-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66bc3-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66bc3-116">Référence à une instance de la classe [**MSVM \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) qui représente les paramètres du service de migration.</span><span class="sxs-lookup"><span data-stu-id="66bc3-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="66bc3-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="66bc3-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bc3-118">Type de données : **MSVM \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="66bc3-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="66bc3-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bc3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bc3-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="66bc3-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="66bc3-121">Référence à une instance de la classe [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) qui représente les paramètres réseau de la migration.</span><span class="sxs-lookup"><span data-stu-id="66bc3-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66bc3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66bc3-122">Requirements</span></span>



| <span data-ttu-id="66bc3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66bc3-123">Requirement</span></span> | <span data-ttu-id="66bc3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="66bc3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bc3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66bc3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66bc3-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66bc3-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="66bc3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66bc3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66bc3-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66bc3-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66bc3-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66bc3-129">Namespace</span></span><br/>                | <span data-ttu-id="66bc3-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="66bc3-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66bc3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="66bc3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66bc3-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66bc3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66bc3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="66bc3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bc3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66bc3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


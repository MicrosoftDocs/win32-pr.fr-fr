---
description: Établissez une relation entre une instance de la \_ classe MSVM EmulatedEthernetPortSettingData ou MSVM \_ SyntheticEthernetPortSettingData avec une instance de la \_ classe MSVM GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Classe Msvm_SettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952318"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="e328e-103">MSVM \_ SettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="e328e-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="e328e-104">Établissez une relation entre une instance de la classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) avec une instance de la classe MSVM [**\_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e328e-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="e328e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e328e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e328e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e328e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e328e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e328e-107">Members</span></span>

<span data-ttu-id="e328e-108">La classe **MSVM \_ SettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e328e-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e328e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e328e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e328e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e328e-110">Properties</span></span>

<span data-ttu-id="e328e-111">La classe **MSVM \_ SettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e328e-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e328e-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e328e-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e328e-113">Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="e328e-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="e328e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e328e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e328e-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e328e-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e328e-116">Référence à une instance de la classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) qui représente un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e328e-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="e328e-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e328e-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e328e-118">Type de données : **[ **MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="e328e-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e328e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e328e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e328e-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e328e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e328e-121">Référence à une instance de la classe [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) qui représente une configuration de carte réseau invitée.</span><span class="sxs-lookup"><span data-stu-id="e328e-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e328e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e328e-122">Requirements</span></span>



| <span data-ttu-id="e328e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e328e-123">Requirement</span></span> | <span data-ttu-id="e328e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e328e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e328e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e328e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e328e-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e328e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e328e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e328e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e328e-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e328e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e328e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e328e-129">Namespace</span></span><br/>                | <span data-ttu-id="e328e-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e328e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e328e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e328e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e328e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e328e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e328e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e328e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e328e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e328e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


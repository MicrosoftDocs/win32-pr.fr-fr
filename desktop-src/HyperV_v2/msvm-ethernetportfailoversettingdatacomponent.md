---
description: Association utilisée pour établir des relations entre une instance d’un \_ EmulatedEthernetPortSettingData MSVM et une ou plusieurs instances d’un \_ EthernetSwitchFeatureSettingData MSVM.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Classe Msvm_EthernetPortFailoverSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529259"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="38470-103">MSVM \_ EthernetPortFailoverSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="38470-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="38470-104">Association utilisée pour établir des relations entre une instance d’un [**\_ EmulatedEthernetPortSettingData MSVM**](msvm-emulatedethernetportsettingdata.md) et une ou plusieurs instances d’un [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="38470-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="38470-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="38470-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38470-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38470-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="38470-107">Membres</span><span class="sxs-lookup"><span data-stu-id="38470-107">Members</span></span>

<span data-ttu-id="38470-108">La classe **MSVM \_ EthernetPortFailoverSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="38470-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="38470-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38470-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38470-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38470-110">Properties</span></span>

<span data-ttu-id="38470-111">La classe **MSVM \_ EthernetPortFailoverSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="38470-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38470-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="38470-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38470-113">Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="38470-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="38470-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38470-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38470-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38470-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38470-116">Référence à une instance de la classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) qui représente le port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="38470-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="38470-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="38470-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38470-118">Type de données : **[ **MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="38470-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="38470-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38470-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38470-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="38470-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="38470-121">Référence à une instance de la classe [**MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) qui représente la configuration de la carte réseau invitée.</span><span class="sxs-lookup"><span data-stu-id="38470-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38470-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38470-122">Requirements</span></span>



| <span data-ttu-id="38470-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38470-123">Requirement</span></span> | <span data-ttu-id="38470-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="38470-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38470-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38470-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38470-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38470-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38470-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38470-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38470-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38470-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38470-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38470-129">Namespace</span></span><br/>                | <span data-ttu-id="38470-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="38470-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38470-131">MOF</span><span class="sxs-lookup"><span data-stu-id="38470-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38470-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38470-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38470-133">DLL</span><span class="sxs-lookup"><span data-stu-id="38470-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38470-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38470-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


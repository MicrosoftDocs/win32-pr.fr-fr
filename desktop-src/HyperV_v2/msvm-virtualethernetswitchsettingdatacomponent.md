---
description: Association utilisée pour établir &\# 0034 ; partie de&\# 0034 ; relations entre une instance de MSVM \_ VirtualEthernetSwitchSettingData et une ou plusieurs instances de MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Classe Msvm_VirtualEthernetSwitchSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202206"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="e6d81-103">MSVM \_ VirtualEthernetSwitchSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="e6d81-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="e6d81-104">Association utilisée pour établir des relations de « partie de » entre une instance de [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) et une ou plusieurs instances de [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="e6d81-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="e6d81-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e6d81-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d81-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6d81-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e6d81-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e6d81-107">Members</span></span>

<span data-ttu-id="e6d81-108">La classe **MSVM \_ VirtualEthernetSwitchSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6d81-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e6d81-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6d81-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6d81-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6d81-110">Properties</span></span>

<span data-ttu-id="e6d81-111">La classe **MSVM \_ VirtualEthernetSwitchSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6d81-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6d81-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e6d81-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d81-113">Type de données : **MSVM \_ VirtualEthernetSwitchSettingData**</span><span class="sxs-lookup"><span data-stu-id="e6d81-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e6d81-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6d81-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d81-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6d81-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6d81-116">Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) qui représente un port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e6d81-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="e6d81-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e6d81-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d81-118">Type de données : **MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="e6d81-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e6d81-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6d81-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d81-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e6d81-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e6d81-121">Référence à une instance de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) qui représente les paramètres appliqués au commutateur.</span><span class="sxs-lookup"><span data-stu-id="e6d81-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6d81-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6d81-122">Requirements</span></span>



| <span data-ttu-id="e6d81-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6d81-123">Requirement</span></span> | <span data-ttu-id="e6d81-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6d81-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d81-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6d81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d81-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6d81-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6d81-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6d81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d81-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6d81-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6d81-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6d81-129">Namespace</span></span><br/>                | <span data-ttu-id="e6d81-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6d81-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6d81-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e6d81-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6d81-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6d81-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6d81-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d81-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6d81-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6d81-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


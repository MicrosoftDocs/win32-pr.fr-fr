---
description: Association utilisée pour établir &\# 0034 ; partie de&\# 0034 ; relations entre une instance d’un EthernetPortAllocationSettingData MSVM \_ et une ou plusieurs instances d’un EthernetSwitchFeatureSettingData MSVM \_ .
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Classe Msvm_EthernetPortSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530869"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="b8f39-103">MSVM \_ EthernetPortSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="b8f39-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="b8f39-104">Association utilisée pour établir des relations de « partie de » entre une instance d' [**un \_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) et une ou plusieurs instances d' [**un \_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="b8f39-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="b8f39-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b8f39-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f39-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8f39-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b8f39-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b8f39-107">Members</span></span>

<span data-ttu-id="b8f39-108">La classe **MSVM \_ EthernetPortSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8f39-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b8f39-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8f39-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8f39-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8f39-110">Properties</span></span>

<span data-ttu-id="b8f39-111">La classe **MSVM \_ EthernetPortSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8f39-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8f39-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b8f39-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8f39-113">Type de données : **[ **MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b8f39-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b8f39-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8f39-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8f39-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8f39-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8f39-116">Référence à une instance de la classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) qui représente le port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b8f39-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="b8f39-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b8f39-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8f39-118">Type de données : **[ **MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b8f39-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b8f39-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8f39-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8f39-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b8f39-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b8f39-121">Référence à une instance de la classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) qui représente les paramètres de fonctionnalités appliqués au port.</span><span class="sxs-lookup"><span data-stu-id="b8f39-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8f39-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8f39-122">Requirements</span></span>



| <span data-ttu-id="b8f39-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8f39-123">Requirement</span></span> | <span data-ttu-id="b8f39-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8f39-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f39-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8f39-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f39-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8f39-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8f39-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8f39-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f39-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8f39-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8f39-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b8f39-129">Namespace</span></span><br/>                | <span data-ttu-id="b8f39-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8f39-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8f39-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b8f39-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8f39-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8f39-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8f39-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f39-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f39-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8f39-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


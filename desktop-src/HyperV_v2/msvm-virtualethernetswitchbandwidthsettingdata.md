---
description: Représente les paramètres de bande passante pour un commutateur virtuel.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Classe Msvm_VirtualEthernetSwitchBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543120"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="a7a59-103">MSVM \_ VirtualEthernetSwitchBandwidthSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="a7a59-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="a7a59-104">Représente les paramètres de bande passante pour un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a7a59-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="a7a59-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a7a59-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a59-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7a59-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="a7a59-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a7a59-107">Members</span></span>

<span data-ttu-id="a7a59-108">La classe **MSVM \_ VirtualEthernetSwitchBandwidthSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7a59-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a7a59-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a59-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7a59-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a59-110">Properties</span></span>

<span data-ttu-id="a7a59-111">La classe **MSVM \_ VirtualEthernetSwitchBandwidthSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7a59-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7a59-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a7a59-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7a59-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a59-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7a59-115">A short description of the object.</span></span> <span data-ttu-id="a7a59-116">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et est toujours définie sur « paramètres Ethernet de bande passante ».</span><span class="sxs-lookup"><span data-stu-id="a7a59-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a7a59-117">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="a7a59-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-118">Type de données : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a7a59-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a7a59-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-120">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a7a59-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-121">Spécifie la réservation de bande passante absolue pour les flux non classifiés sur l’adaptateur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="a7a59-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a7a59-122">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="a7a59-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-123">Type de données : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a7a59-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a7a59-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-125">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a7a59-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-126">Spécifie la réservation de bande passante en poids pour les flux non classifiés sur l’adaptateur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="a7a59-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a7a59-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7a59-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7a59-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a59-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-130">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="a7a59-130">A description of the object.</span></span> <span data-ttu-id="a7a59-131">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les paramètres de bande passante du commutateur. ».</span><span class="sxs-lookup"><span data-stu-id="a7a59-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="a7a59-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a7a59-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7a59-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a59-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-135">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7a59-135">A display name for the object.</span></span> <span data-ttu-id="a7a59-136">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « paramètres Ethernet de bande passante ».</span><span class="sxs-lookup"><span data-stu-id="a7a59-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a7a59-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7a59-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a59-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7a59-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a59-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7a59-140">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="a7a59-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a7a59-141">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a7a59-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a7a59-142">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft : définition \\ *GUID* \\ default ».</span><span class="sxs-lookup"><span data-stu-id="a7a59-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7a59-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7a59-143">Requirements</span></span>



| <span data-ttu-id="a7a59-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7a59-144">Requirement</span></span> | <span data-ttu-id="a7a59-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7a59-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a59-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a59-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a59-147">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7a59-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7a59-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a59-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a59-149">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7a59-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7a59-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7a59-150">Namespace</span></span><br/>                | <span data-ttu-id="a7a59-151">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a7a59-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7a59-152">MOF</span><span class="sxs-lookup"><span data-stu-id="a7a59-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7a59-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7a59-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7a59-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a7a59-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7a59-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7a59-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


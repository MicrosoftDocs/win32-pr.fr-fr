---
description: Représente les paramètres de la bande passante du port.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Classe Msvm_EthernetSwitchPortBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521145"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="70eb5-103">MSVM \_ EthernetSwitchPortBandwidthSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="70eb5-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="70eb5-104">Représente les paramètres de la bande passante du port.</span><span class="sxs-lookup"><span data-stu-id="70eb5-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="70eb5-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70eb5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eb5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70eb5-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="70eb5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="70eb5-107">Members</span></span>

<span data-ttu-id="70eb5-108">La classe **MSVM \_ EthernetSwitchPortBandwidthSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70eb5-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="70eb5-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70eb5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70eb5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70eb5-110">Properties</span></span>

<span data-ttu-id="70eb5-111">La classe **MSVM \_ EthernetSwitchPortBandwidthSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="70eb5-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70eb5-112">**BurstLimit**</span><span class="sxs-lookup"><span data-stu-id="70eb5-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70eb5-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70eb5-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-115">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="70eb5-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-116">Bande passante maximale autorisée à partir du port au cours des pics.</span><span class="sxs-lookup"><span data-stu-id="70eb5-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-117">**BurstSize**</span><span class="sxs-lookup"><span data-stu-id="70eb5-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-118">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70eb5-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70eb5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-120">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="70eb5-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-121">Taille de rafale maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="70eb5-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="70eb5-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70eb5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70eb5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-125">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70eb5-125">A short description of the object.</span></span> <span data-ttu-id="70eb5-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de la bande passante du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="70eb5-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="70eb5-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70eb5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70eb5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-130">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="70eb5-130">A description of the object.</span></span> <span data-ttu-id="70eb5-131">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les paramètres de bande passante du port ».</span><span class="sxs-lookup"><span data-stu-id="70eb5-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="70eb5-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70eb5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70eb5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-135">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70eb5-135">A display name for the object.</span></span> <span data-ttu-id="70eb5-136">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de la bande passante du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="70eb5-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="70eb5-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70eb5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70eb5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-140">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="70eb5-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-141">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="70eb5-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="70eb5-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="70eb5-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-143">**Limite**</span><span class="sxs-lookup"><span data-stu-id="70eb5-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-144">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70eb5-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70eb5-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-146">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="70eb5-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-147">Limite de bande passante autorisée pour le port.</span><span class="sxs-lookup"><span data-stu-id="70eb5-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-148">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="70eb5-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-149">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70eb5-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70eb5-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-151">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="70eb5-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-152">Bande passante absolue minimale garantie pour le port.</span><span class="sxs-lookup"><span data-stu-id="70eb5-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="70eb5-153">**Poids**</span><span class="sxs-lookup"><span data-stu-id="70eb5-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70eb5-154">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70eb5-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70eb5-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="70eb5-156">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="70eb5-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="70eb5-157">La bande passante minimale du poids est garantie pour le port.</span><span class="sxs-lookup"><span data-stu-id="70eb5-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70eb5-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70eb5-158">Requirements</span></span>



| <span data-ttu-id="70eb5-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70eb5-159">Requirement</span></span> | <span data-ttu-id="70eb5-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="70eb5-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70eb5-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70eb5-161">Minimum supported client</span></span><br/> | <span data-ttu-id="70eb5-162">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70eb5-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70eb5-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70eb5-163">Minimum supported server</span></span><br/> | <span data-ttu-id="70eb5-164">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70eb5-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70eb5-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70eb5-165">Namespace</span></span><br/>                | <span data-ttu-id="70eb5-166">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="70eb5-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70eb5-167">MOF</span><span class="sxs-lookup"><span data-stu-id="70eb5-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70eb5-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70eb5-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70eb5-169">DLL</span><span class="sxs-lookup"><span data-stu-id="70eb5-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70eb5-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70eb5-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


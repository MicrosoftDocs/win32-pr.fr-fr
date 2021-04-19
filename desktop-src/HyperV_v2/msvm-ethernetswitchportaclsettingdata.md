---
description: Représente la liste de contrôle d’accès (ACL) pour les paramètres de port de commutateur.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Classe Msvm_EthernetSwitchPortAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522255"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="01ba6-103">MSVM \_ EthernetSwitchPortAclSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="01ba6-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="01ba6-104">Représente la liste de contrôle d’accès (ACL) pour les paramètres de port de commutateur.</span><span class="sxs-lookup"><span data-stu-id="01ba6-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="01ba6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="01ba6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ba6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01ba6-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="01ba6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="01ba6-107">Members</span></span>

<span data-ttu-id="01ba6-108">La classe **MSVM \_ EthernetSwitchPortAclSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01ba6-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="01ba6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01ba6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01ba6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01ba6-110">Properties</span></span>

<span data-ttu-id="01ba6-111">La classe **MSVM \_ EthernetSwitchPortAclSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="01ba6-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01ba6-112">**AclType**</span><span class="sxs-lookup"><span data-stu-id="01ba6-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-115">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-116">Cela indique le type de point de terminaison de liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="01ba6-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01ba6-117">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="01ba6-118">**ACL Mac** (1)</span><span class="sxs-lookup"><span data-stu-id="01ba6-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="01ba6-119">**ACL IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="01ba6-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="01ba6-120">**ACL IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="01ba6-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01ba6-121">**Action**</span><span class="sxs-lookup"><span data-stu-id="01ba6-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-122">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-124">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-125">Cela indique l’action de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="01ba6-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01ba6-126">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="01ba6-127">**Autoriser** (1)</span><span class="sxs-lookup"><span data-stu-id="01ba6-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="01ba6-128">**Refuser** (2)</span><span class="sxs-lookup"><span data-stu-id="01ba6-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="01ba6-129">**Compteur** (3)</span><span class="sxs-lookup"><span data-stu-id="01ba6-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01ba6-130">**Applicabilité**</span><span class="sxs-lookup"><span data-stu-id="01ba6-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-131">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-133">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-134">Cela indique si la liste de contrôle d’accès s’applique au point de terminaison local ou distant.</span><span class="sxs-lookup"><span data-stu-id="01ba6-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01ba6-135">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="01ba6-136">**Local** (1)</span><span class="sxs-lookup"><span data-stu-id="01ba6-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="01ba6-137">**Distant** (2)</span><span class="sxs-lookup"><span data-stu-id="01ba6-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01ba6-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="01ba6-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01ba6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="01ba6-141">A short description of the object.</span></span> <span data-ttu-id="01ba6-142">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de liste de contrôle d’accès de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="01ba6-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-143">**Description**</span><span class="sxs-lookup"><span data-stu-id="01ba6-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01ba6-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-146">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="01ba6-146">A description of the object.</span></span> <span data-ttu-id="01ba6-147">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente la classe de base pour les paramètres de port de commutateur. ».</span><span class="sxs-lookup"><span data-stu-id="01ba6-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-148">**Sens**</span><span class="sxs-lookup"><span data-stu-id="01ba6-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-149">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-151">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-152">Cela indique si la liste de contrôle d’accès s’applique à la direction d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="01ba6-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01ba6-153">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="01ba6-154">**Entrant** (1)</span><span class="sxs-lookup"><span data-stu-id="01ba6-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="01ba6-155">**Sortant** (2)</span><span class="sxs-lookup"><span data-stu-id="01ba6-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01ba6-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="01ba6-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01ba6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-159">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="01ba6-159">A display name for the object.</span></span> <span data-ttu-id="01ba6-160">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de liste de contrôle d’accès de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="01ba6-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01ba6-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01ba6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-164">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="01ba6-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-165">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="01ba6-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="01ba6-166">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="01ba6-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="01ba6-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-170">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-171">Adresse locale de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="01ba6-171">The local address of the virtual machine.</span></span> <span data-ttu-id="01ba6-172">Il peut s’agir d’une adresse IPv4, IPv6 ou MAC.</span><span class="sxs-lookup"><span data-stu-id="01ba6-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-173">**LocalAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="01ba6-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-174">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-176">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-177">Longueur du préfixe d’adresse locale.</span><span class="sxs-lookup"><span data-stu-id="01ba6-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-178">**Nom**</span><span class="sxs-lookup"><span data-stu-id="01ba6-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-181">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-182">Nom complet de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="01ba6-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="01ba6-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01ba6-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-186">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-187">Adresse distante de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="01ba6-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="01ba6-188">Il peut s’agir d’une adresse IPv4, IPv6 ou MAC.</span><span class="sxs-lookup"><span data-stu-id="01ba6-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="01ba6-189">**RemoteAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="01ba6-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba6-190">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="01ba6-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="01ba6-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01ba6-192">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="01ba6-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="01ba6-193">Longueur du préfixe d’adresse distante.</span><span class="sxs-lookup"><span data-stu-id="01ba6-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01ba6-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01ba6-194">Requirements</span></span>



| <span data-ttu-id="01ba6-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01ba6-195">Requirement</span></span> | <span data-ttu-id="01ba6-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="01ba6-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01ba6-197">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01ba6-197">Minimum supported client</span></span><br/> | <span data-ttu-id="01ba6-198">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01ba6-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="01ba6-199">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01ba6-199">Minimum supported server</span></span><br/> | <span data-ttu-id="01ba6-200">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01ba6-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01ba6-201">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01ba6-201">Namespace</span></span><br/>                | <span data-ttu-id="01ba6-202">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="01ba6-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="01ba6-203">MOF</span><span class="sxs-lookup"><span data-stu-id="01ba6-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01ba6-204"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01ba6-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01ba6-205">DLL</span><span class="sxs-lookup"><span data-stu-id="01ba6-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ba6-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01ba6-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


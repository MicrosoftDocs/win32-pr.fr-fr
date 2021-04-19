---
description: Représente les paramètres d’une carte réseau au sein du système d’exploitation invité, qui seront appliqués au moment du basculement.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Classe Msvm_FailoverNetworkAdapterSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514861"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="ee602-103">MSVM \_ FailoverNetworkAdapterSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ee602-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="ee602-104">Représente les paramètres d’une carte réseau au sein du système d’exploitation invité, qui seront appliqués au moment du basculement.</span><span class="sxs-lookup"><span data-stu-id="ee602-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="ee602-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee602-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee602-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee602-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="ee602-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ee602-107">Members</span></span>

<span data-ttu-id="ee602-108">La classe **MSVM \_ FailoverNetworkAdapterSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee602-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ee602-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee602-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee602-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee602-110">Properties</span></span>

<span data-ttu-id="ee602-111">La classe **MSVM \_ FailoverNetworkAdapterSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee602-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee602-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ee602-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee602-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee602-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee602-115">A short description of the object.</span></span> <span data-ttu-id="ee602-116">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ee602-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-117">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="ee602-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee602-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee602-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee602-120">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ee602-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ee602-121">Tableau de chaînes qui spécifient les passerelles IP par défaut configurées sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ee602-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="ee602-122">Le nombre maximal de passerelles IP par défaut qui peuvent être configurées sur une seule carte réseau est de cinq.</span><span class="sxs-lookup"><span data-stu-id="ee602-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee602-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee602-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee602-126">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ee602-126">A description of the object.</span></span> <span data-ttu-id="ee602-127">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ee602-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="ee602-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee602-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee602-131">Spécifie si le protocole DHCP est activé sur l’interface IPv4 de la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ee602-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="ee602-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee602-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee602-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee602-135">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ee602-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ee602-136">Tableau de chaînes qui spécifient les serveurs DNS configurés sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ee602-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ee602-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee602-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee602-140">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee602-140">A display name for the object.</span></span> <span data-ttu-id="ee602-141">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ee602-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ee602-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee602-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee602-145">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ee602-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ee602-146">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ee602-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ee602-147">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ee602-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="ee602-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-149">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee602-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee602-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee602-151">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ee602-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ee602-152">Tableau de chaînes qui spécifient les adresses IP configurées sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ee602-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ee602-153">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="ee602-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee602-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee602-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee602-156">Identifie les protocoles Internet auxquels s’appliquent les paramètres spécifiés par cette instance.</span><span class="sxs-lookup"><span data-stu-id="ee602-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="ee602-157">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee602-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee602-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee602-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee602-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee602-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="ee602-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="ee602-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="ee602-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="ee602-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="ee602-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="ee602-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="ee602-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="ee602-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee602-164">**Sous-réseaux**</span><span class="sxs-lookup"><span data-stu-id="ee602-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee602-165">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee602-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee602-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee602-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee602-167">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ee602-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ee602-168">Tableau de chaînes qui spécifient les sous-réseaux configurés sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ee602-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="ee602-169">Chaque élément de ce tableau s’applique à l’élément correspondant dans le tableau **adressesIP** .</span><span class="sxs-lookup"><span data-stu-id="ee602-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee602-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee602-170">Requirements</span></span>



| <span data-ttu-id="ee602-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee602-171">Requirement</span></span> | <span data-ttu-id="ee602-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee602-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee602-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee602-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ee602-174">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee602-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee602-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee602-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ee602-176">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee602-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee602-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee602-177">Namespace</span></span><br/>                | <span data-ttu-id="ee602-178">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ee602-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee602-179">MOF</span><span class="sxs-lookup"><span data-stu-id="ee602-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee602-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee602-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee602-181">DLL</span><span class="sxs-lookup"><span data-stu-id="ee602-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee602-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee602-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


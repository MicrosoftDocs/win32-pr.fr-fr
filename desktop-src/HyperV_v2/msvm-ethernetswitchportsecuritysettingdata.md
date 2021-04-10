---
description: Représente les données de paramètre de la fonctionnalité de sécurité.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Classe Msvm_EthernetSwitchPortSecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869269"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="0236c-103">MSVM \_ EthernetSwitchPortSecuritySettingData, classe</span><span class="sxs-lookup"><span data-stu-id="0236c-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="0236c-104">Représente les données de paramètre de la fonctionnalité de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0236c-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="0236c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0236c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0236c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0236c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="0236c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0236c-107">Members</span></span>

<span data-ttu-id="0236c-108">La classe **MSVM \_ EthernetSwitchPortSecuritySettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0236c-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0236c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0236c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0236c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0236c-110">Properties</span></span>

<span data-ttu-id="0236c-111">La classe **MSVM \_ EthernetSwitchPortSecuritySettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0236c-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0236c-112">**AllowIeeePriorityTag**</span><span class="sxs-lookup"><span data-stu-id="0236c-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-115">Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-116">Spécifie si le trafic vers/depuis le port conserve les informations 802.1 P.</span><span class="sxs-lookup"><span data-stu-id="0236c-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="0236c-117">Contient la **valeur true** si le trafic vers/depuis le port conserve les informations 802.1 p ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0236c-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="0236c-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="0236c-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-119">**AllowMacSpoofing**</span><span class="sxs-lookup"><span data-stu-id="0236c-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-122">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-123">Indique si le port autorise l’usurpation MAC.</span><span class="sxs-lookup"><span data-stu-id="0236c-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="0236c-124">Si cette propriété a la **valeur true**, le port autorise l’usurpation des adresses Mac.</span><span class="sxs-lookup"><span data-stu-id="0236c-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="0236c-125">Toutes les valeurs d’adresse MAC monodiffusion valides sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="0236c-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="0236c-126">Si cette propriété a la **valeur false**, le port n’autorise l’utilisation que des adresses Mac configurées dans la gestion Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0236c-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="0236c-127">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="0236c-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-128">**AllowTeaming**</span><span class="sxs-lookup"><span data-stu-id="0236c-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-131">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-132">Indique si les cartes réseau connectées au port peuvent faire partie d’une équipe.</span><span class="sxs-lookup"><span data-stu-id="0236c-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="0236c-133">Cela s’applique uniquement aux cartes réseau connectées à des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="0236c-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="0236c-134">Contient la **valeur true** si l’Association de cartes réseau est autorisée ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0236c-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="0236c-135">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="0236c-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0236c-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0236c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0236c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0236c-139">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0236c-139">A short description of the object.</span></span> <span data-ttu-id="0236c-140">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de sécurité du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="0236c-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0236c-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="0236c-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0236c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0236c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0236c-144">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="0236c-144">A description of the object.</span></span> <span data-ttu-id="0236c-145">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les données de paramètre de la fonctionnalité de sécurité ».</span><span class="sxs-lookup"><span data-stu-id="0236c-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="0236c-146">**DynamicIPAddressLimit**</span><span class="sxs-lookup"><span data-stu-id="0236c-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0236c-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-149">Qualificateurs : **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-150">Définit la limite du nombre d’adresses IP dynamiques apprises.</span><span class="sxs-lookup"><span data-stu-id="0236c-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="0236c-151">La valeur par défaut est none.</span><span class="sxs-lookup"><span data-stu-id="0236c-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0236c-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0236c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0236c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0236c-155">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0236c-155">A display name for the object.</span></span> <span data-ttu-id="0236c-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de sécurité du port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="0236c-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0236c-157">**EnableDhcpGuard**</span><span class="sxs-lookup"><span data-stu-id="0236c-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-158">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-160">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-161">Spécifie si les offres DHCP sont bloquées par le port.</span><span class="sxs-lookup"><span data-stu-id="0236c-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="0236c-162">Contient la **valeur true** si les offres DHCP sont bloquées à partir du port ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0236c-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="0236c-163">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="0236c-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="0236c-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-165">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-167">Qualificateurs : **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-168">Définie sur TRUE si la vitesse fixe 10G est activée, sinon FALSe.</span><span class="sxs-lookup"><span data-stu-id="0236c-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="0236c-169">La valeur par défaut est FALSe.</span><span class="sxs-lookup"><span data-stu-id="0236c-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="0236c-170">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0236c-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="0236c-171">**EnableRouterGuard**</span><span class="sxs-lookup"><span data-stu-id="0236c-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-174">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-175">Spécifie si les publications de routeur et les redirections de routeur sont bloquées à partir du port.</span><span class="sxs-lookup"><span data-stu-id="0236c-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="0236c-176">Contient la **valeur true** si les annonces de routeur et les redirections de routeur sont bloquées à partir du port ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0236c-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="0236c-177">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="0236c-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0236c-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0236c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0236c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0236c-181">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="0236c-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0236c-182">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0236c-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0236c-183">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0236c-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0236c-184">**MonitorMode**</span><span class="sxs-lookup"><span data-stu-id="0236c-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-185">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0236c-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-186">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-187">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-188">Cela indique le mode d’analyse du port.</span><span class="sxs-lookup"><span data-stu-id="0236c-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0236c-189">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="0236c-190">**Destination** (1)</span><span class="sxs-lookup"><span data-stu-id="0236c-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="0236c-191">**Source** (2)</span><span class="sxs-lookup"><span data-stu-id="0236c-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0236c-192">**MonitorSession**</span><span class="sxs-lookup"><span data-stu-id="0236c-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-193">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0236c-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-194">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-195">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-196">Spécifie l’identificateur de la session d’analyse à laquelle ce port appartient.</span><span class="sxs-lookup"><span data-stu-id="0236c-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0236c-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-198">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0236c-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-200">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-201">Réservé</span><span class="sxs-lookup"><span data-stu-id="0236c-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="0236c-202">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0236c-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="0236c-203">**StormLimit**</span><span class="sxs-lookup"><span data-stu-id="0236c-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-204">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0236c-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-206">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-207">Définit la limite de paquets par seconde pour le trafic de diffusion et de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="0236c-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="0236c-208">La valeur par défaut est none.</span><span class="sxs-lookup"><span data-stu-id="0236c-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-209">**TeamName**</span><span class="sxs-lookup"><span data-stu-id="0236c-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0236c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-212">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-213">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="0236c-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="0236c-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-215">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0236c-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-216">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-217">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0236c-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-218">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="0236c-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0236c-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="0236c-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0236c-220">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0236c-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0236c-221">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0236c-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0236c-222">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="0236c-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="0236c-223">Spécifie l’identificateur du sous-réseau virtuel dont le port est membre.</span><span class="sxs-lookup"><span data-stu-id="0236c-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="0236c-224">La valeur par défaut est aucune gestion.</span><span class="sxs-lookup"><span data-stu-id="0236c-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0236c-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0236c-225">Requirements</span></span>



| <span data-ttu-id="0236c-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0236c-226">Requirement</span></span> | <span data-ttu-id="0236c-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="0236c-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0236c-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0236c-228">Minimum supported client</span></span><br/> | <span data-ttu-id="0236c-229">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0236c-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0236c-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0236c-230">Minimum supported server</span></span><br/> | <span data-ttu-id="0236c-231">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0236c-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0236c-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0236c-232">Namespace</span></span><br/>                | <span data-ttu-id="0236c-233">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0236c-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0236c-234">MOF</span><span class="sxs-lookup"><span data-stu-id="0236c-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0236c-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0236c-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0236c-236">DLL</span><span class="sxs-lookup"><span data-stu-id="0236c-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0236c-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0236c-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


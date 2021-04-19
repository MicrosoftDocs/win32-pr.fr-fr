---
description: Représente les paramètres de liste de contrôle d’accès des ports étendus.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Classe Msvm_EthernetSwitchPortExtendedAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519364"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="ddb86-103">MSVM \_ EthernetSwitchPortExtendedAclSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ddb86-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="ddb86-104">Représente les paramètres de liste de contrôle d’accès des ports étendus.</span><span class="sxs-lookup"><span data-stu-id="ddb86-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="ddb86-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ddb86-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb86-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddb86-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="ddb86-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ddb86-107">Members</span></span>

<span data-ttu-id="ddb86-108">La classe **MSVM \_ EthernetSwitchPortExtendedAclSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddb86-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ddb86-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddb86-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddb86-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddb86-110">Properties</span></span>

<span data-ttu-id="ddb86-111">La classe **MSVM \_ EthernetSwitchPortExtendedAclSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddb86-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddb86-112">**Action**</span><span class="sxs-lookup"><span data-stu-id="ddb86-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ddb86-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-115">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-116">Action de la liste de contrôle d’accès étendue.</span><span class="sxs-lookup"><span data-stu-id="ddb86-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddb86-117">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="ddb86-118">**Autoriser** (1)</span><span class="sxs-lookup"><span data-stu-id="ddb86-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="ddb86-119">**Refuser** (2)</span><span class="sxs-lookup"><span data-stu-id="ddb86-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb86-120">**Sens**</span><span class="sxs-lookup"><span data-stu-id="ddb86-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-121">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ddb86-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-123">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-124">Indique si la liste de contrôle d’accès étendue s’applique à la direction entrante ou sortante.</span><span class="sxs-lookup"><span data-stu-id="ddb86-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddb86-125">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="ddb86-126">**Entrant** (1)</span><span class="sxs-lookup"><span data-stu-id="ddb86-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="ddb86-127">**Sortant** (2)</span><span class="sxs-lookup"><span data-stu-id="ddb86-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb86-128">**IdleSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="ddb86-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-129">Type de données : **Uint16**</span><span class="sxs-lookup"><span data-stu-id="ddb86-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-131">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-132">Valeur du délai d’expiration de la session inactive (en secondes) pour l’ACL avec état.</span><span class="sxs-lookup"><span data-stu-id="ddb86-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-133">**IsolationID**</span><span class="sxs-lookup"><span data-stu-id="ddb86-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb86-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-136">Qualificateurs : **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="ddb86-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-137">ID d’isolation pour lequel la liste de contrôle d’accès étendue doit être appliquée.</span><span class="sxs-lookup"><span data-stu-id="ddb86-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-138">**LocalIPAddress**</span><span class="sxs-lookup"><span data-stu-id="ddb86-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-141">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-142">Adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="ddb86-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="ddb86-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-147">Plage de ports locaux.</span><span class="sxs-lookup"><span data-stu-id="ddb86-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-148">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ddb86-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-152">Nom convivial de la liste de contrôle d’accès étendue.</span><span class="sxs-lookup"><span data-stu-id="ddb86-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-153">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="ddb86-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-156">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-157">Chaîne de protocole.</span><span class="sxs-lookup"><span data-stu-id="ddb86-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-158">**RemoteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="ddb86-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-161">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-162">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="ddb86-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-163">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="ddb86-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddb86-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-166">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-167">Plage de ports distants.</span><span class="sxs-lookup"><span data-stu-id="ddb86-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-168">**Avec état**</span><span class="sxs-lookup"><span data-stu-id="ddb86-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-169">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ddb86-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-171">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-172">Indique si la liste de contrôle d’accès étendue est avec état ou sans État.</span><span class="sxs-lookup"><span data-stu-id="ddb86-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="ddb86-173">**Poids**</span><span class="sxs-lookup"><span data-stu-id="ddb86-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb86-174">Type de données : **Uint16**</span><span class="sxs-lookup"><span data-stu-id="ddb86-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ddb86-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddb86-176">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ddb86-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ddb86-177">Pondération appliquée à la liste de contrôle d’accès étendue.</span><span class="sxs-lookup"><span data-stu-id="ddb86-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddb86-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddb86-178">Requirements</span></span>



| <span data-ttu-id="ddb86-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddb86-179">Requirement</span></span> | <span data-ttu-id="ddb86-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddb86-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb86-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb86-181">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb86-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ddb86-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ddb86-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb86-183">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb86-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ddb86-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ddb86-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ddb86-185">Namespace</span></span><br/>                | <span data-ttu-id="ddb86-186">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ddb86-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ddb86-187">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb86-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb86-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddb86-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb86-189">DLL</span><span class="sxs-lookup"><span data-stu-id="ddb86-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb86-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ddb86-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ddb86-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb86-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb86-192">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="ddb86-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 


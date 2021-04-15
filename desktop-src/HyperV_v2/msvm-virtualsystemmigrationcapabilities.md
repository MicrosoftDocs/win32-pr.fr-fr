---
description: Définit les moyens permettant à un client de découvrir les méthodes fournies par le service de migration, ainsi que la plage valide des données de paramètres de migration de système virtuel.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Classe Msvm_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525192"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="0cb98-103">MSVM \_ VirtualSystemMigrationCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="0cb98-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="0cb98-104">Définit les moyens permettant à un client de découvrir les méthodes fournies par le service de migration, ainsi que la plage valide des données de paramètres de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="0cb98-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="0cb98-105">L’objet **MSVM \_ VirtualSystemMigrationCapabilities** est associé aux objets [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb98-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="0cb98-106">Ces associations définissent la plage valide des services de migration disponibles.</span><span class="sxs-lookup"><span data-stu-id="0cb98-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="0cb98-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0cb98-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb98-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cb98-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="0cb98-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0cb98-109">Members</span></span>

<span data-ttu-id="0cb98-110">La classe **MSVM \_ VirtualSystemMigrationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0cb98-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0cb98-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cb98-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cb98-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cb98-112">Properties</span></span>

<span data-ttu-id="0cb98-113">La classe **MSVM \_ VirtualSystemMigrationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cb98-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cb98-114">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="0cb98-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-115">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb98-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-117">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="0cb98-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-118">Identifie les méthodes dont l’implémentation peut être asynchrone ; autrement dit, l’opération ne se terminera pas immédiatement et renverra un travail.</span><span class="sxs-lookup"><span data-stu-id="0cb98-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="0cb98-119">Cette propriété est héritée de la **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="0cb98-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="0cb98-120">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="0cb98-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="0cb98-121">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="0cb98-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="0cb98-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span><span class="sxs-lookup"><span data-stu-id="0cb98-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb98-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0cb98-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cb98-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-126">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0cb98-126">A short description of the object.</span></span> <span data-ttu-id="0cb98-127">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de migration ».</span><span class="sxs-lookup"><span data-stu-id="0cb98-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="0cb98-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="0cb98-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cb98-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-131">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="0cb98-131">A description of the object.</span></span> <span data-ttu-id="0cb98-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de migration du système virtuel ».</span><span class="sxs-lookup"><span data-stu-id="0cb98-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="0cb98-133">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="0cb98-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb98-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-136">Tableau des formats de nom pris en charge pour le paramètre *DestinationHost* des méthodes [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) et [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb98-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="0cb98-137">Cette propriété est héritée de la **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="0cb98-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="0cb98-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb98-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="0cb98-139">Signification</span><span class="sxs-lookup"><span data-stu-id="0cb98-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="0cb98-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0cb98-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="0cb98-141">Prise en charge du format de nom de domaine conformément à la norme RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="0cb98-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="0cb98-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0cb98-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0cb98-143">Prise en charge du format décimal avec points IPv4 conformément à la norme RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="0cb98-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="0cb98-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0cb98-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="0cb98-145">Prise en charge du format de texte IPv6 conformément à la norme RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="0cb98-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="0cb98-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0cb98-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cb98-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-149">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0cb98-149">A display name for the object.</span></span> <span data-ttu-id="0cb98-150">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0cb98-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0cb98-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0cb98-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cb98-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-154">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="0cb98-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-155">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0cb98-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0cb98-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0cb98-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0cb98-157">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="0cb98-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb98-158">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb98-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cb98-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb98-160">Identifie les méthodes dont l’implémentation peut être synchrone ; autrement dit, l’opération est effectuée immédiatement et ne retourne pas de tâche.</span><span class="sxs-lookup"><span data-stu-id="0cb98-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="0cb98-161">Cette propriété est héritée de la **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="0cb98-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="0cb98-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="0cb98-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="0cb98-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="0cb98-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="0cb98-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0cb98-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="0cb98-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0cb98-167">)</span><span class="sxs-lookup"><span data-stu-id="0cb98-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cb98-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cb98-168">Requirements</span></span>



| <span data-ttu-id="0cb98-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cb98-169">Requirement</span></span> | <span data-ttu-id="0cb98-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb98-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb98-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb98-171">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb98-172">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cb98-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0cb98-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb98-173">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb98-174">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cb98-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0cb98-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0cb98-175">Namespace</span></span><br/>                | <span data-ttu-id="0cb98-176">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0cb98-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0cb98-177">MOF</span><span class="sxs-lookup"><span data-stu-id="0cb98-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cb98-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cb98-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cb98-179">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb98-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb98-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0cb98-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


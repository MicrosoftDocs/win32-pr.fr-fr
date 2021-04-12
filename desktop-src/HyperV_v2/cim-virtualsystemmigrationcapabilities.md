---
description: Représente les fonctionnalités d’un \_ objet CIM VirtualSystemMigrationService.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: Classe CIM_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528894"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="88e09-103">\_Classe CIM VirtualSystemMigrationCapabilities</span><span class="sxs-lookup"><span data-stu-id="88e09-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="88e09-104">Représente les fonctionnalités d’un objet [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="88e09-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88e09-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="88e09-106">Membres</span><span class="sxs-lookup"><span data-stu-id="88e09-106">Members</span></span>

<span data-ttu-id="88e09-107">La classe **CIM \_ VirtualSystemMigrationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="88e09-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="88e09-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88e09-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88e09-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88e09-109">Properties</span></span>

<span data-ttu-id="88e09-110">La classe **CIM \_ VirtualSystemMigrationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="88e09-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88e09-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="88e09-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e09-112">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88e09-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88e09-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88e09-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e09-114">Tableau qui indique les méthodes [**\_ VirtualSystemMigrationService CIM**](cim-virtualsystemmigrationservice.md) prises en charge pour les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="88e09-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="88e09-115">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="88e09-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="88e09-116">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="88e09-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88e09-117">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="88e09-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88e09-118">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="88e09-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e09-119">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88e09-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88e09-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88e09-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88e09-121">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost (DestinationHost)**","**CIM \_ VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost (DestinationHost)**")</span><span class="sxs-lookup"><span data-stu-id="88e09-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="88e09-122">Tableau qui contient les formats pris en charge pour le paramètre *DestinationHost* des méthodes [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) et [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) pour l’objet [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="88e09-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="88e09-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="88e09-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88e09-124">Prise en charge du format de texte de nom de domaine conformément à la norme RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="88e09-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="88e09-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="88e09-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88e09-126">Prise en charge du format décimal avec points IPv4 conformément à la norme RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="88e09-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="88e09-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="88e09-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88e09-128">Prise en charge du format de texte IPv6 conformément à la norme RFC 4291</span><span class="sxs-lookup"><span data-stu-id="88e09-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88e09-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="88e09-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88e09-130">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="88e09-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88e09-131">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88e09-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88e09-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88e09-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88e09-133">Tableau qui indique les méthodes [**\_ VirtualSystemMigrationService CIM**](cim-virtualsystemmigrationservice.md) prises en charge pour les opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="88e09-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="88e09-134">Énumération des identificateurs de méthode dont l’implémentation peut être synchrone ; autrement dit, l’opération peut se terminer immédiatement et, par conséquent, la méthode ne peut pas retourner de tâche.</span><span class="sxs-lookup"><span data-stu-id="88e09-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="88e09-135">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="88e09-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="88e09-136">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="88e09-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="88e09-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="88e09-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="88e09-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="88e09-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88e09-139">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="88e09-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="88e09-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88e09-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="88e09-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88e09-141">Requirements</span></span>



| <span data-ttu-id="88e09-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88e09-142">Requirement</span></span> | <span data-ttu-id="88e09-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="88e09-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e09-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88e09-144">Minimum supported client</span></span><br/> | <span data-ttu-id="88e09-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="88e09-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="88e09-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88e09-146">Minimum supported server</span></span><br/> | <span data-ttu-id="88e09-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88e09-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="88e09-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88e09-148">Namespace</span></span><br/>                | <span data-ttu-id="88e09-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="88e09-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88e09-150">MOF</span><span class="sxs-lookup"><span data-stu-id="88e09-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88e09-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88e09-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88e09-152">DLL</span><span class="sxs-lookup"><span data-stu-id="88e09-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88e09-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88e09-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88e09-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88e09-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e09-155">**\_Fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="88e09-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 


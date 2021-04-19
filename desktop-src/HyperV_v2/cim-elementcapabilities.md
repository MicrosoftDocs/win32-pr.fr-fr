---
description: Représente une association entre un élément managé et ses fonctionnalités.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: Classe CIM_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531807"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="6d4de-103">\_Classe CIM ElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="6d4de-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="6d4de-104">Représente une association entre un élément managé et ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6d4de-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d4de-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="6d4de-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6d4de-106">Members</span></span>

<span data-ttu-id="6d4de-107">La classe **CIM \_ ElementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6d4de-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6d4de-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d4de-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d4de-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d4de-109">Properties</span></span>

<span data-ttu-id="6d4de-110">La classe **CIM \_ ElementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d4de-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d4de-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6d4de-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d4de-112">Type de données **: \_ fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="6d4de-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="6d4de-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d4de-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d4de-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d4de-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d4de-115">Fonctionnalités associées à l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="6d4de-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="6d4de-116">**Caractéristiques**</span><span class="sxs-lookup"><span data-stu-id="6d4de-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d4de-117">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6d4de-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6d4de-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d4de-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d4de-119">Ensemble d’informations descriptives sur les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6d4de-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="6d4de-120">**Par défaut** (2)</span><span class="sxs-lookup"><span data-stu-id="6d4de-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="6d4de-121">**Actuel** (3)</span><span class="sxs-lookup"><span data-stu-id="6d4de-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6d4de-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6d4de-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="6d4de-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6d4de-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d4de-124">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6d4de-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d4de-125">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6d4de-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="6d4de-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d4de-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d4de-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6d4de-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6d4de-128">Élément managé.</span><span class="sxs-lookup"><span data-stu-id="6d4de-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d4de-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d4de-129">Requirements</span></span>



| <span data-ttu-id="6d4de-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d4de-130">Requirement</span></span> | <span data-ttu-id="6d4de-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d4de-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4de-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4de-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4de-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6d4de-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6d4de-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d4de-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4de-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d4de-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6d4de-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d4de-136">Namespace</span></span><br/>                | <span data-ttu-id="6d4de-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6d4de-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6d4de-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6d4de-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d4de-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d4de-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d4de-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6d4de-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d4de-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d4de-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


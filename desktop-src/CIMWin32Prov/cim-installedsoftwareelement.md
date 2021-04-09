---
description: La \_ classe CIM InstalledSoftwareElement associe un système informatique à un élément logiciel installé.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: Classe CIM_InstalledSoftwareElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110843"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="1faf7-103">\_Classe CIM InstalledSoftwareElement</span><span class="sxs-lookup"><span data-stu-id="1faf7-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="1faf7-104">La classe **CIM \_ InstalledSoftwareElement** associe un système informatique à un élément logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="1faf7-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1faf7-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1faf7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1faf7-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1faf7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1faf7-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1faf7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1faf7-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1faf7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1faf7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1faf7-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="1faf7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1faf7-110">Members</span></span>

<span data-ttu-id="1faf7-111">La classe **CIM \_ InstalledSoftwareElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1faf7-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="1faf7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1faf7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1faf7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1faf7-113">Properties</span></span>

<span data-ttu-id="1faf7-114">La classe **CIM \_ InstalledSoftwareElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1faf7-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1faf7-115">**Logiciels**</span><span class="sxs-lookup"><span data-stu-id="1faf7-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1faf7-116">Type de données : **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="1faf7-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="1faf7-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1faf7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1faf7-118">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="1faf7-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="1faf7-119">Référence à l’élément logiciel installé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="1faf7-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="1faf7-120">**Système**</span><span class="sxs-lookup"><span data-stu-id="1faf7-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1faf7-121">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="1faf7-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1faf7-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1faf7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1faf7-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="1faf7-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="1faf7-124">Référence au système informatique hébergeant un élément logiciel particulier.</span><span class="sxs-lookup"><span data-stu-id="1faf7-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1faf7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1faf7-125">Remarks</span></span>

<span data-ttu-id="1faf7-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1faf7-126">WMI does not implement this class.</span></span> <span data-ttu-id="1faf7-127">Pour les classes dérivées de **CIM \_ InstalledSoftwareElement**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1faf7-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1faf7-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1faf7-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1faf7-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1faf7-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1faf7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1faf7-130">Requirements</span></span>



| <span data-ttu-id="1faf7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1faf7-131">Requirement</span></span> | <span data-ttu-id="1faf7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1faf7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1faf7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1faf7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1faf7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1faf7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1faf7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1faf7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1faf7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1faf7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1faf7-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1faf7-137">Namespace</span></span><br/>                | <span data-ttu-id="1faf7-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1faf7-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1faf7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1faf7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1faf7-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1faf7-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1faf7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1faf7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1faf7-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1faf7-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


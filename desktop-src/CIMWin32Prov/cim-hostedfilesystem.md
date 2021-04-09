---
description: L' \_ Association CIM HostedFileSystem représente un lien entre le système informatique et le système de fichiers hébergé sur le système informatique.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: Classe CIM_HostedFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110850"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="5c561-103">\_Classe CIM HostedFileSystem</span><span class="sxs-lookup"><span data-stu-id="5c561-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="5c561-104">L’Association **CIM \_ HostedFileSystem** représente un lien entre le système informatique et le système de fichiers hébergé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="5c561-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c561-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5c561-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5c561-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5c561-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5c561-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5c561-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5c561-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5c561-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c561-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c561-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5c561-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5c561-110">Members</span></span>

<span data-ttu-id="5c561-111">La classe **CIM \_ HostedFileSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5c561-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="5c561-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c561-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c561-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c561-113">Properties</span></span>

<span data-ttu-id="5c561-114">La classe **CIM \_ HostedFileSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5c561-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c561-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5c561-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c561-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="5c561-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5c561-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c561-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c561-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5c561-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5c561-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique.</span><span class="sxs-lookup"><span data-stu-id="5c561-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="5c561-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5c561-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c561-121">Type de données **: \_ système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="5c561-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5c561-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c561-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c561-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c561-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c561-124">Un système de fichiers [**CIM \_**](cim-filesystem.md) qui décrit le système de fichiers appartenant au système informatique.</span><span class="sxs-lookup"><span data-stu-id="5c561-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c561-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5c561-125">Remarks</span></span>

<span data-ttu-id="5c561-126">La classe **CIM \_ HostedFileSystem** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5c561-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="5c561-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="5c561-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5c561-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5c561-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5c561-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5c561-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c561-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c561-130">Requirements</span></span>



| <span data-ttu-id="5c561-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c561-131">Requirement</span></span> | <span data-ttu-id="5c561-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c561-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c561-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c561-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c561-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c561-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c561-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c561-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c561-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c561-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c561-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5c561-137">Namespace</span></span><br/>                | <span data-ttu-id="5c561-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5c561-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c561-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5c561-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c561-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c561-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c561-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5c561-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c561-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c561-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c561-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c561-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c561-144">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5c561-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


---
description: La \_ classe d’exportation CIM représente une association entre un système de fichiers local et ses répertoires, ce qui indique que les répertoires spécifiés sont disponibles pour le montage.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Classe CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950658"
---
# <a name="cim_export-class"></a><span data-ttu-id="cf5a9-103">\_Classe d’exportation CIM</span><span class="sxs-lookup"><span data-stu-id="cf5a9-103">CIM\_Export class</span></span>

<span data-ttu-id="cf5a9-104">La classe d' **\_ exportation CIM** représente une association entre un système de fichiers local et ses répertoires, ce qui indique que les répertoires spécifiés sont disponibles pour le montage.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="cf5a9-105">Lorsque vous exportez un système de fichiers entier, le répertoire doit référencer le répertoire le plus haut du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf5a9-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf5a9-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf5a9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf5a9-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cf5a9-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5a9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf5a9-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="cf5a9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cf5a9-111">Members</span></span>

<span data-ttu-id="cf5a9-112">La classe d' **\_ exportation CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf5a9-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="cf5a9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf5a9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf5a9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf5a9-114">Properties</span></span>

<span data-ttu-id="cf5a9-115">La classe d' **\_ exportation CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf5a9-116">**Directory**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a9-117">Type de données **: \_ répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf5a9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a9-119">Référence au répertoire exporté pour le montage NFS (Network File System).</span><span class="sxs-lookup"><span data-stu-id="cf5a9-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="cf5a9-120">**ExportedDirectoryName**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a9-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf5a9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a9-123">Nom sous lequel le répertoire est exporté.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="cf5a9-124">**LocalFS**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a9-125">Type de données : **CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="cf5a9-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a9-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf5a9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a9-127">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cf5a9-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cf5a9-128">Référence au système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf5a9-129">Notes</span><span class="sxs-lookup"><span data-stu-id="cf5a9-129">Remarks</span></span>

<span data-ttu-id="cf5a9-130">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-130">WMI does not implement this class.</span></span>

<span data-ttu-id="cf5a9-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf5a9-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cf5a9-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf5a9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf5a9-133">Requirements</span></span>



| <span data-ttu-id="cf5a9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf5a9-134">Requirement</span></span> | <span data-ttu-id="cf5a9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf5a9-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5a9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf5a9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5a9-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf5a9-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf5a9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf5a9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5a9-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf5a9-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf5a9-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf5a9-140">Namespace</span></span><br/>                | <span data-ttu-id="cf5a9-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cf5a9-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf5a9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cf5a9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf5a9-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf5a9-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf5a9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cf5a9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf5a9-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf5a9-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


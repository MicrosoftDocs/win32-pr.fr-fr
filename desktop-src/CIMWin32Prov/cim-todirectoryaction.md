---
description: L' \_ Association CIM ToDirectoryAction identifie le répertoire cible de l’action de fichier.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: Classe CIM_ToDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749052"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="0ec01-103">\_Classe CIM ToDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="0ec01-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="0ec01-104">L’Association **CIM \_ ToDirectoryAction** identifie le répertoire cible de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="0ec01-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="0ec01-105">Lorsque cette association est utilisée, il est supposé que le répertoire cible a été créé par une action précédente.</span><span class="sxs-lookup"><span data-stu-id="0ec01-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="0ec01-106">Cette association ne peut pas exister avec une association [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) , car une action de fichier ne peut impliquer qu’un seul répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="0ec01-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ec01-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0ec01-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0ec01-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0ec01-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0ec01-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0ec01-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0ec01-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0ec01-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec01-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ec01-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="0ec01-112">Membres</span><span class="sxs-lookup"><span data-stu-id="0ec01-112">Members</span></span>

<span data-ttu-id="0ec01-113">La classe **CIM \_ ToDirectoryAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0ec01-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="0ec01-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ec01-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ec01-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ec01-115">Properties</span></span>

<span data-ttu-id="0ec01-116">La classe **CIM \_ ToDirectoryAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ec01-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ec01-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="0ec01-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec01-118">Type de données : **CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="0ec01-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="0ec01-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ec01-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec01-120">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="0ec01-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ec01-121">Référence au répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="0ec01-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="0ec01-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="0ec01-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec01-123">Type de données : **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="0ec01-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="0ec01-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ec01-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec01-125">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="0ec01-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ec01-126">Référence au nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="0ec01-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ec01-127">Notes</span><span class="sxs-lookup"><span data-stu-id="0ec01-127">Remarks</span></span>

<span data-ttu-id="0ec01-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0ec01-128">WMI does not implement this class.</span></span>

<span data-ttu-id="0ec01-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0ec01-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0ec01-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0ec01-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec01-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ec01-131">Requirements</span></span>



| <span data-ttu-id="0ec01-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ec01-132">Requirement</span></span> | <span data-ttu-id="0ec01-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ec01-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec01-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ec01-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec01-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ec01-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ec01-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ec01-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec01-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ec01-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ec01-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ec01-138">Namespace</span></span><br/>                | <span data-ttu-id="0ec01-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0ec01-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0ec01-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0ec01-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ec01-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ec01-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ec01-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0ec01-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ec01-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ec01-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


---
description: L' \_ Association CIM ToDirectorySpecification identifie le répertoire cible de l’action de fichier.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Classe CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111654"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="30664-103">\_Classe CIM ToDirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="30664-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="30664-104">L’Association **CIM \_ ToDirectorySpecification** identifie le répertoire cible de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="30664-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="30664-105">Lorsque cette association est utilisée, il est supposé que le répertoire cible existe déjà.</span><span class="sxs-lookup"><span data-stu-id="30664-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="30664-106">Cette association ne peut pas exister avec une association [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) , car une action de fichier ne peut impliquer qu’un seul répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="30664-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30664-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="30664-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="30664-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="30664-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="30664-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="30664-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="30664-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="30664-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="30664-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30664-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="30664-112">Membres</span><span class="sxs-lookup"><span data-stu-id="30664-112">Members</span></span>

<span data-ttu-id="30664-113">La classe **CIM \_ ToDirectorySpecification** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="30664-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="30664-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30664-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30664-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30664-115">Properties</span></span>

<span data-ttu-id="30664-116">La classe **CIM \_ ToDirectorySpecification** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="30664-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30664-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="30664-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30664-118">Type de données : **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="30664-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="30664-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30664-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30664-120">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="30664-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="30664-121">Référence au répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="30664-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="30664-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="30664-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30664-123">Type de données : **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="30664-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="30664-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30664-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30664-125">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="30664-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="30664-126">Référence au nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="30664-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30664-127">Notes</span><span class="sxs-lookup"><span data-stu-id="30664-127">Remarks</span></span>

<span data-ttu-id="30664-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="30664-128">WMI does not implement this class.</span></span>

<span data-ttu-id="30664-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="30664-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="30664-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="30664-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="30664-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30664-131">Requirements</span></span>



| <span data-ttu-id="30664-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30664-132">Requirement</span></span> | <span data-ttu-id="30664-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="30664-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30664-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30664-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30664-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30664-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30664-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30664-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30664-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30664-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30664-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30664-138">Namespace</span></span><br/>                | <span data-ttu-id="30664-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="30664-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30664-140">MOF</span><span class="sxs-lookup"><span data-stu-id="30664-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30664-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30664-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30664-142">DLL</span><span class="sxs-lookup"><span data-stu-id="30664-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30664-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30664-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


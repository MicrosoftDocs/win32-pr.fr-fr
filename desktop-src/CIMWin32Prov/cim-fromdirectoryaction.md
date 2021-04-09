---
description: L' \_ Association CIM FromDirectoryAction identifie le répertoire source de l’action de fichier.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: Classe CIM_FromDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f485fa32561e746afa16a899a1392b4fddc18f1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861253"
---
# <a name="cim_fromdirectoryaction-class"></a><span data-ttu-id="1db53-103">\_Classe CIM FromDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="1db53-103">CIM\_FromDirectoryAction class</span></span>

<span data-ttu-id="1db53-104">L’Association **CIM \_ FromDirectoryAction** identifie le répertoire source de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="1db53-104">The **CIM\_FromDirectoryAction** association identifies the source directory for the file action.</span></span> <span data-ttu-id="1db53-105">Lorsque cette association est utilisée, l’hypothèse est que le répertoire source a été créé par une action précédente.</span><span class="sxs-lookup"><span data-stu-id="1db53-105">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="1db53-106">Cette association ne peut pas exister avec une association [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) ; une action de fichier ne peut impliquer qu’un seul répertoire source.</span><span class="sxs-lookup"><span data-stu-id="1db53-106">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1db53-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1db53-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1db53-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1db53-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1db53-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1db53-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1db53-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1db53-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db53-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1db53-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="1db53-112">Membres</span><span class="sxs-lookup"><span data-stu-id="1db53-112">Members</span></span>

<span data-ttu-id="1db53-113">La classe **CIM \_ FromDirectoryAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1db53-113">The **CIM\_FromDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="1db53-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1db53-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1db53-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1db53-115">Properties</span></span>

<span data-ttu-id="1db53-116">La classe **CIM \_ FromDirectoryAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1db53-116">The **CIM\_FromDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1db53-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1db53-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db53-118">Type de données : **CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="1db53-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="1db53-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1db53-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1db53-120">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="1db53-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="1db53-121">Référence au nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1db53-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="1db53-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="1db53-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db53-123">Type de données : **CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="1db53-123">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="1db53-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1db53-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1db53-125">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="1db53-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="1db53-126">Référence au répertoire source.</span><span class="sxs-lookup"><span data-stu-id="1db53-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1db53-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1db53-127">Remarks</span></span>

<span data-ttu-id="1db53-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1db53-128">WMI does not implement this class.</span></span>

<span data-ttu-id="1db53-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1db53-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1db53-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1db53-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1db53-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1db53-131">Requirements</span></span>



| <span data-ttu-id="1db53-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1db53-132">Requirement</span></span> | <span data-ttu-id="1db53-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1db53-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1db53-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1db53-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1db53-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1db53-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1db53-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1db53-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1db53-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1db53-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1db53-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1db53-138">Namespace</span></span><br/>                | <span data-ttu-id="1db53-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1db53-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1db53-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1db53-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1db53-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1db53-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1db53-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1db53-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1db53-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1db53-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


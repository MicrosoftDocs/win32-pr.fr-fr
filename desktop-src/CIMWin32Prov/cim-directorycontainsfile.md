---
description: La \_ classe CIM DirectoryContainsFile représente une association entre un répertoire et des fichiers contenus dans ce répertoire.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Classe CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861402"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="8db74-103">\_Classe CIM DirectoryContainsFile</span><span class="sxs-lookup"><span data-stu-id="8db74-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="8db74-104">La classe **CIM \_ DirectoryContainsFile** représente une association entre un répertoire et des fichiers contenus dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="8db74-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8db74-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8db74-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8db74-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8db74-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8db74-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8db74-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8db74-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8db74-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db74-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8db74-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="8db74-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8db74-110">Members</span></span>

<span data-ttu-id="8db74-111">La classe **CIM \_ DirectoryContainsFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8db74-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="8db74-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8db74-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8db74-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8db74-113">Properties</span></span>

<span data-ttu-id="8db74-114">La classe **CIM \_ DirectoryContainsFile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8db74-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8db74-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8db74-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8db74-116">Type de données **: \_ répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="8db74-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="8db74-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8db74-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8db74-118">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8db74-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8db74-119">[**\_ Répertoire CIM**](cim-directory.md) qui décrit le répertoire.</span><span class="sxs-lookup"><span data-stu-id="8db74-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="8db74-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8db74-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8db74-121">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="8db74-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="8db74-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8db74-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8db74-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8db74-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8db74-124">Un [**\_ fichier de fichier CIM**](cim-datafile.md) qui décrit les LogicalFile contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="8db74-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8db74-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8db74-125">Remarks</span></span>

<span data-ttu-id="8db74-126">WMI implémente la classe **CIM \_ DirectoryContainsFile** , qui est une classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="8db74-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="8db74-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8db74-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8db74-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8db74-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db74-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8db74-129">Requirements</span></span>



| <span data-ttu-id="8db74-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8db74-130">Requirement</span></span> | <span data-ttu-id="8db74-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db74-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8db74-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8db74-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8db74-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8db74-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8db74-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8db74-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8db74-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8db74-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8db74-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8db74-136">Namespace</span></span><br/>                | <span data-ttu-id="8db74-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8db74-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8db74-138">MOF</span><span class="sxs-lookup"><span data-stu-id="8db74-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8db74-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8db74-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8db74-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8db74-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db74-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db74-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db74-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8db74-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db74-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="8db74-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


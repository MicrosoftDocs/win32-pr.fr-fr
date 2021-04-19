---
description: L' \_ Association CIM filestorage lie le système de fichiers et les fichiers logiques adressés via le système de fichiers.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: Classe CIM_FileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545770"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="5eea5-103">\_Classe CIM FileStorage</span><span class="sxs-lookup"><span data-stu-id="5eea5-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="5eea5-104">L’Association **CIM \_ FileStorage** lie le système de fichiers et les fichiers logiques adressés via le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5eea5-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5eea5-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5eea5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5eea5-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5eea5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5eea5-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5eea5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5eea5-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5eea5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eea5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5eea5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5eea5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5eea5-110">Members</span></span>

<span data-ttu-id="5eea5-111">La classe **CIM \_ FileStorage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5eea5-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="5eea5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5eea5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5eea5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5eea5-113">Properties</span></span>

<span data-ttu-id="5eea5-114">La classe **CIM \_ FileStorage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5eea5-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5eea5-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5eea5-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eea5-116">Type de données **: \_ système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="5eea5-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5eea5-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5eea5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eea5-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5eea5-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5eea5-119">Système [**de \_ fichiers CIM**](cim-filesystem.md) décrivant le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5eea5-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="5eea5-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5eea5-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eea5-121">Type de données : **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="5eea5-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="5eea5-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5eea5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eea5-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5eea5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5eea5-124">[**\_ LogicalFile CIM**](cim-logicalfile.md) décrivant le fichier logique stocké dans le contexte du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5eea5-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eea5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5eea5-125">Remarks</span></span>

<span data-ttu-id="5eea5-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="5eea5-126">WMI does not implement this class.</span></span>

<span data-ttu-id="5eea5-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5eea5-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5eea5-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5eea5-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eea5-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5eea5-129">Requirements</span></span>



| <span data-ttu-id="5eea5-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5eea5-130">Requirement</span></span> | <span data-ttu-id="5eea5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5eea5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eea5-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eea5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5eea5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5eea5-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5eea5-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eea5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5eea5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5eea5-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5eea5-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5eea5-136">Namespace</span></span><br/>                | <span data-ttu-id="5eea5-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5eea5-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5eea5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5eea5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eea5-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eea5-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5eea5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5eea5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eea5-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eea5-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eea5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eea5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eea5-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="5eea5-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


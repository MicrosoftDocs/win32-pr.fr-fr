---
description: La \_ classe WMI de l’Association LogicalDiskRootDirectory Win32 associe un disque logique et sa structure de répertoires.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847041"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="ebe56-103">\_Classe LogicalDiskRootDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="ebe56-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="ebe56-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LogicalDiskRootDirectory Win32** associe un disque logique et sa structure de répertoires.</span><span class="sxs-lookup"><span data-stu-id="ebe56-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="ebe56-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ebe56-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ebe56-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ebe56-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe56-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe56-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ebe56-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ebe56-108">Members</span></span>

<span data-ttu-id="ebe56-109">La classe **Win32 \_ LogicalDiskRootDirectory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ebe56-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="ebe56-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebe56-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebe56-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebe56-111">Properties</span></span>

<span data-ttu-id="ebe56-112">La classe **Win32 \_ LogicalDiskRootDirectory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ebe56-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebe56-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ebe56-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe56-114">Type de données **: \_ disque logique Win32**</span><span class="sxs-lookup"><span data-stu-id="ebe56-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="ebe56-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ebe56-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe56-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="ebe56-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="ebe56-117">Référence à l’instance représentant les propriétés du disque logique.</span><span class="sxs-lookup"><span data-stu-id="ebe56-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="ebe56-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ebe56-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebe56-119">Type de données **: \_ répertoire win32**</span><span class="sxs-lookup"><span data-stu-id="ebe56-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="ebe56-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ebe56-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebe56-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« PartComponent »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| répertoire win32 Win32 \_ »)</span><span class="sxs-lookup"><span data-stu-id="ebe56-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="ebe56-122">Référence à l’instance de qui représente les propriétés de la structure de répertoires de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ebe56-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebe56-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ebe56-123">Remarks</span></span>

<span data-ttu-id="ebe56-124">La classe **Win32 \_ LogicalDiskRootDirectory** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="ebe56-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe56-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe56-125">Requirements</span></span>



| <span data-ttu-id="ebe56-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebe56-126">Requirement</span></span> | <span data-ttu-id="ebe56-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebe56-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe56-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe56-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe56-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebe56-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebe56-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe56-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe56-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebe56-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebe56-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ebe56-132">Namespace</span></span><br/>                | <span data-ttu-id="ebe56-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ebe56-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ebe56-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ebe56-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebe56-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebe56-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebe56-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ebe56-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebe56-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebe56-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe56-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe56-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe56-139">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="ebe56-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="ebe56-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebe56-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


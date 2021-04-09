---
description: La \_ classe WMI de l’Association ProgramGroupContents Win32 associe un ordre de groupe de programmes et un groupe de programmes individuel ou un élément qu’elle contient.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033614"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="6a8f3-103">\_Classe ProgramGroupContents Win32</span><span class="sxs-lookup"><span data-stu-id="6a8f3-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="6a8f3-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ ProgramGroupContents Win32** associe un ordre de groupe de programmes et un groupe de programmes individuel ou un élément qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="6a8f3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6a8f3-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a8f3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6a8f3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6a8f3-108">Members</span></span>

<span data-ttu-id="6a8f3-109">La classe **Win32 \_ ProgramGroupContents** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a8f3-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="6a8f3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a8f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a8f3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a8f3-111">Properties</span></span>

<span data-ttu-id="6a8f3-112">La classe **Win32 \_ ProgramGroupContents** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a8f3-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6a8f3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a8f3-114">Type de données : **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="6a8f3-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="6a8f3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a8f3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a8f3-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="6a8f3-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="6a8f3-117">Référence à l’instance de qui représente le groupe de programmes logique pour cette association.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="6a8f3-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6a8f3-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a8f3-119">Type de données : **Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="6a8f3-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="6a8f3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a8f3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a8f3-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")</span><span class="sxs-lookup"><span data-stu-id="6a8f3-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="6a8f3-122">Référence à l’instance représentant le groupe ou l’élément du menu **Démarrer** pour cette association.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a8f3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6a8f3-123">Remarks</span></span>

<span data-ttu-id="6a8f3-124">La classe **Win32 \_ ProgramGroupContents** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="6a8f3-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8f3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a8f3-125">Requirements</span></span>



| <span data-ttu-id="6a8f3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a8f3-126">Requirement</span></span> | <span data-ttu-id="6a8f3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8f3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8f3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8f3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8f3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a8f3-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a8f3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8f3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8f3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a8f3-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a8f3-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a8f3-132">Namespace</span></span><br/>                | <span data-ttu-id="6a8f3-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6a8f3-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a8f3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6a8f3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a8f3-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a8f3-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a8f3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8f3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8f3-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a8f3-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a8f3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a8f3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8f3-139">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="6a8f3-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="6a8f3-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6a8f3-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

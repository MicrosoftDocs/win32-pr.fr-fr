---
description: La \_ classe WMI de l’Association SystemResources Win32 associe une ressource système et le système informatique sur lequel elle réside.
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Classe Win32_SystemResources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950624"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="687f8-103">\_Classe SystemResources Win32</span><span class="sxs-lookup"><span data-stu-id="687f8-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="687f8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemResources Win32** associe une ressource système et le système informatique sur lequel elle réside.</span><span class="sxs-lookup"><span data-stu-id="687f8-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="687f8-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="687f8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="687f8-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="687f8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="687f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="687f8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="687f8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="687f8-108">Members</span></span>

<span data-ttu-id="687f8-109">La classe **Win32 \_ SystemResources** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="687f8-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="687f8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="687f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="687f8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="687f8-111">Properties</span></span>

<span data-ttu-id="687f8-112">La classe **Win32 \_ SystemResources** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="687f8-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687f8-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="687f8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687f8-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="687f8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="687f8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="687f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687f8-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="687f8-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="687f8-117">Référence à l’instance représentant le système de l’ordinateur où se trouve la ressource.</span><span class="sxs-lookup"><span data-stu-id="687f8-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="687f8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="687f8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687f8-119">Type de données : **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="687f8-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="687f8-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="687f8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687f8-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="687f8-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="687f8-122">Référence à l’instance représentant la ressource (par exemple, les services d’e/s et les ressources mémoire) disponible sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="687f8-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="687f8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="687f8-123">Remarks</span></span>

<span data-ttu-id="687f8-124">La classe **Win32 \_ SystemResources** est dérivée de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="687f8-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="687f8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="687f8-125">Requirements</span></span>



| <span data-ttu-id="687f8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="687f8-126">Requirement</span></span> | <span data-ttu-id="687f8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="687f8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="687f8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687f8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="687f8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="687f8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="687f8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687f8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="687f8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="687f8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="687f8-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="687f8-132">Namespace</span></span><br/>                | <span data-ttu-id="687f8-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="687f8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="687f8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="687f8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687f8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="687f8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="687f8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="687f8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687f8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687f8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="687f8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="687f8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687f8-139">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="687f8-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="687f8-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="687f8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

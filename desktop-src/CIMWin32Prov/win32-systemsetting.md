---
description: La \_ classe WMI d’association abstraite SystemSetting de Win32 associe un système informatique et un paramètre général sur ce système.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Classe Win32_SystemSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483896"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="80bcd-103">\_Classe SystemSetting Win32</span><span class="sxs-lookup"><span data-stu-id="80bcd-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="80bcd-104">La [classe WMI](../wmisdk/retrieving-a-class.md) d’association abstraite **\_ SystemSetting de Win32** associe un système informatique et un paramètre général sur ce système.</span><span class="sxs-lookup"><span data-stu-id="80bcd-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="80bcd-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80bcd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="80bcd-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="80bcd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bcd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80bcd-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="80bcd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="80bcd-108">Members</span></span>

<span data-ttu-id="80bcd-109">La classe **Win32 \_ SystemSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80bcd-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="80bcd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80bcd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80bcd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80bcd-111">Properties</span></span>

<span data-ttu-id="80bcd-112">La classe **Win32 \_ SystemSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="80bcd-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80bcd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="80bcd-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bcd-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="80bcd-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="80bcd-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80bcd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bcd-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="80bcd-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="80bcd-117">Référence à l’instance de qui représente les propriétés d’un système informatique sur lequel ce paramètre peut être appliqué.</span><span class="sxs-lookup"><span data-stu-id="80bcd-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="80bcd-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="80bcd-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bcd-119">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="80bcd-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="80bcd-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80bcd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bcd-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« paramètre »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« paramètre CIM \| CIM \_ »)</span><span class="sxs-lookup"><span data-stu-id="80bcd-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="80bcd-122">Référence à l’instance de qui représente les propriétés du paramètre qui peut être appliqué au système informatique.</span><span class="sxs-lookup"><span data-stu-id="80bcd-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80bcd-123">Notes</span><span class="sxs-lookup"><span data-stu-id="80bcd-123">Remarks</span></span>

<span data-ttu-id="80bcd-124">La classe **Win32 \_ SystemSetting** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="80bcd-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80bcd-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80bcd-125">Requirements</span></span>



| <span data-ttu-id="80bcd-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80bcd-126">Requirement</span></span> | <span data-ttu-id="80bcd-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="80bcd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80bcd-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80bcd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="80bcd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80bcd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80bcd-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80bcd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="80bcd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80bcd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80bcd-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80bcd-132">Namespace</span></span><br/>                | <span data-ttu-id="80bcd-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="80bcd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="80bcd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="80bcd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80bcd-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80bcd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="80bcd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="80bcd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80bcd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80bcd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80bcd-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80bcd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bcd-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="80bcd-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="80bcd-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="80bcd-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

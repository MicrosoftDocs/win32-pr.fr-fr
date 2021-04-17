---
description: La \_ classe WMI de l’Association SystemSystemDriver Win32 associe un système informatique et un pilote système s’exécutant sur ce système informatique.
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Classe Win32_SystemSystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524231"
---
# <a name="win32_systemsystemdriver-class"></a><span data-ttu-id="e2e0f-103">\_Classe SystemSystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="e2e0f-103">Win32\_SystemSystemDriver class</span></span>

<span data-ttu-id="e2e0f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemSystemDriver Win32** associe un système informatique et un pilote système s’exécutant sur ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-104">The **Win32\_SystemSystemDriver** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a system driver running on that computer system.</span></span>

<span data-ttu-id="e2e0f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e2e0f-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2e0f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e2e0f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e2e0f-108">Members</span></span>

<span data-ttu-id="e2e0f-109">La classe **Win32 \_ SystemSystemDriver** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2e0f-109">The **Win32\_SystemSystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="e2e0f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2e0f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2e0f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2e0f-111">Properties</span></span>

<span data-ttu-id="e2e0f-112">La classe **Win32 \_ SystemSystemDriver** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-112">The **Win32\_SystemSystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2e0f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e2e0f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e0f-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e2e0f-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e2e0f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2e0f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e0f-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="e2e0f-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="e2e0f-117">Référence à l’instance de qui représente les propriétés du système informatique sur lequel le pilote s’exécute.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-117">Reference to the instance representing the properties of the computer system upon which the driver is running.</span></span>

</dd> <dt>

<span data-ttu-id="e2e0f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e2e0f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e0f-119">Type de données : **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="e2e0f-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="e2e0f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2e0f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e0f-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="e2e0f-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="e2e0f-122">Référence à l’instance de qui représente le pilote système en cours d’exécution sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="e2e0f-122">Reference to the instance representing the system driver running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2e0f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e2e0f-123">Remarks</span></span>

<span data-ttu-id="e2e0f-124">La classe **Win32 \_ SystemSystemDriver** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="e2e0f-124">The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e0f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e0f-125">Requirements</span></span>



| <span data-ttu-id="e2e0f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e0f-126">Requirement</span></span> | <span data-ttu-id="e2e0f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e0f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e0f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e0f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e0f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2e0f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2e0f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e0f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e0f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2e0f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2e0f-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e2e0f-132">Namespace</span></span><br/>                | <span data-ttu-id="e2e0f-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e2e0f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2e0f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e2e0f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2e0f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2e0f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2e0f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e0f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2e0f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e0f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e0f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e0f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e0f-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e2e0f-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="e2e0f-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e2e0f-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

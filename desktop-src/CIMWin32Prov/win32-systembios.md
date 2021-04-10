---
description: La \_ classe WMI de l’Association SystemBIOS Win32 associe un système informatique (y compris des données telles que les propriétés de démarrage, les fuseaux horaires, les configurations de démarrage ou les mots de passe d’administration) et un BIOS système (services, langues et propriétés de gestion du système).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Classe Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861574"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="69a12-103">\_Classe SystemBIOS Win32</span><span class="sxs-lookup"><span data-stu-id="69a12-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="69a12-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemBIOS Win32** associe un système informatique (y compris des données telles que les propriétés de démarrage, les fuseaux horaires, les configurations de démarrage ou les mots de passe d’administration) et un BIOS système (services, langues et propriétés de gestion du système).</span><span class="sxs-lookup"><span data-stu-id="69a12-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="69a12-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="69a12-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="69a12-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="69a12-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a12-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69a12-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="69a12-108">Membres</span><span class="sxs-lookup"><span data-stu-id="69a12-108">Members</span></span>

<span data-ttu-id="69a12-109">La classe **Win32 \_ SystemBIOS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="69a12-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="69a12-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69a12-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69a12-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69a12-111">Properties</span></span>

<span data-ttu-id="69a12-112">La classe **Win32 \_ SystemBIOS** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="69a12-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69a12-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="69a12-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a12-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="69a12-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="69a12-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69a12-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69a12-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="69a12-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="69a12-117">Le [**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) qui contient le BIOS de l’Association.</span><span class="sxs-lookup"><span data-stu-id="69a12-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="69a12-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="69a12-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a12-119">Type de données **: \_ BIOS Win32**</span><span class="sxs-lookup"><span data-stu-id="69a12-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="69a12-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69a12-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69a12-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« PartComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| BIOS Win32 WMI \_ »)</span><span class="sxs-lookup"><span data-stu-id="69a12-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="69a12-122">Un [**\_ BIOS Win32**](win32-bios.md) contenu dans le système informatique de cette association.</span><span class="sxs-lookup"><span data-stu-id="69a12-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69a12-123">Notes</span><span class="sxs-lookup"><span data-stu-id="69a12-123">Remarks</span></span>

<span data-ttu-id="69a12-124">La classe **Win32 \_ SystemBIOS** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="69a12-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69a12-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69a12-125">Requirements</span></span>



| <span data-ttu-id="69a12-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69a12-126">Requirement</span></span> | <span data-ttu-id="69a12-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="69a12-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69a12-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69a12-128">Minimum supported client</span></span><br/> | <span data-ttu-id="69a12-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69a12-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69a12-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69a12-130">Minimum supported server</span></span><br/> | <span data-ttu-id="69a12-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69a12-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69a12-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69a12-132">Namespace</span></span><br/>                | <span data-ttu-id="69a12-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="69a12-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69a12-134">MOF</span><span class="sxs-lookup"><span data-stu-id="69a12-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69a12-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69a12-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69a12-136">DLL</span><span class="sxs-lookup"><span data-stu-id="69a12-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69a12-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69a12-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69a12-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a12-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a12-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="69a12-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="69a12-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="69a12-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

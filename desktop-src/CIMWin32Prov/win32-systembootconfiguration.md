---
description: La \_ classe WMI de l’Association SystemBootConfiguration Win32 associe un système informatique et sa configuration de démarrage.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Classe Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861166"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="68217-103">\_Classe SystemBootConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="68217-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="68217-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemBootConfiguration Win32** associe un système informatique et sa configuration de démarrage.</span><span class="sxs-lookup"><span data-stu-id="68217-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="68217-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="68217-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68217-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="68217-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68217-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68217-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="68217-108">Membres</span><span class="sxs-lookup"><span data-stu-id="68217-108">Members</span></span>

<span data-ttu-id="68217-109">La classe **Win32 \_ SystemBootConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="68217-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="68217-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68217-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68217-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68217-111">Properties</span></span>

<span data-ttu-id="68217-112">La classe **Win32 \_ SystemBootConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="68217-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68217-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68217-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68217-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="68217-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="68217-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68217-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68217-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="68217-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="68217-117">Référence à l’instance de qui représente le système informatique à l’aide de la configuration de démarrage.</span><span class="sxs-lookup"><span data-stu-id="68217-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="68217-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="68217-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68217-119">Type de données : **Win32 \_ BootConfiguration**</span><span class="sxs-lookup"><span data-stu-id="68217-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="68217-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68217-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68217-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")</span><span class="sxs-lookup"><span data-stu-id="68217-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="68217-122">Référence à l’instance représentant la configuration de démarrage pour le système informatique.</span><span class="sxs-lookup"><span data-stu-id="68217-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68217-123">Notes</span><span class="sxs-lookup"><span data-stu-id="68217-123">Remarks</span></span>

<span data-ttu-id="68217-124">La classe **Win32 \_ SystemBootConfiguration** est dérivée de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="68217-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68217-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68217-125">Requirements</span></span>



| <span data-ttu-id="68217-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68217-126">Requirement</span></span> | <span data-ttu-id="68217-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="68217-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68217-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68217-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68217-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68217-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68217-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68217-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68217-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68217-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68217-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68217-132">Namespace</span></span><br/>                | <span data-ttu-id="68217-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="68217-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68217-134">MOF</span><span class="sxs-lookup"><span data-stu-id="68217-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68217-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68217-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68217-136">DLL</span><span class="sxs-lookup"><span data-stu-id="68217-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68217-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68217-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68217-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68217-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68217-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="68217-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="68217-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="68217-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

---
description: La \_ classe WMI de l’Association SystemDesktop Win32 associe un système informatique et sa configuration de bureau.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Classe Win32_SystemDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950820"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="dcd03-103">\_Classe SystemDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="dcd03-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="dcd03-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemDesktop Win32** associe un système informatique et sa configuration de bureau.</span><span class="sxs-lookup"><span data-stu-id="dcd03-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="dcd03-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dcd03-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dcd03-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="dcd03-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcd03-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="dcd03-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dcd03-108">Members</span></span>

<span data-ttu-id="dcd03-109">La classe **Win32 \_ SystemDesktop** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dcd03-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="dcd03-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dcd03-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcd03-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dcd03-111">Properties</span></span>

<span data-ttu-id="dcd03-112">La classe **Win32 \_ SystemDesktop** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dcd03-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcd03-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dcd03-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcd03-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="dcd03-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="dcd03-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dcd03-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcd03-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="dcd03-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="dcd03-117">Référence à l’instance représentant le système de l’ordinateur où se trouve la configuration du bureau.</span><span class="sxs-lookup"><span data-stu-id="dcd03-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="dcd03-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="dcd03-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcd03-119">Type de données **: \_ Bureau Win32**</span><span class="sxs-lookup"><span data-stu-id="dcd03-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="dcd03-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dcd03-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcd03-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="dcd03-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="dcd03-122">Référence à l’instance représentant la configuration existante sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="dcd03-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcd03-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dcd03-123">Remarks</span></span>

<span data-ttu-id="dcd03-124">La classe **Win32 \_ SystemDesktop** est dérivée de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="dcd03-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd03-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcd03-125">Requirements</span></span>



| <span data-ttu-id="dcd03-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcd03-126">Requirement</span></span> | <span data-ttu-id="dcd03-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcd03-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd03-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcd03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd03-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcd03-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dcd03-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcd03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd03-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcd03-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dcd03-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dcd03-132">Namespace</span></span><br/>                | <span data-ttu-id="dcd03-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dcd03-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dcd03-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dcd03-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcd03-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcd03-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcd03-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dcd03-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcd03-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcd03-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd03-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcd03-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd03-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="dcd03-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="dcd03-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="dcd03-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

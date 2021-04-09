---
description: La \_ classe WMI de l’Association SystemTimeZone Win32 associe un système informatique et un fuseau horaire.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Classe Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861157"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="7c35f-103">\_Classe SystemTimeZone Win32</span><span class="sxs-lookup"><span data-stu-id="7c35f-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="7c35f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemTimeZone Win32** associe un système informatique et un fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="7c35f-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="7c35f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7c35f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7c35f-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7c35f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c35f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c35f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="7c35f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7c35f-108">Members</span></span>

<span data-ttu-id="7c35f-109">La classe **Win32 \_ SystemTimeZone** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c35f-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="7c35f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c35f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c35f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c35f-111">Properties</span></span>

<span data-ttu-id="7c35f-112">La classe **Win32 \_ SystemTimeZone** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c35f-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c35f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c35f-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c35f-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="7c35f-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7c35f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c35f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c35f-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="7c35f-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7c35f-117">Référence à l’instance représentant le système informatique effectuant le suivi du fuseau horaire système.</span><span class="sxs-lookup"><span data-stu-id="7c35f-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="7c35f-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="7c35f-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c35f-119">Type de données **: \_ fuseau horaire Win32**</span><span class="sxs-lookup"><span data-stu-id="7c35f-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="7c35f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c35f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c35f-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")</span><span class="sxs-lookup"><span data-stu-id="7c35f-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="7c35f-122">Référence à l’instance représentant les propriétés de fuseau horaire suivies par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="7c35f-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c35f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7c35f-123">Remarks</span></span>

<span data-ttu-id="7c35f-124">La classe **Win32 \_ SystemTimeZone** est dérivée de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="7c35f-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c35f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c35f-125">Requirements</span></span>



| <span data-ttu-id="7c35f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c35f-126">Requirement</span></span> | <span data-ttu-id="7c35f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c35f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c35f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c35f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c35f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c35f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c35f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c35f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c35f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c35f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c35f-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c35f-132">Namespace</span></span><br/>                | <span data-ttu-id="7c35f-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7c35f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c35f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7c35f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c35f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c35f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c35f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c35f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c35f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c35f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c35f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c35f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c35f-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="7c35f-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="7c35f-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7c35f-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

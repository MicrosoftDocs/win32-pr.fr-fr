---
description: La \_ classe WMI de l’Association SystemUsers Win32 associe un système informatique et un compte d’utilisateur sur ce système.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Classe Win32_SystemUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950818"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="6c9b8-103">\_Classe SystemUsers Win32</span><span class="sxs-lookup"><span data-stu-id="6c9b8-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="6c9b8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemUsers Win32** associe un système informatique et un compte d’utilisateur sur ce système.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="6c9b8-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6c9b8-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9b8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c9b8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6c9b8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6c9b8-108">Members</span></span>

<span data-ttu-id="6c9b8-109">La classe **Win32 \_ SystemUsers** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6c9b8-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="6c9b8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c9b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c9b8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c9b8-111">Properties</span></span>

<span data-ttu-id="6c9b8-112">La classe **Win32 \_ SystemUsers** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c9b8-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6c9b8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9b8-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6c9b8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6c9b8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c9b8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9b8-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="6c9b8-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="6c9b8-117">Référence à l’instance de qui représente le système informatique contenant le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="6c9b8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6c9b8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9b8-119">Type de données : **Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="6c9b8-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="6c9b8-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c9b8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9b8-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")</span><span class="sxs-lookup"><span data-stu-id="6c9b8-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="6c9b8-122">Référence à l’instance de qui représente le compte d’utilisateur sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="6c9b8-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c9b8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6c9b8-123">Remarks</span></span>

<span data-ttu-id="6c9b8-124">La classe **Win32 \_ SystemUsers** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6c9b8-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9b8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c9b8-125">Requirements</span></span>



| <span data-ttu-id="6c9b8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c9b8-126">Requirement</span></span> | <span data-ttu-id="6c9b8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c9b8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9b8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9b8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c9b8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c9b8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9b8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c9b8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c9b8-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c9b8-132">Namespace</span></span><br/>                | <span data-ttu-id="6c9b8-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6c9b8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c9b8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6c9b8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c9b8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c9b8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c9b8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6c9b8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c9b8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c9b8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9b8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c9b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9b8-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6c9b8-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="6c9b8-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6c9b8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

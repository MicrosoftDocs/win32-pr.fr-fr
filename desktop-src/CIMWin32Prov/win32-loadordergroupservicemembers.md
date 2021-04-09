---
description: La \_ classe WMI de l’Association LoadOrderGroupServiceMembers Win32 associe un groupe d’ordre de chargement et un service de base.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceMembers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861650"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="fe022-103">\_Classe LoadOrderGroupServiceMembers Win32</span><span class="sxs-lookup"><span data-stu-id="fe022-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="fe022-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LoadOrderGroupServiceMembers Win32** associe un groupe d’ordre de chargement et un service de base.</span><span class="sxs-lookup"><span data-stu-id="fe022-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="fe022-105">[**Win32 \_**](win32-systemdriver.md) Les objets SystemDriver sont membres de ce groupe d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="fe022-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="fe022-106">Tous les services ne sont pas membres de groupes, et tous les groupes ne disposent pas de services.</span><span class="sxs-lookup"><span data-stu-id="fe022-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="fe022-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fe022-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fe022-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fe022-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe022-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe022-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fe022-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fe022-110">Members</span></span>

<span data-ttu-id="fe022-111">La classe **Win32 \_ LoadOrderGroupServiceMembers** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fe022-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="fe022-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe022-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe022-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe022-113">Properties</span></span>

<span data-ttu-id="fe022-114">La classe **Win32 \_ LoadOrderGroupServiceMembers** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fe022-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe022-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fe022-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe022-116">Type de données : **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="fe022-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="fe022-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe022-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe022-118">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="fe022-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="fe022-119">Référence à l’instance représentant les propriétés de groupe d’ordre de chargement associées au service de base.</span><span class="sxs-lookup"><span data-stu-id="fe022-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="fe022-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fe022-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe022-121">Type de données : **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="fe022-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="fe022-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe022-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe022-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="fe022-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="fe022-124">Référence à l’instance représentant le service qui est membre d’un groupe d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="fe022-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe022-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fe022-125">Remarks</span></span>

<span data-ttu-id="fe022-126">La classe **Win32 \_ LoadOrderGroupServiceMembers** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="fe022-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe022-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe022-127">Requirements</span></span>



| <span data-ttu-id="fe022-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe022-128">Requirement</span></span> | <span data-ttu-id="fe022-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe022-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe022-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe022-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fe022-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe022-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe022-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe022-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fe022-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe022-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe022-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe022-134">Namespace</span></span><br/>                | <span data-ttu-id="fe022-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fe022-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe022-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fe022-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe022-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe022-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe022-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fe022-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe022-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe022-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe022-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe022-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe022-141">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="fe022-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="fe022-142">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe022-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


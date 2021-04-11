---
description: La \_ classe WMI d’association abstraite COMApplicationClasses de Win32 lie un composant COM (Component Object Model) et l’application com où il réside.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111231"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="967ab-103">\_Classe COMApplicationClasses Win32</span><span class="sxs-lookup"><span data-stu-id="967ab-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="967ab-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) d’association abstraite **\_ COMApplicationClasses de Win32** lie un composant COM (Component Object Model) et l’application com où il réside.</span><span class="sxs-lookup"><span data-stu-id="967ab-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="967ab-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="967ab-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="967ab-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="967ab-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="967ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="967ab-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="967ab-108">Membres</span><span class="sxs-lookup"><span data-stu-id="967ab-108">Members</span></span>

<span data-ttu-id="967ab-109">La classe **Win32 \_ COMApplicationClasses** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="967ab-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="967ab-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="967ab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="967ab-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="967ab-111">Properties</span></span>

<span data-ttu-id="967ab-112">La classe **Win32 \_ COMApplicationClasses** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="967ab-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="967ab-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="967ab-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="967ab-114">Type de données : **Win32 \_ comapplication**</span><span class="sxs-lookup"><span data-stu-id="967ab-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="967ab-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="967ab-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="967ab-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comapplication")</span><span class="sxs-lookup"><span data-stu-id="967ab-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="967ab-117">Une [**\_ application Win32**](win32-comapplication.md) qui représente l’application com contenant le composant com.</span><span class="sxs-lookup"><span data-stu-id="967ab-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="967ab-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="967ab-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="967ab-119">Type de données : **Win32 \_ ComClass**</span><span class="sxs-lookup"><span data-stu-id="967ab-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="967ab-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="967ab-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="967ab-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComClass")</span><span class="sxs-lookup"><span data-stu-id="967ab-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="967ab-122">Une [**\_ classe Win32**](win32-comclass.md) qui représente le composant com groupé sous l’application com.</span><span class="sxs-lookup"><span data-stu-id="967ab-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="967ab-123">Notes</span><span class="sxs-lookup"><span data-stu-id="967ab-123">Remarks</span></span>

<span data-ttu-id="967ab-124">La classe **Win32 \_ COMApplicationClasses** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="967ab-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="967ab-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="967ab-125">Requirements</span></span>



| <span data-ttu-id="967ab-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="967ab-126">Requirement</span></span> | <span data-ttu-id="967ab-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="967ab-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="967ab-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="967ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="967ab-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="967ab-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="967ab-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="967ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="967ab-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="967ab-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="967ab-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="967ab-132">Namespace</span></span><br/>                | <span data-ttu-id="967ab-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="967ab-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="967ab-134">MOF</span><span class="sxs-lookup"><span data-stu-id="967ab-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="967ab-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="967ab-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="967ab-136">DLL</span><span class="sxs-lookup"><span data-stu-id="967ab-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967ab-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967ab-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967ab-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="967ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967ab-139">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="967ab-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="967ab-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="967ab-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


---
description: La \_ classe WMI de l’Association Win32 ClassicCOMClassSettings lie une classe com (Component Object Model) et les paramètres utilisés pour configurer des instances de la classe com.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860698"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="9e2ea-103">\_Classe ClassicCOMClassSettings Win32</span><span class="sxs-lookup"><span data-stu-id="9e2ea-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="9e2ea-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **Win32 \_ CLASSICCOMCLASSSETTINGS** lie une classe com (Component Object Model) et les paramètres utilisés pour configurer des instances de la classe com.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="9e2ea-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9e2ea-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e2ea-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="9e2ea-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9e2ea-108">Members</span></span>

<span data-ttu-id="9e2ea-109">La classe **Win32 \_ ClassicCOMClassSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e2ea-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="9e2ea-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e2ea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e2ea-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e2ea-111">Properties</span></span>

<span data-ttu-id="9e2ea-112">La classe **Win32 \_ ClassicCOMClassSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e2ea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e2ea-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e2ea-114">Type de données : **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="9e2ea-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="9e2ea-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e2ea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e2ea-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="9e2ea-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="9e2ea-117">[**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) qui représente la classe com dans laquelle les paramètres sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="9e2ea-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="9e2ea-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e2ea-119">Type de données : **Win32 \_ ClassicCOMClassSetting**</span><span class="sxs-lookup"><span data-stu-id="9e2ea-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="9e2ea-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e2ea-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e2ea-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")</span><span class="sxs-lookup"><span data-stu-id="9e2ea-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="9e2ea-122">[**\_ ClassicCOMClassSetting Win32**](win32-classiccomclasssetting.md) qui représente les paramètres de configuration associés à la classe com.</span><span class="sxs-lookup"><span data-stu-id="9e2ea-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e2ea-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9e2ea-123">Remarks</span></span>

<span data-ttu-id="9e2ea-124">La classe **Win32 \_ ClassicCOMClassSettings** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9e2ea-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2ea-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e2ea-125">Requirements</span></span>



| <span data-ttu-id="9e2ea-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e2ea-126">Requirement</span></span> | <span data-ttu-id="9e2ea-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2ea-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2ea-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e2ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2ea-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e2ea-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e2ea-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e2ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2ea-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e2ea-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e2ea-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e2ea-132">Namespace</span></span><br/>                | <span data-ttu-id="9e2ea-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9e2ea-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e2ea-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9e2ea-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e2ea-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e2ea-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e2ea-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9e2ea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e2ea-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e2ea-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2ea-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e2ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2ea-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="9e2ea-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="9e2ea-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e2ea-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


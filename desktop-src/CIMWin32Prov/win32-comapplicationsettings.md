---
description: La \_ classe WMI de l’Association COMApplicationSettings Win32 lie une application DCOM et ses paramètres de configuration.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200891"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="c49e0-103">\_Classe COMApplicationSettings Win32</span><span class="sxs-lookup"><span data-stu-id="c49e0-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="c49e0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ COMApplicationSettings Win32** lie une application DCOM et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c49e0-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="c49e0-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c49e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c49e0-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c49e0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49e0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c49e0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="c49e0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c49e0-108">Members</span></span>

<span data-ttu-id="c49e0-109">La classe **Win32 \_ COMApplicationSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c49e0-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="c49e0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c49e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c49e0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c49e0-111">Properties</span></span>

<span data-ttu-id="c49e0-112">La classe **Win32 \_ COMApplicationSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c49e0-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c49e0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c49e0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49e0-114">Type de données : **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="c49e0-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="c49e0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c49e0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c49e0-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="c49e0-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="c49e0-117">[**\_ DCOMApplication Win32**](win32-dcomapplication.md) qui représente l’application DCOM dans laquelle les paramètres sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="c49e0-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="c49e0-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="c49e0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c49e0-119">Type de données : **Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="c49e0-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="c49e0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c49e0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c49e0-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")</span><span class="sxs-lookup"><span data-stu-id="c49e0-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="c49e0-122">[**\_ DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md) qui représente les paramètres de configuration associés à l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="c49e0-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c49e0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c49e0-123">Remarks</span></span>

<span data-ttu-id="c49e0-124">La classe **Win32 \_ COMApplicationSettings** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="c49e0-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c49e0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c49e0-125">Requirements</span></span>



| <span data-ttu-id="c49e0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c49e0-126">Requirement</span></span> | <span data-ttu-id="c49e0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c49e0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c49e0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c49e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c49e0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c49e0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c49e0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c49e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c49e0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c49e0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c49e0-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c49e0-132">Namespace</span></span><br/>                | <span data-ttu-id="c49e0-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c49e0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c49e0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c49e0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c49e0-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c49e0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c49e0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c49e0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c49e0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c49e0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49e0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c49e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49e0-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="c49e0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="c49e0-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c49e0-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


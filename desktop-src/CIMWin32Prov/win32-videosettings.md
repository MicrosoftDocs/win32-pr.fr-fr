---
description: La \_ classe WMI de l’Association VideoSettings Win32 associe un contrôleur vidéo et des paramètres vidéo qui peuvent être appliqués à celle-ci.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Classe Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514106"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="7c0ea-103">\_Classe VideoSettings Win32</span><span class="sxs-lookup"><span data-stu-id="7c0ea-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="7c0ea-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ VideoSettings Win32** associe un contrôleur vidéo et des paramètres vidéo qui peuvent être appliqués à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="7c0ea-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7c0ea-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c0ea-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="7c0ea-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7c0ea-108">Members</span></span>

<span data-ttu-id="7c0ea-109">La classe **Win32 \_ VideoSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c0ea-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="7c0ea-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c0ea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c0ea-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c0ea-111">Properties</span></span>

<span data-ttu-id="7c0ea-112">La classe **Win32 \_ VideoSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c0ea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0ea-114">Type de données : **Win32 \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="7c0ea-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c0ea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0ea-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ VideoController")</span><span class="sxs-lookup"><span data-stu-id="7c0ea-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="7c0ea-117">[**\_ VideoController Win32**](win32-videocontroller.md) contenant les propriétés du contrôleur vidéo sur lequel un paramètre vidéo peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="7c0ea-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c0ea-119">Type de données : **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="7c0ea-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c0ea-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c0ea-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")</span><span class="sxs-lookup"><span data-stu-id="7c0ea-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="7c0ea-122">[**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) contenant les paramètres qui peuvent être appliqués au contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c0ea-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7c0ea-123">Remarks</span></span>

<span data-ttu-id="7c0ea-124">La classe **Win32 \_ VideoSettings** est dérivée de [**CIM \_ VideoSetting**](cim-videosetting.md).</span><span class="sxs-lookup"><span data-stu-id="7c0ea-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0ea-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c0ea-125">Requirements</span></span>



| <span data-ttu-id="7c0ea-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c0ea-126">Requirement</span></span> | <span data-ttu-id="7c0ea-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c0ea-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0ea-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c0ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0ea-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c0ea-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c0ea-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c0ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0ea-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c0ea-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c0ea-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c0ea-132">Namespace</span></span><br/>                | <span data-ttu-id="7c0ea-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7c0ea-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c0ea-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7c0ea-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c0ea-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ea-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c0ea-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c0ea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c0ea-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ea-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0ea-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c0ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0ea-139">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="7c0ea-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="7c0ea-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

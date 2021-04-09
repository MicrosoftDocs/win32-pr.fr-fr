---
description: La \_ classe WMI de l’Association WMIElementSetting Win32 associe un service s’exécutant dans le système Windows et les paramètres WMI qu’il peut utiliser.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Classe Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860686"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="bebe0-103">\_Classe WMIElementSetting Win32</span><span class="sxs-lookup"><span data-stu-id="bebe0-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="bebe0-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ WMIElementSetting Win32** associe un service s’exécutant dans le système Windows et les paramètres WMI qu’il peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="bebe0-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="bebe0-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bebe0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bebe0-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bebe0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebe0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bebe0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="bebe0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bebe0-108">Members</span></span>

<span data-ttu-id="bebe0-109">La classe **Win32 \_ WMIElementSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bebe0-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bebe0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bebe0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bebe0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bebe0-111">Properties</span></span>

<span data-ttu-id="bebe0-112">La classe **Win32 \_ WMIElementSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bebe0-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bebe0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bebe0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bebe0-114">Type de données **: \_ service Win32**</span><span class="sxs-lookup"><span data-stu-id="bebe0-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="bebe0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bebe0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bebe0-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ service")</span><span class="sxs-lookup"><span data-stu-id="bebe0-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="bebe0-117">Référence à l’instance représentant le service Windows à l’aide de ou de l’accès aux propriétés WMI.</span><span class="sxs-lookup"><span data-stu-id="bebe0-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="bebe0-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="bebe0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bebe0-119">Type de données : **Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="bebe0-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="bebe0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bebe0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bebe0-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")</span><span class="sxs-lookup"><span data-stu-id="bebe0-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="bebe0-122">Référence à l’instance représentant les paramètres WMI disponibles pour le service Windows.</span><span class="sxs-lookup"><span data-stu-id="bebe0-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bebe0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bebe0-123">Remarks</span></span>

<span data-ttu-id="bebe0-124">La classe **Win32 \_ WMIElementSetting** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="bebe0-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bebe0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bebe0-125">Requirements</span></span>



| <span data-ttu-id="bebe0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bebe0-126">Requirement</span></span> | <span data-ttu-id="bebe0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bebe0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bebe0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebe0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bebe0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bebe0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bebe0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bebe0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bebe0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bebe0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bebe0-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bebe0-132">Namespace</span></span><br/>                | <span data-ttu-id="bebe0-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bebe0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bebe0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bebe0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bebe0-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bebe0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bebe0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bebe0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bebe0-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bebe0-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebe0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bebe0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebe0-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="bebe0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="bebe0-140">Classes de gestion des services WMI</span><span class="sxs-lookup"><span data-stu-id="bebe0-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 

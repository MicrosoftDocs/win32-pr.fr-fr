---
description: La \_ classe WMI de l’Association PageFileElementSetting Win32 associe les paramètres initiaux d’un fichier d’échange et l’état de ces paramètres lors d’une utilisation normale.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Classe Win32_PageFileElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950787"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="73e86-103">\_Classe PageFileElementSetting Win32</span><span class="sxs-lookup"><span data-stu-id="73e86-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="73e86-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PageFileElementSetting Win32** associe les paramètres initiaux d’un fichier d’échange et l’état de ces paramètres lors d’une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="73e86-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="73e86-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="73e86-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="73e86-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="73e86-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e86-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73e86-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="73e86-108">Membres</span><span class="sxs-lookup"><span data-stu-id="73e86-108">Members</span></span>

<span data-ttu-id="73e86-109">La classe **Win32 \_ PageFileElementSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73e86-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="73e86-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73e86-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73e86-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73e86-111">Properties</span></span>

<span data-ttu-id="73e86-112">La classe **Win32 \_ PageFileElementSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="73e86-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73e86-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="73e86-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e86-114">Type de données : **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="73e86-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="73e86-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73e86-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e86-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")</span><span class="sxs-lookup"><span data-stu-id="73e86-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="73e86-117">Référence à l’instance de qui représente les propriétés d’un fichier d’échange pendant que le système Win32 est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="73e86-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="73e86-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="73e86-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e86-119">Type de données : **Win32 \_ PageFileSetting**</span><span class="sxs-lookup"><span data-stu-id="73e86-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="73e86-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73e86-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e86-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")</span><span class="sxs-lookup"><span data-stu-id="73e86-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="73e86-122">Référence à l’instance représentant les paramètres initiaux d’un fichier d’échange lorsque le système Win32 démarre.</span><span class="sxs-lookup"><span data-stu-id="73e86-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73e86-123">Notes</span><span class="sxs-lookup"><span data-stu-id="73e86-123">Remarks</span></span>

<span data-ttu-id="73e86-124">La classe **Win32 \_ PageFileElementSetting** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="73e86-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73e86-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73e86-125">Requirements</span></span>



| <span data-ttu-id="73e86-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73e86-126">Requirement</span></span> | <span data-ttu-id="73e86-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="73e86-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73e86-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73e86-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73e86-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73e86-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73e86-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73e86-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73e86-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73e86-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73e86-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73e86-132">Namespace</span></span><br/>                | <span data-ttu-id="73e86-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="73e86-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73e86-134">MOF</span><span class="sxs-lookup"><span data-stu-id="73e86-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73e86-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73e86-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73e86-136">DLL</span><span class="sxs-lookup"><span data-stu-id="73e86-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e86-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e86-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e86-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73e86-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e86-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="73e86-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="73e86-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="73e86-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

---
description: La \_ classe WMI de l’Association Win32 SystemDriverPNPEntity associe un appareil plug-and-Play sur le système d’ordinateur exécutant Windows et le pilote qui prend en charge le périphérique Plug-and-Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Classe Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523684"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="b5318-103">\_Classe SystemDriverPNPEntity Win32</span><span class="sxs-lookup"><span data-stu-id="b5318-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="b5318-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **Win32 \_ SystemDriverPNPEntity** associe un appareil plug-and-Play sur le système d’ordinateur exécutant Windows et le pilote qui prend en charge le périphérique Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="b5318-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="b5318-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5318-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b5318-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b5318-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5318-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5318-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b5318-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b5318-108">Members</span></span>

<span data-ttu-id="b5318-109">La classe **Win32 \_ SystemDriverPNPEntity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5318-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="b5318-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5318-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5318-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5318-111">Properties</span></span>

<span data-ttu-id="b5318-112">La classe **Win32 \_ SystemDriverPNPEntity** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5318-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5318-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b5318-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5318-114">Type de données : **Win32 \_ PNPEntity**</span><span class="sxs-lookup"><span data-stu-id="b5318-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="b5318-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5318-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5318-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")</span><span class="sxs-lookup"><span data-stu-id="b5318-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="b5318-117">Représente l’appareil Plug-and-Play contrôlé par le pilote.</span><span class="sxs-lookup"><span data-stu-id="b5318-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="b5318-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b5318-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5318-119">Type de données : **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="b5318-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="b5318-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5318-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5318-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ SystemDriver »)</span><span class="sxs-lookup"><span data-stu-id="b5318-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="b5318-122">[**\_ SystemDriver Win32**](win32-systemdriver.md) qui représente le pilote qui prend en charge l’appareil plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="b5318-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5318-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b5318-123">Remarks</span></span>

<span data-ttu-id="b5318-124">La classe **Win32 \_ SystemDriverPNPEntity** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b5318-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5318-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5318-125">Requirements</span></span>



| <span data-ttu-id="b5318-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5318-126">Requirement</span></span> | <span data-ttu-id="b5318-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5318-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5318-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5318-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5318-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5318-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5318-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5318-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5318-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5318-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5318-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5318-132">Namespace</span></span><br/>                | <span data-ttu-id="b5318-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b5318-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5318-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b5318-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5318-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5318-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5318-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b5318-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5318-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5318-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5318-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5318-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5318-139">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="b5318-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="b5318-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b5318-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

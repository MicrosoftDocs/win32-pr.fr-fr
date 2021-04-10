---
description: La \_ classe WMI de l’Association OperatingSystemQFE Win32 associe un système d’exploitation et les mises à jour du produit appliquées comme représenté dans Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950790"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="29fd5-103">\_Classe OperatingSystemQFE Win32</span><span class="sxs-lookup"><span data-stu-id="29fd5-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="29fd5-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ OperatingSystemQFE Win32** associe un système d’exploitation et les mises à jour du produit appliquées comme représenté dans [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).</span><span class="sxs-lookup"><span data-stu-id="29fd5-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="29fd5-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="29fd5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="29fd5-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="29fd5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29fd5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29fd5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="29fd5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="29fd5-108">Members</span></span>

<span data-ttu-id="29fd5-109">La classe **Win32 \_ OperatingSystemQFE** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29fd5-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="29fd5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29fd5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29fd5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29fd5-111">Properties</span></span>

<span data-ttu-id="29fd5-112">La classe **Win32 \_ OperatingSystemQFE** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="29fd5-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29fd5-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="29fd5-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29fd5-114">Type de données : **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="29fd5-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="29fd5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29fd5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29fd5-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="29fd5-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="29fd5-117">Référence à l’instance représentant le système affecté par la mise à jour du produit dans cette association.</span><span class="sxs-lookup"><span data-stu-id="29fd5-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="29fd5-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="29fd5-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29fd5-119">Type de données : **Win32 \_ QuickFixEngineering**</span><span class="sxs-lookup"><span data-stu-id="29fd5-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="29fd5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29fd5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29fd5-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**faible**](../wmisdk/standard-qualifiers.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ QuickFixEngineering »)</span><span class="sxs-lookup"><span data-stu-id="29fd5-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="29fd5-122">Référence à l’instance de qui représente l’instance d’objet appliquée au système d’exploitation dans cette association.</span><span class="sxs-lookup"><span data-stu-id="29fd5-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29fd5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="29fd5-123">Remarks</span></span>

<span data-ttu-id="29fd5-124">La classe **Win32 \_ OperatingSystemQFE** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="29fd5-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29fd5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29fd5-125">Requirements</span></span>



| <span data-ttu-id="29fd5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29fd5-126">Requirement</span></span> | <span data-ttu-id="29fd5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="29fd5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29fd5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29fd5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="29fd5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29fd5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29fd5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29fd5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="29fd5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29fd5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29fd5-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29fd5-132">Namespace</span></span><br/>                | <span data-ttu-id="29fd5-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="29fd5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29fd5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="29fd5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29fd5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29fd5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29fd5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="29fd5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29fd5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29fd5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fd5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29fd5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fd5-139">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="29fd5-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="29fd5-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="29fd5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

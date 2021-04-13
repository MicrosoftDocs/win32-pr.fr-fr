---
description: La \_ classe WMI de l’Association PrinterDriverDll Win32 lie une imprimante locale et son fichier de pilote.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483696"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="5676b-103">\_Classe PrinterDriverDll Win32</span><span class="sxs-lookup"><span data-stu-id="5676b-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="5676b-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterDriverDll Win32** lie une imprimante locale et son fichier de pilote.</span><span class="sxs-lookup"><span data-stu-id="5676b-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="5676b-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5676b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5676b-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5676b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5676b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5676b-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5676b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5676b-108">Members</span></span>

<span data-ttu-id="5676b-109">La classe **Win32 \_ PrinterDriverDll** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5676b-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="5676b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5676b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5676b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5676b-111">Properties</span></span>

<span data-ttu-id="5676b-112">La classe **Win32 \_ PrinterDriverDll** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5676b-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5676b-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="5676b-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5676b-114">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="5676b-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="5676b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5676b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5676b-116">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5676b-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5676b-117">Référence à l’instance de fichier de fichier [**CIM \_**](cim-datafile.md) représentant le fichier de pilote pour cette imprimante Windows.</span><span class="sxs-lookup"><span data-stu-id="5676b-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="5676b-118">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5676b-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="5676b-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="5676b-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5676b-120">Type de données **: \_ imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="5676b-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="5676b-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5676b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5676b-122">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5676b-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5676b-123">Référence à l’instance de l' [**\_ imprimante Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="5676b-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="5676b-124">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5676b-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5676b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5676b-125">Remarks</span></span>

<span data-ttu-id="5676b-126">La classe **Win32 \_ PrinterDriverDll** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5676b-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5676b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5676b-127">Requirements</span></span>



| <span data-ttu-id="5676b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5676b-128">Requirement</span></span> | <span data-ttu-id="5676b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5676b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5676b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5676b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5676b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5676b-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5676b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5676b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5676b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5676b-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5676b-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5676b-134">Namespace</span></span><br/>                | <span data-ttu-id="5676b-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5676b-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5676b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5676b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5676b-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5676b-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5676b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5676b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5676b-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5676b-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5676b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5676b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5676b-141">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="5676b-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="5676b-142">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="5676b-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

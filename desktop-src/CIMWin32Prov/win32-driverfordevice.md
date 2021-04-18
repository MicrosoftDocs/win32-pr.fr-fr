---
description: La \_ classe WMI de l’Association DriverForDevice Win32 associe une instance d’imprimante à une instance de pilote d’imprimante.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519222"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="c99d1-103">\_Classe DriverForDevice Win32</span><span class="sxs-lookup"><span data-stu-id="c99d1-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="c99d1-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DriverForDevice Win32** associe une instance d’imprimante à une instance de pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c99d1-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="c99d1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c99d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c99d1-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c99d1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c99d1-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c99d1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c99d1-108">Members</span></span>

<span data-ttu-id="c99d1-109">La classe **Win32 \_ DriverForDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c99d1-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c99d1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c99d1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c99d1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c99d1-111">Properties</span></span>

<span data-ttu-id="c99d1-112">La classe **Win32 \_ DriverForDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c99d1-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c99d1-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="c99d1-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c99d1-114">Type de données **: \_ imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="c99d1-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="c99d1-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c99d1-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c99d1-116">Référence à l’instance d' [**\_ imprimante Win32**](win32-printer.md) qui représente l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c99d1-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="c99d1-117">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c99d1-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="c99d1-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="c99d1-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c99d1-119">Type de données : **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c99d1-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="c99d1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c99d1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c99d1-121">Référence à l’instance [**Win32 \_ PrinterDriver**](win32-printerdriver.md) qui représente le pilote d’imprimante pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c99d1-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="c99d1-122">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c99d1-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c99d1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c99d1-123">Remarks</span></span>

<span data-ttu-id="c99d1-124">La classe **Win32 \_ DriverForDevice** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c99d1-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c99d1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c99d1-125">Requirements</span></span>



| <span data-ttu-id="c99d1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c99d1-126">Requirement</span></span> | <span data-ttu-id="c99d1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c99d1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c99d1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c99d1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c99d1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c99d1-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c99d1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c99d1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c99d1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c99d1-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c99d1-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c99d1-132">Namespace</span></span><br/>                | <span data-ttu-id="c99d1-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c99d1-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c99d1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c99d1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c99d1-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c99d1-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c99d1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c99d1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c99d1-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c99d1-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c99d1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c99d1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99d1-139">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="c99d1-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


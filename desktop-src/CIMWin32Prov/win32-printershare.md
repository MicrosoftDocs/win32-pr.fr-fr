---
description: La \_ classe WMI de l’Association PrinterShare Win32 lie une imprimante locale et le partage qui la représente lorsqu’elle est affichée sur un réseau.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Classe Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861497"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="7ae13-103">\_Classe PrinterShare Win32</span><span class="sxs-lookup"><span data-stu-id="7ae13-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="7ae13-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterShare Win32** lie une imprimante locale et le partage qui la représente lorsqu’elle est affichée sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="7ae13-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="7ae13-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7ae13-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7ae13-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7ae13-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae13-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ae13-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7ae13-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7ae13-108">Members</span></span>

<span data-ttu-id="7ae13-109">La classe **Win32 \_ PrinterShare** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7ae13-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="7ae13-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ae13-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ae13-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ae13-111">Properties</span></span>

<span data-ttu-id="7ae13-112">La classe **Win32 \_ PrinterShare** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7ae13-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ae13-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7ae13-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ae13-114">Type de données **: \_ imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="7ae13-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="7ae13-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ae13-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ae13-116">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ae13-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ae13-117">Référence à l’instance de qui représente l’imprimante locale partagée dans cette association.</span><span class="sxs-lookup"><span data-stu-id="7ae13-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="7ae13-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7ae13-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ae13-119">Type de données **: \_ partage Win32**</span><span class="sxs-lookup"><span data-stu-id="7ae13-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="7ae13-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ae13-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ae13-121">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ae13-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ae13-122">Référence à l’instance représentant le partage de l’imprimante dans cette association.</span><span class="sxs-lookup"><span data-stu-id="7ae13-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ae13-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae13-123">Remarks</span></span>

<span data-ttu-id="7ae13-124">La classe **Win32 \_ PrinterShare** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7ae13-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae13-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ae13-125">Requirements</span></span>



| <span data-ttu-id="7ae13-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae13-126">Requirement</span></span> | <span data-ttu-id="7ae13-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ae13-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae13-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae13-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ae13-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7ae13-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae13-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ae13-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7ae13-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ae13-132">Namespace</span></span><br/>                | <span data-ttu-id="7ae13-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7ae13-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7ae13-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7ae13-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ae13-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ae13-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ae13-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae13-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ae13-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ae13-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7ae13-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae13-139">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7ae13-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

---
description: La \_ classe CIM ErrorCountersForDevice associe la \_ classe CIM DeviceErrorCounts à l’unité logique à laquelle elle s’applique.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: Classe CIM_ErrorCountersForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861265"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="36e66-103">\_Classe CIM ErrorCountersForDevice</span><span class="sxs-lookup"><span data-stu-id="36e66-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="36e66-104">La classe **CIM \_ ErrorCountersForDevice** associe la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) à l’unité logique à laquelle elle s’applique.</span><span class="sxs-lookup"><span data-stu-id="36e66-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36e66-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="36e66-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36e66-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36e66-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36e66-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36e66-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="36e66-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="36e66-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e66-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36e66-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="36e66-110">Membres</span><span class="sxs-lookup"><span data-stu-id="36e66-110">Members</span></span>

<span data-ttu-id="36e66-111">La classe **CIM \_ ErrorCountersForDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36e66-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="36e66-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36e66-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36e66-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36e66-113">Properties</span></span>

<span data-ttu-id="36e66-114">La classe **CIM \_ ErrorCountersForDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="36e66-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36e66-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="36e66-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e66-116">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="36e66-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="36e66-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36e66-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e66-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="36e66-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="36e66-119">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil auquel les compteurs d’erreur s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="36e66-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="36e66-120">**Stats**</span><span class="sxs-lookup"><span data-stu-id="36e66-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e66-121">Type de données : **CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="36e66-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="36e66-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36e66-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e66-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36e66-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36e66-124">[**\_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) décrivant l’objet statistique (dans ce cas, la classe de compteur d’erreurs).</span><span class="sxs-lookup"><span data-stu-id="36e66-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36e66-125">Notes</span><span class="sxs-lookup"><span data-stu-id="36e66-125">Remarks</span></span>

<span data-ttu-id="36e66-126">La classe **CIM \_ ErrorCountersForDevice** est héritée [**des \_ statistiques CIM**](cim-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="36e66-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="36e66-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="36e66-127">WMI does not implement this class.</span></span>

<span data-ttu-id="36e66-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="36e66-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36e66-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="36e66-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e66-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36e66-130">Requirements</span></span>



| <span data-ttu-id="36e66-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36e66-131">Requirement</span></span> | <span data-ttu-id="36e66-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="36e66-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36e66-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e66-133">Minimum supported client</span></span><br/> | <span data-ttu-id="36e66-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36e66-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36e66-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e66-135">Minimum supported server</span></span><br/> | <span data-ttu-id="36e66-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36e66-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36e66-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36e66-137">Namespace</span></span><br/>                | <span data-ttu-id="36e66-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36e66-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36e66-139">MOF</span><span class="sxs-lookup"><span data-stu-id="36e66-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36e66-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36e66-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36e66-141">DLL</span><span class="sxs-lookup"><span data-stu-id="36e66-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36e66-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36e66-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e66-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36e66-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e66-144">**\_Statistiques CIM**</span><span class="sxs-lookup"><span data-stu-id="36e66-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 


---
description: La \_ classe CIM ComputerSystemResource représente une association entre un système informatique et les ressources système disponibles.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033715"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="0a72c-103">\_Classe CIM ComputerSystemResource</span><span class="sxs-lookup"><span data-stu-id="0a72c-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="0a72c-104">La classe **CIM \_ ComputerSystemResource** représente une association entre un système informatique et les ressources système disponibles.</span><span class="sxs-lookup"><span data-stu-id="0a72c-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a72c-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0a72c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a72c-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a72c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a72c-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0a72c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0a72c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0a72c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a72c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a72c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="0a72c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="0a72c-110">Members</span></span>

<span data-ttu-id="0a72c-111">La classe **CIM \_ ComputerSystemResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a72c-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="0a72c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a72c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a72c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a72c-113">Properties</span></span>

<span data-ttu-id="0a72c-114">La classe **CIM \_ ComputerSystemResource** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a72c-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a72c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0a72c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a72c-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="0a72c-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0a72c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a72c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a72c-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="0a72c-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0a72c-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique.</span><span class="sxs-lookup"><span data-stu-id="0a72c-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="0a72c-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0a72c-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a72c-121">Type de données : **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="0a72c-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="0a72c-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a72c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a72c-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0a72c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0a72c-124">[**\_ SystemResource CIM**](cim-systemresource.md) qui décrit une ressource système du système informatique.</span><span class="sxs-lookup"><span data-stu-id="0a72c-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a72c-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0a72c-125">Remarks</span></span>

<span data-ttu-id="0a72c-126">La classe **CIM \_ ComputerSystemResource** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0a72c-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="0a72c-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0a72c-127">WMI does not implement this class.</span></span> <span data-ttu-id="0a72c-128">Pour plus d’informations sur les classes dérivées de **CIM \_ ComputerSystemResource**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0a72c-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0a72c-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0a72c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a72c-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0a72c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a72c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a72c-131">Requirements</span></span>



| <span data-ttu-id="0a72c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a72c-132">Requirement</span></span> | <span data-ttu-id="0a72c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a72c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a72c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a72c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0a72c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a72c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a72c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a72c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0a72c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a72c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a72c-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a72c-138">Namespace</span></span><br/>                | <span data-ttu-id="0a72c-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0a72c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a72c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0a72c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a72c-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a72c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a72c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0a72c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a72c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a72c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a72c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a72c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a72c-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0a72c-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


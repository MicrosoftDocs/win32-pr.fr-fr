---
description: L' \_ Association de composants CIM représente les parties d’une relation entre les MSEs.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: CIM_Component, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861337"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="fafb1-103">CIM_Component, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="fafb1-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fafb1-104">L’Association de **\_ composants CIM** représente les parties d’une relation entre les MSEs.</span><span class="sxs-lookup"><span data-stu-id="fafb1-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fafb1-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fafb1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fafb1-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fafb1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fafb1-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fafb1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fafb1-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fafb1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafb1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fafb1-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fafb1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fafb1-110">Members</span></span>

<span data-ttu-id="fafb1-111">La classe de **\_ composant CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fafb1-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="fafb1-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fafb1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fafb1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fafb1-113">Properties</span></span>

<span data-ttu-id="fafb1-114">La classe de **\_ composant CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fafb1-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fafb1-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fafb1-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fafb1-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="fafb1-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="fafb1-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fafb1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fafb1-118">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fafb1-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fafb1-119">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="fafb1-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="fafb1-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fafb1-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fafb1-121">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="fafb1-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="fafb1-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fafb1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fafb1-123">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="fafb1-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fafb1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="fafb1-124">Remarks</span></span>

<span data-ttu-id="fafb1-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="fafb1-125">WMI does not implement this class.</span></span> <span data-ttu-id="fafb1-126">Pour plus d’informations sur les classes dérivées du **\_ composant CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fafb1-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fafb1-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fafb1-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fafb1-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fafb1-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fafb1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fafb1-129">Requirements</span></span>



| <span data-ttu-id="fafb1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fafb1-130">Requirement</span></span> | <span data-ttu-id="fafb1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fafb1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fafb1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafb1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fafb1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fafb1-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fafb1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafb1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fafb1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fafb1-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fafb1-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fafb1-136">Namespace</span></span><br/>                | <span data-ttu-id="fafb1-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fafb1-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fafb1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="fafb1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fafb1-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fafb1-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fafb1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fafb1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafb1-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafb1-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


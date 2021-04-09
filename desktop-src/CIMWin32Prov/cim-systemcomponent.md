---
description: Classe d’association Common Information Model (CIM) qui établit les relations entre un système et les éléments système gérés dont il est composé.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: CIM_SystemComponent, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110986"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="520b0-103">CIM_SystemComponent, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="520b0-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="520b0-104">La classe **CIM \_ SystemComponent** est une classe d’association Common Information Model (CIM) qui établit les relations entre un système et les éléments système gérés dont il est composé.</span><span class="sxs-lookup"><span data-stu-id="520b0-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="520b0-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="520b0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="520b0-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="520b0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="520b0-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="520b0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="520b0-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="520b0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="520b0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="520b0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="520b0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="520b0-110">Members</span></span>

<span data-ttu-id="520b0-111">La classe **CIM \_ SystemComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="520b0-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="520b0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="520b0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="520b0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="520b0-113">Properties</span></span>

<span data-ttu-id="520b0-114">La classe **CIM \_ SystemComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="520b0-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="520b0-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="520b0-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520b0-116">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="520b0-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="520b0-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="520b0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="520b0-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="520b0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="520b0-119">[**\_ Système CIM**](cim-system.md) qui décrit le système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="520b0-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="520b0-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="520b0-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520b0-121">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="520b0-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="520b0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="520b0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="520b0-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="520b0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="520b0-124">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément enfant qui est un composant d’un système.</span><span class="sxs-lookup"><span data-stu-id="520b0-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="520b0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="520b0-125">Remarks</span></span>

<span data-ttu-id="520b0-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="520b0-126">WMI does not implement this class.</span></span> <span data-ttu-id="520b0-127">Pour les classes WMI dérivées de **CIM \_ SystemComponent**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="520b0-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="520b0-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="520b0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="520b0-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="520b0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="520b0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="520b0-130">Requirements</span></span>



| <span data-ttu-id="520b0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="520b0-131">Requirement</span></span> | <span data-ttu-id="520b0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="520b0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="520b0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="520b0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="520b0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520b0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="520b0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="520b0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="520b0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="520b0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="520b0-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="520b0-137">Namespace</span></span><br/>                | <span data-ttu-id="520b0-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="520b0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="520b0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="520b0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="520b0-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="520b0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="520b0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="520b0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520b0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520b0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520b0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="520b0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520b0-144">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="520b0-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


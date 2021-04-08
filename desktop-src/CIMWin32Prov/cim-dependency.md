---
description: La \_ classe de dépendance CIM représente une association qui établit des relations de dépendance entre des objets.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: CIM_Dependency, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748500"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="4b641-103">CIM_Dependency, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4b641-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4b641-104">La classe de **\_ dépendance CIM** représente une association qui établit des relations de dépendance entre des objets.</span><span class="sxs-lookup"><span data-stu-id="4b641-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b641-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4b641-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b641-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b641-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b641-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4b641-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b641-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4b641-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b641-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b641-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4b641-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4b641-110">Members</span></span>

<span data-ttu-id="4b641-111">La classe de **\_ dépendance CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b641-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4b641-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b641-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b641-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b641-113">Properties</span></span>

<span data-ttu-id="4b641-114">La classe de **\_ dépendance CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4b641-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b641-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4b641-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b641-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="4b641-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4b641-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b641-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b641-118">Référence à l’objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="4b641-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="4b641-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4b641-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b641-120">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="4b641-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4b641-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b641-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b641-122">Référence à l’objet qui est dépendant de la propriété **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="4b641-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b641-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4b641-123">Remarks</span></span>

<span data-ttu-id="4b641-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4b641-124">WMI does not implement this class.</span></span> <span data-ttu-id="4b641-125">Pour plus d’informations sur les classes dérivées de la **\_ dépendance CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4b641-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4b641-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b641-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b641-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4b641-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b641-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b641-128">Requirements</span></span>



| <span data-ttu-id="4b641-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b641-129">Requirement</span></span> | <span data-ttu-id="4b641-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b641-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b641-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b641-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4b641-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b641-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b641-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b641-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4b641-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b641-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b641-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b641-135">Namespace</span></span><br/>                | <span data-ttu-id="4b641-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4b641-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b641-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4b641-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b641-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b641-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b641-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4b641-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b641-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b641-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 





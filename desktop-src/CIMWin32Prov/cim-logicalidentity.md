---
description: La \_ classe LOGICALIDENTITY CIM est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950495"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="4de2c-103">CIM_LogicalIdentity, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4de2c-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4de2c-104">La **classe \_ LogicalIdentity CIM** est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="4de2c-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="4de2c-105">L’Association transmet ce qui peut être défini avec un héritage multiple et est limité aux aspects logiques d’un élément système géré.</span><span class="sxs-lookup"><span data-stu-id="4de2c-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="4de2c-106">Dans la plupart des scénarios, la relation d’identité est déterminée par l’équivalence des clés, ou d’autres propriétés d’identification des éléments associés.</span><span class="sxs-lookup"><span data-stu-id="4de2c-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="4de2c-107">L’Association doit être utilisée uniquement dans les scénarios bien compris, ce qui permet une définition et une clarification plus concrètes dans les sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4de2c-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="4de2c-108">Un scénario dans lequel la relation est raisonnable, par exemple, représente un appareil qui est à la fois une entité de bus et une entité fonctionnelle où l’appareil est une entité USB (bus) et un clavier (fonctionnel).</span><span class="sxs-lookup"><span data-stu-id="4de2c-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4de2c-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4de2c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4de2c-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4de2c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4de2c-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4de2c-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4de2c-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4de2c-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de2c-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4de2c-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="4de2c-114">Membres</span><span class="sxs-lookup"><span data-stu-id="4de2c-114">Members</span></span>

<span data-ttu-id="4de2c-115">La classe **CIM \_ LogicalIdentity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4de2c-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="4de2c-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4de2c-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4de2c-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4de2c-117">Properties</span></span>

<span data-ttu-id="4de2c-118">La classe **CIM \_ LogicalIdentity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4de2c-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4de2c-119">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="4de2c-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de2c-120">Type de données : **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4de2c-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="4de2c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4de2c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de2c-122">Référence à un autre aspect de l’entité système.</span><span class="sxs-lookup"><span data-stu-id="4de2c-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="4de2c-123">**SYSTEME**</span><span class="sxs-lookup"><span data-stu-id="4de2c-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de2c-124">Type de données : **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4de2c-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="4de2c-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4de2c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de2c-126">Référence à un aspect de l’élément logique.</span><span class="sxs-lookup"><span data-stu-id="4de2c-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4de2c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4de2c-127">Remarks</span></span>

<span data-ttu-id="4de2c-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4de2c-128">WMI does not implement this class.</span></span> <span data-ttu-id="4de2c-129">Pour les classes dérivées de **CIM \_ LogicalIdentity**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4de2c-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4de2c-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4de2c-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4de2c-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4de2c-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de2c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4de2c-132">Requirements</span></span>



| <span data-ttu-id="4de2c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4de2c-133">Requirement</span></span> | <span data-ttu-id="4de2c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4de2c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de2c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de2c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4de2c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de2c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4de2c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de2c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4de2c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4de2c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4de2c-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4de2c-139">Namespace</span></span><br/>                | <span data-ttu-id="4de2c-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4de2c-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4de2c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4de2c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4de2c-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4de2c-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4de2c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4de2c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de2c-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de2c-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 





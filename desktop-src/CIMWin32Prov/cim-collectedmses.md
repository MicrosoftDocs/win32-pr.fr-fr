---
description: La \_ classe d’association CIM CollectedMSEs représente les membres de l’objet de regroupement, une classe CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483544"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="2bfd2-103">CIM_CollectedMSEs, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="2bfd2-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="2bfd2-104">La classe d’association **CIM \_ CollectedMSEs** représente les membres de l’objet de regroupement, une classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="2bfd2-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bfd2-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2bfd2-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2bfd2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2bfd2-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2bfd2-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bfd2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bfd2-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="2bfd2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2bfd2-110">Members</span></span>

<span data-ttu-id="2bfd2-111">La classe **CIM \_ CollectedMSEs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2bfd2-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="2bfd2-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2bfd2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bfd2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2bfd2-113">Properties</span></span>

<span data-ttu-id="2bfd2-114">La classe **CIM \_ CollectedMSEs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bfd2-115">**Collection**</span><span class="sxs-lookup"><span data-stu-id="2bfd2-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bfd2-116">Type de données : **cm \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="2bfd2-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="2bfd2-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2bfd2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bfd2-118">Référence au regroupement ou à l’objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="2bfd2-119">**Membre**</span><span class="sxs-lookup"><span data-stu-id="2bfd2-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bfd2-120">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="2bfd2-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="2bfd2-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2bfd2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bfd2-122">Référence à un membre de la collection.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bfd2-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2bfd2-123">Remarks</span></span>

<span data-ttu-id="2bfd2-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-124">WMI does not implement this class.</span></span> <span data-ttu-id="2bfd2-125">Pour plus d’informations sur les classes WMI dérivées de **CIM \_ CollectedMSEs**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2bfd2-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2bfd2-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2bfd2-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2bfd2-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bfd2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bfd2-128">Requirements</span></span>



| <span data-ttu-id="2bfd2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bfd2-129">Requirement</span></span> | <span data-ttu-id="2bfd2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bfd2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfd2-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bfd2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2bfd2-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bfd2-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bfd2-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bfd2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2bfd2-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bfd2-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bfd2-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2bfd2-135">Namespace</span></span><br/>                | <span data-ttu-id="2bfd2-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2bfd2-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bfd2-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2bfd2-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bfd2-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bfd2-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bfd2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2bfd2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bfd2-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bfd2-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 





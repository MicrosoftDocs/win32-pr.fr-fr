---
description: La \_ classe CIM PhysicalElementLocation associe un élément physique à un \_ objet d’emplacement CIM à des fins d’inventaire ou de remplacement.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElementLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111267"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="b5e9f-103">\_Classe CIM PhysicalElementLocation</span><span class="sxs-lookup"><span data-stu-id="b5e9f-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="b5e9f-104">La classe **CIM \_ PhysicalElementLocation** associe un élément physique à un objet d' [**\_ emplacement CIM**](cim-location.md) à des fins d’inventaire ou de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5e9f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5e9f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5e9f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5e9f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b5e9f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e9f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5e9f-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="b5e9f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b5e9f-110">Members</span></span>

<span data-ttu-id="b5e9f-111">La classe **CIM \_ PhysicalElementLocation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5e9f-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="b5e9f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5e9f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5e9f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5e9f-113">Properties</span></span>

<span data-ttu-id="b5e9f-114">La classe **CIM \_ PhysicalElementLocation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5e9f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5e9f-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e9f-116">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="b5e9f-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="b5e9f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5e9f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5e9f-118">Référence à l’élément physique dont l’emplacement est spécifié.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="b5e9f-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="b5e9f-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e9f-120">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="b5e9f-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="b5e9f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5e9f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e9f-122">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b5e9f-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b5e9f-123">Référence à l’emplacement de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5e9f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b5e9f-124">Remarks</span></span>

<span data-ttu-id="b5e9f-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-125">WMI does not implement this class.</span></span>

<span data-ttu-id="b5e9f-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5e9f-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b5e9f-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e9f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5e9f-128">Requirements</span></span>



| <span data-ttu-id="b5e9f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5e9f-129">Requirement</span></span> | <span data-ttu-id="b5e9f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5e9f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e9f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5e9f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e9f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5e9f-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5e9f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5e9f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e9f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5e9f-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5e9f-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5e9f-135">Namespace</span></span><br/>                | <span data-ttu-id="b5e9f-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b5e9f-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5e9f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b5e9f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5e9f-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5e9f-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5e9f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b5e9f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5e9f-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5e9f-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


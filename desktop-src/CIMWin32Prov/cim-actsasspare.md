---
description: L' \_ Association CIM ActsAsSpare indique les éléments qui peuvent être des éléments de rechange ou remplacer d’autres éléments agrégés. Un Spare peut fonctionner dans &\# 0034 ; le mode de secours&\# 0034 ;, comme spécifié élément par élément.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: Classe CIM_ActsAsSpare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950733"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="eed46-104">\_Classe CIM ActsAsSpare</span><span class="sxs-lookup"><span data-stu-id="eed46-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="eed46-105">L’Association **CIM \_ ActsAsSpare** indique les éléments qui peuvent être des éléments de rechange ou remplacer d’autres éléments agrégés.</span><span class="sxs-lookup"><span data-stu-id="eed46-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="eed46-106">Un Spare peut fonctionner en mode de « secours », comme spécifié élément par élément.</span><span class="sxs-lookup"><span data-stu-id="eed46-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eed46-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="eed46-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eed46-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eed46-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eed46-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eed46-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eed46-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="eed46-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed46-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eed46-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="eed46-112">Membres</span><span class="sxs-lookup"><span data-stu-id="eed46-112">Members</span></span>

<span data-ttu-id="eed46-113">La classe **CIM \_ ActsAsSpare** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eed46-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="eed46-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eed46-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eed46-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eed46-115">Properties</span></span>

<span data-ttu-id="eed46-116">La classe **CIM \_ ActsAsSpare** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eed46-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eed46-117">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="eed46-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed46-118">Type de données : **CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="eed46-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="eed46-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eed46-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eed46-120">Référence à la propriété de **groupe** qui représente la classe [**\_ SpareGroup CIM**](cim-sparegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="eed46-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="eed46-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="eed46-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed46-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eed46-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eed46-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eed46-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eed46-124">Si la **valeur est true**, le spare fonctionne comme un secours à chaud.</span><span class="sxs-lookup"><span data-stu-id="eed46-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="eed46-125">**Chambres**</span><span class="sxs-lookup"><span data-stu-id="eed46-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed46-126">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="eed46-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="eed46-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eed46-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eed46-128">Référence à un élément système géré agissant comme un Spare et participant au groupe Spare.</span><span class="sxs-lookup"><span data-stu-id="eed46-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eed46-129">Notes</span><span class="sxs-lookup"><span data-stu-id="eed46-129">Remarks</span></span>

<span data-ttu-id="eed46-130">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="eed46-130">WMI does not implement this class.</span></span>

<span data-ttu-id="eed46-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="eed46-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eed46-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="eed46-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed46-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eed46-133">Requirements</span></span>



| <span data-ttu-id="eed46-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eed46-134">Requirement</span></span> | <span data-ttu-id="eed46-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="eed46-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed46-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eed46-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eed46-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eed46-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eed46-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eed46-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eed46-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eed46-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eed46-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eed46-140">Namespace</span></span><br/>                | <span data-ttu-id="eed46-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="eed46-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eed46-142">MOF</span><span class="sxs-lookup"><span data-stu-id="eed46-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eed46-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eed46-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eed46-144">DLL</span><span class="sxs-lookup"><span data-stu-id="eed46-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eed46-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed46-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed46-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eed46-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed46-147">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="eed46-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 


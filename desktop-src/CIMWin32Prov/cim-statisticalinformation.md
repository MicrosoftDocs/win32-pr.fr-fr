---
description: La \_ classe STATISTICALINFORMATION CIM est une classe racine pour la collection arbitraire de données statistiques ou de mesures applicables à un ou plusieurs éléments système gérés.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: Classe CIM_StatisticalInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861658"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="387b8-103">\_Classe CIM StatisticalInformation</span><span class="sxs-lookup"><span data-stu-id="387b8-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="387b8-104">La **classe \_ StatisticalInformation CIM** est une classe racine pour la collection arbitraire de données statistiques ou de mesures applicables à un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="387b8-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="387b8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="387b8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="387b8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="387b8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="387b8-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="387b8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="387b8-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="387b8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="387b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="387b8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="387b8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="387b8-110">Members</span></span>

<span data-ttu-id="387b8-111">La classe **CIM \_ StatisticalInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="387b8-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="387b8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="387b8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="387b8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="387b8-113">Properties</span></span>

<span data-ttu-id="387b8-114">La classe **CIM \_ StatisticalInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="387b8-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="387b8-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="387b8-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="387b8-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="387b8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="387b8-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="387b8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="387b8-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="387b8-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="387b8-119">Description textuelle courte pour la statistique ou la métrique.</span><span class="sxs-lookup"><span data-stu-id="387b8-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="387b8-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="387b8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="387b8-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="387b8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="387b8-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="387b8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="387b8-123">Description textuelle de la statistique ou métrique.</span><span class="sxs-lookup"><span data-stu-id="387b8-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="387b8-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="387b8-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="387b8-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="387b8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="387b8-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="387b8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="387b8-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="387b8-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="387b8-128">Étiquette par laquelle la statistique ou la métrique est connue.</span><span class="sxs-lookup"><span data-stu-id="387b8-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="387b8-129">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="387b8-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="387b8-130">Notes</span><span class="sxs-lookup"><span data-stu-id="387b8-130">Remarks</span></span>

<span data-ttu-id="387b8-131">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="387b8-131">WMI does not implement this class.</span></span> <span data-ttu-id="387b8-132">Pour les classes WMI dérivées de **CIM \_ StatisticalInformation**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="387b8-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="387b8-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="387b8-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="387b8-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="387b8-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="387b8-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="387b8-135">Requirements</span></span>



| <span data-ttu-id="387b8-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="387b8-136">Requirement</span></span> | <span data-ttu-id="387b8-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="387b8-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="387b8-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387b8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="387b8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="387b8-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="387b8-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387b8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="387b8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="387b8-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="387b8-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="387b8-142">Namespace</span></span><br/>                | <span data-ttu-id="387b8-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="387b8-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="387b8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="387b8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="387b8-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="387b8-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="387b8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="387b8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="387b8-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="387b8-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 


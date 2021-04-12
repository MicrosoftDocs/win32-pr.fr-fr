---
description: La \_ classe CIM ConnectedTo représente une association qui indique que deux ou plusieurs connecteurs physiques sont connectés.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: Classe CIM_ConnectedTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033714"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="8bfb0-103">\_Classe CIM ConnectedTo</span><span class="sxs-lookup"><span data-stu-id="8bfb0-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="8bfb0-104">La classe **CIM \_ ConnectedTo** représente une association qui indique que deux ou plusieurs connecteurs physiques sont connectés.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bfb0-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8bfb0-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8bfb0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8bfb0-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8bfb0-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfb0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bfb0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8bfb0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8bfb0-110">Members</span></span>

<span data-ttu-id="8bfb0-111">La classe **CIM \_ ConnectedTo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8bfb0-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="8bfb0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bfb0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bfb0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bfb0-113">Properties</span></span>

<span data-ttu-id="8bfb0-114">La classe **CIM \_ ConnectedTo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bfb0-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="8bfb0-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bfb0-116">Type de données : **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="8bfb0-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="8bfb0-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bfb0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bfb0-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="8bfb0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8bfb0-119">[**\_ PhysicalConnector CIM**](cim-physicalconnector.md) qui représente un connecteur physique qui sert d’unique extrémité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="8bfb0-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="8bfb0-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bfb0-121">Type de données : **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="8bfb0-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="8bfb0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bfb0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bfb0-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="8bfb0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8bfb0-124">[**\_ PhysicalConnector CIM**](cim-physicalconnector.md) qui représente un autre connecteur physique qui sert d’autre terminaison de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bfb0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8bfb0-125">Remarks</span></span>

<span data-ttu-id="8bfb0-126">La classe **CIM \_ ConnectedTo** est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8bfb0-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8bfb0-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-127">WMI does not implement this class.</span></span>

<span data-ttu-id="8bfb0-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8bfb0-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8bfb0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfb0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bfb0-130">Requirements</span></span>



| <span data-ttu-id="8bfb0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bfb0-131">Requirement</span></span> | <span data-ttu-id="8bfb0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bfb0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfb0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bfb0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8bfb0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bfb0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bfb0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bfb0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8bfb0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bfb0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bfb0-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8bfb0-137">Namespace</span></span><br/>                | <span data-ttu-id="8bfb0-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8bfb0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bfb0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8bfb0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bfb0-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bfb0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8bfb0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bfb0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfb0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bfb0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfb0-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="8bfb0-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


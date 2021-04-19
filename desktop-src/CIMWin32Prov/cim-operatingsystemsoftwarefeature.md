---
description: La \_ classe CIM OperatingSystemSoftwareFeature représente les fonctionnalités logicielles qui composent le système d’exploitation.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515368"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="4e02d-103">\_Classe CIM OperatingSystemSoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="4e02d-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="4e02d-104">La classe **CIM \_ OperatingSystemSoftwareFeature** représente les fonctionnalités logicielles qui composent le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4e02d-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e02d-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4e02d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e02d-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e02d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e02d-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4e02d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4e02d-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4e02d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e02d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e02d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4e02d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4e02d-110">Members</span></span>

<span data-ttu-id="4e02d-111">La classe **CIM \_ OperatingSystemSoftwareFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4e02d-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="4e02d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e02d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e02d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e02d-113">Properties</span></span>

<span data-ttu-id="4e02d-114">La classe **CIM \_ OperatingSystemSoftwareFeature** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4e02d-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e02d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4e02d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e02d-116">Type de données : **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="4e02d-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4e02d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e02d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e02d-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4e02d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4e02d-119">Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) décrivant le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4e02d-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4e02d-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4e02d-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e02d-121">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4e02d-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4e02d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e02d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e02d-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4e02d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4e02d-124">[**\_ SoftwareFeature CIM**](cim-softwarefeature.md) décrivant les fonctionnalités logicielles qui composent le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4e02d-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e02d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4e02d-125">Remarks</span></span>

<span data-ttu-id="4e02d-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4e02d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4e02d-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e02d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e02d-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4e02d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e02d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e02d-129">Requirements</span></span>



| <span data-ttu-id="4e02d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e02d-130">Requirement</span></span> | <span data-ttu-id="4e02d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e02d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e02d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e02d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e02d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e02d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e02d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e02d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e02d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e02d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e02d-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4e02d-136">Namespace</span></span><br/>                | <span data-ttu-id="4e02d-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4e02d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e02d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4e02d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e02d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e02d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e02d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4e02d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e02d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e02d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e02d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e02d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e02d-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="4e02d-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


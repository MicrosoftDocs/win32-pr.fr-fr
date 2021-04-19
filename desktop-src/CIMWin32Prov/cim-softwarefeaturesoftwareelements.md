---
description: L' \_ Association CIM SoftwareFeatureSoftwareElements identifie les éléments logiciels qui composent une fonctionnalité logicielle spécifique.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSoftwareElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515551"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="080d2-103">\_Classe CIM SoftwareFeatureSoftwareElements</span><span class="sxs-lookup"><span data-stu-id="080d2-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="080d2-104">L’Association **CIM \_ SoftwareFeatureSoftwareElements** identifie les éléments logiciels qui composent une fonctionnalité logicielle spécifique.</span><span class="sxs-lookup"><span data-stu-id="080d2-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="080d2-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="080d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="080d2-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="080d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="080d2-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="080d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="080d2-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="080d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="080d2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="080d2-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="080d2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="080d2-110">Members</span></span>

<span data-ttu-id="080d2-111">La classe **CIM \_ SoftwareFeatureSoftwareElements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="080d2-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="080d2-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="080d2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="080d2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="080d2-113">Properties</span></span>

<span data-ttu-id="080d2-114">La classe **CIM \_ SoftwareFeatureSoftwareElements** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="080d2-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="080d2-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="080d2-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080d2-116">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="080d2-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="080d2-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="080d2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080d2-118">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="080d2-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="080d2-119">Composant du groupe.</span><span class="sxs-lookup"><span data-stu-id="080d2-119">The group component.</span></span>

<span data-ttu-id="080d2-120">Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="080d2-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="080d2-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="080d2-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080d2-122">Type de données : **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="080d2-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="080d2-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="080d2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080d2-124">Composant de partie.</span><span class="sxs-lookup"><span data-stu-id="080d2-124">The part component.</span></span>

<span data-ttu-id="080d2-125">Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="080d2-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="080d2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="080d2-126">Remarks</span></span>

<span data-ttu-id="080d2-127">L’Association **CIM \_ SoftwareFeatureSoftwareElements** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="080d2-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="080d2-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="080d2-128">WMI does not implement this class.</span></span> <span data-ttu-id="080d2-129">Pour les classes WMI dérivées de **CIM \_ SoftwareFeatureSoftwareElements**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="080d2-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="080d2-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="080d2-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="080d2-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="080d2-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="080d2-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="080d2-132">Requirements</span></span>



| <span data-ttu-id="080d2-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="080d2-133">Requirement</span></span> | <span data-ttu-id="080d2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="080d2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="080d2-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="080d2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="080d2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="080d2-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="080d2-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="080d2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="080d2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="080d2-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="080d2-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="080d2-139">Namespace</span></span><br/>                | <span data-ttu-id="080d2-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="080d2-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="080d2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="080d2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="080d2-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="080d2-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="080d2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="080d2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080d2-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="080d2-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="080d2-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="080d2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="080d2-146">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="080d2-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


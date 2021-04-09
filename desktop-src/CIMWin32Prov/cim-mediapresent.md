---
description: L' \_ Association CIM MediaPresent décrit une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès aux médias.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: CIM_MediaPresent, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869541"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="c8011-103">CIM_MediaPresent, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c8011-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c8011-104">L’Association **CIM \_ MediaPresent** décrit une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="c8011-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8011-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c8011-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8011-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8011-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8011-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c8011-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c8011-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c8011-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8011-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8011-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c8011-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c8011-110">Members</span></span>

<span data-ttu-id="c8011-111">La classe **CIM \_ MediaPresent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8011-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="c8011-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8011-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8011-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8011-113">Properties</span></span>

<span data-ttu-id="c8011-114">La classe **CIM \_ MediaPresent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8011-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8011-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="c8011-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8011-116">Type de données : **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="c8011-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c8011-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8011-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8011-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c8011-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c8011-119">[**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md) qui décrit l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="c8011-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="c8011-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="c8011-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8011-121">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="c8011-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="c8011-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8011-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8011-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="c8011-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c8011-124">[**\_ StorageExtent CIM**](cim-storageextent.md) qui décrit l’étendue de stockage accessible à l’aide de l’appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="c8011-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8011-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c8011-125">Remarks</span></span>

<span data-ttu-id="c8011-126">La classe **CIM \_ MediaPresent** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c8011-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c8011-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="c8011-127">WMI does not implement this class.</span></span> <span data-ttu-id="c8011-128">Pour les classes dérivées de **CIM \_ MediaPresent**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c8011-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c8011-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8011-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8011-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c8011-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8011-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8011-131">Requirements</span></span>



| <span data-ttu-id="c8011-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8011-132">Requirement</span></span> | <span data-ttu-id="c8011-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8011-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8011-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8011-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c8011-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8011-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8011-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8011-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c8011-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8011-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8011-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8011-138">Namespace</span></span><br/>                | <span data-ttu-id="c8011-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c8011-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8011-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c8011-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8011-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8011-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8011-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c8011-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8011-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8011-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8011-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8011-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8011-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="c8011-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


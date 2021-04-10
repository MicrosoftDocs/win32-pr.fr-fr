---
description: Représente une collection de points de référence de système virtuel.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Classe Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865525"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="05c68-103">MSVM \_ ReferencePointCollection, classe</span><span class="sxs-lookup"><span data-stu-id="05c68-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="05c68-104">Représente une collection de points de référence de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="05c68-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="05c68-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="05c68-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c68-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05c68-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="05c68-107">Membres</span><span class="sxs-lookup"><span data-stu-id="05c68-107">Members</span></span>

<span data-ttu-id="05c68-108">La classe **MSVM \_ ReferencePointCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="05c68-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="05c68-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05c68-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05c68-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05c68-110">Properties</span></span>

<span data-ttu-id="05c68-111">La classe **MSVM \_ ReferencePointCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="05c68-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05c68-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="05c68-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05c68-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05c68-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05c68-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« porte »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="05c68-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="05c68-116">Identification unique de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="05c68-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="05c68-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="05c68-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05c68-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="05c68-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05c68-120">Niveau de cohérence du point de référence.</span><span class="sxs-lookup"><span data-stu-id="05c68-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05c68-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05c68-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="05c68-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (1)</span><span class="sxs-lookup"><span data-stu-id="05c68-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="05c68-123">Le point de référence indique un point dans le temps où le système virtuel se trouvait dans un état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="05c68-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="05c68-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (2)</span><span class="sxs-lookup"><span data-stu-id="05c68-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="05c68-125">Le point de référence indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.</span><span class="sxs-lookup"><span data-stu-id="05c68-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05c68-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="05c68-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05c68-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05c68-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05c68-129">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="05c68-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="05c68-130">Nom défini par l’utilisateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="05c68-130">An user-defined name for the collection.</span></span> <span data-ttu-id="05c68-131">Notez qu’il n’est pas garanti qu’il soit unique.</span><span class="sxs-lookup"><span data-stu-id="05c68-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="05c68-132">**HasAssociatedLog**</span><span class="sxs-lookup"><span data-stu-id="05c68-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05c68-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="05c68-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05c68-135">**true** si tous les points de référence de membre ont des journaux associés.</span><span class="sxs-lookup"><span data-stu-id="05c68-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="05c68-136">Cela est valide uniquement pour les points de référence basés sur un journal.</span><span class="sxs-lookup"><span data-stu-id="05c68-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="05c68-137">Pour les points de référence basés sur RCT, **HasAssociatedLog** est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="05c68-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="05c68-138">Pour les points de référence basés sur un journal, une fois le journal ignoré, **HasAssociatedLog** prend la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="05c68-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="05c68-139">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="05c68-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05c68-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05c68-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05c68-142">Qualificateurs : [ **dans**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="05c68-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="05c68-143">Indique le type du point de référence.</span><span class="sxs-lookup"><span data-stu-id="05c68-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05c68-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05c68-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="05c68-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basé sur le journal** (1)</span><span class="sxs-lookup"><span data-stu-id="05c68-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="05c68-146">Suivi du journal de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="05c68-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="05c68-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basé sur RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="05c68-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="05c68-148">Basé sur une Change Tracking résiliente des disques virtuels.</span><span class="sxs-lookup"><span data-stu-id="05c68-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="05c68-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="05c68-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="05c68-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="05c68-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05c68-151">**VirtualSystemCollectionId**</span><span class="sxs-lookup"><span data-stu-id="05c68-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c68-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05c68-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05c68-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05c68-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05c68-154">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).\*\*\*\* L’un des «»)</span><span class="sxs-lookup"><span data-stu-id="05c68-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="05c68-155">Identificateur du [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) auquel ce point de référence appartient.</span><span class="sxs-lookup"><span data-stu-id="05c68-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05c68-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05c68-156">Requirements</span></span>



| <span data-ttu-id="05c68-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05c68-157">Requirement</span></span> | <span data-ttu-id="05c68-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="05c68-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c68-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05c68-159">Minimum supported client</span></span><br/> | <span data-ttu-id="05c68-160">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05c68-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="05c68-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05c68-161">Minimum supported server</span></span><br/> | <span data-ttu-id="05c68-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="05c68-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="05c68-163">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="05c68-163">Namespace</span></span><br/>                | <span data-ttu-id="05c68-164">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="05c68-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05c68-165">MOF</span><span class="sxs-lookup"><span data-stu-id="05c68-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05c68-166"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05c68-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05c68-167">DLL</span><span class="sxs-lookup"><span data-stu-id="05c68-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05c68-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05c68-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05c68-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05c68-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c68-170">**\_Collection CIM**</span><span class="sxs-lookup"><span data-stu-id="05c68-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 


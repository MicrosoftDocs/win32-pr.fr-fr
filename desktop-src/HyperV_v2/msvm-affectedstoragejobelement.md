---
description: Représente l’association entre un travail et les éléments managés qui peuvent être affectés par son exécution.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515811"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="33534-103">MSVM \_ AffectedStorageJobElement, classe</span><span class="sxs-lookup"><span data-stu-id="33534-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="33534-104">Représente l’association entre un travail et les éléments managés qui peuvent être affectés par son exécution.</span><span class="sxs-lookup"><span data-stu-id="33534-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="33534-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="33534-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33534-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33534-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="33534-107">Membres</span><span class="sxs-lookup"><span data-stu-id="33534-107">Members</span></span>

<span data-ttu-id="33534-108">La classe **MSVM \_ AffectedStorageJobElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="33534-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="33534-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33534-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33534-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33534-110">Properties</span></span>

<span data-ttu-id="33534-111">La classe **MSVM \_ AffectedStorageJobElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="33534-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33534-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="33534-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33534-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="33534-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="33534-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33534-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33534-115">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="33534-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="33534-116">Élément managé affecté par l’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="33534-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="33534-117">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33534-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33534-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="33534-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33534-119">Type de données : **[ **MSVM \_ StorageJob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="33534-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="33534-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33534-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33534-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. AffectingElement")</span><span class="sxs-lookup"><span data-stu-id="33534-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="33534-122">Travail qui affecte l’élément affecté.</span><span class="sxs-lookup"><span data-stu-id="33534-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="33534-123">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33534-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33534-124">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="33534-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33534-125">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33534-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="33534-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33534-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33534-127">Énumération qui décrit l’effet sur l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="33534-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="33534-128">Ce tableau correspond au tableau de propriétés **OtherElementEffectsDescriptions** , où ce dernier fournit des détails relatifs aux effets de haut niveau énumérés par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="33534-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="33534-129">Des détails supplémentaires sont requis si le tableau de propriétés **ElementEffects** contient la valeur 1, (other).</span><span class="sxs-lookup"><span data-stu-id="33534-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="33534-130">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33534-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="33534-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="33534-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33534-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="33534-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33534-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Utilisation exclusive** (2)</span><span class="sxs-lookup"><span data-stu-id="33534-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33534-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Impact sur les performances** (3)</span><span class="sxs-lookup"><span data-stu-id="33534-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33534-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Intégrité de l’élément** (4)</span><span class="sxs-lookup"><span data-stu-id="33534-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33534-136">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="33534-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33534-137">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="33534-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33534-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33534-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33534-139">Fournit des détails sur l’effet à la position de tableau correspondante dans le tableau de propriétés **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="33534-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="33534-140">Ces informations sont requises chaque fois que l’élément correspondant dans le tableau de propriétés **ElementEffects** contient la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="33534-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="33534-141">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33534-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33534-142">Notes</span><span class="sxs-lookup"><span data-stu-id="33534-142">Remarks</span></span>

<span data-ttu-id="33534-143">L’accès à la classe **MSVM \_ AffectedStorageJobElement** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="33534-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="33534-144">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="33534-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="33534-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33534-145">Requirements</span></span>



| <span data-ttu-id="33534-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33534-146">Requirement</span></span> | <span data-ttu-id="33534-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="33534-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33534-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33534-148">Minimum supported client</span></span><br/> | <span data-ttu-id="33534-149">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33534-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33534-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33534-150">Minimum supported server</span></span><br/> | <span data-ttu-id="33534-151">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33534-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33534-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33534-152">Namespace</span></span><br/>                | <span data-ttu-id="33534-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="33534-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33534-154">MOF</span><span class="sxs-lookup"><span data-stu-id="33534-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33534-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33534-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33534-156">DLL</span><span class="sxs-lookup"><span data-stu-id="33534-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33534-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33534-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33534-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33534-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33534-159">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="33534-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="33534-160">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33534-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33534-161">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="33534-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


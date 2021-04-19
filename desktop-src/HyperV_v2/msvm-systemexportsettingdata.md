---
description: Associe un ordinateur virtuel et ses données de paramètre d’exportation.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513362"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="fb57b-103">MSVM \_ SystemExportSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="fb57b-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="fb57b-104">Associe un ordinateur virtuel et ses données de paramètre d’exportation.</span><span class="sxs-lookup"><span data-stu-id="fb57b-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="fb57b-105">Avant d’appeler la méthode [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) , vous pouvez récupérer une instance de [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) à l’aide de cette association.</span><span class="sxs-lookup"><span data-stu-id="fb57b-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="fb57b-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fb57b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb57b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb57b-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="fb57b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fb57b-108">Members</span></span>

<span data-ttu-id="fb57b-109">La classe **MSVM \_ SystemExportSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb57b-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fb57b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb57b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb57b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb57b-111">Properties</span></span>

<span data-ttu-id="fb57b-112">La classe **MSVM \_ SystemExportSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb57b-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb57b-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="fb57b-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb57b-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb57b-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb57b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb57b-116">Indique si le paramètre référencé est actuellement utilisé dans l’opération de l’élément, ou si ces informations sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="fb57b-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="fb57b-117">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fb57b-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="fb57b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb57b-118">Value</span></span>                                                                        | <span data-ttu-id="fb57b-119">Signification</span><span class="sxs-lookup"><span data-stu-id="fb57b-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="fb57b-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fb57b-121">Unknown</span><span class="sxs-lookup"><span data-stu-id="fb57b-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="fb57b-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fb57b-123">Actuel</span><span class="sxs-lookup"><span data-stu-id="fb57b-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="fb57b-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="fb57b-125">Non actuel</span><span class="sxs-lookup"><span data-stu-id="fb57b-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb57b-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="fb57b-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb57b-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb57b-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb57b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb57b-129">Indique si le paramètre référencé est un paramètre par défaut pour l’élément, ou si ces informations sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="fb57b-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="fb57b-130">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fb57b-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="fb57b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb57b-131">Value</span></span>                                                                        | <span data-ttu-id="fb57b-132">Signification</span><span class="sxs-lookup"><span data-stu-id="fb57b-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="fb57b-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fb57b-134">Unknown</span><span class="sxs-lookup"><span data-stu-id="fb57b-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="fb57b-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fb57b-136">Default</span><span class="sxs-lookup"><span data-stu-id="fb57b-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="fb57b-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="fb57b-138">Pas par défaut</span><span class="sxs-lookup"><span data-stu-id="fb57b-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb57b-139">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="fb57b-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb57b-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb57b-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb57b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb57b-142">Indique si le paramètre référencé est ou non le paramètre suivant à appliquer.</span><span class="sxs-lookup"><span data-stu-id="fb57b-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="fb57b-143">Par exemple, l’application peut être exécutée sur une demande de réinitialisation, de réinitialisation et de reconfiguration.</span><span class="sxs-lookup"><span data-stu-id="fb57b-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="fb57b-144">Il peut s’agir d’un paramètre permanent, ou d’un paramètre utilisé une seule fois, comme indiqué par l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="fb57b-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="fb57b-145">S’il s’agit d’un paramètre permanent, le paramètre est appliqué à chaque réinitialisation de l’élément managé, jusqu’à ce que cet indicateur soit réinitialisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="fb57b-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="fb57b-146">Toutefois, s’il s’agit d’une utilisation unique, l’indicateur est automatiquement effacé après l’application des paramètres.</span><span class="sxs-lookup"><span data-stu-id="fb57b-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="fb57b-147">En outre, si cet indicateur est spécifié (c’est-à-dire défini sur une valeur autre que 0 (inconnu)), il est prioritaire sur les données de paramètre qui ont pu être spécifiées comme valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb57b-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="fb57b-148">Par exemple : si l’élément géré est un système informatique et que la valeur de cet indicateur est 1 (suivant), le paramètre sera effectif à la prochaine réinitialisation du système.</span><span class="sxs-lookup"><span data-stu-id="fb57b-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="fb57b-149">Et, sauf si cet indicateur est modifié, il est conservé pour les réinitialisations ultérieures du système.</span><span class="sxs-lookup"><span data-stu-id="fb57b-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="fb57b-150">Toutefois, si cet indicateur a la valeur 3 (est ensuite utilisé pour une utilisation unique), ce paramètre n’est utilisé qu’une seule fois et l’indicateur est réinitialisé après cela sur 2 (n’est pas suivant).</span><span class="sxs-lookup"><span data-stu-id="fb57b-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="fb57b-151">Ainsi, dans l’exemple ci-dessus, si le système redémarre rapidement en succession, le paramètre ne sera pas utilisé au deuxième redémarrage.</span><span class="sxs-lookup"><span data-stu-id="fb57b-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="fb57b-152">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fb57b-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="fb57b-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb57b-153">Value</span></span>                                                                        | <span data-ttu-id="fb57b-154">Signification</span><span class="sxs-lookup"><span data-stu-id="fb57b-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fb57b-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fb57b-156">Unknown</span><span class="sxs-lookup"><span data-stu-id="fb57b-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="fb57b-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fb57b-158">Est ensuite</span><span class="sxs-lookup"><span data-stu-id="fb57b-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="fb57b-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="fb57b-160">N’est pas suivant</span><span class="sxs-lookup"><span data-stu-id="fb57b-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="fb57b-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="fb57b-162">Est ensuite utilisé pour une utilisation unique</span><span class="sxs-lookup"><span data-stu-id="fb57b-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb57b-163">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fb57b-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb57b-164">Type de données : **[ **CIM CIM \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="fb57b-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb57b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-166">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. propriété ManagedElement")</span><span class="sxs-lookup"><span data-stu-id="fb57b-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="fb57b-167">Référence à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fb57b-167">Reference to the virtual machine.</span></span> <span data-ttu-id="fb57b-168">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fb57b-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb57b-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="fb57b-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb57b-170">Type de données : **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="fb57b-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb57b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb57b-172">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")</span><span class="sxs-lookup"><span data-stu-id="fb57b-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="fb57b-173">Référence aux données de paramètre d’exportation pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fb57b-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="fb57b-174">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fb57b-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb57b-175">Notes</span><span class="sxs-lookup"><span data-stu-id="fb57b-175">Remarks</span></span>

<span data-ttu-id="fb57b-176">L’accès à la classe **MSVM \_ SystemExportSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="fb57b-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fb57b-177">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fb57b-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb57b-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb57b-178">Requirements</span></span>



| <span data-ttu-id="fb57b-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb57b-179">Requirement</span></span> | <span data-ttu-id="fb57b-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb57b-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb57b-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb57b-181">Minimum supported client</span></span><br/> | <span data-ttu-id="fb57b-182">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb57b-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb57b-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb57b-183">Minimum supported server</span></span><br/> | <span data-ttu-id="fb57b-184">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb57b-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb57b-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb57b-185">Namespace</span></span><br/>                | <span data-ttu-id="fb57b-186">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb57b-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb57b-187">MOF</span><span class="sxs-lookup"><span data-stu-id="fb57b-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb57b-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb57b-189">DLL</span><span class="sxs-lookup"><span data-stu-id="fb57b-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb57b-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb57b-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


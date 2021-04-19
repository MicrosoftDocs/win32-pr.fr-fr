---
description: Représente un service d’appareil virtuel de la plateforme Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514393"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="ffa0f-103">MSVM \_ VirtualSystemResourceComponent, classe</span><span class="sxs-lookup"><span data-stu-id="ffa0f-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="ffa0f-104">Représente un service d’appareil virtuel de la plateforme Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="ffa0f-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa0f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa0f-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="ffa0f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ffa0f-107">Members</span></span>

<span data-ttu-id="ffa0f-108">La classe **MSVM \_ VirtualSystemResourceComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffa0f-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="ffa0f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffa0f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffa0f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffa0f-110">Properties</span></span>

<span data-ttu-id="ffa0f-111">La classe **MSVM \_ VirtualSystemResourceComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffa0f-112">**AdditionalClassNames**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-115">Tableau de chaînes contenant des classes non associées supplémentaires qui sont exposées par cette instance **MSVM \_ VirtualSystemResourceComponent** .</span><span class="sxs-lookup"><span data-stu-id="ffa0f-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="ffa0f-116">Ces classes doivent dériver d' [**un \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ou d’un [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ffa0f-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-117">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-120">GUID qui représente l’identificateur de classe de l’objet COM du service.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="ffa0f-121">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="ffa0f-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-122">**Contexte**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-125">Contexte dans lequel l’objet nouvellement créé s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="ffa0f-126">Cette valeur est passée dans le paramètre *dwClsContext* à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="ffa0f-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="ffa0f-127">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-131">**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="ffa0f-132">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-133">**HotAdd**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-136">**True** si cette instance peut être ajoutée à chaud à un ordinateur virtuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="ffa0f-137">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-138">**HotRemove**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-141">**True** si cette instance peut être supprimée à chaud d’une machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="ffa0f-142">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-146">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-147">Chaîne indépendante du langage qui identifie de façon unique le service.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="ffa0f-148">Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ».</span><span class="sxs-lookup"><span data-stu-id="ffa0f-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="ffa0f-149">Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="ffa0f-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="ffa0f-150">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="ffa0f-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffa0f-151">**Type**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa0f-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffa0f-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffa0f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffa0f-154">Relation de l’objet WMI décrit ici avec l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="ffa0f-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa0f-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="ffa0f-156">Signification</span><span class="sxs-lookup"><span data-stu-id="ffa0f-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="ffa0f-157"><dt>**« Non modifiable »**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="ffa0f-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="ffa0f-159">Singleton est un objet WMI de niveau supérieur qui est lié 1:1 avec un appareil virtuel et qui ne peut exister qu’une seule fois par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="ffa0f-160">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="ffa0f-161"><dt>**« MultiInstance »**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="ffa0f-162">Multi-instance est un objet WMI de niveau supérieur qui peut exister plusieurs fois par machine virtuelle et est lié 1:1 avec un appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="ffa0f-163"><dt>**« Sous-appareil »**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="ffa0f-164">Le sous-appareil est un objet WMI qui n’a pas de référence parent, mais qui est contrôlé par un seul appareil virtuel qui ne peut exister qu’une seule fois par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="ffa0f-165">L’objet WMI peut cependant exister plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffa0f-166">Notes</span><span class="sxs-lookup"><span data-stu-id="ffa0f-166">Remarks</span></span>

<span data-ttu-id="ffa0f-167">L’accès à la classe **MSVM \_ VirtualSystemResourceComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="ffa0f-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ffa0f-168">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ffa0f-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa0f-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa0f-169">Requirements</span></span>



| <span data-ttu-id="ffa0f-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa0f-170">Requirement</span></span> | <span data-ttu-id="ffa0f-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa0f-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa0f-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa0f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa0f-173">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffa0f-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ffa0f-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa0f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa0f-175">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffa0f-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffa0f-176">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ffa0f-176">End of client support</span></span><br/>    | <span data-ttu-id="ffa0f-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffa0f-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffa0f-178">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ffa0f-178">End of server support</span></span><br/>    | <span data-ttu-id="ffa0f-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffa0f-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffa0f-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ffa0f-180">Namespace</span></span><br/>                | <span data-ttu-id="ffa0f-181">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffa0f-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ffa0f-182">MOF</span><span class="sxs-lookup"><span data-stu-id="ffa0f-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffa0f-183"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffa0f-184">DLL</span><span class="sxs-lookup"><span data-stu-id="ffa0f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa0f-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffa0f-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffa0f-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa0f-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa0f-187">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="ffa0f-188">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="ffa0f-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 


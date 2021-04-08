---
description: Décrit les fonctionnalités de la classe MSVM \_ ResourcePoolConfigurationService associée.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Classe Msvm_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866110"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="79d97-103">MSVM \_ ResourcePoolConfigurationCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="79d97-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="79d97-104">Décrit les fonctionnalités de la classe [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) associée.</span><span class="sxs-lookup"><span data-stu-id="79d97-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="79d97-105">Les clients peuvent utiliser des instances de cette classe pour déterminer les méthodes prises en charge de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="79d97-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="79d97-106">La même méthode ne doit pas figurer dans les deux listes.</span><span class="sxs-lookup"><span data-stu-id="79d97-106">The same method must not be in both lists.</span></span> <span data-ttu-id="79d97-107">Les implémentations de méthode doivent être synchrones ou asynchrones.</span><span class="sxs-lookup"><span data-stu-id="79d97-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="79d97-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="79d97-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d97-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79d97-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="79d97-110">Membres</span><span class="sxs-lookup"><span data-stu-id="79d97-110">Members</span></span>

<span data-ttu-id="79d97-111">La classe **MSVM \_ ResourcePoolConfigurationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="79d97-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="79d97-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79d97-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79d97-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79d97-113">Properties</span></span>

<span data-ttu-id="79d97-114">La classe **MSVM \_ ResourcePoolConfigurationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="79d97-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79d97-115">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="79d97-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-116">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79d97-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="79d97-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79d97-118">Tableau d’identificateurs de méthode, chacun identifiant une méthode de la classe [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) qui est prise en charge de façon asynchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="79d97-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79d97-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="79d97-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-120">**CreatePool est pris en charge** (32768)</span><span class="sxs-lookup"><span data-stu-id="79d97-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-121">**ChangePoolResources est pris en charge** (32769)</span><span class="sxs-lookup"><span data-stu-id="79d97-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-122">**ChangePoolSettings est pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="79d97-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-123">**DeletePool est pris en charge** (32771)</span><span class="sxs-lookup"><span data-stu-id="79d97-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79d97-124">**Fournisseur réservé** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="79d97-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79d97-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="79d97-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79d97-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79d97-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79d97-128">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79d97-128">A short description of the object.</span></span> <span data-ttu-id="79d97-129">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de configuration du pool de ressources ».</span><span class="sxs-lookup"><span data-stu-id="79d97-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="79d97-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="79d97-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79d97-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79d97-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79d97-133">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="79d97-133">A description of the object.</span></span> <span data-ttu-id="79d97-134">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de configuration de pool de ressources Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="79d97-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="79d97-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="79d97-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79d97-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79d97-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79d97-138">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79d97-138">A display name for the object.</span></span> <span data-ttu-id="79d97-139">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de configuration du pool de ressources ».</span><span class="sxs-lookup"><span data-stu-id="79d97-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="79d97-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="79d97-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79d97-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79d97-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79d97-143">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="79d97-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="79d97-144">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="79d97-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="79d97-145">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79d97-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79d97-146">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="79d97-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d97-147">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79d97-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="79d97-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79d97-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79d97-149">Tableau d’identificateurs de méthode, chacun identifiant une méthode de la classe [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) qui est prise en charge de façon synchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="79d97-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79d97-150">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="79d97-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-151">**CreatePool est pris en charge** (32768)</span><span class="sxs-lookup"><span data-stu-id="79d97-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-152">**ChangePoolResources est pris en charge** (32769)</span><span class="sxs-lookup"><span data-stu-id="79d97-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-153">**ChangePoolSettings est pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="79d97-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="79d97-154">**DeletePool est pris en charge** (32771)</span><span class="sxs-lookup"><span data-stu-id="79d97-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79d97-155">**Fournisseur réservé** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="79d97-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="79d97-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79d97-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="79d97-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79d97-157">Requirements</span></span>



| <span data-ttu-id="79d97-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79d97-158">Requirement</span></span> | <span data-ttu-id="79d97-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="79d97-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d97-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79d97-160">Minimum supported client</span></span><br/> | <span data-ttu-id="79d97-161">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79d97-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="79d97-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79d97-162">Minimum supported server</span></span><br/> | <span data-ttu-id="79d97-163">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79d97-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79d97-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79d97-164">Namespace</span></span><br/>                | <span data-ttu-id="79d97-165">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="79d97-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79d97-166">MOF</span><span class="sxs-lookup"><span data-stu-id="79d97-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79d97-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79d97-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79d97-168">DLL</span><span class="sxs-lookup"><span data-stu-id="79d97-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79d97-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79d97-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


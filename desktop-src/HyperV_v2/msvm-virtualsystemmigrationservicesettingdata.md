---
description: Représente les paramètres pour le service de migration de système virtuel sur un ordinateur hôte.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Classe Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516420"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="b9869-103">MSVM \_ VirtualSystemMigrationServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="b9869-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="b9869-104">Représente les paramètres pour le service de migration de système virtuel sur un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="b9869-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="b9869-105">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="b9869-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="b9869-106">Le client doit appeler la méthode **MSVM \_ VirtualSystemMigrationService. ModifyServiceSettings** pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b9869-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="b9869-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b9869-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9869-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9869-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="b9869-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b9869-109">Members</span></span>

<span data-ttu-id="b9869-110">La classe **MSVM \_ VirtualSystemMigrationServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b9869-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b9869-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b9869-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9869-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b9869-112">Properties</span></span>

<span data-ttu-id="b9869-113">La classe **MSVM \_ VirtualSystemMigrationServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9869-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9869-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="b9869-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9869-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-117">Spécifie le mécanisme d’authentification utilisé pour les connexions réseau de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="b9869-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="b9869-118">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="b9869-119">**CredSSP** (0)</span><span class="sxs-lookup"><span data-stu-id="b9869-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="b9869-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="b9869-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9869-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b9869-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9869-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-124">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b9869-124">A short description of the object.</span></span> <span data-ttu-id="b9869-125">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="b9869-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="b9869-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9869-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9869-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-129">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="b9869-129">A description of the object.</span></span> <span data-ttu-id="b9869-130">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b9869-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b9869-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b9869-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9869-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-134">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b9869-134">A display name for the object.</span></span> <span data-ttu-id="b9869-135">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9869-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b9869-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="b9869-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b9869-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b9869-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b9869-139">Indique si la compression du trafic de migration dynamique est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="b9869-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="b9869-140">True indique que l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="b9869-140">True indicates enabled.</span></span>

<span data-ttu-id="b9869-141">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="b9869-142">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b9869-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="b9869-143">**EnableSmbTransport**</span><span class="sxs-lookup"><span data-stu-id="b9869-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b9869-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b9869-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b9869-146">Indique si l’utilisation de SMB comme type de transport pour transférer l’état de la machine virtuelle entre les ordinateurs hôtes Hyper-V pendant la migration du système virtuel est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="b9869-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="b9869-147">**True** indique que l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="b9869-147">**True** indicates enabled.</span></span> <span data-ttu-id="b9869-148">Des performances supérieures sont obtenues si les cartes réseau RDMA sont configurées pour le transport SMB lors de la migration dynamique de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b9869-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="b9869-149">Si la valeur de **EnableSmbTransport** est true, la valeur de **EnableCompression** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="b9869-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="b9869-150">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="b9869-151">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b9869-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="b9869-152">**EnableVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="b9869-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-153">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b9869-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-155">Spécifie si la migration du système virtuel est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="b9869-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="b9869-156">La migration du stockage est toujours activée.</span><span class="sxs-lookup"><span data-stu-id="b9869-156">Storage migration is always enabled.</span></span> <span data-ttu-id="b9869-157">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b9869-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9869-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9869-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9869-161">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b9869-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b9869-162">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b9869-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b9869-163">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b9869-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b9869-164">**MaximumActiveStorageMigration**</span><span class="sxs-lookup"><span data-stu-id="b9869-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9869-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-167">Spécifie le nombre maximal de migrations de stockage actives autorisées.</span><span class="sxs-lookup"><span data-stu-id="b9869-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="b9869-168">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b9869-169">**MaximumActiveVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="b9869-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9869-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9869-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9869-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9869-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9869-172">Spécifie le nombre maximal de migrations de système virtuel actives autorisées.</span><span class="sxs-lookup"><span data-stu-id="b9869-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="b9869-173">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b9869-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9869-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9869-174">Requirements</span></span>



| <span data-ttu-id="b9869-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9869-175">Requirement</span></span> | <span data-ttu-id="b9869-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9869-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9869-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9869-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b9869-178">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9869-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9869-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9869-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b9869-180">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9869-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9869-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b9869-181">Namespace</span></span><br/>                | <span data-ttu-id="b9869-182">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b9869-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9869-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b9869-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9869-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9869-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9869-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b9869-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9869-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9869-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9869-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9869-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9869-188">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b9869-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="b9869-189">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="b9869-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


---
description: Représente les paramètres pour le service de virtualisation présent sur un système hôte unique.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Classe Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514987"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="f1623-103">MSVM \_ VirtualSystemManagementServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="f1623-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="f1623-104">Représente les paramètres pour le service de virtualisation présent sur un système hôte unique.</span><span class="sxs-lookup"><span data-stu-id="f1623-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="f1623-105">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="f1623-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="f1623-106">Le client doit appeler la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f1623-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="f1623-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f1623-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1623-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1623-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="f1623-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f1623-109">Members</span></span>

<span data-ttu-id="f1623-110">La classe **MSVM \_ VirtualSystemManagementServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1623-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f1623-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1623-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1623-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1623-112">Properties</span></span>

<span data-ttu-id="f1623-113">La classe **MSVM \_ VirtualSystemManagementServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1623-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1623-114">**BiosLockString**</span><span class="sxs-lookup"><span data-stu-id="f1623-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1623-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="f1623-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="f1623-118">Utilisé par les fabricants d’ordinateurs OEM pour permettre aux systèmes d’exploitation Windows verrouillés du BIOS de s’exécuter sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f1623-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="f1623-119">Cette chaîne doit avoir une longueur de 32 caractères exactement.</span><span class="sxs-lookup"><span data-stu-id="f1623-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="f1623-120">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1623-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-124">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1623-124">A short description of the object.</span></span> <span data-ttu-id="f1623-125">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="f1623-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="f1623-126">**CurrentWWNNAddress**</span><span class="sxs-lookup"><span data-stu-id="f1623-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-129">Adresse WWNN (World World Node Name) pour les adresses de nom WWN générées dynamiquement utilisées pour les adaptateurs de bus hôte synthétiques.</span><span class="sxs-lookup"><span data-stu-id="f1623-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="f1623-130">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-131">**DefaultExternalDataRoot**</span><span class="sxs-lookup"><span data-stu-id="f1623-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1623-134">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span><span class="sxs-lookup"><span data-stu-id="f1623-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="f1623-135">Racine de données externes par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1623-135">The default external data root.</span></span> <span data-ttu-id="f1623-136">Par défaut, «*root* \\ ProgramData \\ Microsoft \\ Windows \\ Virtualization ».</span><span class="sxs-lookup"><span data-stu-id="f1623-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="f1623-137">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-138">**DefaultVirtualHardDiskCachingMode**</span><span class="sxs-lookup"><span data-stu-id="f1623-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1623-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-141">Indique si la mise en cache des fichiers en mémoire doit être utilisée par défaut pour les disques.</span><span class="sxs-lookup"><span data-stu-id="f1623-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="f1623-142">Cette valeur peut être remplacée par disque dans le champ **CachingMode** de la classe [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="f1623-143">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f1623-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1623-144">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f1623-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="f1623-145">**Aucune mise en cache** (3)</span><span class="sxs-lookup"><span data-stu-id="f1623-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="f1623-146">Mettre **en cache les parents partageables** (4)</span><span class="sxs-lookup"><span data-stu-id="f1623-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1623-147">**DefaultVirtualHardDiskPath**</span><span class="sxs-lookup"><span data-stu-id="f1623-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-150">Chemin d’accès au disque dur virtuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1623-150">The default virtual hard disk path.</span></span> <span data-ttu-id="f1623-151">Par défaut, «*root* \\ Users \\ public \\ documents \\ Hard Disks ».</span><span class="sxs-lookup"><span data-stu-id="f1623-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="f1623-152">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1623-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-156">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f1623-156">A description of the object.</span></span> <span data-ttu-id="f1623-157">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres pour le service de gestion du système virtuel ».</span><span class="sxs-lookup"><span data-stu-id="f1623-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="f1623-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f1623-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-161">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1623-161">A display name for the object.</span></span> <span data-ttu-id="f1623-162">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="f1623-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="f1623-163">La modification de cette propriété entraînera la modification de la propriété **ElementName** de la dérivée [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associée.</span><span class="sxs-lookup"><span data-stu-id="f1623-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-164">**EnhancedSessionModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="f1623-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-165">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f1623-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-167">Indique si le mode de session étendu est autorisé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f1623-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="f1623-168">**True** indique que l’autorisation est autorisée ; sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="f1623-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="f1623-169">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f1623-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-170">**HbaLunTimeout**</span><span class="sxs-lookup"><span data-stu-id="f1623-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1623-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-173">Spécifie la durée pendant laquelle l’appareil virtuel de Fibre Channel synthétique attendra qu’un numéro d’unité logique apparaisse avant de démarrer un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f1623-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="f1623-174">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-175">**HypervisorRootSchedulerEnabled**</span><span class="sxs-lookup"><span data-stu-id="f1623-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-176">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f1623-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-178">Indique si le planificateur racine de l’hyperviseur est activé.</span><span class="sxs-lookup"><span data-stu-id="f1623-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="f1623-179">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="f1623-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f1623-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1623-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1623-183">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f1623-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f1623-184">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1623-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f1623-185">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « Microsoft :*Host*», où *Host* est le nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="f1623-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-186">**MaximumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="f1623-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-189">Adresse MAC maximale pour les adresses MAC générées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="f1623-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="f1623-190">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-191">**MaximumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="f1623-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-194">Adresse du nom WWN (WWPN) maximale pour les adresses de nom WWN générées dynamiquement utilisées pour les adaptateurs de bus hôte synthétiques.</span><span class="sxs-lookup"><span data-stu-id="f1623-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="f1623-195">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-196">**MinimumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="f1623-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-199">Adresse MAC minimale pour les adresses MAC générées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="f1623-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="f1623-200">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-201">**MinimumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="f1623-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-204">Adresse du nom de port WWN minimale pour les adresses de nom WWN générées dynamiquement utilisées pour les adaptateurs de bus hôte synthétiques.</span><span class="sxs-lookup"><span data-stu-id="f1623-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="f1623-205">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-206">**NumaSpanningEnabled**</span><span class="sxs-lookup"><span data-stu-id="f1623-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-207">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f1623-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1623-209">Spécifie si la mémoire peut être allouée à partir de nœuds NUMA (non-Uniform Memory Access) distants au démarrage d’un ordinateur virtuel ou lors de l’affectation de la mémoire à un ordinateur virtuel par la mémoire dynamique.</span><span class="sxs-lookup"><span data-stu-id="f1623-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="f1623-210">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1623-210">This can be one of the following values.</span></span>



| <span data-ttu-id="f1623-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1623-211">Value</span></span>                                                                                | <span data-ttu-id="f1623-212">Signification</span><span class="sxs-lookup"><span data-stu-id="f1623-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1623-213"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="f1623-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="f1623-214">La mémoire peut être allouée à partir des nœuds NUMA locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="f1623-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="f1623-215"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="f1623-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="f1623-216">La mémoire ne peut être allouée qu’à partir du nœud NUMA affecté à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f1623-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="f1623-217">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="f1623-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1623-221">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="f1623-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f1623-222">Décrit comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="f1623-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="f1623-223">Par défaut, vide.</span><span class="sxs-lookup"><span data-stu-id="f1623-223">By default, empty.</span></span> <span data-ttu-id="f1623-224">Ce nom ne doit pas dépasser 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="f1623-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="f1623-225">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1623-226">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="f1623-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1623-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1623-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1623-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1623-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1623-229">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="f1623-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1623-230">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="f1623-230">The name of the primary system owner.</span></span> <span data-ttu-id="f1623-231">Par défaut, « administrateurs ».</span><span class="sxs-lookup"><span data-stu-id="f1623-231">By default, "Administrators".</span></span> <span data-ttu-id="f1623-232">Cette valeur ne doit pas dépasser 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="f1623-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="f1623-233">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1623-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1623-234">Notes</span><span class="sxs-lookup"><span data-stu-id="f1623-234">Remarks</span></span>

<span data-ttu-id="f1623-235">L’accès à la classe **MSVM \_ VirtualSystemManagementServiceSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="f1623-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f1623-236">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f1623-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1623-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1623-237">Requirements</span></span>



| <span data-ttu-id="f1623-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1623-238">Requirement</span></span> | <span data-ttu-id="f1623-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1623-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1623-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1623-240">Minimum supported client</span></span><br/> | <span data-ttu-id="f1623-241">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1623-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1623-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1623-242">Minimum supported server</span></span><br/> | <span data-ttu-id="f1623-243">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1623-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1623-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1623-244">Namespace</span></span><br/>                | <span data-ttu-id="f1623-245">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1623-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1623-246">MOF</span><span class="sxs-lookup"><span data-stu-id="f1623-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1623-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1623-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1623-248">DLL</span><span class="sxs-lookup"><span data-stu-id="f1623-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1623-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1623-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1623-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1623-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1623-251">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="f1623-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="f1623-252">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="f1623-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="f1623-253">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1623-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1623-254">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="f1623-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


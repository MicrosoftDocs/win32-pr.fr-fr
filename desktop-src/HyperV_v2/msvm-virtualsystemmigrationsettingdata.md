---
description: Représente les paramètres de migration pour la migration d’un système virtuel et du stockage attaché à un système virtuel.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862054"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="ee658-103">MSVM \_ VirtualSystemMigrationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ee658-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="ee658-104">Représente les paramètres de migration pour la migration d’un système virtuel et du stockage attaché à un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ee658-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="ee658-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee658-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee658-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee658-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="ee658-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ee658-107">Members</span></span>

<span data-ttu-id="ee658-108">La classe **MSVM \_ VirtualSystemMigrationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee658-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ee658-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee658-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee658-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee658-110">Properties</span></span>

<span data-ttu-id="ee658-111">La classe **MSVM \_ VirtualSystemMigrationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee658-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee658-112">**AllowOverwriteExistingFile**</span><span class="sxs-lookup"><span data-stu-id="ee658-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-115">Autoriser l’opération de migration du stockage à remplacer les fichiers. vhdx existants.</span><span class="sxs-lookup"><span data-stu-id="ee658-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-116">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="ee658-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ee658-117">**AvoidRemovingVHDs**</span><span class="sxs-lookup"><span data-stu-id="ee658-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-120">Ne supprimez pas les disques durs virtuels pendant la migration, c’est-à-dire les VHD sur la source dans successand VHD sur la destination en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ee658-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-121">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ee658-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ee658-122">**Bande passante**</span><span class="sxs-lookup"><span data-stu-id="ee658-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee658-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-125">Spécifie la bande passante affectée ou demandée pour une opération de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ee658-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="ee658-126">Les unités de bande passante sont spécifiées par la propriété **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="ee658-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="ee658-127">Dans une migration, la valeur 0 indique la bande passante par défaut.</span><span class="sxs-lookup"><span data-stu-id="ee658-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="ee658-128">Dans le cas contraire, la valeur 0 indique que les bandes passantes ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ee658-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="ee658-129">**La bande passante et la** **priorité** peuvent être utilisées conjointement.</span><span class="sxs-lookup"><span data-stu-id="ee658-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="ee658-130">Les processus de migration ayant la valeur de priorité la plus élevée partagent la bande passante disponible en fonction de la bande passante demandée.</span><span class="sxs-lookup"><span data-stu-id="ee658-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="ee658-131">Si la bande passante n’est pas consommée par cet ensemble de processus, les processus de migration avec la priorité la plus basse égale partagent la bande passante restante.</span><span class="sxs-lookup"><span data-stu-id="ee658-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="ee658-132">Si la bande passante est toujours supérieure, les processus de migration avec la priorité égale inférieure suivante sont considérés, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ee658-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="ee658-133">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-134">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="ee658-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-137">Spécifie les unités utilisées par la propriété de **bande passante** .</span><span class="sxs-lookup"><span data-stu-id="ee658-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="ee658-138">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ee658-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="ee658-139">Si la valeur de cette propriété est « percent », la valeur de la propriété de **bande passante** doit être comprise entre 0 et 100, avec des valeurs plus élevées indiquant une bande passante plus élevée.</span><span class="sxs-lookup"><span data-stu-id="ee658-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="ee658-140">La valeur 100 indique la bande passante totale disponible pour l’exécution des opérations de migration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ee658-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="ee658-141">Les valeurs comprises entre 1 et 100 doivent correspondre de manière linéaire à la plage de bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="ee658-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="ee658-142">Par exemple, une valeur de 50 doit demander la moitié de la bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="ee658-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="ee658-143">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-144">**CancelIfBlackoutThresholdExceeded**</span><span class="sxs-lookup"><span data-stu-id="ee658-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-147">Annule la migration si le temps de dépassement du seuil d’indisponibilité est dépassé.</span><span class="sxs-lookup"><span data-stu-id="ee658-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-148">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="ee658-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ee658-149">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ee658-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-152">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee658-152">A short description of the object.</span></span> <span data-ttu-id="ee658-153">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee658-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee658-154">**CPUCappingMagnitude**</span><span class="sxs-lookup"><span data-stu-id="ee658-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee658-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ee658-157">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span><span class="sxs-lookup"><span data-stu-id="ee658-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="ee658-158">Degré de limitation de l’UC pendant la migration.</span><span class="sxs-lookup"><span data-stu-id="ee658-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-159">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="ee658-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="ee658-160">**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="ee658-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="ee658-161">**Faible** (1)</span><span class="sxs-lookup"><span data-stu-id="ee658-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="ee658-162">**Élevé** (2)</span><span class="sxs-lookup"><span data-stu-id="ee658-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee658-163">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee658-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-166">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ee658-166">A description of the object.</span></span> <span data-ttu-id="ee658-167">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee658-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee658-168">**DestinationIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="ee658-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-169">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee658-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee658-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-171">Il s’agit d’une **valeur null** pour la migration du stockage.</span><span class="sxs-lookup"><span data-stu-id="ee658-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="ee658-172">Pour la migration du système virtuel, il peut contenir une liste d’adresses IP de l’hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-173">**DestinationPlannedVirtualSystemId**</span><span class="sxs-lookup"><span data-stu-id="ee658-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-176">Si une machine virtuelle planifiée existe à la destination de la migration, cette propriété est définie sur le GUID de la machine virtuelle planifiée de destination dans laquelle la machine virtuelle doit être migrée.</span><span class="sxs-lookup"><span data-stu-id="ee658-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="ee658-177">Cela est utile dans les cas où un utilisateur a créé un ordinateur virtuel planifié à la destination, ainsi que la configuration des ressources, et qu’il souhaite qu’un ordinateur virtuel de la source migre vers cet ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="ee658-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ee658-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-181">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee658-181">A display name for the object.</span></span> <span data-ttu-id="ee658-182">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee658-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee658-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="ee658-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-186">Indique s’il faut compresser le trafic de migration dynamique.</span><span class="sxs-lookup"><span data-stu-id="ee658-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="ee658-187">**True** indique la compression ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ee658-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="ee658-188">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ee658-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ee658-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee658-192">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ee658-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ee658-193">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ee658-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ee658-194">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee658-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee658-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="ee658-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee658-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ee658-198">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span><span class="sxs-lookup"><span data-stu-id="ee658-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="ee658-199">Spécifie le type d’opération de migration à effectuer.</span><span class="sxs-lookup"><span data-stu-id="ee658-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="ee658-200">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee658-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee658-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="ee658-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span><span class="sxs-lookup"><span data-stu-id="ee658-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-203">Migre le système virtuel vers l’ordinateur hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="ee658-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Stockage** (32769)</span><span class="sxs-lookup"><span data-stu-id="ee658-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-205">Migre uniquement les ressources de stockage du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ee658-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="ee658-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Intermédiaire** (32770)</span><span class="sxs-lookup"><span data-stu-id="ee658-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-207">À l’aide de la configuration du système virtuel, crée un système virtuel planifié sur l’ordinateur hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="ee658-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span><span class="sxs-lookup"><span data-stu-id="ee658-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-209">Migre le système virtuel et son stockage vers l’ordinateur hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="ee658-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span><span class="sxs-lookup"><span data-stu-id="ee658-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-211">Effectue une vérification de la capacité de migration des ressources de stockage du système virtuel sur l’ordinateur hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee658-212">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="ee658-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee658-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-215">Spécifie le type de transport à appliquer si la valeur de **TransportType** est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="ee658-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="ee658-216">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-217">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ee658-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-218">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee658-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee658-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee658-220">Spécifie l’importance de la migration relative que le système de migration peut utiliser pour commander ou accorder des préférences entre plusieurs demandes de migration en attente.</span><span class="sxs-lookup"><span data-stu-id="ee658-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="ee658-221">Plus la valeur est faible, plus la priorité est élevée.</span><span class="sxs-lookup"><span data-stu-id="ee658-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="ee658-222">Dans une migration, la valeur 0 indique la priorité par défaut.</span><span class="sxs-lookup"><span data-stu-id="ee658-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="ee658-223">Dans le cas contraire, la valeur 0 indique que les priorités ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ee658-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="ee658-224">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-225">**RemoveSourceUnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="ee658-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-226">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-227">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-228">Supprimez les disques durs virtuels non gérés source.</span><span class="sxs-lookup"><span data-stu-id="ee658-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-229">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ee658-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ee658-230">**RetainVhdCopiesOnSource**</span><span class="sxs-lookup"><span data-stu-id="ee658-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee658-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee658-233">Pour une migration de stockage, cette valeur spécifie si les disques durs virtuels en lecture seule sur l’hôte source doivent être supprimés une fois la migration terminée.</span><span class="sxs-lookup"><span data-stu-id="ee658-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="ee658-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-235">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee658-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee658-236">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ee658-237">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="ee658-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="ee658-238">Spécifie le type de transport à appliquer pour une opération de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ee658-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="ee658-239">Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="ee658-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee658-240">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee658-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee658-241">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee658-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="ee658-242">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="ee658-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="ee658-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="ee658-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="ee658-244">**TLS strict** (4)</span><span class="sxs-lookup"><span data-stu-id="ee658-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="ee658-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="ee658-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="ee658-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="ee658-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ee658-247">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ee658-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ee658-248">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="ee658-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="ee658-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ee658-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="ee658-250">Pour la migration en direct, cette propriété spécifie le type de transport à utiliser pour transférer l’état du système virtuel vers l’ordinateur hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="ee658-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="ee658-251">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee658-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="ee658-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="ee658-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-253">Indique le type de transport TCP.</span><span class="sxs-lookup"><span data-stu-id="ee658-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="ee658-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="ee658-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="ee658-255">Indique que le type de transport pour le transfert de l’état de l’ordinateur virtuel est SMB.</span><span class="sxs-lookup"><span data-stu-id="ee658-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee658-256">**UnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="ee658-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee658-257">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ee658-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee658-258">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee658-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ee658-259">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ MoveUnmanagedVhd")</span><span class="sxs-lookup"><span data-stu-id="ee658-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="ee658-260">Tableau d’instances [**MSVM \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) incorporées qui contiennent des informations sur les disques durs virtuels non managés.</span><span class="sxs-lookup"><span data-stu-id="ee658-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="ee658-261">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ee658-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee658-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee658-262">Requirements</span></span>



| <span data-ttu-id="ee658-263">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee658-263">Requirement</span></span> | <span data-ttu-id="ee658-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee658-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee658-265">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee658-265">Minimum supported client</span></span><br/> | <span data-ttu-id="ee658-266">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee658-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee658-267">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee658-267">Minimum supported server</span></span><br/> | <span data-ttu-id="ee658-268">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee658-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee658-269">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee658-269">Namespace</span></span><br/>                | <span data-ttu-id="ee658-270">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ee658-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee658-271">MOF</span><span class="sxs-lookup"><span data-stu-id="ee658-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee658-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee658-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee658-273">DLL</span><span class="sxs-lookup"><span data-stu-id="ee658-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee658-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee658-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee658-275">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee658-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee658-276">**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ee658-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ee658-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="ee658-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


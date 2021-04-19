---
description: Représente la configuration actuelle d’un commutateur Ethernet virtuel.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Classe Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544255"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="94e38-103">MSVM \_ VirtualEthernetSwitchSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="94e38-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="94e38-104">Représente la configuration actuelle d’un commutateur Ethernet virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="94e38-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="94e38-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e38-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94e38-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="94e38-107">Membres</span><span class="sxs-lookup"><span data-stu-id="94e38-107">Members</span></span>

<span data-ttu-id="94e38-108">La classe **MSVM \_ VirtualEthernetSwitchSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="94e38-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="94e38-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94e38-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94e38-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94e38-110">Properties</span></span>

<span data-ttu-id="94e38-111">La classe **MSVM \_ VirtualEthernetSwitchSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="94e38-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94e38-112">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="94e38-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94e38-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94e38-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-115">Liste des pools de ressources hôtes à associer ou actuellement associés au commutateur Ethernet dans le but d’allouer des connexions Ethernet entre un ordinateur virtuel et un commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="94e38-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="94e38-116">Chaque valeur doit être conforme à l’URI WBEM de production \_ \_ UntypedInstancePath tel que défini dans DSP0207.</span><span class="sxs-lookup"><span data-stu-id="94e38-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="94e38-117">Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="94e38-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-118">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="94e38-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94e38-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-121">Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="94e38-122">Dans ce cas, les échecs signifient qu’il s’agit d’une défaillance pouvant être détectée par la plateforme hôte, telle qu’une condition d’état d’attente non interruptible.</span><span class="sxs-lookup"><span data-stu-id="94e38-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="94e38-123">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-124">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="94e38-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94e38-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-127">Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté.</span><span class="sxs-lookup"><span data-stu-id="94e38-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="94e38-128">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-129">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="94e38-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94e38-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-132">Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="94e38-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="94e38-133">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-134">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="94e38-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94e38-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-137">Délai avant le démarrage automatique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="94e38-138">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-139">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="94e38-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94e38-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-142">Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte.</span><span class="sxs-lookup"><span data-stu-id="94e38-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="94e38-143">Un nombre inférieur indique une activation antérieure.</span><span class="sxs-lookup"><span data-stu-id="94e38-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="94e38-144">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-145">**BandwidthReservationMode**</span><span class="sxs-lookup"><span data-stu-id="94e38-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94e38-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="94e38-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e38-148">Mode de réservation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="94e38-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="94e38-149">**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="94e38-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="94e38-150">**Poids** (1)</span><span class="sxs-lookup"><span data-stu-id="94e38-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="94e38-151">**Absolu** (2)</span><span class="sxs-lookup"><span data-stu-id="94e38-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="94e38-152">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="94e38-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94e38-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="94e38-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-156">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="94e38-156">A short description of the object.</span></span> <span data-ttu-id="94e38-157">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du commutateur Ethernet virtuel ».</span><span class="sxs-lookup"><span data-stu-id="94e38-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94e38-158">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="94e38-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-161">Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="94e38-162">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-163">**Fichier ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="94e38-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-166">Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="94e38-167">Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="94e38-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="94e38-168">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="94e38-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-172">Identificateur unique de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="94e38-173">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="94e38-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-175">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94e38-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-177">Date et heure de création des paramètres.</span><span class="sxs-lookup"><span data-stu-id="94e38-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="94e38-178">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e38-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94e38-179">**Description**</span><span class="sxs-lookup"><span data-stu-id="94e38-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-182">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="94e38-182">A description of the object.</span></span> <span data-ttu-id="94e38-183">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres actifs pour le commutateur Ethernet virtuel ».</span><span class="sxs-lookup"><span data-stu-id="94e38-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="94e38-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="94e38-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-187">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="94e38-187">A display name for the object.</span></span> <span data-ttu-id="94e38-188">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e38-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94e38-189">**ExtensionOrder**</span><span class="sxs-lookup"><span data-stu-id="94e38-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-190">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94e38-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94e38-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="94e38-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e38-192">Tableau d’instances incorporées de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représentent les extensions de commutateur liées à ce commutateur, dans l’ordre dans lequel elles sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="94e38-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94e38-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94e38-196">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="94e38-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="94e38-197">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="94e38-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="94e38-198">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».</span><span class="sxs-lookup"><span data-stu-id="94e38-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="94e38-199">**IOVPreferred**</span><span class="sxs-lookup"><span data-stu-id="94e38-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-200">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94e38-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-201">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="94e38-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e38-202">Spécifie si la virtualisation d’e/s de racine unique (SR-IOV) est préférée ou non, si elle est disponible, sur la carte sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="94e38-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-203">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="94e38-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-206">Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="94e38-207">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-208">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="94e38-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-209">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94e38-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-211">Spécifie le nombre maximal d’adresses MAC uniques qui peuvent être appris par le commutateur pour prendre en charge l’apprentissage des adresses MAC, comme défini dans la norme IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="94e38-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="94e38-212">Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="94e38-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-213">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="94e38-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-214">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94e38-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94e38-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-216">Les notes fournies par l’utilisateur sont liées à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="94e38-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="94e38-217">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e38-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94e38-218">**PacketDirectEnabled**</span><span class="sxs-lookup"><span data-stu-id="94e38-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94e38-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="94e38-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e38-221">Spécifie si le PacketDirect doit être utilisé, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="94e38-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="94e38-222">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94e38-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="94e38-223">Cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="94e38-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="94e38-224">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="94e38-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-227">Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="94e38-228">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-229">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="94e38-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-232">Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="94e38-233">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-234">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="94e38-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-237">Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="94e38-238">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-239">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="94e38-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-242">Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94e38-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="94e38-243">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94e38-244">**TeamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="94e38-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94e38-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-246">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="94e38-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94e38-247">Spécifie si l’Association de cartes réseau doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="94e38-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="94e38-248">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94e38-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="94e38-249">Cette propriété a été ajoutée à Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="94e38-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="94e38-250">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="94e38-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-253">Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="94e38-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="94e38-254">Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e38-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94e38-255">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="94e38-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94e38-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94e38-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-258">Spécifie le type de machine virtuelle que les données de paramètre représentent.</span><span class="sxs-lookup"><span data-stu-id="94e38-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="94e38-259">Cette propriété est héritée de [**la \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94e38-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94e38-260">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="94e38-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e38-261">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94e38-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94e38-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94e38-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e38-263">Liste d’identificateurs de réseau local virtuel auxquels ce commutateur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="94e38-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="94e38-264">Cette propriété est héritée de la **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="94e38-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94e38-265">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94e38-265">Requirements</span></span>



| <span data-ttu-id="94e38-266">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94e38-266">Requirement</span></span> | <span data-ttu-id="94e38-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="94e38-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e38-268">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94e38-268">Minimum supported client</span></span><br/> | <span data-ttu-id="94e38-269">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94e38-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94e38-270">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94e38-270">Minimum supported server</span></span><br/> | <span data-ttu-id="94e38-271">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94e38-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94e38-272">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94e38-272">Namespace</span></span><br/>                | <span data-ttu-id="94e38-273">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="94e38-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94e38-274">MOF</span><span class="sxs-lookup"><span data-stu-id="94e38-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94e38-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94e38-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94e38-276">DLL</span><span class="sxs-lookup"><span data-stu-id="94e38-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94e38-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94e38-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


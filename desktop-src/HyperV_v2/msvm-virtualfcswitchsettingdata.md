---
description: Représente la configuration d’un commutateur de Fibre Channel virtuel.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Classe Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525216"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="11590-103">MSVM \_ VirtualFcSwitchSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="11590-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="11590-104">Représente la configuration d’un commutateur de Fibre Channel virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="11590-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="11590-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11590-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11590-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
};
```

## <a name="members"></a><span data-ttu-id="11590-107">Membres</span><span class="sxs-lookup"><span data-stu-id="11590-107">Members</span></span>

<span data-ttu-id="11590-108">La classe **MSVM \_ VirtualFcSwitchSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="11590-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="11590-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11590-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11590-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11590-110">Properties</span></span>

<span data-ttu-id="11590-111">La classe **MSVM \_ VirtualFcSwitchSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="11590-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11590-112">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="11590-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11590-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11590-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-115">Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="11590-116">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-117">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="11590-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11590-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11590-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-120">Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté.</span><span class="sxs-lookup"><span data-stu-id="11590-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="11590-121">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-122">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="11590-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11590-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11590-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-125">Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="11590-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="11590-126">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-127">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="11590-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11590-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11590-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-130">Délai avant le démarrage automatique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="11590-131">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-132">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="11590-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11590-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11590-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-135">Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte.</span><span class="sxs-lookup"><span data-stu-id="11590-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="11590-136">Un nombre inférieur indique une activation antérieure.</span><span class="sxs-lookup"><span data-stu-id="11590-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="11590-137">Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="11590-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="11590-138">La valeur 0 indique que la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="11590-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="11590-139">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="11590-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-143">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11590-143">A short description of the object.</span></span> <span data-ttu-id="11590-144">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="11590-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="11590-145">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11590-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-148">Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="11590-149">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-150">**Fichier ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="11590-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-153">Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="11590-154">Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="11590-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="11590-155">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="11590-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-159">Identificateur unique de la configuration.</span><span class="sxs-lookup"><span data-stu-id="11590-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="11590-160">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="11590-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11590-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11590-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-164">Date et heure de création des paramètres.</span><span class="sxs-lookup"><span data-stu-id="11590-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="11590-165">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="11590-166">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-167">**Description**</span><span class="sxs-lookup"><span data-stu-id="11590-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-170">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="11590-170">A description of the object.</span></span> <span data-ttu-id="11590-171">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="11590-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="11590-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="11590-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-175">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11590-175">A display name for the object.</span></span> <span data-ttu-id="11590-176">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11590-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11590-180">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="11590-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="11590-181">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="11590-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="11590-182">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-183">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11590-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-186">Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="11590-187">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-188">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="11590-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-189">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="11590-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="11590-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-191">Les notes fournies par l’utilisateur sont liées à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="11590-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="11590-192">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-193">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="11590-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-196">Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="11590-197">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-198">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11590-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-201">Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="11590-202">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-203">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11590-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-206">Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="11590-207">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-208">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11590-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-211">Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="11590-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="11590-212">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="11590-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11590-213">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="11590-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-216">Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="11590-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="11590-217">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11590-218">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="11590-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11590-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11590-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11590-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11590-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11590-221">Spécifie le type de machine virtuelle que les données de paramètre représentent.</span><span class="sxs-lookup"><span data-stu-id="11590-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="11590-222">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="11590-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11590-223">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11590-223">Requirements</span></span>



| <span data-ttu-id="11590-224">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11590-224">Requirement</span></span> | <span data-ttu-id="11590-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="11590-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11590-226">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11590-226">Minimum supported client</span></span><br/> | <span data-ttu-id="11590-227">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11590-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="11590-228">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11590-228">Minimum supported server</span></span><br/> | <span data-ttu-id="11590-229">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11590-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11590-230">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11590-230">Namespace</span></span><br/>                | <span data-ttu-id="11590-231">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="11590-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="11590-232">MOF</span><span class="sxs-lookup"><span data-stu-id="11590-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11590-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11590-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11590-234">DLL</span><span class="sxs-lookup"><span data-stu-id="11590-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11590-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11590-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


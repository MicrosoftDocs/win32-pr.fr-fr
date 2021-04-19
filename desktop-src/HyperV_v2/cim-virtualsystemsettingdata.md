---
description: Décrit les aspects virtuels d’un système virtuel via un ensemble de propriétés spécifiques à la virtualisation. \_Le VIRTUALSYSTEMSETTINGDATA CIM est également utilisé comme classe de niveau supérieur des configurations du système virtuel.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Classe CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535483"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="c5453-104">\_Classe CIM VirtualSystemSettingData</span><span class="sxs-lookup"><span data-stu-id="c5453-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="c5453-105">Décrit les aspects virtuels d’un système virtuel via un ensemble de propriétés spécifiques à la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="c5453-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="c5453-106">**CIM \_ VirtualSystemSettingData** est également utilisé comme classe de niveau supérieur des configurations du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5453-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5453-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
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

## <a name="members"></a><span data-ttu-id="c5453-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c5453-108">Members</span></span>

<span data-ttu-id="c5453-109">La classe **CIM \_ VirtualSystemSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c5453-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c5453-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c5453-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5453-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c5453-111">Properties</span></span>

<span data-ttu-id="c5453-112">La classe **CIM \_ VirtualSystemSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5453-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5453-113">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="c5453-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5453-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-116">Action à entreprendre pour le système virtuel lorsque le logiciel exécuté par le système virtuel échoue.</span><span class="sxs-lookup"><span data-stu-id="c5453-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="c5453-117">Les échecs résolus par cette propriété incluent uniquement ceux qui sont détectables par la plateforme hôte, tels qu’une condition d’état d’attente non interruptible.</span><span class="sxs-lookup"><span data-stu-id="c5453-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="c5453-118">**Aucun** (2)</span><span class="sxs-lookup"><span data-stu-id="c5453-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="c5453-119">**Redémarrer** (3)</span><span class="sxs-lookup"><span data-stu-id="c5453-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="c5453-120">**Revenir à l’instantané** (4)</span><span class="sxs-lookup"><span data-stu-id="c5453-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5453-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c5453-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5453-122">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="c5453-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5453-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-125">Action à entreprendre pour le système virtuel lorsque l’ordinateur hôte est arrêté.</span><span class="sxs-lookup"><span data-stu-id="c5453-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="c5453-126">**Désactiver** (2)</span><span class="sxs-lookup"><span data-stu-id="c5453-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="c5453-127">**Enregistrer l’État** (3)</span><span class="sxs-lookup"><span data-stu-id="c5453-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="c5453-128">**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="c5453-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5453-129">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c5453-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5453-130">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="c5453-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5453-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-133">Action à effectuer sur le système virtuel au démarrage de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c5453-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="c5453-134">**Aucun** (2)</span><span class="sxs-lookup"><span data-stu-id="c5453-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="c5453-135">**Redémarrer si précédemment actif** (3)</span><span class="sxs-lookup"><span data-stu-id="c5453-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="c5453-136">**Toujours démarrer** (4)</span><span class="sxs-lookup"><span data-stu-id="c5453-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5453-137">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c5453-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5453-138">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="c5453-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-139">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5453-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-141">Délai de l’action de démarrage.</span><span class="sxs-lookup"><span data-stu-id="c5453-141">The delay for the startup action.</span></span> <span data-ttu-id="c5453-142">Cette valeur est une variante d’intervalle du type de données **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c5453-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-143">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c5453-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5453-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-146">Numéro de séquence pour l’activation du système virtuel lorsque le système hôte est démarré.</span><span class="sxs-lookup"><span data-stu-id="c5453-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="c5453-147">Un nombre inférieur indique une activation antérieure.</span><span class="sxs-lookup"><span data-stu-id="c5453-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="c5453-148">Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c5453-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="c5453-149">La valeur « 0 » indique que la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c5453-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-150">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c5453-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-153">Chemin d’accès du répertoire dans lequel sont stockées les informations relatives à la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="c5453-154">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-155">**Fichier ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="c5453-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-158">Chemin d’accès relatif du fichier dans lequel sont stockées les informations relatives à la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="c5453-159">Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c5453-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c5453-160">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="c5453-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-164">ID unique de la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="c5453-165">**ConfigurationID** est différent de l' **InstanceID** et est assigné par l’implémentation à un système virtuel ou à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="c5453-166">**ConfigurationID** n’est pas une clé, et la même valeur peut se produire pour plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="c5453-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="c5453-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="c5453-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-168">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5453-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-170">Date et heure de création de la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-171">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c5453-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-174">Chemin d’accès relatif du répertoire où sont stockées les informations de journalisation du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="c5453-175">Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c5453-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c5453-176">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-177">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c5453-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-178">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c5453-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5453-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-180">Tableau qui contient les notes fournies par l’utilisateur qui sont liées au système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-181">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="c5453-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-184">Chemin d’accès du fichier dans lequel sont stockées les informations relatives à la récupération du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="c5453-185">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-186">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c5453-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-189">Chemin d’accès relatif du répertoire où sont stockées les informations sur les instantanés de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="c5453-190">Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c5453-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c5453-191">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-192">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c5453-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-195">Chemin d’accès relatif du répertoire dans lequel sont stockées les informations relatives à l’interruption du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="c5453-196">Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c5453-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c5453-197">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-198">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c5453-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-201">Chemin d’accès relatif du répertoire où sont stockés les fichiers d’échange du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="c5453-202">Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c5453-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c5453-203">Le format de cette propriété est un URI basé sur la norme RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="c5453-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-204">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="c5453-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-207">Nom unique du système au sein de la plateforme de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="c5453-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="c5453-208">**Attribut virtualsystemidentifier** n’est pas le nom d’hôte affecté à l’instance de système d’exploitation en cours d’exécution dans le système virtuel, et il ne s’agit pas d’une adresse IP ou d’une adresse Mac affectée à l’un de ses ports réseau.</span><span class="sxs-lookup"><span data-stu-id="c5453-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="c5453-209">Le **attribut virtualsystemidentifier** peut contenir des règles spécifiques d’implémentation, comme des modèles simples ou une expression régulière qui peut être interprétée par l’implémentation lors de la définition de **attribut virtualsystemidentifier**.</span><span class="sxs-lookup"><span data-stu-id="c5453-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="c5453-210">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="c5453-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5453-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c5453-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5453-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5453-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5453-213">Type du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="c5453-214">Si le type de système virtuel est inconnu, cette valeur doit être définie sur « DMTF : Unknown ».</span><span class="sxs-lookup"><span data-stu-id="c5453-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="c5453-215">Cette propriété est mise en forme à l’aide du format de ABNF (Backus Naur Form) augmenté suivant :</span><span class="sxs-lookup"><span data-stu-id="c5453-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="c5453-216">vs-type = DMTF-value/Other-org-value/Legacy-value ; DMTF-value = "DMTF :" Defining-org " :" org-vs-type ; Other-org-value = définition-org " :" org-vs-type ;</span><span class="sxs-lookup"><span data-stu-id="c5453-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="c5453-217">La valeur du format ABNF ci-dessus est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c5453-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="c5453-218">*DMTF-valeur*   une valeur de propriété définie par DMTF et est définie dans la description de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c5453-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="c5453-219">*other-org-value*   est une valeur de propriété définie par une entité commerciale autre que DMTF et n’est pas définie dans la description de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c5453-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="c5453-220">*valeur héritée*   une valeur de propriété définie par une entité métier autre que DMTF et n’est pas définie dans la description de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c5453-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="c5453-221">Ces valeurs sont autorisées, mais elles sont recommandées pour être dépréciées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="c5453-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="c5453-222">*définition-org*   identificateur de l’entité métier qui définit le type de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5453-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="c5453-223">Il doit inclure un nom de droits d’auteur, de marque déposée ou unique qui appartient à l’entité métier.</span><span class="sxs-lookup"><span data-stu-id="c5453-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="c5453-224">Il ne doit pas être « DMTF » et ne doit pas contenir de deux-points.</span><span class="sxs-lookup"><span data-stu-id="c5453-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="c5453-225">*org-vs-tapez*   un identificateur pour le type de système virtuel au sein de l’entité métier de définition.</span><span class="sxs-lookup"><span data-stu-id="c5453-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="c5453-226">Elle doit être unique au sein de la définition-org. org-vs-type peut utiliser n’importe quel caractère autorisé pour les chaînes CIM, à l’exception des suivantes : U0000-U001F (contrôles C0 Unicode), U0020 (Space), U007F (contrôles Unicode C0) ou U0080-U009F (contrôles C1 Unicode).</span><span class="sxs-lookup"><span data-stu-id="c5453-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="c5453-227">S’il est nécessaire de structurer la valeur en segments, les segments doivent être séparés par un seul signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="c5453-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="c5453-228">Les valeurs de cette propriété doivent être traitées en respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="c5453-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="c5453-229">Ils sont destinés à être traités par programmation, au lieu d’être un nom complet, et doivent être courts.</span><span class="sxs-lookup"><span data-stu-id="c5453-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5453-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5453-230">Requirements</span></span>



| <span data-ttu-id="c5453-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5453-231">Requirement</span></span> | <span data-ttu-id="c5453-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5453-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5453-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5453-233">Minimum supported client</span></span><br/> | <span data-ttu-id="c5453-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5453-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c5453-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5453-235">Minimum supported server</span></span><br/> | <span data-ttu-id="c5453-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5453-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c5453-237">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c5453-237">Namespace</span></span><br/>                | <span data-ttu-id="c5453-238">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5453-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5453-239">MOF</span><span class="sxs-lookup"><span data-stu-id="c5453-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5453-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5453-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5453-241">DLL</span><span class="sxs-lookup"><span data-stu-id="c5453-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5453-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5453-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5453-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5453-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5453-244">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c5453-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 





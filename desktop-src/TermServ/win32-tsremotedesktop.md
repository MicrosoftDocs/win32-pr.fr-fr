---
title: Classe Win32_TSRemoteDesktop
description: Décrit une connexion Bureau à distance qui est disponible via Bureau à distance Accès web (RD Accès web).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteDesktop de la classe Services Bureau à distance
- Win32_TSRemoteDesktop de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103005"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="5b1df-105">\_Classe TSRemoteDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="5b1df-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="5b1df-106">Décrit une connexion Bureau à distance qui est disponible via Bureau à distance Accès web (RD Accès web).</span><span class="sxs-lookup"><span data-stu-id="5b1df-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1df-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b1df-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="5b1df-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5b1df-108">Members</span></span>

<span data-ttu-id="5b1df-109">La classe **Win32 \_ TSRemoteDesktop** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b1df-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="5b1df-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b1df-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b1df-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b1df-111">Properties</span></span>

<span data-ttu-id="5b1df-112">La classe **Win32 \_ TSRemoteDesktop** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5b1df-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b1df-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5b1df-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-116">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="5b1df-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-117">Alias de la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5b1df-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b1df-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-122">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5b1df-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b1df-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="5b1df-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-127">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-127">Description of the object.</span></span>

<span data-ttu-id="5b1df-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b1df-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-129">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="5b1df-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-130">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="5b1df-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-132">Contenu en octets de l’icône qui correspond à la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-133">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="5b1df-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-134">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b1df-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-136">L’index ou l’ID de l’icône pour la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="5b1df-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-140">Chemin d’accès de l’icône pour la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5b1df-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-142">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b1df-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-144">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5b1df-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-145">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="5b1df-145">The date the object was installed.</span></span> <span data-ttu-id="5b1df-146">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="5b1df-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5b1df-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b1df-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-148">**IsVmFarm**</span><span class="sxs-lookup"><span data-stu-id="5b1df-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-149">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b1df-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-151">Indique si cette connexion Bureau à distance fait partie d’une batterie de serveurs de machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="5b1df-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5b1df-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-155">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-155">The name of the object.</span></span>

<span data-ttu-id="5b1df-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b1df-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-157">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="5b1df-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-160">Contenu du fichier RDP qui correspond à la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5b1df-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-164">Descripteur de sécurité qui contrôle l’accès à la connexion Bureau à distance, au format SDDL.</span><span class="sxs-lookup"><span data-stu-id="5b1df-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="5b1df-165">Une chaîne vide implique l’autorisation tous les accès.</span><span class="sxs-lookup"><span data-stu-id="5b1df-165">An empty string implies allow all access.</span></span> <span data-ttu-id="5b1df-166">Ce descripteur de sécurité ne prend pas en charge les ACE de refus ou les ACE qui font référence à des utilisateurs ou des groupes qui n’ont pas de domaine.</span><span class="sxs-lookup"><span data-stu-id="5b1df-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-167">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="5b1df-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b1df-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-170">Indique si la connexion Bureau à distance doit être affichée dans les Accès web RD.</span><span class="sxs-lookup"><span data-stu-id="5b1df-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="5b1df-171">**État**</span><span class="sxs-lookup"><span data-stu-id="5b1df-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b1df-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-174">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5b1df-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-175">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-175">Current status of the object.</span></span> <span data-ttu-id="5b1df-176">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="5b1df-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5b1df-177">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="5b1df-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5b1df-178">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5b1df-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5b1df-179">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5b1df-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5b1df-180">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5b1df-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5b1df-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b1df-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5b1df-182">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-183">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-184">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-185">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="5b1df-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-186">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-187">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-188">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b1df-189">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="5b1df-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b1df-190">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="5b1df-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b1df-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b1df-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b1df-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b1df-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b1df-193">Paramètres de la batterie de machines virtuelles pour la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5b1df-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b1df-194">Notes</span><span class="sxs-lookup"><span data-stu-id="5b1df-194">Remarks</span></span>

<span data-ttu-id="5b1df-195">Vous devez être membre du groupe administrateurs pour définir des propriétés à l’aide de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5b1df-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="5b1df-196">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5b1df-197">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="5b1df-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="5b1df-198">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="5b1df-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5b1df-199">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="5b1df-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5b1df-200">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5b1df-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5b1df-201">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5b1df-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5b1df-202">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5b1df-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5b1df-203">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5b1df-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1df-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b1df-204">Requirements</span></span>



| <span data-ttu-id="5b1df-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b1df-205">Requirement</span></span> | <span data-ttu-id="5b1df-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b1df-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1df-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b1df-207">Minimum supported client</span></span><br/> | <span data-ttu-id="5b1df-208">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b1df-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5b1df-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b1df-209">Minimum supported server</span></span><br/> | <span data-ttu-id="5b1df-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b1df-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b1df-211">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b1df-211">Namespace</span></span><br/>                | <span data-ttu-id="5b1df-212">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5b1df-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5b1df-213">MOF</span><span class="sxs-lookup"><span data-stu-id="5b1df-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b1df-214"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b1df-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5b1df-215">DLL</span><span class="sxs-lookup"><span data-stu-id="5b1df-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b1df-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b1df-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


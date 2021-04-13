---
title: Classe Win32_RDCentralPublishedRemoteDesktop
description: Desktop publié sur un autre ordinateur, pour une utilisation à distance via les services Terminal Server.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteDesktop de la classe Services Bureau à distance
- Win32_RDCentralPublishedRemoteDesktop de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464970"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="2ca58-105">\_Classe RDCentralPublishedRemoteDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="2ca58-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="2ca58-106">Desktop publié sur un autre ordinateur, pour une utilisation à distance via les services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="2ca58-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="2ca58-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2ca58-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca58-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ca58-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="2ca58-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2ca58-109">Members</span></span>

<span data-ttu-id="2ca58-110">La classe **Win32 \_ RDCentralPublishedRemoteDesktop** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2ca58-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="2ca58-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ca58-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ca58-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ca58-112">Properties</span></span>

<span data-ttu-id="2ca58-113">La classe **Win32 \_ RDCentralPublishedRemoteDesktop** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2ca58-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ca58-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="2ca58-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ca58-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ca58-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-118">Alias du bureau.</span><span class="sxs-lookup"><span data-stu-id="2ca58-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2ca58-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2ca58-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-123">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ca58-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2ca58-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2ca58-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ca58-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-128">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ca58-128">Description of the object.</span></span>

<span data-ttu-id="2ca58-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2ca58-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-130">**Dossiers**</span><span class="sxs-lookup"><span data-stu-id="2ca58-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-131">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2ca58-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ca58-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-133">Liste des dossiers dans lesquels cette ressource doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="2ca58-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-134">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="2ca58-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-135">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2ca58-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ca58-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-137">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ca58-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-138">Contenu de l’icône correspondant à l’application.</span><span class="sxs-lookup"><span data-stu-id="2ca58-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2ca58-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2ca58-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-142">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2ca58-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-143">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2ca58-143">The date the object was installed.</span></span> <span data-ttu-id="2ca58-144">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2ca58-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2ca58-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2ca58-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2ca58-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-149">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2ca58-149">The name of the object.</span></span>

<span data-ttu-id="2ca58-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2ca58-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-151">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="2ca58-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ca58-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-154">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ca58-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-155">Alias de la batterie de serveurs qui a publié le bureau.</span><span class="sxs-lookup"><span data-stu-id="2ca58-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-156">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="2ca58-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-159">Contenu du fichier RDP correspondant au bureau.</span><span class="sxs-lookup"><span data-stu-id="2ca58-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-160">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="2ca58-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-161">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2ca58-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2ca58-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-163">**true** si cette application doit être affichée dans le accès Web TS ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2ca58-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2ca58-164">**État**</span><span class="sxs-lookup"><span data-stu-id="2ca58-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca58-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ca58-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ca58-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca58-167">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2ca58-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2ca58-168">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ca58-168">Current status of the object.</span></span> <span data-ttu-id="2ca58-169">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="2ca58-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2ca58-170">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="2ca58-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2ca58-171">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2ca58-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2ca58-172">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2ca58-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2ca58-173">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2ca58-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2ca58-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2ca58-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2ca58-175">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-176">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-177">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-178">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="2ca58-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-179">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-180">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-181">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2ca58-182">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="2ca58-182">("Service")</span></span>


<span data-ttu-id="2ca58-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2ca58-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2ca58-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ca58-184">Requirements</span></span>



| <span data-ttu-id="2ca58-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ca58-185">Requirement</span></span> | <span data-ttu-id="2ca58-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ca58-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca58-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ca58-187">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca58-188">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ca58-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2ca58-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ca58-189">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca58-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ca58-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="2ca58-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ca58-191">Namespace</span></span><br/>                | <span data-ttu-id="2ca58-192">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2ca58-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2ca58-193">MOF</span><span class="sxs-lookup"><span data-stu-id="2ca58-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ca58-194"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ca58-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2ca58-195">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca58-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca58-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca58-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 


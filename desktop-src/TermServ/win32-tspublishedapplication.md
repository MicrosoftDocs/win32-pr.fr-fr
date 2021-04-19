---
title: Classe Win32_TSPublishedApplication
description: Définit les applications qui sont disponibles pour une utilisation à distance par le biais de Windows Server 2008 R2 RemoteApp.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplication de la classe Services Bureau à distance
- Win32_TSPublishedApplication de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509710"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="7097b-105">\_Classe TSPublishedApplication Win32</span><span class="sxs-lookup"><span data-stu-id="7097b-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="7097b-106">Définit les applications qui sont disponibles pour une utilisation à distance par le biais de Windows Server 2008 R2 RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7097b-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="7097b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7097b-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="7097b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7097b-108">Members</span></span>

<span data-ttu-id="7097b-109">La classe **Win32 \_ TSPublishedApplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7097b-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="7097b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7097b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7097b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7097b-111">Properties</span></span>

<span data-ttu-id="7097b-112">La classe **Win32 \_ TSPublishedApplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7097b-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7097b-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="7097b-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7097b-116">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="7097b-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7097b-117">Alias de l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-117">The alias of the application.</span></span> <span data-ttu-id="7097b-118">L’alias est un identificateur unique pour le programme qui correspond par défaut au nom de fichier du programme (sans l’extension).</span><span class="sxs-lookup"><span data-stu-id="7097b-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="7097b-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7097b-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7097b-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7097b-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7097b-123">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7097b-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="7097b-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7097b-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7097b-125">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="7097b-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7097b-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-128">Paramètre des arguments de ligne de commande pour l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="7097b-129">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="7097b-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="7097b-130">0</span><span class="sxs-lookup"><span data-stu-id="7097b-130">0</span></span>
</dt> <dd>

<span data-ttu-id="7097b-131">N’autorisez pas les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7097b-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-132">1</span><span class="sxs-lookup"><span data-stu-id="7097b-132">1</span></span>
</dt> <dd>

<span data-ttu-id="7097b-133">Autorisez tous les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7097b-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-134">2</span><span class="sxs-lookup"><span data-stu-id="7097b-134">2</span></span>
</dt> <dd>

<span data-ttu-id="7097b-135">Utilisez toujours les arguments de ligne de commande requis (spécifiés dans **RequiredCommandLine**).</span><span class="sxs-lookup"><span data-stu-id="7097b-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7097b-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="7097b-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7097b-139">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7097b-139">Description of the object.</span></span>

<span data-ttu-id="7097b-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7097b-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7097b-141">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="7097b-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-142">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7097b-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7097b-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7097b-144">Contenu en octets de l’icône qui correspond à l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-145">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="7097b-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-146">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7097b-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-148">Index ou ID de l’icône.</span><span class="sxs-lookup"><span data-stu-id="7097b-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="7097b-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-152">Chemin d’accès de l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7097b-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-154">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7097b-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7097b-156">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="7097b-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="7097b-157">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="7097b-157">The date the object was installed.</span></span> <span data-ttu-id="7097b-158">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="7097b-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7097b-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7097b-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7097b-160">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7097b-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7097b-163">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="7097b-163">The name of the object.</span></span>

<span data-ttu-id="7097b-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7097b-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7097b-165">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="7097b-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-168">Chemin d'accès de l'application.</span><span class="sxs-lookup"><span data-stu-id="7097b-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-169">**PathExists**</span><span class="sxs-lookup"><span data-stu-id="7097b-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7097b-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7097b-172">Indique si le chemin d’accès de l’application est valide.</span><span class="sxs-lookup"><span data-stu-id="7097b-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-173">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="7097b-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-176">Contenu du fichier RDP qui correspond à l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-177">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="7097b-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-180">Arguments de ligne de commande requis pour l’application.</span><span class="sxs-lookup"><span data-stu-id="7097b-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7097b-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-184">Descripteur de sécurité qui contrôle l’accès à l’application, au format SDDL.</span><span class="sxs-lookup"><span data-stu-id="7097b-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="7097b-185">Une chaîne vide implique l’autorisation tous les accès.</span><span class="sxs-lookup"><span data-stu-id="7097b-185">An empty string implies allow all access.</span></span> <span data-ttu-id="7097b-186">Ce descripteur de sécurité ne prend pas en charge les ACE de refus ou les ACE qui font référence à des utilisateurs ou des groupes qui n’ont pas de domaine.</span><span class="sxs-lookup"><span data-stu-id="7097b-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-187">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="7097b-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-188">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7097b-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-189">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-190">Indique si l’application doit être affichée dans la Accès web des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7097b-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="7097b-191">**État**</span><span class="sxs-lookup"><span data-stu-id="7097b-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7097b-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7097b-194">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="7097b-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="7097b-195">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7097b-195">Current status of the object.</span></span> <span data-ttu-id="7097b-196">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="7097b-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7097b-197">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="7097b-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7097b-198">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="7097b-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7097b-199">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="7097b-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7097b-200">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="7097b-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7097b-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7097b-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="7097b-202">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="7097b-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-203">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="7097b-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-204">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="7097b-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-205">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="7097b-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-206">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="7097b-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-207">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="7097b-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-208">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="7097b-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7097b-209">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="7097b-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7097b-210">**VPath**</span><span class="sxs-lookup"><span data-stu-id="7097b-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7097b-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7097b-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7097b-212">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7097b-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7097b-213">Chemin d’accès virtuel de l’application, c’est-à-dire le chemin d’accès avec les variables d’environnement incluses.</span><span class="sxs-lookup"><span data-stu-id="7097b-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7097b-214">Notes</span><span class="sxs-lookup"><span data-stu-id="7097b-214">Remarks</span></span>

<span data-ttu-id="7097b-215">Vous devez être membre du groupe administrateurs pour définir des propriétés à l’aide de cette classe.</span><span class="sxs-lookup"><span data-stu-id="7097b-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="7097b-216">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="7097b-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="7097b-217">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="7097b-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="7097b-218">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="7097b-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="7097b-219">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="7097b-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="7097b-220">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7097b-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7097b-221">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7097b-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7097b-222">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7097b-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7097b-223">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7097b-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7097b-224">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7097b-224">Requirements</span></span>



| <span data-ttu-id="7097b-225">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7097b-225">Requirement</span></span> | <span data-ttu-id="7097b-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="7097b-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7097b-227">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7097b-227">Minimum supported client</span></span><br/> | <span data-ttu-id="7097b-228">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7097b-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7097b-229">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7097b-229">Minimum supported server</span></span><br/> | <span data-ttu-id="7097b-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7097b-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7097b-231">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7097b-231">Namespace</span></span><br/>                | <span data-ttu-id="7097b-232">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7097b-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7097b-233">MOF</span><span class="sxs-lookup"><span data-stu-id="7097b-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7097b-234"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7097b-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="7097b-235">DLL</span><span class="sxs-lookup"><span data-stu-id="7097b-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7097b-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7097b-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


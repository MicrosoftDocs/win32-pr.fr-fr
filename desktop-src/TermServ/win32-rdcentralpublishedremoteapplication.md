---
title: Classe Win32_RDCentralPublishedRemoteApplication
description: Décrit une application publiée sur un autre ordinateur, pour une utilisation à distance par le biais des services Terminal Server.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteApplication de la classe Services Bureau à distance
- Win32_RDCentralPublishedRemoteApplication de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941992"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="7b6ac-105">\_Classe RDCentralPublishedRemoteApplication Win32</span><span class="sxs-lookup"><span data-stu-id="7b6ac-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="7b6ac-106">Décrit une application publiée sur un autre ordinateur, pour une utilisation à distance par le biais des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="7b6ac-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b6ac-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="7b6ac-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7b6ac-109">Members</span></span>

<span data-ttu-id="7b6ac-110">La classe **Win32 \_ RDCentralPublishedRemoteApplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b6ac-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="7b6ac-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b6ac-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b6ac-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b6ac-112">Properties</span></span>

<span data-ttu-id="7b6ac-113">La classe **Win32 \_ RDCentralPublishedRemoteApplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b6ac-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-118">Alias de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-122">AppID est utilisé pour l’épinglage sur les clients.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-126">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-127">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="7b6ac-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-129">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-132">Indique si des arguments de ligne de commande sont requis pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="7b6ac-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7b6ac-134">Ne pas autoriser</span><span class="sxs-lookup"><span data-stu-id="7b6ac-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="7b6ac-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Autoriser** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="7b6ac-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Exiger** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6ac-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-140">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-140">Description of the object.</span></span>

<span data-ttu-id="7b6ac-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-142">**Dossiers**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-143">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-145">Liste des dossiers dans lesquels cette ressource doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-146">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-147">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-149">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-150">Contenu de l’icône correspondant à l’application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-152">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-154">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="7b6ac-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-155">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-155">The date the object was installed.</span></span> <span data-ttu-id="7b6ac-156">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7b6ac-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-161">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-161">The name of the object.</span></span>

<span data-ttu-id="7b6ac-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-163">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-166">Chemin d’accès à l’application</span><span class="sxs-lookup"><span data-stu-id="7b6ac-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-167">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-170">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-171">Alias de la batterie de serveurs qui a publié l’application</span><span class="sxs-lookup"><span data-stu-id="7b6ac-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-172">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-175">Contenu du fichier RDP correspondant à l’application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-176">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-179">Arguments de ligne de commande requis pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-183">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-184">Descripteur de sécurité contrôlant l’accès à l’application, au format SDDL.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="7b6ac-185">Une chaîne vide implique l’autorisation tous les accès.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-186">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-187">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-189">**true** si cette application doit être affichée dans le accès Web TS ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7b6ac-190">**État**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b6ac-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-193">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-194">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-194">Current status of the object.</span></span> <span data-ttu-id="7b6ac-195">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7b6ac-196">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7b6ac-197">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="7b6ac-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7b6ac-198">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7b6ac-199">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7b6ac-200">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ac-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="7b6ac-201">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-202">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-203">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-204">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="7b6ac-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-205">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-206">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-207">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7b6ac-208">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="7b6ac-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6ac-209">**VPath**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ac-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b6ac-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ac-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b6ac-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7b6ac-212">Chemin d’accès virtuel à l’application.</span><span class="sxs-lookup"><span data-stu-id="7b6ac-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b6ac-213">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b6ac-213">Requirements</span></span>



| <span data-ttu-id="7b6ac-214">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b6ac-214">Requirement</span></span> | <span data-ttu-id="7b6ac-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b6ac-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6ac-216">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b6ac-216">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6ac-217">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b6ac-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7b6ac-218">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b6ac-218">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6ac-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b6ac-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="7b6ac-220">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b6ac-220">Namespace</span></span><br/>                | <span data-ttu-id="7b6ac-221">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7b6ac-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7b6ac-222">MOF</span><span class="sxs-lookup"><span data-stu-id="7b6ac-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b6ac-223"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b6ac-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="7b6ac-224">DLL</span><span class="sxs-lookup"><span data-stu-id="7b6ac-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b6ac-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b6ac-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 


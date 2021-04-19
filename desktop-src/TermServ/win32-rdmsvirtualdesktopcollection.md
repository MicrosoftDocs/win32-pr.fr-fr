---
title: Classe Win32_RDMSVirtualDesktopCollection
description: Crée et gère une collection de bureaux virtuels.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509711"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="167d3-105">\_Classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="167d3-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="167d3-106">Crée et gère une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="167d3-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="167d3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="167d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="167d3-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="167d3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="167d3-109">Members</span></span>

<span data-ttu-id="167d3-110">La classe **Win32 \_ RDMSVirtualDesktopCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="167d3-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="167d3-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="167d3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="167d3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="167d3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="167d3-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="167d3-113">Methods</span></span>

<span data-ttu-id="167d3-114">La classe **Win32 \_ RDMSVirtualDesktopCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="167d3-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="167d3-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="167d3-115">Method</span></span>                                                                                            | <span data-ttu-id="167d3-116">Description</span><span class="sxs-lookup"><span data-stu-id="167d3-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="167d3-117">**AddVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="167d3-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="167d3-118">Ajoute un bureau virtuel à une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="167d3-119">**CancelPatch**</span><span class="sxs-lookup"><span data-stu-id="167d3-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="167d3-120">Annule un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="167d3-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="167d3-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="167d3-122">Récupère une valeur de propriété entière à partir d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="167d3-123">**GetPatchProperties**</span><span class="sxs-lookup"><span data-stu-id="167d3-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="167d3-124">Récupère les propriétés d’un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="167d3-125">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="167d3-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="167d3-126">Récupère une valeur de propriété de type chaîne à partir d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="167d3-127">**ProvisioningEnumerateJobs**</span><span class="sxs-lookup"><span data-stu-id="167d3-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="167d3-128">Énumère les tâches de provisionnement de bureau virtuel pour ce service.</span><span class="sxs-lookup"><span data-stu-id="167d3-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="167d3-129">**ProvisioningJobCancel**</span><span class="sxs-lookup"><span data-stu-id="167d3-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="167d3-130">Annule un travail d’approvisionnement de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="167d3-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="167d3-131">**ProvisioningJobExecute**</span><span class="sxs-lookup"><span data-stu-id="167d3-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="167d3-132">Exécute un travail d’approvisionnement de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="167d3-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="167d3-133">**ProvisioningJobGetReport**</span><span class="sxs-lookup"><span data-stu-id="167d3-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="167d3-134">Obtient un rapport sur l’état d’un travail d’approvisionnement de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="167d3-135">**ProvisioningPrepJob**</span><span class="sxs-lookup"><span data-stu-id="167d3-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="167d3-136">Crée un travail d’approvisionnement de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="167d3-137">**RemoveVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="167d3-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="167d3-138">Supprime un bureau virtuel d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="167d3-139">**SchedulePatch**</span><span class="sxs-lookup"><span data-stu-id="167d3-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="167d3-140">Planifie un travail d’approvisionnement des mises à jour logicielles qui installe les mises à jour logicielles sur les machines virtuelles d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="167d3-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="167d3-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="167d3-142">Met à jour une valeur de propriété entière d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="167d3-143">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="167d3-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="167d3-144">Met à jour une valeur de propriété de type chaîne d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="167d3-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="167d3-145">Propriétés</span><span class="sxs-lookup"><span data-stu-id="167d3-145">Properties</span></span>

<span data-ttu-id="167d3-146">La classe **Win32 \_ RDMSVirtualDesktopCollection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="167d3-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="167d3-147">**Alias**</span><span class="sxs-lookup"><span data-stu-id="167d3-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-150">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="167d3-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-151">Obtient ou définit l’alias de la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="167d3-152">**CollectionDescription**</span><span class="sxs-lookup"><span data-stu-id="167d3-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-155">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="167d3-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-156">Obtient ou définit la description de la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="167d3-157">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="167d3-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-158">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="167d3-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="167d3-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-160">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="167d3-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-161">Obtient ou définit un tableau de valeurs qui spécifient des icônes pour la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-162">**IsHA**</span><span class="sxs-lookup"><span data-stu-id="167d3-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-163">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="167d3-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-165">Obtient ou définit une valeur qui indique si la collection contient des machines virtuelles à haut niveau de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="167d3-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="167d3-166">**True** si la collection contient des machines virtuelles à haut niveau de disponibilité ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="167d3-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="167d3-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="167d3-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-170">Obtient ou définit une valeur qui indique si la collection est managée.</span><span class="sxs-lookup"><span data-stu-id="167d3-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="167d3-171">**True** si la collection est managée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="167d3-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-172">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="167d3-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-173">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="167d3-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-175">Obtient ou définit une valeur qui indique si un utilisateur est un administrateur sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="167d3-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="167d3-176">**True** si l’utilisateur est un administrateur sur une machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="167d3-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-177">**Nom**</span><span class="sxs-lookup"><span data-stu-id="167d3-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-180">Obtient ou définit le nom de la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-181">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="167d3-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-182">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="167d3-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-184">Obtient ou définit une valeur qui indique si une machine virtuelle a été déployée avec un instantané de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="167d3-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="167d3-185">**True** si la machine virtuelle a été déployée avec un instantané de machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="167d3-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="167d3-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-189">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="167d3-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-190">Obtient ou définit un descripteur de sécurité au format SSDL qui contrôle l’accès à la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-191">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="167d3-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-192">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="167d3-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-194">Obtient ou définit une valeur qui indique si la collection est affichée dans les Accès web Terminal Services (TS Accès web).</span><span class="sxs-lookup"><span data-stu-id="167d3-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="167d3-195">**True** pour afficher la collection dans les accès Web TS ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="167d3-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-196">**Type**</span><span class="sxs-lookup"><span data-stu-id="167d3-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="167d3-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="167d3-199">Obtient ou définit une valeur qui indique le type des sessions d’ordinateur virtuel hébergées par la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="167d3-200">Cette propriété contient l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="167d3-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="167d3-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="167d3-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="167d3-202">Machines virtuelles temporaires.</span><span class="sxs-lookup"><span data-stu-id="167d3-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="167d3-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="167d3-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="167d3-204">Machines virtuelles créées manuellement.</span><span class="sxs-lookup"><span data-stu-id="167d3-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="167d3-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="167d3-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="167d3-206">Machines virtuelles générées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="167d3-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="167d3-207">**UserVHDSetting**</span><span class="sxs-lookup"><span data-stu-id="167d3-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-209">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-210">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="167d3-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-211">Obtient ou définit le paramètre VHD des données utilisateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="167d3-212">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="167d3-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="167d3-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="167d3-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="167d3-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="167d3-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="167d3-215">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="167d3-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="167d3-216">Obtient ou définit les paramètres de bureau pour les machines virtuelles de la collection.</span><span class="sxs-lookup"><span data-stu-id="167d3-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="167d3-217">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="167d3-217">Requirements</span></span>



| <span data-ttu-id="167d3-218">Condition requise</span><span class="sxs-lookup"><span data-stu-id="167d3-218">Requirement</span></span> | <span data-ttu-id="167d3-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="167d3-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="167d3-220">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="167d3-220">Minimum supported client</span></span><br/> | <span data-ttu-id="167d3-221">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="167d3-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="167d3-222">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="167d3-222">Minimum supported server</span></span><br/> | <span data-ttu-id="167d3-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="167d3-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="167d3-224">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="167d3-224">Namespace</span></span><br/>                | <span data-ttu-id="167d3-225">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="167d3-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="167d3-226">MOF</span><span class="sxs-lookup"><span data-stu-id="167d3-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="167d3-227"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="167d3-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="167d3-228">DLL</span><span class="sxs-lookup"><span data-stu-id="167d3-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="167d3-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="167d3-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="167d3-230">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="167d3-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="167d3-231">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="167d3-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 


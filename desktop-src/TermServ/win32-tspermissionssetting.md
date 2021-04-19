---
title: Classe Win32_TSPermissionsSetting
description: Comprend une méthode pour ajouter de nouveaux comptes au terminal et une méthode pour restaurer les autorisations par défaut sur un terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Win32_TSPermissionsSetting de la classe Services Bureau à distance
- Win32_TSPermissionsSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509555"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="f3b14-105">\_Classe TSPermissionsSetting Win32</span><span class="sxs-lookup"><span data-stu-id="f3b14-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="f3b14-106">La classe WMI **\_ TSPermissionsSetting** WMI comprend une méthode pour ajouter de nouveaux comptes au terminal et une méthode pour restaurer les autorisations par défaut sur un terminal.</span><span class="sxs-lookup"><span data-stu-id="f3b14-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="f3b14-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="f3b14-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f3b14-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f3b14-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3b14-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="f3b14-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f3b14-110">Members</span></span>

<span data-ttu-id="f3b14-111">La classe **Win32 \_ TSPermissionsSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f3b14-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f3b14-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f3b14-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3b14-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f3b14-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3b14-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f3b14-114">Methods</span></span>

<span data-ttu-id="f3b14-115">La classe **Win32 \_ TSPermissionsSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f3b14-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="f3b14-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="f3b14-116">Method</span></span>                                                                | <span data-ttu-id="f3b14-117">Description</span><span class="sxs-lookup"><span data-stu-id="f3b14-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b14-118">**AddAccount**</span><span class="sxs-lookup"><span data-stu-id="f3b14-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="f3b14-119">Ajoute un compte au terminal avec le jeu d’autorisations spécifié dans la valeur du paramètre *PermissionPreSet* .</span><span class="sxs-lookup"><span data-stu-id="f3b14-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="f3b14-120">**RestoreDefaults**</span><span class="sxs-lookup"><span data-stu-id="f3b14-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="f3b14-121">Restaure les valeurs de jeu d’autorisations par défaut pour le terminal.</span><span class="sxs-lookup"><span data-stu-id="f3b14-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="f3b14-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f3b14-122">Properties</span></span>

<span data-ttu-id="f3b14-123">La classe **Win32 \_ TSPermissionsSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3b14-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3b14-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f3b14-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3b14-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-128">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f3b14-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-130">**DenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="f3b14-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b14-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-133">Spécifie si l’administrateur local est autorisé à personnaliser.</span><span class="sxs-lookup"><span data-stu-id="f3b14-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="f3b14-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-137">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-137">Description of the object.</span></span>

<span data-ttu-id="f3b14-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3b14-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3b14-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-142">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f3b14-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-143">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="f3b14-143">The date the object was installed.</span></span> <span data-ttu-id="f3b14-144">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="f3b14-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3b14-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f3b14-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-149">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-149">The name of the object.</span></span>

<span data-ttu-id="f3b14-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-151">**PolicySourceDenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="f3b14-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b14-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-154">Indique si la propriété **MinEncryptionLevel** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="f3b14-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="f3b14-155">0</span><span class="sxs-lookup"><span data-stu-id="f3b14-155">0</span></span>
</dt> <dd>

<span data-ttu-id="f3b14-156">Serveur</span><span class="sxs-lookup"><span data-stu-id="f3b14-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-157">1</span><span class="sxs-lookup"><span data-stu-id="f3b14-157">1</span></span>
</dt> <dd>

<span data-ttu-id="f3b14-158">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="f3b14-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3b14-159">**État**</span><span class="sxs-lookup"><span data-stu-id="f3b14-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f3b14-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-163">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-163">Current status of the object.</span></span> <span data-ttu-id="f3b14-164">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="f3b14-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f3b14-165">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="f3b14-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f3b14-166">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="f3b14-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3b14-167">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="f3b14-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3b14-168">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="f3b14-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3b14-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f3b14-170">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-171">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-172">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-173">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="f3b14-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-174">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-175">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-176">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3b14-177">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="f3b14-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3b14-178">**StringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3b14-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f3b14-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-181">Descripteur de sécurité associé au terminal dans le format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="f3b14-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="f3b14-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="f3b14-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b14-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f3b14-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b14-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f3b14-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b14-185">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="f3b14-185">The name of the terminal.</span></span>

<span data-ttu-id="f3b14-186">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="f3b14-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3b14-187">Notes</span><span class="sxs-lookup"><span data-stu-id="f3b14-187">Remarks</span></span>

<span data-ttu-id="f3b14-188">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f3b14-189">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="f3b14-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f3b14-190">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="f3b14-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f3b14-191">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="f3b14-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f3b14-192">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f3b14-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3b14-193">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f3b14-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3b14-194">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f3b14-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3b14-195">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f3b14-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b14-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3b14-196">Requirements</span></span>



| <span data-ttu-id="f3b14-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3b14-197">Requirement</span></span> | <span data-ttu-id="f3b14-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3b14-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b14-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b14-199">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b14-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b14-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3b14-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b14-201">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b14-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b14-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3b14-203">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3b14-203">Namespace</span></span><br/>                | <span data-ttu-id="f3b14-204">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f3b14-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f3b14-205">MOF</span><span class="sxs-lookup"><span data-stu-id="f3b14-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3b14-206"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3b14-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3b14-207">DLL</span><span class="sxs-lookup"><span data-stu-id="f3b14-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3b14-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3b14-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b14-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3b14-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b14-210">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f3b14-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


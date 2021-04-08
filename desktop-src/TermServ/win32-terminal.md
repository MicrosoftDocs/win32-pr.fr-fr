---
title: Classe Win32_Terminal
description: Représente un terminal.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal de la classe Services Bureau à distance
- Win32_Terminal de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103148"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="54531-105">\_Classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="54531-105">Win32\_Terminal class</span></span>

<span data-ttu-id="54531-106">La classe WMI de **\_ Terminal Win32** représente un terminal.</span><span class="sxs-lookup"><span data-stu-id="54531-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="54531-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="54531-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="54531-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="54531-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="54531-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54531-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="54531-110">Membres</span><span class="sxs-lookup"><span data-stu-id="54531-110">Members</span></span>

<span data-ttu-id="54531-111">La classe de **\_ Terminal Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="54531-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="54531-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54531-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="54531-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54531-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54531-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54531-114">Methods</span></span>

<span data-ttu-id="54531-115">La classe de **\_ Terminal Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="54531-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="54531-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="54531-116">Method</span></span>                                  | <span data-ttu-id="54531-117">Description</span><span class="sxs-lookup"><span data-stu-id="54531-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54531-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="54531-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="54531-119">Crée un terminal avec les paramètres par défaut qui peuvent être personnalisés à l’aide des propriétés et des méthodes des classes [**\_ TerminalSetting Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="54531-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="54531-120">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="54531-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="54531-121">Supprime le terminal spécifié.</span><span class="sxs-lookup"><span data-stu-id="54531-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="54531-122">**Activer**</span><span class="sxs-lookup"><span data-stu-id="54531-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="54531-123">Désactive ou active le terminal.</span><span class="sxs-lookup"><span data-stu-id="54531-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="54531-124">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="54531-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="54531-125">Renomme le terminal.</span><span class="sxs-lookup"><span data-stu-id="54531-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="54531-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54531-126">Properties</span></span>

<span data-ttu-id="54531-127">La classe de **\_ Terminal Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="54531-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54531-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="54531-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54531-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54531-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54531-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="54531-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="54531-132">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54531-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="54531-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54531-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54531-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="54531-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54531-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54531-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54531-137">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54531-137">Description of the object.</span></span>

<span data-ttu-id="54531-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54531-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54531-139">**fEnableTerminal**</span><span class="sxs-lookup"><span data-stu-id="54531-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54531-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54531-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54531-142">Spécifie si le terminal spécifié est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="54531-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="54531-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="54531-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="54531-144">Le terminal est désactivé.</span><span class="sxs-lookup"><span data-stu-id="54531-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="54531-145"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="54531-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="54531-146">Le terminal est activé.</span><span class="sxs-lookup"><span data-stu-id="54531-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="54531-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="54531-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-148">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="54531-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54531-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54531-150">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="54531-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="54531-151">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="54531-151">The date the object was installed.</span></span> <span data-ttu-id="54531-152">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="54531-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="54531-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54531-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54531-154">**LoggedOnUsers**</span><span class="sxs-lookup"><span data-stu-id="54531-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54531-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54531-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54531-157">Nombre de sessions de connexion pour le terminal.</span><span class="sxs-lookup"><span data-stu-id="54531-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="54531-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="54531-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54531-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54531-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54531-161">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="54531-161">The name of the object.</span></span>

<span data-ttu-id="54531-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54531-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54531-163">**État**</span><span class="sxs-lookup"><span data-stu-id="54531-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54531-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54531-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54531-166">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="54531-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="54531-167">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54531-167">Current status of the object.</span></span> <span data-ttu-id="54531-168">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="54531-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="54531-169">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="54531-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="54531-170">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="54531-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="54531-171">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="54531-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="54531-172">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="54531-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="54531-173">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54531-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="54531-174">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="54531-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-175">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="54531-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-176">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="54531-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-177">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="54531-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-178">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="54531-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-179">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="54531-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-180">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="54531-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="54531-181">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="54531-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54531-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="54531-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54531-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54531-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54531-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54531-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54531-185">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54531-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54531-186">Nom unique qui identifie l’instance du terminal.</span><span class="sxs-lookup"><span data-stu-id="54531-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54531-187">Notes</span><span class="sxs-lookup"><span data-stu-id="54531-187">Remarks</span></span>

<span data-ttu-id="54531-188">**Win32 \_ Le terminal** est associé [**à Win32 \_ TerminalSetting**](win32-terminalsetting.md) comme propriété d' **élément** de l’Association [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="54531-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="54531-189">Les classes suivantes sont des sous-classes de la classe de **\_ Terminal Win32** : [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), [**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) [**, Win32 TSNetworkAdapterListSetting, \_**](win32-tsnetworkadapterlistsetting.md) [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)et [**Win32 \_ TSAccount**](win32-tsaccount.md).</span><span class="sxs-lookup"><span data-stu-id="54531-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="54531-190">Notez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="54531-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="54531-191">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété **TerminalName** , les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="54531-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="54531-192">Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="54531-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="54531-193">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="54531-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="54531-194">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="54531-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="54531-195">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="54531-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="54531-196">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="54531-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="54531-197">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="54531-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="54531-198">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="54531-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="54531-199">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="54531-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="54531-200">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="54531-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="54531-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54531-201">Requirements</span></span>



| <span data-ttu-id="54531-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54531-202">Requirement</span></span> | <span data-ttu-id="54531-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="54531-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54531-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54531-204">Minimum supported client</span></span><br/> | <span data-ttu-id="54531-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54531-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54531-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54531-206">Minimum supported server</span></span><br/> | <span data-ttu-id="54531-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54531-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54531-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54531-208">Namespace</span></span><br/>                | <span data-ttu-id="54531-209">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="54531-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="54531-210">MOF</span><span class="sxs-lookup"><span data-stu-id="54531-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54531-211"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54531-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="54531-212">DLL</span><span class="sxs-lookup"><span data-stu-id="54531-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54531-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54531-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54531-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54531-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54531-215">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="54531-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="54531-216">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="54531-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="54531-217">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="54531-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 


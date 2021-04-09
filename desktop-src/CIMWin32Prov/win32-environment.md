---
description: Représente un environnement ou un paramètre d’environnement système sur un système informatique Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Classe Win32_Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861714"
---
# <a name="win32_environment-class"></a><span data-ttu-id="03dcf-103">\_Classe d’environnement Win32</span><span class="sxs-lookup"><span data-stu-id="03dcf-103">Win32\_Environment class</span></span>

<span data-ttu-id="03dcf-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l' **\_ environnement Win32** représente un environnement ou un paramètre d’environnement système sur un système informatique Windows.</span><span class="sxs-lookup"><span data-stu-id="03dcf-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="03dcf-105">L’interrogation de cette classe retourne les variables d’environnement trouvées dans :</span><span class="sxs-lookup"><span data-stu-id="03dcf-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="03dcf-106">**HKEY \_ \_** Environnement de \\  \\  \\ **contrôle** \\  \\  CurrentControlSet de système d’ordinateur local sessionmanager</span><span class="sxs-lookup"><span data-stu-id="03dcf-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="03dcf-107">et</span><span class="sxs-lookup"><span data-stu-id="03dcf-107">and</span></span>

<span data-ttu-id="03dcf-108">**HKEY \_** \\ Environnement **< utilisateur >** des utilisateurs \\ </span><span class="sxs-lookup"><span data-stu-id="03dcf-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="03dcf-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="03dcf-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03dcf-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="03dcf-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03dcf-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03dcf-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="03dcf-112">Membres</span><span class="sxs-lookup"><span data-stu-id="03dcf-112">Members</span></span>

<span data-ttu-id="03dcf-113">La classe d' **\_ environnement Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="03dcf-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="03dcf-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03dcf-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03dcf-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03dcf-115">Properties</span></span>

<span data-ttu-id="03dcf-116">La classe d' **\_ environnement Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="03dcf-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03dcf-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="03dcf-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-121">A short textual description of the object.</span></span>

<span data-ttu-id="03dcf-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="03dcf-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-126">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="03dcf-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-127">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-127">A textual description of the object.</span></span>

<span data-ttu-id="03dcf-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03dcf-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03dcf-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="03dcf-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-133">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="03dcf-133">Indicates when the object was installed.</span></span> <span data-ttu-id="03dcf-134">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="03dcf-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="03dcf-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-136">**Nom**</span><span class="sxs-lookup"><span data-stu-id="03dcf-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="03dcf-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-139">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-140">Chaîne de caractères qui spécifie le nom d’une variable d’environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="03dcf-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="03dcf-141">En spécifiant le nom d’une variable qui n’existe pas encore, une application crée une nouvelle variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="03dcf-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="03dcf-142">Exemple : "path"</span><span class="sxs-lookup"><span data-stu-id="03dcf-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-143">**État**</span><span class="sxs-lookup"><span data-stu-id="03dcf-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="03dcf-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-147">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="03dcf-148">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="03dcf-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="03dcf-149">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="03dcf-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="03dcf-150">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="03dcf-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="03dcf-151">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="03dcf-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="03dcf-152">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="03dcf-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="03dcf-153">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="03dcf-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="03dcf-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="03dcf-155">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="03dcf-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03dcf-156">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03dcf-157">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03dcf-158">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03dcf-159">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="03dcf-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03dcf-160">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03dcf-161">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03dcf-162">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03dcf-163">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03dcf-164">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03dcf-165">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03dcf-166">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03dcf-167">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03dcf-168">**SystemVariable**</span><span class="sxs-lookup"><span data-stu-id="03dcf-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-169">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="03dcf-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-171">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-172">Indique si la variable est une variable système.</span><span class="sxs-lookup"><span data-stu-id="03dcf-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="03dcf-173">Une variable système est définie par le système d’exploitation et est indépendante des paramètres de l’environnement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="03dcf-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03dcf-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-177">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="03dcf-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-178">Nom du propriétaire du paramètre d’environnement.</span><span class="sxs-lookup"><span data-stu-id="03dcf-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="03dcf-179">Elle est définie sur <SYSTEM> pour les paramètres spécifiques au système Windows (par opposition à un utilisateur spécifique) et <DEFAULT> pour les paramètres utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="03dcf-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="03dcf-180">Exemple : « jdupont »</span><span class="sxs-lookup"><span data-stu-id="03dcf-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="03dcf-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="03dcf-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03dcf-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03dcf-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="03dcf-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03dcf-184">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment »)</span><span class="sxs-lookup"><span data-stu-id="03dcf-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="03dcf-185">Variable d’espace réservé d’une variable d’environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="03dcf-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="03dcf-186">Les informations telles que le répertoire du système de fichiers peuvent passer d’un ordinateur à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="03dcf-187">Le système d’exploitation remplace ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="03dcf-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="03dcf-188">Exemple : « % SystemRoot% »</span><span class="sxs-lookup"><span data-stu-id="03dcf-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03dcf-189">Notes</span><span class="sxs-lookup"><span data-stu-id="03dcf-189">Remarks</span></span>

<span data-ttu-id="03dcf-190">La classe d' **\_ environnement Win32** est dérivée de [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="03dcf-191">Vous pouvez utiliser cette classe pour rechercher les chemins d’accès de dossiers spéciaux, tels que le dossier système ou les fichiers programme sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="03dcf-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="03dcf-192">Voici quelques exemples : windir, systemroot, ProgramFiles et UserProfile.</span><span class="sxs-lookup"><span data-stu-id="03dcf-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="03dcf-193">**Win32 \_** Fondamentalement, l’environnement retourne ce qui se trouve dans :</span><span class="sxs-lookup"><span data-stu-id="03dcf-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="03dcf-194">**HKEY \_ \_** Environnement de \\  \\  \\ **contrôle** \\  \\  CurrentControlSet de système d’ordinateur local sessionmanager</span><span class="sxs-lookup"><span data-stu-id="03dcf-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="03dcf-195">et</span><span class="sxs-lookup"><span data-stu-id="03dcf-195">and</span></span>

<span data-ttu-id="03dcf-196">**HKEY \_** \\ Environnement **< utilisateur >** des utilisateurs \\ </span><span class="sxs-lookup"><span data-stu-id="03dcf-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="03dcf-197">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="03dcf-198">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="03dcf-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="03dcf-199">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="03dcf-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="03dcf-200">Exemples</span><span class="sxs-lookup"><span data-stu-id="03dcf-200">Examples</span></span>

<span data-ttu-id="03dcf-201">L’exemple de [liste de variables d’environnement sur un ordinateur](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) perl utilise WMI pour retourner des informations sur toutes les variables d’environnement sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="03dcf-202">L’exemple de code VBScript suivant énumère les variables d’environnement sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="03dcf-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="03dcf-203">L’exemple de code VBScript suivant modifie une variable d’environnement nommée BUILD \_ type en une valeur entrée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="03dcf-204">Le script suppose que la variable de \_ type de build existe déjà.</span><span class="sxs-lookup"><span data-stu-id="03dcf-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="03dcf-205">S’il n’existe pas, le script se termine.</span><span class="sxs-lookup"><span data-stu-id="03dcf-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="03dcf-206">La valeur d’entrée est vérifiée : elle doit être « Build1 », « Build2 » ou « Build3 », et aucune autre valeur n’est acceptée.</span><span class="sxs-lookup"><span data-stu-id="03dcf-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="03dcf-207">La fonction VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) rend l’entrée non sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="03dcf-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="03dcf-208">Si ce qui est tapé n’est pas l’une des trois valeurs acceptables, le script se termine.</span><span class="sxs-lookup"><span data-stu-id="03dcf-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="03dcf-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03dcf-209">Requirements</span></span>



| <span data-ttu-id="03dcf-210">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03dcf-210">Requirement</span></span> | <span data-ttu-id="03dcf-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="03dcf-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03dcf-212">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03dcf-212">Minimum supported client</span></span><br/> | <span data-ttu-id="03dcf-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03dcf-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03dcf-214">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03dcf-214">Minimum supported server</span></span><br/> | <span data-ttu-id="03dcf-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03dcf-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03dcf-216">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="03dcf-216">Namespace</span></span><br/>                | <span data-ttu-id="03dcf-217">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="03dcf-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03dcf-218">MOF</span><span class="sxs-lookup"><span data-stu-id="03dcf-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03dcf-219"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03dcf-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03dcf-220">DLL</span><span class="sxs-lookup"><span data-stu-id="03dcf-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03dcf-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03dcf-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03dcf-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03dcf-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03dcf-223">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="03dcf-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="03dcf-224">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03dcf-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


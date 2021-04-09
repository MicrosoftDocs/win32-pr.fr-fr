---
description: Le \_ StartupCommand Win32&\# 8194 ; La classe WMI représente une commande qui s’exécute automatiquement lorsqu’un utilisateur ouvre une session sur le système informatique.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Classe Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861581"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="e29bd-103">\_Classe StartupCommand Win32</span><span class="sxs-lookup"><span data-stu-id="e29bd-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="e29bd-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand** WMI représente une commande qui s’exécute automatiquement lorsqu’un utilisateur ouvre une session sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="e29bd-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="e29bd-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e29bd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e29bd-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e29bd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e29bd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e29bd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="e29bd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e29bd-108">Members</span></span>

<span data-ttu-id="e29bd-109">La classe **Win32 \_ StartupCommand** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e29bd-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="e29bd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e29bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e29bd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e29bd-111">Properties</span></span>

<span data-ttu-id="e29bd-112">La classe **Win32 \_ StartupCommand** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e29bd-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e29bd-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e29bd-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="e29bd-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-117">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e29bd-117">Short textual description of the current object.</span></span>

<span data-ttu-id="e29bd-118">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-119">**Commande**</span><span class="sxs-lookup"><span data-stu-id="e29bd-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-122">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-123">Commande exécutée par la commande de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e29bd-123">Command run by the startup command.</span></span>

<span data-ttu-id="e29bd-124">WMI obtient ces données à partir de la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="e29bd-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="e29bd-125">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**</span><span class="sxs-lookup"><span data-stu-id="e29bd-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="e29bd-126">Exemple : « C : \\ Windows \\notepad.exe myfile.txt »</span><span class="sxs-lookup"><span data-stu-id="e29bd-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="e29bd-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-130">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e29bd-130">Textual description of the current object.</span></span>

<span data-ttu-id="e29bd-131">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-132">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="e29bd-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-135">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-136">Chemin d’accès où la commande de démarrage réside sur le système de fichiers du disque.</span><span class="sxs-lookup"><span data-stu-id="e29bd-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="e29bd-137">Par exemple : HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="e29bd-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="e29bd-138">**Startup** (« Startup »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="e29bd-139">**Démarrage commun** (« démarrage commun »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="e29bd-140">**\\ HKLM \\ LOGICIEL \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** (« HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="e29bd-141">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")</span><span class="sxs-lookup"><span data-stu-id="e29bd-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e29bd-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e29bd-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-145">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de fichiers win32api \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")</span><span class="sxs-lookup"><span data-stu-id="e29bd-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-146">Nom de fichier de la commande de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e29bd-146">File name of the startup command.</span></span>

<span data-ttu-id="e29bd-147">Exemple : « FindFast »</span><span class="sxs-lookup"><span data-stu-id="e29bd-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e29bd-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-151">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="e29bd-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-152">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="e29bd-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e29bd-153">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-154">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e29bd-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-157">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-158">Nom d’utilisateur pour lequel cette commande de démarrage s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="e29bd-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="e29bd-159">Exemple : « MyDomain \\ myname »</span><span class="sxs-lookup"><span data-stu-id="e29bd-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="e29bd-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="e29bd-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e29bd-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e29bd-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29bd-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e29bd-163">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="e29bd-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e29bd-164">La propriété UserSID indique le SID de l’utilisateur pour lequel cette commande de démarrage s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="e29bd-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="e29bd-165">Cette propriété d’utilisateur peut être vide, mais UserSID a toujours une valeur si le nom d’utilisateur ne peut pas être résolu (comme dans le cas d’un utilisateur supprimé).</span><span class="sxs-lookup"><span data-stu-id="e29bd-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="e29bd-166">La propriété permet de faire la distinction entre les commandes associées à w/deux utilisateurs avec des noms non résolus.</span><span class="sxs-lookup"><span data-stu-id="e29bd-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="e29bd-167">Il peut s’agir de la valeur NULL lorsque la commande est associée à des éléments qui n’identifient pas réellement un utilisateur comme tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e29bd-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="e29bd-168">Exemple : S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="e29bd-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e29bd-169">Notes</span><span class="sxs-lookup"><span data-stu-id="e29bd-169">Remarks</span></span>

<span data-ttu-id="e29bd-170">La classe **Win32 \_ StartupCommand** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="e29bd-171">Le démarrage de l’ordinateur ne se termine pas après le chargement du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e29bd-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="e29bd-172">Au lieu de cela, le système d’exploitation Windows peut être configuré de sorte que les commandes de démarrage soient exécutées à chaque démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="e29bd-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="e29bd-173">Les commandes de démarrage sont stockées dans le registre ou dans le cadre du profil utilisateur et sont utilisées pour démarrer automatiquement des scripts ou des applications spécifiés à chaque fois que Windows est chargé.</span><span class="sxs-lookup"><span data-stu-id="e29bd-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="e29bd-174">Dans la plupart des cas, les programmes AutoStart sont utiles. ils garantissent que certaines applications, telles que les outils antivirus, sont automatiquement démarrées et exécutées chaque fois que Windows est chargé.</span><span class="sxs-lookup"><span data-stu-id="e29bd-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="e29bd-175">Toutefois, les programmes de démarrage automatique peuvent également être responsables des problèmes tels que :</span><span class="sxs-lookup"><span data-stu-id="e29bd-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="e29bd-176">Les ordinateurs qui prennent beaucoup de temps à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e29bd-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="e29bd-177">Cela peut être dû à un grand nombre d’applications qui doivent être démarrées à chaque démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="e29bd-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="e29bd-178">Applications qui sont représentées dans la barre des tâches ou dans le gestionnaire des tâches, même si l’utilisateur ne les a pas démarrées.</span><span class="sxs-lookup"><span data-stu-id="e29bd-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="e29bd-179">Bien que ces applications ne causent pas nécessairement des problèmes, elles peuvent entraîner des appels au support technique émis par des utilisateurs qui se sont déconcertés en ce qui concerne l’origine de ces programmes et pourquoi ils sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e29bd-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="e29bd-180">Ordinateurs rencontrant des problèmes même lorsqu’ils semblent inactifs.</span><span class="sxs-lookup"><span data-stu-id="e29bd-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="e29bd-181">Ces problèmes sont souvent suivis dans des commandes de démarrage qui s’exécutent lorsque personne n’est conscient qu’elles sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e29bd-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="e29bd-182">L’identification des applications et des scripts qui s’exécutent automatiquement au démarrage est une tâche administrative importante mais difficile, car les commandes de démarrage peuvent être stockées dans différents emplacements :</span><span class="sxs-lookup"><span data-stu-id="e29bd-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="e29bd-183">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="e29bd-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="e29bd-184">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="e29bd-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="e29bd-185">\\Logiciel HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="e29bd-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="e29bd-186">\\Logiciel HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="e29bd-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="e29bd-187">HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="e29bd-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="e29bd-188">\\fichiers du lecteur_système et paramètres \\ tous les utilisateurs \\ démarrage des \\ programmes du menu démarrer \\</span><span class="sxs-lookup"><span data-stu-id="e29bd-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="e29bd-189">lecteur_système \\ Documents and Settings \\ NomUtilisateur \\ menu démarrer \\ programmes \\ démarrage</span><span class="sxs-lookup"><span data-stu-id="e29bd-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="e29bd-190">Vous pouvez utiliser la classe WMI Win32 \_ StartupCommand pour énumérer les programmes de démarrage automatique, quel que soit l’emplacement de stockage des informations.</span><span class="sxs-lookup"><span data-stu-id="e29bd-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="e29bd-191">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="e29bd-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="e29bd-192">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="e29bd-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="e29bd-193">Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="e29bd-194">Vous pouvez modifier les valeurs de Registre dans lesquelles **Win32 \_ StartupCommand** obtient des données en appelant les méthodes de [fournisseur du Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI dans un script ou en C++.</span><span class="sxs-lookup"><span data-stu-id="e29bd-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="e29bd-195">Pour plus d’informations, consultez [modification du Registre système](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="e29bd-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e29bd-196">Exemples</span><span class="sxs-lookup"><span data-stu-id="e29bd-196">Examples</span></span>

<span data-ttu-id="e29bd-197">Le code VBScript suivant énumère les commandes de démarrage sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e29bd-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="e29bd-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e29bd-198">Requirements</span></span>



| <span data-ttu-id="e29bd-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e29bd-199">Requirement</span></span> | <span data-ttu-id="e29bd-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="e29bd-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e29bd-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e29bd-201">Minimum supported client</span></span><br/> | <span data-ttu-id="e29bd-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e29bd-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e29bd-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e29bd-203">Minimum supported server</span></span><br/> | <span data-ttu-id="e29bd-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e29bd-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e29bd-205">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e29bd-205">Namespace</span></span><br/>                | <span data-ttu-id="e29bd-206">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e29bd-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e29bd-207">MOF</span><span class="sxs-lookup"><span data-stu-id="e29bd-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e29bd-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e29bd-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e29bd-209">DLL</span><span class="sxs-lookup"><span data-stu-id="e29bd-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e29bd-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e29bd-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e29bd-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e29bd-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29bd-212">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="e29bd-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="e29bd-213">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e29bd-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

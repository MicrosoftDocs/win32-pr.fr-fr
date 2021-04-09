---
description: Modifie un objet de service dérivé de Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111111"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="def69-103">Modifier la méthode de la \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="def69-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="def69-104">La méthode de la classe **change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifie un objet de service dérivé de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="def69-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="def69-105">Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un groupe de services système qui définissent des dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="def69-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="def69-106">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="def69-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="def69-107">Ces services dépendants requièrent que les services antécédents fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="def69-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="def69-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="def69-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="def69-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="def69-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="def69-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="def69-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="def69-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="def69-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def69-112">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-113">Nom complet d’un service.</span><span class="sxs-lookup"><span data-stu-id="def69-113">The display name for a service.</span></span> <span data-ttu-id="def69-114">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="def69-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="def69-115">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="def69-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="def69-116">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="def69-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="def69-117">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="def69-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="def69-118">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="def69-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="def69-119">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-120">Chemin d’accès qualifié complet au fichier exécutable qui implémente un service.</span><span class="sxs-lookup"><span data-stu-id="def69-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="def69-121">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="def69-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="def69-122">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-123">Type de services fourni aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="def69-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="def69-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Pilote de noyau** (1)</span><span class="sxs-lookup"><span data-stu-id="def69-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="def69-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Pilote du système de fichiers** (2)</span><span class="sxs-lookup"><span data-stu-id="def69-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="def69-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptateur** (4)</span><span class="sxs-lookup"><span data-stu-id="def69-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="def69-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Pilote de reconnaissance** (8)</span><span class="sxs-lookup"><span data-stu-id="def69-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="def69-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Propre processus** (16)</span><span class="sxs-lookup"><span data-stu-id="def69-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="def69-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processus de partage** (32)</span><span class="sxs-lookup"><span data-stu-id="def69-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="def69-130">(256)</span><span class="sxs-lookup"><span data-stu-id="def69-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="def69-131">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="def69-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="def69-132">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-133">Gravité d’une erreur si ce service ne démarre pas au démarrage.</span><span class="sxs-lookup"><span data-stu-id="def69-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="def69-134">La valeur indique l’action prise par le programme de démarrage si une défaillance se produit.</span><span class="sxs-lookup"><span data-stu-id="def69-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="def69-135">Le système journalise toutes les erreurs.</span><span class="sxs-lookup"><span data-stu-id="def69-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="def69-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** (0)</span><span class="sxs-lookup"><span data-stu-id="def69-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="def69-137">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="def69-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="def69-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="def69-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="def69-139">Normal.</span><span class="sxs-lookup"><span data-stu-id="def69-139">Normal.</span></span> <span data-ttu-id="def69-140">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="def69-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="def69-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="def69-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="def69-142">Le système est redémarré avec la dernière bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="def69-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="def69-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="def69-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="def69-144">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="def69-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="def69-145">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-146">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="def69-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="def69-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="def69-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="def69-148">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="def69-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="def69-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="def69-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="def69-150">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="def69-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="def69-151">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="def69-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="def69-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="def69-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="def69-153">Service pour démarrer automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="def69-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="def69-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="def69-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="def69-155">Service à démarrer par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="def69-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="def69-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="def69-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="def69-157">Service qui ne peut pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="def69-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="def69-158">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-159">Si la **valeur est true**, le service peut créer ou communiquer avec une fenêtre sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="def69-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="def69-160">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-161">Nom du compte sous lequel le service s’exécute, qui dépend du type de service.</span><span class="sxs-lookup"><span data-stu-id="def69-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="def69-162">Le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="def69-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="def69-163">Lorsqu’il s’exécute, le processus de service est enregistré à l’aide de l’une des deux formes précédentes.</span><span class="sxs-lookup"><span data-stu-id="def69-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="def69-164">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="def69-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="def69-165">Si une chaîne vide est spécifiée, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="def69-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="def69-166">Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote, par exemple, système de \\ fichiers \\ RDR ou \\ pilote \\ XNS, que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="def69-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="def69-167">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, \\ administrateur DWDOM.</span><span class="sxs-lookup"><span data-stu-id="def69-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="def69-168">Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="def69-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="def69-169">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-170">Mot de passe du nom de compte que le paramètre *StartName* spécifie.</span><span class="sxs-lookup"><span data-stu-id="def69-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="def69-171">Spécifiez **null** lorsque vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="def69-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="def69-172">Spécifiez une chaîne vide si le service n’a pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="def69-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="def69-173">Lorsque vous modifiez un service de système local en réseau ou de réseau à système local, *StartPassword* doit être une chaîne vide ("") et non **null**.</span><span class="sxs-lookup"><span data-stu-id="def69-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="def69-174">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-175">Nom du groupe auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="def69-175">Group name that it is associated with.</span></span> <span data-ttu-id="def69-176">Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent la séquence de chargement des services dans un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="def69-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="def69-177">Si le pointeur est **null** ou pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="def69-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="def69-178">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="def69-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="def69-179">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="def69-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="def69-180">Le registre système contient une liste de groupes d’ordre de chargement situés dans **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="def69-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="def69-181">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-182">Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="def69-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="def69-183">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="def69-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="def69-184">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="def69-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="def69-185">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="def69-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="def69-186">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="def69-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="def69-187">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="def69-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def69-188">Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="def69-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="def69-189">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="def69-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="def69-190">Si le pointeur est **null** ou pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="def69-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="def69-191">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="def69-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def69-192">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="def69-192">Return value</span></span>

<span data-ttu-id="def69-193">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="def69-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="def69-194">**Success**</span><span class="sxs-lookup"><span data-stu-id="def69-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="def69-195">0</span><span class="sxs-lookup"><span data-stu-id="def69-195">0</span></span>

<span data-ttu-id="def69-196">La demande est acceptée.</span><span class="sxs-lookup"><span data-stu-id="def69-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="def69-197">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="def69-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="def69-198">1</span><span class="sxs-lookup"><span data-stu-id="def69-198">1</span></span>

<span data-ttu-id="def69-199">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="def69-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="def69-200">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="def69-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="def69-201">2</span><span class="sxs-lookup"><span data-stu-id="def69-201">2</span></span>

<span data-ttu-id="def69-202">L’utilisateur ne dispose pas des privilèges d’accès nécessaires.</span><span class="sxs-lookup"><span data-stu-id="def69-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="def69-203">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="def69-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="def69-204">3</span><span class="sxs-lookup"><span data-stu-id="def69-204">3</span></span>

<span data-ttu-id="def69-205">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="def69-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="def69-206">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="def69-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="def69-207">4</span><span class="sxs-lookup"><span data-stu-id="def69-207">4</span></span>

<span data-ttu-id="def69-208">Le code de contrôle demandé n’est pas valide ou n’est pas acceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="def69-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-209">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="def69-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="def69-210">5</span><span class="sxs-lookup"><span data-stu-id="def69-210">5</span></span>

<span data-ttu-id="def69-211">Le code de contrôle demandé ne peut pas être envoyé au service, car la propriété d' [**État**](win32-baseservice.md) de l’objet [**\_ BaseService Win32**](win32-baseservice.md) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="def69-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="def69-212">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="def69-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="def69-213">6</span><span class="sxs-lookup"><span data-stu-id="def69-213">6</span></span>

<span data-ttu-id="def69-214">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="def69-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="def69-215">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="def69-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="def69-216">7</span><span class="sxs-lookup"><span data-stu-id="def69-216">7</span></span>

<span data-ttu-id="def69-217">Le service ne répond pas rapidement à la demande de démarrage.</span><span class="sxs-lookup"><span data-stu-id="def69-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="def69-218">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="def69-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="def69-219">8</span><span class="sxs-lookup"><span data-stu-id="def69-219">8</span></span>

<span data-ttu-id="def69-220">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="def69-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="def69-221">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="def69-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="def69-222">9</span><span class="sxs-lookup"><span data-stu-id="def69-222">9</span></span>

<span data-ttu-id="def69-223">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="def69-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="def69-224">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="def69-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="def69-225">10</span><span class="sxs-lookup"><span data-stu-id="def69-225">10</span></span>

<span data-ttu-id="def69-226">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="def69-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="def69-227">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="def69-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="def69-228">11</span><span class="sxs-lookup"><span data-stu-id="def69-228">11</span></span>

<span data-ttu-id="def69-229">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="def69-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="def69-230">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="def69-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="def69-231">12</span><span class="sxs-lookup"><span data-stu-id="def69-231">12</span></span>

<span data-ttu-id="def69-232">Une dépendance sur laquelle ce service repose est supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="def69-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-233">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="def69-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="def69-234">13</span><span class="sxs-lookup"><span data-stu-id="def69-234">13</span></span>

<span data-ttu-id="def69-235">Le service ne trouve pas le service nécessaire à partir d’un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="def69-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-236">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="def69-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="def69-237">14</span><span class="sxs-lookup"><span data-stu-id="def69-237">14</span></span>

<span data-ttu-id="def69-238">Le service est désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="def69-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-239">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="def69-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="def69-240">15</span><span class="sxs-lookup"><span data-stu-id="def69-240">15</span></span>

<span data-ttu-id="def69-241">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="def69-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-242">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="def69-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="def69-243">16</span><span class="sxs-lookup"><span data-stu-id="def69-243">16</span></span>

<span data-ttu-id="def69-244">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="def69-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-245">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="def69-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="def69-246">17</span><span class="sxs-lookup"><span data-stu-id="def69-246">17</span></span>

<span data-ttu-id="def69-247">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="def69-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-248">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="def69-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="def69-249">18</span><span class="sxs-lookup"><span data-stu-id="def69-249">18</span></span>

<span data-ttu-id="def69-250">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="def69-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-251">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="def69-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="def69-252">19</span><span class="sxs-lookup"><span data-stu-id="def69-252">19</span></span>

<span data-ttu-id="def69-253">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="def69-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="def69-254">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="def69-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="def69-255">20</span><span class="sxs-lookup"><span data-stu-id="def69-255">20</span></span>

<span data-ttu-id="def69-256">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="def69-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-257">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="def69-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="def69-258">21</span><span class="sxs-lookup"><span data-stu-id="def69-258">21</span></span>

<span data-ttu-id="def69-259">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="def69-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-260">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="def69-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="def69-261">22</span><span class="sxs-lookup"><span data-stu-id="def69-261">22</span></span>

<span data-ttu-id="def69-262">Le compte pour lequel ce service doit être exécuté n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="def69-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="def69-263">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="def69-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="def69-264">23</span><span class="sxs-lookup"><span data-stu-id="def69-264">23</span></span>

<span data-ttu-id="def69-265">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="def69-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-266">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="def69-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="def69-267">24</span><span class="sxs-lookup"><span data-stu-id="def69-267">24</span></span>

<span data-ttu-id="def69-268">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="def69-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="def69-269">**Autres**</span><span class="sxs-lookup"><span data-stu-id="def69-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="def69-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="def69-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="def69-271">Notes</span><span class="sxs-lookup"><span data-stu-id="def69-271">Remarks</span></span>

<span data-ttu-id="def69-272">Pour modifier un service d’un réseau en un système local, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="def69-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="def69-273">Pour modifier un service d’un système local en réseau, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="def69-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="def69-274">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="def69-274">Requirements</span></span>



| <span data-ttu-id="def69-275">Condition requise</span><span class="sxs-lookup"><span data-stu-id="def69-275">Requirement</span></span> | <span data-ttu-id="def69-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="def69-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="def69-277">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="def69-277">Minimum supported client</span></span><br/> | <span data-ttu-id="def69-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="def69-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="def69-279">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="def69-279">Minimum supported server</span></span><br/> | <span data-ttu-id="def69-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="def69-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="def69-281">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="def69-281">Namespace</span></span><br/>                | <span data-ttu-id="def69-282">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="def69-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="def69-283">En-tête</span><span class="sxs-lookup"><span data-stu-id="def69-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="def69-284"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="def69-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="def69-285">MOF</span><span class="sxs-lookup"><span data-stu-id="def69-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="def69-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="def69-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="def69-287">DLL</span><span class="sxs-lookup"><span data-stu-id="def69-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def69-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def69-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def69-289">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="def69-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="def69-290">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="def69-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="def69-291">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="def69-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


---
description: Modifie un \_ service SystemDriver Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483561"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="f2204-103">Modifier la méthode de la \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="f2204-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="f2204-104">La méthode **change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifie un service [**\_ SystemDriver Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="f2204-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="f2204-105">Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un regroupement de services système définissant les dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f2204-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="f2204-106">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="f2204-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="f2204-107">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="f2204-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="f2204-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f2204-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f2204-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f2204-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2204-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2204-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f2204-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2204-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2204-112">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-113">Nom d’affichage du service.</span><span class="sxs-lookup"><span data-stu-id="f2204-113">The display name of the service.</span></span> <span data-ttu-id="f2204-114">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="f2204-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="f2204-115">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="f2204-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="f2204-116">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="f2204-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="f2204-117">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="f2204-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="f2204-118">Exemple : « Atdisk »</span><span class="sxs-lookup"><span data-stu-id="f2204-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="f2204-119">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-120">Chemin d’accès qualifié complet au fichier exécutable qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="f2204-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="f2204-121">Exemple : *\\ racine_système \\ System32 \\ drivers \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="f2204-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="f2204-122">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-123">Type des services fournis aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="f2204-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="f2204-124">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f2204-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-125">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="f2204-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="f2204-126">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="f2204-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-127">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="f2204-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="f2204-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f2204-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-129">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="f2204-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="f2204-130">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f2204-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-131">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="f2204-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="f2204-132">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="f2204-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-133">Propre processus</span><span class="sxs-lookup"><span data-stu-id="f2204-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="f2204-134">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="f2204-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-135">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="f2204-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="f2204-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="f2204-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="f2204-137">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="f2204-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f2204-138">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-139">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="f2204-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="f2204-140">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f2204-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="f2204-141">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="f2204-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="f2204-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** (0)</span><span class="sxs-lookup"><span data-stu-id="f2204-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f2204-143">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="f2204-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="f2204-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="f2204-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2204-145">Normal.</span><span class="sxs-lookup"><span data-stu-id="f2204-145">Normal.</span></span> <span data-ttu-id="f2204-146">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="f2204-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="f2204-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="f2204-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2204-148">Le système est redémarré avec la dernière bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="f2204-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f2204-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="f2204-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2204-150">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="f2204-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f2204-151">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-152">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="f2204-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="f2204-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Démarrage du démarrage**</span><span class="sxs-lookup"><span data-stu-id="f2204-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-154">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f2204-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="f2204-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Démarrage du démarrage**</span><span class="sxs-lookup"><span data-stu-id="f2204-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-156">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f2204-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="f2204-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage du système**</span><span class="sxs-lookup"><span data-stu-id="f2204-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-158">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f2204-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f2204-159">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="f2204-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="f2204-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique**</span><span class="sxs-lookup"><span data-stu-id="f2204-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-161">Service pour démarrer automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="f2204-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="f2204-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande**</span><span class="sxs-lookup"><span data-stu-id="f2204-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-163">Service à démarrer par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="f2204-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f2204-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**</span><span class="sxs-lookup"><span data-stu-id="f2204-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="f2204-165">Service qui ne peut pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="f2204-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f2204-166">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-167">Valeur qui, si la valeur est **true**, le service peut créer ou communiquer avec les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="f2204-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f2204-168">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-169">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="f2204-169">The account name the service runs under.</span></span> <span data-ttu-id="f2204-170">Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f2204-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="f2204-171">Lorsqu’il s’exécute, le processus de service est enregistré à l’aide de l’une de ces deux formes.</span><span class="sxs-lookup"><span data-stu-id="f2204-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="f2204-172">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f2204-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="f2204-173">Si une chaîne vide est spécifiée, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f2204-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="f2204-174">Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote, par exemple, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS), que le système d’entrée et de sortie (e/s) utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="f2204-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="f2204-175">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, \\ administrateur DWDOM.</span><span class="sxs-lookup"><span data-stu-id="f2204-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="f2204-176">Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="f2204-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="f2204-177">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-178">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="f2204-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="f2204-179">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f2204-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="f2204-180">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f2204-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="f2204-181">Lorsque vous modifiez un service d’un système local à un réseau ou d’un réseau à un système local, *StartPassword* doit être une chaîne vide ("") et non **null**.</span><span class="sxs-lookup"><span data-stu-id="f2204-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2204-182">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-183">Nom du groupe auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="f2204-183">The group name that it is associated with.</span></span> <span data-ttu-id="f2204-184">Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f2204-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="f2204-185">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="f2204-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="f2204-186">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="f2204-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="f2204-187">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="f2204-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="f2204-188">La liste des groupes d’ordre de chargement se trouve dans le registre système à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="f2204-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="f2204-189">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="f2204-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="f2204-190">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-191">Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="f2204-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="f2204-192">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="f2204-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="f2204-193">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="f2204-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f2204-194">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier WinSvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f2204-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="f2204-195">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="f2204-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f2204-196">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2204-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2204-197">Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="f2204-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="f2204-198">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="f2204-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="f2204-199">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="f2204-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f2204-200">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f2204-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2204-201">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2204-201">Return value</span></span>

<span data-ttu-id="f2204-202">Retourne la valeur zéro (0) si le service a été correctement modifié, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f2204-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f2204-203">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="f2204-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-204">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f2204-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-205">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="f2204-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-206">**Services dépendants en cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="f2204-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-207">**Contrôle de service non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="f2204-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-208">**Le service ne peut pas accepter le contrôle** (5)</span><span class="sxs-lookup"><span data-stu-id="f2204-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-209">**Service non actif** (6)</span><span class="sxs-lookup"><span data-stu-id="f2204-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-210">**Délai d’expiration** de la demande de service (7)</span><span class="sxs-lookup"><span data-stu-id="f2204-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-211">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="f2204-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-212">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="f2204-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-213">**Service déjà en cours d’exécution** (10)</span><span class="sxs-lookup"><span data-stu-id="f2204-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-214">**Base de données de service verrouillée** (11)</span><span class="sxs-lookup"><span data-stu-id="f2204-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-215">**Dépendance de service supprimée** (12)</span><span class="sxs-lookup"><span data-stu-id="f2204-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-216">**Échec** de la dépendance du service (13)</span><span class="sxs-lookup"><span data-stu-id="f2204-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-217">**Service désactivé** (14)</span><span class="sxs-lookup"><span data-stu-id="f2204-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-218">**Échec** de l’ouverture de session du service (15)</span><span class="sxs-lookup"><span data-stu-id="f2204-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-219">**Service marqué pour suppression** (16)</span><span class="sxs-lookup"><span data-stu-id="f2204-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-220">**Service sans thread** (17)</span><span class="sxs-lookup"><span data-stu-id="f2204-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-221">**Dépendance circulaire d’État** (18)</span><span class="sxs-lookup"><span data-stu-id="f2204-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-222">**Nom de l’État en double** (19)</span><span class="sxs-lookup"><span data-stu-id="f2204-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-223">**Nom de l’état non valide** (20)</span><span class="sxs-lookup"><span data-stu-id="f2204-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-224">**Paramètre d’État non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="f2204-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-225">**Compte de service de l’état non valide** (22)</span><span class="sxs-lookup"><span data-stu-id="f2204-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-226">Le **service d’État existe** (23)</span><span class="sxs-lookup"><span data-stu-id="f2204-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-227">**Service déjà suspendu** (24)</span><span class="sxs-lookup"><span data-stu-id="f2204-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="f2204-228">**Autre** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="f2204-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f2204-229">Notes</span><span class="sxs-lookup"><span data-stu-id="f2204-229">Remarks</span></span>

<span data-ttu-id="f2204-230">Pour modifier un service à partir d’un service réseau sur le système local, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="f2204-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="f2204-231">Pour modifier un service d’un service système local en service réseau, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="f2204-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="f2204-232">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2204-232">Requirements</span></span>



| <span data-ttu-id="f2204-233">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2204-233">Requirement</span></span> | <span data-ttu-id="f2204-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2204-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2204-235">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2204-235">Minimum supported client</span></span><br/> | <span data-ttu-id="f2204-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2204-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2204-237">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2204-237">Minimum supported server</span></span><br/> | <span data-ttu-id="f2204-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2204-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2204-239">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f2204-239">Namespace</span></span><br/>                | <span data-ttu-id="f2204-240">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f2204-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2204-241">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2204-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2204-242"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2204-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="f2204-243">MOF</span><span class="sxs-lookup"><span data-stu-id="f2204-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2204-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2204-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2204-245">DLL</span><span class="sxs-lookup"><span data-stu-id="f2204-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2204-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2204-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2204-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2204-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2204-248">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2204-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f2204-249">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="f2204-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


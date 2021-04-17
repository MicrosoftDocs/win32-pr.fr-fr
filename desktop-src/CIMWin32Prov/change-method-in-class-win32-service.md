---
description: Modifie un service Win32 \_ .
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523924"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="a04e6-103">Modifier la méthode de la classe Win32_Service (Mbnapi. h)</span><span class="sxs-lookup"><span data-stu-id="a04e6-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="a04e6-104">La méthode de la classe **change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifie [**un \_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="a04e6-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="a04e6-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a04e6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a04e6-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a04e6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a04e6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a04e6-107">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="a04e6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a04e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04e6-109">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-110">Nom d’affichage du service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-110">The display name of the service.</span></span> <span data-ttu-id="a04e6-111">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="a04e6-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="a04e6-112">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="a04e6-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="a04e6-113">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="a04e6-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="a04e6-114">Contraintes : accepte la même valeur que la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="a04e6-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="a04e6-115">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="a04e6-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-116">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-117">Le chemin d’accès complet au fichier exécutable qui implémente le service, par exemple, « \\ racine_système \\ system32 \\ drivers \\afd.sys ».</span><span class="sxs-lookup"><span data-stu-id="a04e6-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-118">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-119">Type des services fournis aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="a04e6-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="a04e6-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a04e6-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-121">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="a04e6-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-122">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="a04e6-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-123">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="a04e6-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a04e6-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-125">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="a04e6-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a04e6-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-127">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="a04e6-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="a04e6-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-129">Propre processus</span><span class="sxs-lookup"><span data-stu-id="a04e6-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="a04e6-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-131">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="a04e6-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="a04e6-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-133">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="a04e6-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a04e6-134">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-135">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="a04e6-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="a04e6-136">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="a04e6-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="a04e6-137">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="a04e6-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** (0)</span><span class="sxs-lookup"><span data-stu-id="a04e6-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a04e6-139">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="a04e6-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="a04e6-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="a04e6-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a04e6-141">Normal.</span><span class="sxs-lookup"><span data-stu-id="a04e6-141">Normal.</span></span> <span data-ttu-id="a04e6-142">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="a04e6-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="a04e6-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="a04e6-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a04e6-144">Le système est redémarré avec la dernière bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="a04e6-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a04e6-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="a04e6-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a04e6-146">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="a04e6-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a04e6-147">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-148">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="a04e6-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="a04e6-149">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a04e6-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="a04e6-150">Démarrage</span><span class="sxs-lookup"><span data-stu-id="a04e6-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-151">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a04e6-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="a04e6-152">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="a04e6-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-153">Système</span><span class="sxs-lookup"><span data-stu-id="a04e6-153">System</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-154">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a04e6-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="a04e6-155">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="a04e6-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-156">Automatique</span><span class="sxs-lookup"><span data-stu-id="a04e6-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-157">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-158">Manuel</span><span class="sxs-lookup"><span data-stu-id="a04e6-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-159">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="a04e6-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-160">Désactivé</span><span class="sxs-lookup"><span data-stu-id="a04e6-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-161">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="a04e6-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a04e6-162">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-163">Si la **valeur est true**, le service peut créer ou communiquer avec une fenêtre sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="a04e6-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-164">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-165">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a04e6-165">Account name the service runs under.</span></span> <span data-ttu-id="a04e6-166">Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a04e6-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="a04e6-167">Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a04e6-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="a04e6-168">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="a04e6-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="a04e6-169">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a04e6-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="a04e6-170">Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a04e6-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="a04e6-171">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, « DWDOM \\ admin ».</span><span class="sxs-lookup"><span data-stu-id="a04e6-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="a04e6-172">Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="a04e6-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-173">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-174">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="a04e6-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="a04e6-175">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="a04e6-176">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="a04e6-177">Lorsque vous modifiez un service d’un système local à un réseau ou d’un réseau à un système local, *StartPassword* doit être une chaîne vide ("") et non **null**.</span><span class="sxs-lookup"><span data-stu-id="a04e6-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="a04e6-178">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-179">Nom du groupe auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="a04e6-179">Group name that it is associated with.</span></span> <span data-ttu-id="a04e6-180">Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a04e6-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="a04e6-181">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="a04e6-182">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a04e6-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="a04e6-183">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="a04e6-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="a04e6-184">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="a04e6-185">La liste des groupes d’ordre de chargement se trouve dans le registre système à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="a04e6-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="a04e6-186">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="a04e6-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-187">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-188">Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="a04e6-189">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="a04e6-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="a04e6-190">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="a04e6-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="a04e6-191">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a04e6-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="a04e6-192">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-193">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a04e6-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-194">Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="a04e6-195">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="a04e6-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="a04e6-196">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="a04e6-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="a04e6-197">La dépendance sur un service indique que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04e6-198">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a04e6-198">Return value</span></span>

<span data-ttu-id="a04e6-199">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a04e6-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a04e6-200">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a04e6-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a04e6-201">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a04e6-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a04e6-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="a04e6-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-203">0</span><span class="sxs-lookup"><span data-stu-id="a04e6-203">0</span></span>

<span data-ttu-id="a04e6-204">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="a04e6-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-205">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a04e6-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-206">1</span><span class="sxs-lookup"><span data-stu-id="a04e6-206">1</span></span>

<span data-ttu-id="a04e6-207">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a04e6-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-208">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="a04e6-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-209">2</span><span class="sxs-lookup"><span data-stu-id="a04e6-209">2</span></span>

<span data-ttu-id="a04e6-210">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a04e6-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-211">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="a04e6-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-212">3</span><span class="sxs-lookup"><span data-stu-id="a04e6-212">3</span></span>

<span data-ttu-id="a04e6-213">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="a04e6-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-214">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="a04e6-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-215">4</span><span class="sxs-lookup"><span data-stu-id="a04e6-215">4</span></span>

<span data-ttu-id="a04e6-216">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-217">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="a04e6-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-218">5</span><span class="sxs-lookup"><span data-stu-id="a04e6-218">5</span></span>

<span data-ttu-id="a04e6-219">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a04e6-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-220">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="a04e6-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-221">6</span><span class="sxs-lookup"><span data-stu-id="a04e6-221">6</span></span>

<span data-ttu-id="a04e6-222">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="a04e6-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-223">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="a04e6-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-224">7</span><span class="sxs-lookup"><span data-stu-id="a04e6-224">7</span></span>

<span data-ttu-id="a04e6-225">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="a04e6-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-226">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="a04e6-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-227">8</span><span class="sxs-lookup"><span data-stu-id="a04e6-227">8</span></span>

<span data-ttu-id="a04e6-228">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-229">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="a04e6-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-230">9</span><span class="sxs-lookup"><span data-stu-id="a04e6-230">9</span></span>

<span data-ttu-id="a04e6-231">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a04e6-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-232">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="a04e6-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-233">10</span><span class="sxs-lookup"><span data-stu-id="a04e6-233">10</span></span>

<span data-ttu-id="a04e6-234">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-235">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="a04e6-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-236">11</span><span class="sxs-lookup"><span data-stu-id="a04e6-236">11</span></span>

<span data-ttu-id="a04e6-237">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="a04e6-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-238">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="a04e6-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-239">12</span><span class="sxs-lookup"><span data-stu-id="a04e6-239">12</span></span>

<span data-ttu-id="a04e6-240">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-241">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="a04e6-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-242">13</span><span class="sxs-lookup"><span data-stu-id="a04e6-242">13</span></span>

<span data-ttu-id="a04e6-243">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="a04e6-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-244">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="a04e6-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-245">14</span><span class="sxs-lookup"><span data-stu-id="a04e6-245">14</span></span>

<span data-ttu-id="a04e6-246">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-247">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="a04e6-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-248">15</span><span class="sxs-lookup"><span data-stu-id="a04e6-248">15</span></span>

<span data-ttu-id="a04e6-249">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-250">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="a04e6-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-251">16</span><span class="sxs-lookup"><span data-stu-id="a04e6-251">16</span></span>

<span data-ttu-id="a04e6-252">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-253">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="a04e6-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-254">17</span><span class="sxs-lookup"><span data-stu-id="a04e6-254">17</span></span>

<span data-ttu-id="a04e6-255">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-256">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="a04e6-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-257">18</span><span class="sxs-lookup"><span data-stu-id="a04e6-257">18</span></span>

<span data-ttu-id="a04e6-258">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="a04e6-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-259">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="a04e6-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-260">19</span><span class="sxs-lookup"><span data-stu-id="a04e6-260">19</span></span>

<span data-ttu-id="a04e6-261">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="a04e6-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-262">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="a04e6-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-263">20</span><span class="sxs-lookup"><span data-stu-id="a04e6-263">20</span></span>

<span data-ttu-id="a04e6-264">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="a04e6-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-265">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="a04e6-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-266">21</span><span class="sxs-lookup"><span data-stu-id="a04e6-266">21</span></span>

<span data-ttu-id="a04e6-267">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-268">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="a04e6-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-269">22</span><span class="sxs-lookup"><span data-stu-id="a04e6-269">22</span></span>

<span data-ttu-id="a04e6-270">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-271">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="a04e6-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-272">23</span><span class="sxs-lookup"><span data-stu-id="a04e6-272">23</span></span>

<span data-ttu-id="a04e6-273">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-274">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="a04e6-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-275">24</span><span class="sxs-lookup"><span data-stu-id="a04e6-275">24</span></span>

<span data-ttu-id="a04e6-276">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="a04e6-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="a04e6-277">**Autres**</span><span class="sxs-lookup"><span data-stu-id="a04e6-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a04e6-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="a04e6-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a04e6-279">Notes</span><span class="sxs-lookup"><span data-stu-id="a04e6-279">Remarks</span></span>

<span data-ttu-id="a04e6-280">Lorsqu’un ordinateur démarre, tous les services de démarrage automatique démarrent également.</span><span class="sxs-lookup"><span data-stu-id="a04e6-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="a04e6-281">Il peut arriver que l’un de ces services ne puisse pas démarrer avec l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a04e6-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="a04e6-282">Lorsqu’un service échoue pendant le démarrage du système, l’ordinateur effectue une action en fonction de la valeur du code de contrôle d’erreur du service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="a04e6-283">la plupart des services sont installés à l’aide du code de contrôle d’erreur normal.</span><span class="sxs-lookup"><span data-stu-id="a04e6-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="a04e6-284">Quelques-unes des exceptions, qui sont installées à l’aide du code d’erreur ignorer, sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a04e6-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="a04e6-285">Service de réplication de fichiers</span><span class="sxs-lookup"><span data-stu-id="a04e6-285">File Replication Service</span></span>
-   <span data-ttu-id="a04e6-286">Carte à puce</span><span class="sxs-lookup"><span data-stu-id="a04e6-286">Smart Card</span></span>
-   <span data-ttu-id="a04e6-287">Ouverture de session secondaire</span><span class="sxs-lookup"><span data-stu-id="a04e6-287">Secondary Logon</span></span>
-   <span data-ttu-id="a04e6-288">WMI</span><span class="sxs-lookup"><span data-stu-id="a04e6-288">WMI</span></span>

<span data-ttu-id="a04e6-289">Pour les services installés à l’aide du code d’erreur ignorer, aucune notification n’est donnée à l’utilisateur pour lequel le service a échoué.</span><span class="sxs-lookup"><span data-stu-id="a04e6-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="a04e6-290">Si vous préférez que la notification à l’écran indique qu’un service n’a pas pu démarrer, vous pouvez utiliser WMI pour modifier le code de contrôle de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a04e6-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="a04e6-291">Les codes de contrôle d’erreur s’appliquent uniquement au démarrage de l’ordinateur. les codes de contrôle d’erreur ne sont pas utilisés si vous arrêtez, puis essayez de redémarrer un service une fois que l’ordinateur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="a04e6-292">Parfois, vous devrez peut-être modifier le compte sous lequel un service donné s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a04e6-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="a04e6-293">Par exemple, vous pouvez exécuter un service sous un compte d’administration.</span><span class="sxs-lookup"><span data-stu-id="a04e6-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="a04e6-294">Étant donné que cela peut créer une faille de sécurité, vous pouvez basculer le service vers un compte avec moins de privilèges.</span><span class="sxs-lookup"><span data-stu-id="a04e6-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="a04e6-295">Vous pouvez également faire en sorte que les services s’exécutent sous un compte qui est sur le lieu d’être supprimé, ou que vous souhaitiez vous assurer que certains services s’exécutent sous certains comptes sur tous vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="a04e6-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="a04e6-296">Vous pouvez utiliser la méthode **change** de la classe de [**\_ service Win32**](win32-service.md) pour configurer des services à exécuter sous un compte d’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a04e6-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="a04e6-297">Lorsque vous sélectionnez un compte, gardez à l’esprit les points suivants :</span><span class="sxs-lookup"><span data-stu-id="a04e6-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="a04e6-298">Le compte utilisé en tant que compte de service doit avoir le droit d’ouvrir une session en tant que service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="a04e6-299">Ce droit peut être accordé à l’aide de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="a04e6-300">Le compte utilisé en tant que compte de service ne doit pas être membre d’un groupe local, d’un domaine ou d’un groupe administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a04e6-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="a04e6-301">Chaque instance d’un service doit s’exécuter sous un compte d’utilisateur unique.</span><span class="sxs-lookup"><span data-stu-id="a04e6-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="a04e6-302">Cela offre une sécurité supplémentaire et permet d’auditer des instances de service individuelles.</span><span class="sxs-lookup"><span data-stu-id="a04e6-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="a04e6-303">Si le service est interactif, le service doit s’exécuter sous le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a04e6-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="a04e6-304">LocalSystem est requis car une seule station Windows (WinSta0) peut être visible et interactive à la fois.</span><span class="sxs-lookup"><span data-stu-id="a04e6-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="a04e6-305">Si un service s’exécute sous un compte autre que LocalSystem, il s’exécute dans la \\ station Windows par défaut du service 0x03e7, qui est une fenêtre invisible.</span><span class="sxs-lookup"><span data-stu-id="a04e6-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="a04e6-306">Les services qui s’exécutent dans cette station Windows ne peuvent pas recevoir de sortie d’entrée ou d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a04e6-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="a04e6-307">Lorsque vous affectez un compte à un service, le SCM requiert le mot de passe correct pour ce compte avant de procéder à l’attribution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="a04e6-308">Si vous fournissez un mot de passe incorrect, le SCM rejette le compte.</span><span class="sxs-lookup"><span data-stu-id="a04e6-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="a04e6-309">Si vous configurez un compte de service à l’aide du compte LocalSystem, LocalService ou NetworkService, vous n’avez pas besoin de fournir un mot de passe de compte, car ces comptes n’ont pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a04e6-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="a04e6-310">Le SCM stocke le mot de passe du compte dans la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="a04e6-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="a04e6-311">Toutefois, une fois le mot de passe affecté, le SCM ne garantit pas que le mot de passe stocké dans la base de données de services et le mot de passe attribué au compte d’utilisateur dans Active Directory continuent de correspondre.</span><span class="sxs-lookup"><span data-stu-id="a04e6-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="a04e6-312">Par conséquent, une situation semblable à la suivante peut se produire :</span><span class="sxs-lookup"><span data-stu-id="a04e6-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="a04e6-313">Vous configurez un service pour qu’il s’exécute sous un compte d’utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="a04e6-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="a04e6-314">Le service démarre sous ce compte à l’aide du mot de passe du compte actuel.</span><span class="sxs-lookup"><span data-stu-id="a04e6-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="a04e6-315">Vous modifiez le mot de passe du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a04e6-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="a04e6-316">Le service continue à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a04e6-316">The service continues to run.</span></span> <span data-ttu-id="a04e6-317">Toutefois, si le service s’arrête, vous ne pouvez pas le redémarrer, car le SCM continue à utiliser l’ancien mot de passe non valide.</span><span class="sxs-lookup"><span data-stu-id="a04e6-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="a04e6-318">La modification du mot de passe dans Active Directory ne modifie pas le mot de passe stocké dans la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="a04e6-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="a04e6-319">Si vous exécutez des services sous des comptes d’utilisateur standard, vous devez mettre à jour ces mots de passe de service chaque fois que le mot de passe du compte d’utilisateur est modifié.</span><span class="sxs-lookup"><span data-stu-id="a04e6-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="a04e6-320">Cela peut s’avérer particulièrement long si vous ne savez pas quels services s’exécutent sous ce compte ou quels sont les ordinateurs qui exécutent les services sous ce compte.</span><span class="sxs-lookup"><span data-stu-id="a04e6-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="a04e6-321">Heureusement, vous pouvez utiliser WMI pour vérifier les comptes de service sur tous vos ordinateurs et, si nécessaire, modifier le mot de passe du compte de service.</span><span class="sxs-lookup"><span data-stu-id="a04e6-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="a04e6-322">Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un groupe de services système qui définissent des dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a04e6-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="a04e6-323">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="a04e6-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="a04e6-324">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="a04e6-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="a04e6-325">Pour modifier un service d’un service réseau en système local, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a04e6-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="a04e6-326">Pour modifier un service d’un service système local sur un réseau, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a04e6-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="a04e6-327">Exemples</span><span class="sxs-lookup"><span data-stu-id="a04e6-327">Examples</span></span>

<span data-ttu-id="a04e6-328">Le code VBScript suivant modifie le compte de service pour les services qui s’exécutent sous un compte d’utilisateur spécifié sur LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a04e6-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="a04e6-329">Le script VBScript suivant modifie le mot de passe du compte de service pour tous les scripts exécutés sous netsvc</span><span class="sxs-lookup"><span data-stu-id="a04e6-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="a04e6-330">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a04e6-330">Requirements</span></span>



| <span data-ttu-id="a04e6-331">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a04e6-331">Requirement</span></span> | <span data-ttu-id="a04e6-332">Valeur</span><span class="sxs-lookup"><span data-stu-id="a04e6-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a04e6-333">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04e6-333">Minimum supported client</span></span><br/> | <span data-ttu-id="a04e6-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a04e6-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a04e6-335">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04e6-335">Minimum supported server</span></span><br/> | <span data-ttu-id="a04e6-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a04e6-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a04e6-337">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a04e6-337">Namespace</span></span><br/>                | <span data-ttu-id="a04e6-338">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a04e6-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a04e6-339">En-tête</span><span class="sxs-lookup"><span data-stu-id="a04e6-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04e6-340"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04e6-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="a04e6-341">MOF</span><span class="sxs-lookup"><span data-stu-id="a04e6-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a04e6-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a04e6-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a04e6-343">DLL</span><span class="sxs-lookup"><span data-stu-id="a04e6-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04e6-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04e6-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04e6-345">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a04e6-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="a04e6-346">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a04e6-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a04e6-347">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="a04e6-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="a04e6-348">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="a04e6-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


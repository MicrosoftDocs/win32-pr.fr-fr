---
description: Crée un nouveau service géré par le pilote système.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111647"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="4233c-103">Créer une méthode de la \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="4233c-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="4233c-104">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service géré par le pilote système.</span><span class="sxs-lookup"><span data-stu-id="4233c-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="4233c-105">Le *paramètre \_ LoadOrderGroup Win32* représente un regroupement de services système définissant les dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4233c-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="4233c-106">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="4233c-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="4233c-107">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="4233c-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="4233c-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4233c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4233c-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4233c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4233c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4233c-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
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



## <a name="parameters"></a><span data-ttu-id="4233c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4233c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4233c-112">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-113">Nom du service à installer dans la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="4233c-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="4233c-114">La longueur de chaîne maximale est de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="4233c-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="4233c-115">La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="4233c-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="4233c-116">Les barres obliques inverses (/) et les barres obliques inverses ( \\ ) sont des caractères de nom de service non valides.</span><span class="sxs-lookup"><span data-stu-id="4233c-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-117">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-118">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="4233c-118">Display name of the service.</span></span> <span data-ttu-id="4233c-119">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="4233c-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4233c-120">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="4233c-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="4233c-121">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="4233c-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4233c-122">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="4233c-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="4233c-123">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="4233c-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="4233c-124">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-125">Chemin d’accès complet au fichier exécutable qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="4233c-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="4233c-126">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="4233c-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="4233c-127">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-128">Type des services fournis aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="4233c-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="4233c-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4233c-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-130">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="4233c-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="4233c-131">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="4233c-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-132">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="4233c-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="4233c-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4233c-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-134">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="4233c-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="4233c-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4233c-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-136">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="4233c-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="4233c-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4233c-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-138">Propre processus</span><span class="sxs-lookup"><span data-stu-id="4233c-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="4233c-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4233c-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-140">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="4233c-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="4233c-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4233c-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="4233c-142">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="4233c-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4233c-143">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-144">Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="4233c-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="4233c-145">Cette valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4233c-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4233c-146">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="4233c-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="4233c-147">0</span><span class="sxs-lookup"><span data-stu-id="4233c-147">0</span></span>
</dt> <dd>

<span data-ttu-id="4233c-148">Tenir</span><span class="sxs-lookup"><span data-stu-id="4233c-148">"Ignore"</span></span>

<span data-ttu-id="4233c-149">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="4233c-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-150">1</span><span class="sxs-lookup"><span data-stu-id="4233c-150">1</span></span>
</dt> <dd>

<span data-ttu-id="4233c-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="4233c-151">"Normal"</span></span>

<span data-ttu-id="4233c-152">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="4233c-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-153">2</span><span class="sxs-lookup"><span data-stu-id="4233c-153">2</span></span>
</dt> <dd>

<span data-ttu-id="4233c-154">Sérieux</span><span class="sxs-lookup"><span data-stu-id="4233c-154">"Severe"</span></span>

<span data-ttu-id="4233c-155">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="4233c-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-156">3</span><span class="sxs-lookup"><span data-stu-id="4233c-156">3</span></span>
</dt> <dd>

<span data-ttu-id="4233c-157">Critique</span><span class="sxs-lookup"><span data-stu-id="4233c-157">"Critical"</span></span>

<span data-ttu-id="4233c-158">Le système tente de démarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="4233c-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4233c-159">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-160">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="4233c-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4233c-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Partition**</span><span class="sxs-lookup"><span data-stu-id="4233c-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="4233c-162">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4233c-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="4233c-163">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="4233c-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4233c-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Requise**</span><span class="sxs-lookup"><span data-stu-id="4233c-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="4233c-165">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4233c-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4233c-166">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="4233c-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4233c-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique**</span><span class="sxs-lookup"><span data-stu-id="4233c-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="4233c-168">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="4233c-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4233c-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuelle**</span><span class="sxs-lookup"><span data-stu-id="4233c-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="4233c-170">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="4233c-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4233c-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**</span><span class="sxs-lookup"><span data-stu-id="4233c-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="4233c-172">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="4233c-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4233c-173">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-174">Si la **valeur est true**, le service peut créer ou communiquer avec les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="4233c-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-175">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-176">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4233c-176">Account name under which the service runs.</span></span> <span data-ttu-id="4233c-177">Selon le type de service, le nom du compte peut être au \\ format nom_domaine nom_utilisateur ou UPN (user principal name) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="4233c-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="4233c-178">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4233c-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="4233c-179">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="4233c-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="4233c-180">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4233c-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="4233c-181">Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4233c-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="4233c-182">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="4233c-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="4233c-183">Exemple : DWDOM \\ admin</span><span class="sxs-lookup"><span data-stu-id="4233c-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="4233c-184">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-185">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="4233c-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="4233c-186">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4233c-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="4233c-187">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4233c-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-188">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-189">Nom du groupe associé au nouveau service.</span><span class="sxs-lookup"><span data-stu-id="4233c-189">Group name associated with the new service.</span></span> <span data-ttu-id="4233c-190">Les groupes d’ordre de chargement sont contenus dans le registre et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4233c-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="4233c-191">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="4233c-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="4233c-192">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="4233c-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="4233c-193">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="4233c-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="4233c-194">Le registre contient une liste de groupes d’ordre de chargement situés à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="4233c-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="4233c-195">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="4233c-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="4233c-196">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-197">Tableau des groupes d’ordre de chargement qui doivent démarrer avant ce service.</span><span class="sxs-lookup"><span data-stu-id="4233c-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="4233c-198">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="4233c-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4233c-199">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="4233c-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4233c-200">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="4233c-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4233c-201">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour le différencier d’un nom de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4233c-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="4233c-202">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="4233c-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4233c-203">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4233c-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4233c-204">Tableau qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="4233c-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="4233c-205">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="4233c-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4233c-206">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="4233c-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4233c-207">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="4233c-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4233c-208">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4233c-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4233c-209">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4233c-209">Return value</span></span>

<span data-ttu-id="4233c-210">Retourne la valeur 0 (zéro) si le service a été créé avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4233c-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4233c-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4233c-211">Requirements</span></span>



| <span data-ttu-id="4233c-212">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4233c-212">Requirement</span></span> | <span data-ttu-id="4233c-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="4233c-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4233c-214">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4233c-214">Minimum supported client</span></span><br/> | <span data-ttu-id="4233c-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4233c-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4233c-216">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4233c-216">Minimum supported server</span></span><br/> | <span data-ttu-id="4233c-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4233c-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4233c-218">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4233c-218">Namespace</span></span><br/>                | <span data-ttu-id="4233c-219">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4233c-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4233c-220">MOF</span><span class="sxs-lookup"><span data-stu-id="4233c-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4233c-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4233c-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4233c-222">DLL</span><span class="sxs-lookup"><span data-stu-id="4233c-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4233c-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4233c-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4233c-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4233c-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="4233c-225">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4233c-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4233c-226">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="4233c-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


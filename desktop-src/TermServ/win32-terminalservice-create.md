---
title: Créer une méthode de la classe Win32_Service (Services Bureau à distance)
description: 'Créer une méthode de la classe Win32_Service (Services Bureau à distance) : crée un nouveau service système.'
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_Service Class
- Win32_Service de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b776d3e451d84c63be5bb61b98ed22081e1a29
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387118"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="f855b-106">Créer une méthode de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="f855b-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="f855b-107">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service système.</span><span class="sxs-lookup"><span data-stu-id="f855b-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="f855b-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f855b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f855b-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f855b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f855b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f855b-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f855b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f855b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f855b-112">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-113">Nom du service à installer dans la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="f855b-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="f855b-114">La longueur de chaîne maximale est de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="f855b-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="f855b-115">La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="f855b-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="f855b-116">Les barres obliques inverses (/) et les barres obliques inverses ( \\ \\ ) sont des caractères de nom de service non valides.</span><span class="sxs-lookup"><span data-stu-id="f855b-116">Forward-slashes (/) and double back-slashes (\\\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-117">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-118">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="f855b-118">Display name of the service.</span></span> <span data-ttu-id="f855b-119">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="f855b-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="f855b-120">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="f855b-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="f855b-121">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="f855b-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="f855b-122">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="f855b-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="f855b-123">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="f855b-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="f855b-124">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-125">Chemin d’accès complet au fichier exécutable qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="f855b-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="f855b-126">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="f855b-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="f855b-127">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-128">Type de services fourni aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="f855b-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="f855b-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f855b-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-130">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="f855b-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="f855b-131">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="f855b-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-132">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="f855b-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="f855b-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f855b-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-134">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="f855b-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="f855b-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f855b-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-136">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="f855b-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="f855b-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="f855b-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-138">Propre processus</span><span class="sxs-lookup"><span data-stu-id="f855b-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="f855b-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="f855b-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-140">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="f855b-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="f855b-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="f855b-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="f855b-142">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="f855b-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f855b-143">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-144">Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="f855b-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="f855b-145">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f855b-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="f855b-146">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="f855b-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="f855b-147">0</span><span class="sxs-lookup"><span data-stu-id="f855b-147">0</span></span>
</dt> <dd>

<span data-ttu-id="f855b-148">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="f855b-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-149">1</span><span class="sxs-lookup"><span data-stu-id="f855b-149">1</span></span>
</dt> <dd>

<span data-ttu-id="f855b-150">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="f855b-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-151">2</span><span class="sxs-lookup"><span data-stu-id="f855b-151">2</span></span>
</dt> <dd>

<span data-ttu-id="f855b-152">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="f855b-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-153">3</span><span class="sxs-lookup"><span data-stu-id="f855b-153">3</span></span>
</dt> <dd>

<span data-ttu-id="f855b-154">Le système tente de démarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="f855b-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f855b-155">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-156">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="f855b-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="f855b-157">Démarrage</span><span class="sxs-lookup"><span data-stu-id="f855b-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="f855b-158">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f855b-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="f855b-159">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="f855b-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-160">Système</span><span class="sxs-lookup"><span data-stu-id="f855b-160">System</span></span>
</dt> <dd>

<span data-ttu-id="f855b-161">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f855b-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f855b-162">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="f855b-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-163">Automatique</span><span class="sxs-lookup"><span data-stu-id="f855b-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="f855b-164">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="f855b-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-165">Manuel</span><span class="sxs-lookup"><span data-stu-id="f855b-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="f855b-166">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f855b-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-167">Désactivé</span><span class="sxs-lookup"><span data-stu-id="f855b-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="f855b-168">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="f855b-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f855b-169">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-170">Si la **valeur est true**, le service peut créer ou communiquer avec Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="f855b-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-171">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-172">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="f855b-172">Account name under which the service runs.</span></span> <span data-ttu-id="f855b-173">Selon le type de service, le nom du compte peut être au \\ format nom_domaine nom_utilisateur ou UPN (user principal name) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="f855b-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="f855b-174">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="f855b-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="f855b-175">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f855b-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="f855b-176">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f855b-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="f855b-177">Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="f855b-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="f855b-178">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="f855b-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="f855b-179">Exemple : DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="f855b-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-180">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-181">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="f855b-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="f855b-182">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f855b-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="f855b-183">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f855b-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-184">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-185">Nom du groupe associé au nouveau service.</span><span class="sxs-lookup"><span data-stu-id="f855b-185">Group name associated with the new service.</span></span> <span data-ttu-id="f855b-186">Les groupes d’ordre de chargement sont contenus dans le registre et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f855b-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="f855b-187">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="f855b-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="f855b-188">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="f855b-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="f855b-189">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="f855b-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="f855b-190">Le registre contient une liste de groupes d’ordre de chargement situés à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="f855b-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="f855b-191">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="f855b-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="f855b-192">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-193">Tableau des groupes d’ordre de chargement qui doivent démarrer avant ce service.</span><span class="sxs-lookup"><span data-stu-id="f855b-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="f855b-194">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="f855b-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f855b-195">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="f855b-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f855b-196">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="f855b-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f855b-197">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour le différencier d’un nom de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f855b-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="f855b-198">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="f855b-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-199">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f855b-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f855b-200">Tableau qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="f855b-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="f855b-201">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="f855b-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f855b-202">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="f855b-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f855b-203">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="f855b-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f855b-204">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f855b-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f855b-205">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f855b-205">Return value</span></span>

<span data-ttu-id="f855b-206">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f855b-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="f855b-207">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f855b-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f855b-208">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f855b-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f855b-209">**0**</span><span class="sxs-lookup"><span data-stu-id="f855b-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-210">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="f855b-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-211">**1**</span><span class="sxs-lookup"><span data-stu-id="f855b-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-212">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f855b-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-213">**2**</span><span class="sxs-lookup"><span data-stu-id="f855b-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-214">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f855b-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-215">**3**</span><span class="sxs-lookup"><span data-stu-id="f855b-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-216">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="f855b-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-217">**4**</span><span class="sxs-lookup"><span data-stu-id="f855b-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-218">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="f855b-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-219">**5**</span><span class="sxs-lookup"><span data-stu-id="f855b-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-220">Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété **State** de la classe [**\_ BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) est égal à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="f855b-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-221">**6**</span><span class="sxs-lookup"><span data-stu-id="f855b-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-222">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="f855b-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-223">**7**</span><span class="sxs-lookup"><span data-stu-id="f855b-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-224">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="f855b-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-225">**8**</span><span class="sxs-lookup"><span data-stu-id="f855b-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-226">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="f855b-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-227">**9**</span><span class="sxs-lookup"><span data-stu-id="f855b-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-228">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f855b-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-229">**10**</span><span class="sxs-lookup"><span data-stu-id="f855b-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-230">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f855b-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-231">**11**</span><span class="sxs-lookup"><span data-stu-id="f855b-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-232">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="f855b-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-233">**12**</span><span class="sxs-lookup"><span data-stu-id="f855b-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-234">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="f855b-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-235">**13**</span><span class="sxs-lookup"><span data-stu-id="f855b-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-236">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="f855b-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-237">**14**</span><span class="sxs-lookup"><span data-stu-id="f855b-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-238">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="f855b-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-239">**15**</span><span class="sxs-lookup"><span data-stu-id="f855b-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-240">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="f855b-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-241">**16**</span><span class="sxs-lookup"><span data-stu-id="f855b-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-242">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="f855b-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-243">**17**</span><span class="sxs-lookup"><span data-stu-id="f855b-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-244">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f855b-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-245">**19**</span><span class="sxs-lookup"><span data-stu-id="f855b-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-246">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="f855b-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-247">**19**</span><span class="sxs-lookup"><span data-stu-id="f855b-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-248">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="f855b-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-249">**20**</span><span class="sxs-lookup"><span data-stu-id="f855b-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-250">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="f855b-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-251">**21**</span><span class="sxs-lookup"><span data-stu-id="f855b-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-252">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="f855b-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-253">**22**</span><span class="sxs-lookup"><span data-stu-id="f855b-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-254">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="f855b-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-255">**23**</span><span class="sxs-lookup"><span data-stu-id="f855b-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-256">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="f855b-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-257">**24**</span><span class="sxs-lookup"><span data-stu-id="f855b-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f855b-258">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="f855b-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f855b-259">Remarques</span><span class="sxs-lookup"><span data-stu-id="f855b-259">Remarks</span></span>

<span data-ttu-id="f855b-260">Les services sont généralement installés de l’une des deux manières suivantes : dans le cadre de l’installation du système d’exploitation ou à l’aide d’un programme d’installation fourni par le développeur du service.</span><span class="sxs-lookup"><span data-stu-id="f855b-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="f855b-261">Toutefois, certains services, en particulier ceux créés en interne, peuvent ne pas avoir de programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="f855b-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="f855b-262">Dans ces instances, vous pouvez utiliser la méthode **Create** pour installer des services par programme.</span><span class="sxs-lookup"><span data-stu-id="f855b-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="f855b-263">Malgré le nom, la méthode de création ne crée pas réellement un service ; Il installe simplement un service existant.</span><span class="sxs-lookup"><span data-stu-id="f855b-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="f855b-264">Pour utiliser cette commande, vous devez copier le fichier exécutable du service sur un ordinateur, puis utiliser **créer** pour installer le service.</span><span class="sxs-lookup"><span data-stu-id="f855b-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="f855b-265">La méthode **Create** est semblable à la méthode [**change**](win32-terminalservice-change.md) .</span><span class="sxs-lookup"><span data-stu-id="f855b-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="f855b-266">Dans les deux cas, les propriétés du service sont passées en tant que paramètres à la méthode.</span><span class="sxs-lookup"><span data-stu-id="f855b-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="f855b-267">Comme avec les paramètres utilisés avec la méthode **change** , l’ordre dans lequel ces paramètres sont transmis est très important.</span><span class="sxs-lookup"><span data-stu-id="f855b-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="f855b-268">Le paramètre *LoadOrderGroup* représente un regroupement de services système définissant les dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f855b-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="f855b-269">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="f855b-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="f855b-270">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="f855b-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f855b-271">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f855b-271">Requirements</span></span>



| <span data-ttu-id="f855b-272">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f855b-272">Requirement</span></span> | <span data-ttu-id="f855b-273">Value</span><span class="sxs-lookup"><span data-stu-id="f855b-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f855b-274">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f855b-274">Minimum supported client</span></span><br/> | <span data-ttu-id="f855b-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f855b-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f855b-276">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f855b-276">Minimum supported server</span></span><br/> | <span data-ttu-id="f855b-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f855b-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f855b-278">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f855b-278">Namespace</span></span><br/>                | <span data-ttu-id="f855b-279">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f855b-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f855b-280">MOF</span><span class="sxs-lookup"><span data-stu-id="f855b-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f855b-281"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f855b-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f855b-282">DLL</span><span class="sxs-lookup"><span data-stu-id="f855b-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f855b-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f855b-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f855b-284">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f855b-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f855b-285">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="f855b-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="f855b-286">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f855b-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="f855b-287">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f855b-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f855b-288">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="f855b-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


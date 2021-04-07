---
description: Crée un nouveau service système.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749037"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="7f62c-103">Créer une méthode de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7f62c-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7f62c-104">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="7f62c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7f62c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7f62c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7f62c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f62c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f62c-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7f62c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f62c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f62c-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-110">Nom du service à installer dans la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="7f62c-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="7f62c-111">La longueur de chaîne maximale est de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="7f62c-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="7f62c-112">La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="7f62c-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="7f62c-113">Les barres obliques inverses (/) et les barres obliques inverses ( \\ ) sont des caractères de nom de service non valides.</span><span class="sxs-lookup"><span data-stu-id="7f62c-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-114">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-115">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-115">Display name of the service.</span></span> <span data-ttu-id="7f62c-116">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="7f62c-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="7f62c-117">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="7f62c-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="7f62c-118">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="7f62c-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="7f62c-119">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="7f62c-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="7f62c-120">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="7f62c-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-121">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-122">Chemin d’accès complet au fichier exécutable qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="7f62c-123">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="7f62c-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-124">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-125">Type de services fourni aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="7f62c-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="7f62c-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f62c-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-127">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="7f62c-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-128">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="7f62c-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-129">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="7f62c-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="7f62c-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-131">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="7f62c-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="7f62c-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-133">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="7f62c-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="7f62c-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-135">Propre processus</span><span class="sxs-lookup"><span data-stu-id="7f62c-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="7f62c-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-137">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="7f62c-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="7f62c-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-139">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="7f62c-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7f62c-140">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-141">Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="7f62c-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="7f62c-142">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="7f62c-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="7f62c-143">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="7f62c-144">0</span><span class="sxs-lookup"><span data-stu-id="7f62c-144">0</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-145">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="7f62c-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-146">1</span><span class="sxs-lookup"><span data-stu-id="7f62c-146">1</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-147">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="7f62c-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-148">2</span><span class="sxs-lookup"><span data-stu-id="7f62c-148">2</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-149">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="7f62c-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-150">3</span><span class="sxs-lookup"><span data-stu-id="7f62c-150">3</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-151">Le système tente de démarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="7f62c-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7f62c-152">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-153">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="7f62c-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="7f62c-154">Démarrage</span><span class="sxs-lookup"><span data-stu-id="7f62c-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-155">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f62c-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="7f62c-156">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="7f62c-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-157">Système</span><span class="sxs-lookup"><span data-stu-id="7f62c-157">System</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-158">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f62c-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="7f62c-159">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="7f62c-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-160">Automatique</span><span class="sxs-lookup"><span data-stu-id="7f62c-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-161">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-162">Manuel</span><span class="sxs-lookup"><span data-stu-id="7f62c-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-163">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="7f62c-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-164">Désactivé</span><span class="sxs-lookup"><span data-stu-id="7f62c-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-165">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="7f62c-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7f62c-166">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-167">Si la **valeur est true**, le service peut créer ou communiquer avec Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="7f62c-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-168">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-169">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="7f62c-169">Account name under which the service runs.</span></span> <span data-ttu-id="7f62c-170">Selon le type de service, le nom du compte peut être au \\ format nom_domaine nom_utilisateur ou UPN (user principal name) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="7f62c-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="7f62c-171">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="7f62c-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="7f62c-172">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f62c-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="7f62c-173">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="7f62c-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="7f62c-174">Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7f62c-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="7f62c-175">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="7f62c-176">Exemple : DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="7f62c-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-177">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-178">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="7f62c-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="7f62c-179">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7f62c-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="7f62c-180">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7f62c-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-181">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-182">Nom du groupe associé au nouveau service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-182">Group name associated with the new service.</span></span> <span data-ttu-id="7f62c-183">Les groupes d’ordre de chargement sont contenus dans le registre et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f62c-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="7f62c-184">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="7f62c-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="7f62c-185">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="7f62c-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="7f62c-186">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="7f62c-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="7f62c-187">Le registre contient une liste de groupes d’ordre de chargement situés à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="7f62c-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="7f62c-188">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="7f62c-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-189">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-190">Tableau des groupes d’ordre de chargement qui doivent démarrer avant ce service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="7f62c-191">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="7f62c-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="7f62c-192">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="7f62c-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="7f62c-193">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="7f62c-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="7f62c-194">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour le différencier d’un nom de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7f62c-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="7f62c-195">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="7f62c-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-196">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f62c-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-197">Tableau qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="7f62c-198">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="7f62c-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="7f62c-199">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="7f62c-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="7f62c-200">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="7f62c-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="7f62c-201">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7f62c-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f62c-202">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f62c-202">Return value</span></span>

<span data-ttu-id="7f62c-203">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7f62c-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="7f62c-204">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7f62c-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7f62c-205">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7f62c-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7f62c-206">**0**</span><span class="sxs-lookup"><span data-stu-id="7f62c-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-207">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="7f62c-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-208">**1**</span><span class="sxs-lookup"><span data-stu-id="7f62c-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-209">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7f62c-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-210">**2**</span><span class="sxs-lookup"><span data-stu-id="7f62c-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-211">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7f62c-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-212">**3**</span><span class="sxs-lookup"><span data-stu-id="7f62c-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-213">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="7f62c-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-214">**4**</span><span class="sxs-lookup"><span data-stu-id="7f62c-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-215">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-216">**5**</span><span class="sxs-lookup"><span data-stu-id="7f62c-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-217">Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété **State** de la classe [**\_ BaseService Win32**](win32-baseservice.md) ) est égal à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="7f62c-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-218">**6**</span><span class="sxs-lookup"><span data-stu-id="7f62c-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-219">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="7f62c-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-220">**7**</span><span class="sxs-lookup"><span data-stu-id="7f62c-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-221">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="7f62c-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-222">**8**</span><span class="sxs-lookup"><span data-stu-id="7f62c-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-223">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-224">**9**</span><span class="sxs-lookup"><span data-stu-id="7f62c-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-225">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7f62c-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-226">**10**</span><span class="sxs-lookup"><span data-stu-id="7f62c-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-227">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7f62c-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-228">**11**</span><span class="sxs-lookup"><span data-stu-id="7f62c-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-229">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="7f62c-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-230">**12**</span><span class="sxs-lookup"><span data-stu-id="7f62c-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-231">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-232">**13**</span><span class="sxs-lookup"><span data-stu-id="7f62c-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-233">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="7f62c-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-234">**14**</span><span class="sxs-lookup"><span data-stu-id="7f62c-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-235">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-236">**15**</span><span class="sxs-lookup"><span data-stu-id="7f62c-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-237">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-238">**16**</span><span class="sxs-lookup"><span data-stu-id="7f62c-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-239">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-240">**17**</span><span class="sxs-lookup"><span data-stu-id="7f62c-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-241">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7f62c-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-242">**19**</span><span class="sxs-lookup"><span data-stu-id="7f62c-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-243">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="7f62c-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-244">**19**</span><span class="sxs-lookup"><span data-stu-id="7f62c-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-245">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="7f62c-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-246">**20**</span><span class="sxs-lookup"><span data-stu-id="7f62c-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-247">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7f62c-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-248">**21**</span><span class="sxs-lookup"><span data-stu-id="7f62c-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-249">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-250">**22**</span><span class="sxs-lookup"><span data-stu-id="7f62c-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-251">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-252">**23**</span><span class="sxs-lookup"><span data-stu-id="7f62c-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-253">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7f62c-254">**24**</span><span class="sxs-lookup"><span data-stu-id="7f62c-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="7f62c-255">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="7f62c-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f62c-256">Notes</span><span class="sxs-lookup"><span data-stu-id="7f62c-256">Remarks</span></span>

<span data-ttu-id="7f62c-257">Les services sont généralement installés de l’une des deux manières suivantes : dans le cadre de l’installation du système d’exploitation ou à l’aide d’un programme d’installation fourni par le développeur du service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="7f62c-258">Toutefois, certains services, en particulier ceux créés en interne, peuvent ne pas avoir de programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="7f62c-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="7f62c-259">Dans ces instances, vous pouvez utiliser la méthode **Create** pour installer des services par programme.</span><span class="sxs-lookup"><span data-stu-id="7f62c-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="7f62c-260">Malgré le nom, la méthode de création ne crée pas réellement un service ; Il installe simplement un service existant.</span><span class="sxs-lookup"><span data-stu-id="7f62c-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="7f62c-261">Pour utiliser cette commande, vous devez copier le fichier exécutable du service sur un ordinateur, puis utiliser **créer** pour installer le service.</span><span class="sxs-lookup"><span data-stu-id="7f62c-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="7f62c-262">La méthode **Create** est semblable à la méthode [**change**](change-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="7f62c-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="7f62c-263">Dans les deux cas, les propriétés du service sont passées en tant que paramètres à la méthode.</span><span class="sxs-lookup"><span data-stu-id="7f62c-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="7f62c-264">Comme avec les paramètres utilisés avec la méthode **change** , l’ordre dans lequel ces paramètres sont transmis est très important.</span><span class="sxs-lookup"><span data-stu-id="7f62c-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="7f62c-265">Le paramètre *LoadOrderGroup* représente un regroupement de services système définissant les dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7f62c-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="7f62c-266">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="7f62c-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="7f62c-267">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="7f62c-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="7f62c-268">Exemples</span><span class="sxs-lookup"><span data-stu-id="7f62c-268">Examples</span></span>

<span data-ttu-id="7f62c-269">Le VBScript suivant installe un service nommé DbService</span><span class="sxs-lookup"><span data-stu-id="7f62c-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="7f62c-270">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f62c-270">Requirements</span></span>



| <span data-ttu-id="7f62c-271">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f62c-271">Requirement</span></span> | <span data-ttu-id="7f62c-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f62c-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f62c-273">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f62c-273">Minimum supported client</span></span><br/> | <span data-ttu-id="7f62c-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f62c-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f62c-275">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f62c-275">Minimum supported server</span></span><br/> | <span data-ttu-id="7f62c-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f62c-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f62c-277">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f62c-277">Namespace</span></span><br/>                | <span data-ttu-id="7f62c-278">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7f62c-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f62c-279">MOF</span><span class="sxs-lookup"><span data-stu-id="7f62c-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f62c-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f62c-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f62c-281">DLL</span><span class="sxs-lookup"><span data-stu-id="7f62c-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f62c-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f62c-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f62c-283">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f62c-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f62c-284">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f62c-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7f62c-285">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="7f62c-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="7f62c-286">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="7f62c-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


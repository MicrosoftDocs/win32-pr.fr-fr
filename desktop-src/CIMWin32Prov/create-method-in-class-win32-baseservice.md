---
description: Crée un nouveau service.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110602"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="ca175-103">Créer une méthode de la \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="ca175-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="ca175-104">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service.</span><span class="sxs-lookup"><span data-stu-id="ca175-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="ca175-105">Le paramètre *LoadOrderGroup* représente un regroupement de services système définissant les dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ca175-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="ca175-106">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="ca175-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="ca175-107">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="ca175-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="ca175-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca175-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca175-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca175-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca175-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca175-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ca175-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca175-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca175-112">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-113">Nom du service à installer dans la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="ca175-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="ca175-114">La longueur de chaîne maximale est de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="ca175-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="ca175-115">La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="ca175-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="ca175-116">Les barres obliques inverses (/) et les barres obliques inverses ( \\ ) sont des caractères de nom de service non valides.</span><span class="sxs-lookup"><span data-stu-id="ca175-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-117">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-118">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="ca175-118">Display name of the service.</span></span> <span data-ttu-id="ca175-119">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="ca175-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="ca175-120">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="ca175-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="ca175-121">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="ca175-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="ca175-122">Contraintes : accepte la même valeur que le paramètre *Name* .</span><span class="sxs-lookup"><span data-stu-id="ca175-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="ca175-123">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="ca175-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="ca175-124">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-125">Chemin d’accès complet au fichier exécutable qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="ca175-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="ca175-126">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="ca175-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="ca175-127">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-128">Type de services fourni aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="ca175-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="ca175-129">La valeur est une bitmap.</span><span class="sxs-lookup"><span data-stu-id="ca175-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="ca175-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Pilote de noyau** (1)</span><span class="sxs-lookup"><span data-stu-id="ca175-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="ca175-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Pilote du système de fichiers** (2)</span><span class="sxs-lookup"><span data-stu-id="ca175-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="ca175-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptateur** (4)</span><span class="sxs-lookup"><span data-stu-id="ca175-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="ca175-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Pilote de reconnaissance** (8)</span><span class="sxs-lookup"><span data-stu-id="ca175-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="ca175-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Propre processus** (16)</span><span class="sxs-lookup"><span data-stu-id="ca175-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="ca175-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processus de partage** (32)</span><span class="sxs-lookup"><span data-stu-id="ca175-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="ca175-136">256</span><span class="sxs-lookup"><span data-stu-id="ca175-136">256</span></span>
</dt> <dd>

<span data-ttu-id="ca175-137">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="ca175-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ca175-138">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-139">Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="ca175-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="ca175-140">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ca175-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="ca175-141">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="ca175-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="ca175-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** (0)</span><span class="sxs-lookup"><span data-stu-id="ca175-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ca175-143">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="ca175-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="ca175-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="ca175-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ca175-145">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="ca175-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="ca175-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="ca175-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ca175-147">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="ca175-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="ca175-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="ca175-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ca175-149">Le système tente de démarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="ca175-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca175-150">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-151">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="ca175-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="ca175-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ca175-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="ca175-153">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ca175-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="ca175-154">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="ca175-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="ca175-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="ca175-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="ca175-156">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ca175-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="ca175-157">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="ca175-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="ca175-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="ca175-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="ca175-159">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="ca175-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="ca175-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="ca175-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="ca175-161">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ca175-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ca175-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="ca175-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="ca175-163">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="ca175-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca175-164">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-165">Si la **valeur est true**, le service peut créer ou communiquer avec Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ca175-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-166">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-167">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="ca175-167">Account name under which the service runs.</span></span> <span data-ttu-id="ca175-168">Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="ca175-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="ca175-169">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="ca175-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="ca175-170">Si le compte appartient au domaine intégré,». \\ Nom d’utilisateur» peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="ca175-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="ca175-171">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="ca175-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="ca175-172">Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="ca175-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="ca175-173">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="ca175-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="ca175-174">Exemple : DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="ca175-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-175">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-176">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="ca175-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="ca175-177">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ca175-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="ca175-178">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ca175-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-179">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-180">Nom du groupe associé au nouveau service.</span><span class="sxs-lookup"><span data-stu-id="ca175-180">Group name associated with the new service.</span></span> <span data-ttu-id="ca175-181">Les groupes d’ordre de chargement sont contenus dans le registre et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ca175-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="ca175-182">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca175-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="ca175-183">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="ca175-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="ca175-184">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca175-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="ca175-185">Le registre contient une liste de groupes d’ordre de chargement situés à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="ca175-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="ca175-186">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="ca175-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="ca175-187">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-188">Tableau des groupes d’ordre de chargement qui doivent démarrer avant ce service.</span><span class="sxs-lookup"><span data-stu-id="ca175-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="ca175-189">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="ca175-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="ca175-190">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="ca175-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="ca175-191">Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="ca175-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="ca175-192">Les noms de groupes doivent être préfixés par l' \_ identificateur de groupe SC \_ (défini dans le fichier winsvc. h) pour le différencier d’un nom de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ca175-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="ca175-193">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="ca175-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-194">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca175-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca175-195">Tableau qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="ca175-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="ca175-196">Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="ca175-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="ca175-197">Dans Visual Basic ou un script, vous pouvez transmettre un vbArray.</span><span class="sxs-lookup"><span data-stu-id="ca175-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="ca175-198">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="ca175-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="ca175-199">La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ca175-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca175-200">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca175-200">Return value</span></span>

<span data-ttu-id="ca175-201">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ca175-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca175-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="ca175-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-203">0</span><span class="sxs-lookup"><span data-stu-id="ca175-203">0</span></span>

<span data-ttu-id="ca175-204">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="ca175-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-205">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="ca175-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-206">1</span><span class="sxs-lookup"><span data-stu-id="ca175-206">1</span></span>

<span data-ttu-id="ca175-207">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca175-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-208">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="ca175-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-209">2</span><span class="sxs-lookup"><span data-stu-id="ca175-209">2</span></span>

<span data-ttu-id="ca175-210">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ca175-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-211">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="ca175-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-212">3</span><span class="sxs-lookup"><span data-stu-id="ca175-212">3</span></span>

<span data-ttu-id="ca175-213">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="ca175-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-214">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="ca175-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-215">4</span><span class="sxs-lookup"><span data-stu-id="ca175-215">4</span></span>

<span data-ttu-id="ca175-216">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="ca175-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-217">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="ca175-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-218">5</span><span class="sxs-lookup"><span data-stu-id="ca175-218">5</span></span>

<span data-ttu-id="ca175-219">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ca175-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-220">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="ca175-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-221">6</span><span class="sxs-lookup"><span data-stu-id="ca175-221">6</span></span>

<span data-ttu-id="ca175-222">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="ca175-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-223">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="ca175-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-224">7</span><span class="sxs-lookup"><span data-stu-id="ca175-224">7</span></span>

<span data-ttu-id="ca175-225">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="ca175-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-226">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="ca175-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-227">8</span><span class="sxs-lookup"><span data-stu-id="ca175-227">8</span></span>

<span data-ttu-id="ca175-228">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="ca175-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-229">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="ca175-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-230">9</span><span class="sxs-lookup"><span data-stu-id="ca175-230">9</span></span>

<span data-ttu-id="ca175-231">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ca175-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-232">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="ca175-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-233">10</span><span class="sxs-lookup"><span data-stu-id="ca175-233">10</span></span>

<span data-ttu-id="ca175-234">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="ca175-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-235">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="ca175-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-236">11</span><span class="sxs-lookup"><span data-stu-id="ca175-236">11</span></span>

<span data-ttu-id="ca175-237">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="ca175-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-238">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="ca175-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-239">12</span><span class="sxs-lookup"><span data-stu-id="ca175-239">12</span></span>

<span data-ttu-id="ca175-240">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="ca175-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-241">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="ca175-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-242">13</span><span class="sxs-lookup"><span data-stu-id="ca175-242">13</span></span>

<span data-ttu-id="ca175-243">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="ca175-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-244">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="ca175-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-245">14</span><span class="sxs-lookup"><span data-stu-id="ca175-245">14</span></span>

<span data-ttu-id="ca175-246">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="ca175-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-247">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="ca175-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-248">15</span><span class="sxs-lookup"><span data-stu-id="ca175-248">15</span></span>

<span data-ttu-id="ca175-249">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="ca175-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-250">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="ca175-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-251">16</span><span class="sxs-lookup"><span data-stu-id="ca175-251">16</span></span>

<span data-ttu-id="ca175-252">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="ca175-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-253">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="ca175-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-254">17</span><span class="sxs-lookup"><span data-stu-id="ca175-254">17</span></span>

<span data-ttu-id="ca175-255">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="ca175-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-256">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="ca175-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-257">18</span><span class="sxs-lookup"><span data-stu-id="ca175-257">18</span></span>

<span data-ttu-id="ca175-258">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="ca175-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-259">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="ca175-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-260">19</span><span class="sxs-lookup"><span data-stu-id="ca175-260">19</span></span>

<span data-ttu-id="ca175-261">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="ca175-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-262">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="ca175-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-263">20</span><span class="sxs-lookup"><span data-stu-id="ca175-263">20</span></span>

<span data-ttu-id="ca175-264">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="ca175-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-265">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="ca175-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-266">21</span><span class="sxs-lookup"><span data-stu-id="ca175-266">21</span></span>

<span data-ttu-id="ca175-267">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="ca175-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-268">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="ca175-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-269">22</span><span class="sxs-lookup"><span data-stu-id="ca175-269">22</span></span>

<span data-ttu-id="ca175-270">Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="ca175-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-271">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="ca175-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-272">23</span><span class="sxs-lookup"><span data-stu-id="ca175-272">23</span></span>

<span data-ttu-id="ca175-273">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="ca175-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-274">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="ca175-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-275">24</span><span class="sxs-lookup"><span data-stu-id="ca175-275">24</span></span>

<span data-ttu-id="ca175-276">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="ca175-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="ca175-277">**Autres**</span><span class="sxs-lookup"><span data-stu-id="ca175-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ca175-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="ca175-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca175-279">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca175-279">Requirements</span></span>



| <span data-ttu-id="ca175-280">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca175-280">Requirement</span></span> | <span data-ttu-id="ca175-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca175-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca175-282">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca175-282">Minimum supported client</span></span><br/> | <span data-ttu-id="ca175-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca175-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca175-284">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca175-284">Minimum supported server</span></span><br/> | <span data-ttu-id="ca175-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca175-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca175-286">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca175-286">Namespace</span></span><br/>                | <span data-ttu-id="ca175-287">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ca175-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca175-288">MOF</span><span class="sxs-lookup"><span data-stu-id="ca175-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca175-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca175-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca175-290">DLL</span><span class="sxs-lookup"><span data-stu-id="ca175-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca175-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca175-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca175-292">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca175-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca175-293">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca175-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca175-294">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="ca175-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


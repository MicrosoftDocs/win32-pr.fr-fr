---
title: Modifier la méthode de la classe Win32_Service (Mbnapi. h) (TerminalService)
description: Modifie un TerminalService Win32 \_ .
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode de modification
- Services Bureau à distance de la méthode de modification, classe Win32_Service
- Services Bureau à distance de la classe Win32_Service, méthode change
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106539319"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="0db77-106">Méthode change de la classe Win32_Service (Mbnapi. h)-TerminalService</span><span class="sxs-lookup"><span data-stu-id="0db77-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="0db77-107">La méthode **change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifie un [**\_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="0db77-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="0db77-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0db77-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0db77-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0db77-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0db77-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0db77-110">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="0db77-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0db77-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db77-112">*DisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-113">Nom d’affichage du service.</span><span class="sxs-lookup"><span data-stu-id="0db77-113">The display name of the service.</span></span> <span data-ttu-id="0db77-114">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="0db77-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="0db77-115">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="0db77-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="0db77-116">Les comparaisons *DisplayName* ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="0db77-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="0db77-117">Contraintes : accepte la même valeur que la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="0db77-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="0db77-118">Exemple : « Atdisk ».</span><span class="sxs-lookup"><span data-stu-id="0db77-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="0db77-119">*Nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-120">Le chemin d’accès complet au fichier exécutable qui implémente le service, par exemple, « \\ racine_système \\ system32 \\ drivers \\afd.sys ».</span><span class="sxs-lookup"><span data-stu-id="0db77-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="0db77-121">*ServiceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-122">Type des services fournis aux processus qui les appellent.</span><span class="sxs-lookup"><span data-stu-id="0db77-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="0db77-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0db77-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-124">Pilote du noyau</span><span class="sxs-lookup"><span data-stu-id="0db77-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="0db77-125">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="0db77-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-126">Pilote du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="0db77-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="0db77-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="0db77-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-128">Adaptateur</span><span class="sxs-lookup"><span data-stu-id="0db77-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="0db77-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0db77-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-130">Pilote de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="0db77-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="0db77-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="0db77-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-132">Propre processus</span><span class="sxs-lookup"><span data-stu-id="0db77-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="0db77-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="0db77-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-134">Processus de partage</span><span class="sxs-lookup"><span data-stu-id="0db77-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="0db77-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="0db77-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="0db77-136">Processus interactif</span><span class="sxs-lookup"><span data-stu-id="0db77-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0db77-137">*ErrorControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-138">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="0db77-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="0db77-139">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="0db77-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="0db77-140">Toutes les erreurs sont consignées par le système.</span><span class="sxs-lookup"><span data-stu-id="0db77-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="0db77-141">0</span><span class="sxs-lookup"><span data-stu-id="0db77-141">0</span></span>
</dt> <dd>

<span data-ttu-id="0db77-142">**Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="0db77-142">**Ignore**.</span></span> <span data-ttu-id="0db77-143">Le démarrage se poursuit.</span><span class="sxs-lookup"><span data-stu-id="0db77-143">Startup continues.</span></span> <span data-ttu-id="0db77-144">Aucune notification n’est donnée à l’utilisateur en raison de l’échec du service.</span><span class="sxs-lookup"><span data-stu-id="0db77-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-145">1</span><span class="sxs-lookup"><span data-stu-id="0db77-145">1</span></span>
</dt> <dd>

<span data-ttu-id="0db77-146">**Normal.**</span><span class="sxs-lookup"><span data-stu-id="0db77-146">**Normal.**</span></span> <span data-ttu-id="0db77-147">Le démarrage se poursuit.</span><span class="sxs-lookup"><span data-stu-id="0db77-147">Startup continues.</span></span> <span data-ttu-id="0db77-148">Avant que l’utilisateur ouvre une session, l’utilisateur reçoit la notification « au moins un service ou un périphérique a échoué au démarrage ».</span><span class="sxs-lookup"><span data-stu-id="0db77-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="0db77-149">2</span><span class="sxs-lookup"><span data-stu-id="0db77-149">2</span></span>
</dt> <dd>

<span data-ttu-id="0db77-150">**Sérieux.**</span><span class="sxs-lookup"><span data-stu-id="0db77-150">**Severe.**</span></span> <span data-ttu-id="0db77-151">L’ordinateur tente de redémarrer avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="0db77-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="0db77-152">Si le service échoue à nouveau, le démarrage se poursuit et la notification est donnée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0db77-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-153">3</span><span class="sxs-lookup"><span data-stu-id="0db77-153">3</span></span>
</dt> <dd>

<span data-ttu-id="0db77-154">**Critique.**</span><span class="sxs-lookup"><span data-stu-id="0db77-154">**Critical.**</span></span> <span data-ttu-id="0db77-155">L’ordinateur tente de redémarrer avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="0db77-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="0db77-156">Si le service échoue à nouveau, le démarrage s’arrête.</span><span class="sxs-lookup"><span data-stu-id="0db77-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0db77-157">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-158">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="0db77-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="0db77-159">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0db77-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="0db77-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Partition**</span><span class="sxs-lookup"><span data-stu-id="0db77-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="0db77-161">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0db77-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="0db77-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Requise**</span><span class="sxs-lookup"><span data-stu-id="0db77-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="0db77-163">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0db77-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="0db77-164">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="0db77-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="0db77-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique**</span><span class="sxs-lookup"><span data-stu-id="0db77-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="0db77-166">Le service est démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="0db77-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="0db77-167">Les services de démarrage automatique démarrent avant qu’un utilisateur ouvre une session sur l’ordinateur et s’exécute même si aucun utilisateur ne se connecte à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0db77-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="0db77-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuelle**</span><span class="sxs-lookup"><span data-stu-id="0db77-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="0db77-169">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0db77-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="0db77-170">Bien que les services manuels doivent être démarrés spécifiquement par un utilisateur (ou par un script), ils continuent à s’exécuter même si l’utilisateur se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="0db77-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="0db77-171">Les services manuels sont souvent appelés services à la demande.</span><span class="sxs-lookup"><span data-stu-id="0db77-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0db77-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**</span><span class="sxs-lookup"><span data-stu-id="0db77-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="0db77-173">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="0db77-173">Service that can no longer be started.</span></span> <span data-ttu-id="0db77-174">Pour démarrer un service désactivé, vous devez d’abord définir l’option de démarrage sur automatique ou manuel.</span><span class="sxs-lookup"><span data-stu-id="0db77-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0db77-175">*DesktopInteract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-176">Si la **valeur est true**, le service peut créer ou communiquer avec une fenêtre sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="0db77-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-177">*StartName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-178">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0db77-178">Account name the service runs under.</span></span> <span data-ttu-id="0db77-179">Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0db77-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="0db77-180">Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0db77-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="0db77-181">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="0db77-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="0db77-182">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="0db77-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="0db77-183">Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0db77-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="0db77-184">Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, « DWDOM \\ admin ».</span><span class="sxs-lookup"><span data-stu-id="0db77-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="0db77-185">Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="0db77-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-186">*StartPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-187">Mot de passe du nom de compte spécifié par le paramètre *StartName* .</span><span class="sxs-lookup"><span data-stu-id="0db77-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="0db77-188">Spécifiez **null** si vous ne modifiez pas le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0db77-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="0db77-189">Spécifiez une chaîne vide si le service ne possède pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0db77-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="0db77-190">Lorsque vous modifiez un service d’un système local à un réseau ou d’un réseau à un système local, *StartPassword* doit être une chaîne vide ("") et non **null**.</span><span class="sxs-lookup"><span data-stu-id="0db77-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="0db77-191">*LoadOrderGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-192">Nom du groupe auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="0db77-192">Group name that it is associated with.</span></span> <span data-ttu-id="0db77-193">Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0db77-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="0db77-194">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="0db77-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="0db77-195">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0db77-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="0db77-196">Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="0db77-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="0db77-197">Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe.</span><span class="sxs-lookup"><span data-stu-id="0db77-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="0db77-198">La liste des groupes d’ordre de chargement se trouve dans le registre système à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="0db77-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="0db77-199">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder</span><span class="sxs-lookup"><span data-stu-id="0db77-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="0db77-200">*LoadOrderGroupDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-201">Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="0db77-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="0db77-202">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="0db77-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="0db77-203">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="0db77-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="0db77-204">Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0db77-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="0db77-205">La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="0db77-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-206">*ServiceDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0db77-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db77-207">Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="0db77-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="0db77-208">Le tableau se termine par un caractère double **null**.</span><span class="sxs-lookup"><span data-stu-id="0db77-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="0db77-209">Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances.</span><span class="sxs-lookup"><span data-stu-id="0db77-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="0db77-210">La dépendance sur un service indique que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0db77-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db77-211">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0db77-211">Return value</span></span>

<span data-ttu-id="0db77-212">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0db77-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="0db77-213">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0db77-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0db77-214">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0db77-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0db77-215">**0**</span><span class="sxs-lookup"><span data-stu-id="0db77-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-216">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="0db77-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-217">**1**</span><span class="sxs-lookup"><span data-stu-id="0db77-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-218">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0db77-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-219">**2**</span><span class="sxs-lookup"><span data-stu-id="0db77-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-220">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0db77-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-221">**3**</span><span class="sxs-lookup"><span data-stu-id="0db77-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-222">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="0db77-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-223">**4**</span><span class="sxs-lookup"><span data-stu-id="0db77-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-224">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="0db77-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-225">**5**</span><span class="sxs-lookup"><span data-stu-id="0db77-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-226">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="0db77-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-227">**6**</span><span class="sxs-lookup"><span data-stu-id="0db77-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-228">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="0db77-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-229">**7**</span><span class="sxs-lookup"><span data-stu-id="0db77-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-230">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="0db77-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-231">**8**</span><span class="sxs-lookup"><span data-stu-id="0db77-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-232">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="0db77-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-233">**9**</span><span class="sxs-lookup"><span data-stu-id="0db77-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-234">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0db77-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-235">**10**</span><span class="sxs-lookup"><span data-stu-id="0db77-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-236">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="0db77-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-237">**11**</span><span class="sxs-lookup"><span data-stu-id="0db77-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-238">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="0db77-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-239">**12**</span><span class="sxs-lookup"><span data-stu-id="0db77-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-240">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="0db77-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-241">**13**</span><span class="sxs-lookup"><span data-stu-id="0db77-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-242">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="0db77-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-243">**14**</span><span class="sxs-lookup"><span data-stu-id="0db77-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-244">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="0db77-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-245">**15**</span><span class="sxs-lookup"><span data-stu-id="0db77-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-246">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="0db77-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-247">**16**</span><span class="sxs-lookup"><span data-stu-id="0db77-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-248">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="0db77-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-249">**17**</span><span class="sxs-lookup"><span data-stu-id="0db77-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-250">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0db77-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-251">**19**</span><span class="sxs-lookup"><span data-stu-id="0db77-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-252">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="0db77-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-253">**19**</span><span class="sxs-lookup"><span data-stu-id="0db77-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-254">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="0db77-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-255">**20**</span><span class="sxs-lookup"><span data-stu-id="0db77-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-256">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="0db77-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-257">**21**</span><span class="sxs-lookup"><span data-stu-id="0db77-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-258">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="0db77-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-259">**22**</span><span class="sxs-lookup"><span data-stu-id="0db77-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-260">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="0db77-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-261">**23**</span><span class="sxs-lookup"><span data-stu-id="0db77-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-262">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="0db77-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0db77-263">**24**</span><span class="sxs-lookup"><span data-stu-id="0db77-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0db77-264">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="0db77-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0db77-265">Notes</span><span class="sxs-lookup"><span data-stu-id="0db77-265">Remarks</span></span>

<span data-ttu-id="0db77-266">Lorsqu’un ordinateur démarre, tous les services de démarrage automatique démarrent également.</span><span class="sxs-lookup"><span data-stu-id="0db77-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="0db77-267">Il peut arriver que l’un de ces services ne puisse pas démarrer avec l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0db77-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="0db77-268">Lorsqu’un service échoue pendant le démarrage du système, l’ordinateur effectue une action en fonction de la valeur du code de contrôle d’erreur du service.</span><span class="sxs-lookup"><span data-stu-id="0db77-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="0db77-269">la plupart des services sont installés à l’aide du code de contrôle d’erreur normal.</span><span class="sxs-lookup"><span data-stu-id="0db77-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="0db77-270">Quelques-unes des exceptions, qui sont installées à l’aide du code d’erreur ignorer, sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0db77-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="0db77-271">Service de réplication de fichiers</span><span class="sxs-lookup"><span data-stu-id="0db77-271">File Replication Service</span></span>
-   <span data-ttu-id="0db77-272">Carte à puce</span><span class="sxs-lookup"><span data-stu-id="0db77-272">Smart Card</span></span>
-   <span data-ttu-id="0db77-273">Ouverture de session secondaire</span><span class="sxs-lookup"><span data-stu-id="0db77-273">Secondary Logon</span></span>
-   <span data-ttu-id="0db77-274">WMI</span><span class="sxs-lookup"><span data-stu-id="0db77-274">WMI</span></span>

<span data-ttu-id="0db77-275">Pour les services installés à l’aide du code d’erreur ignorer, aucune notification n’est donnée à l’utilisateur pour lequel le service a échoué.</span><span class="sxs-lookup"><span data-stu-id="0db77-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="0db77-276">Si vous préférez que la notification à l’écran indique qu’un service n’a pas pu démarrer, vous pouvez utiliser WMI pour modifier le code de contrôle de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0db77-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="0db77-277">Les codes de contrôle d’erreur s’appliquent uniquement au démarrage de l’ordinateur. les codes de contrôle d’erreur ne sont pas utilisés si vous arrêtez, puis essayez de redémarrer un service une fois que l’ordinateur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0db77-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="0db77-278">Parfois, vous devrez peut-être modifier le compte sous lequel un service donné s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0db77-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="0db77-279">Par exemple, vous pouvez exécuter un service sous un compte d’administration.</span><span class="sxs-lookup"><span data-stu-id="0db77-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="0db77-280">Étant donné que cela peut créer une faille de sécurité, vous pouvez basculer le service vers un compte avec moins de privilèges.</span><span class="sxs-lookup"><span data-stu-id="0db77-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="0db77-281">Vous pouvez également faire en sorte que les services s’exécutent sous un compte qui est sur le lieu d’être supprimé, ou que vous souhaitiez vous assurer que certains services s’exécutent sous certains comptes sur tous vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="0db77-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="0db77-282">Vous pouvez utiliser la méthode **change** de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) pour configurer les services à exécuter sous un compte d’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0db77-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="0db77-283">Lorsque vous sélectionnez un compte, gardez à l’esprit les points suivants :</span><span class="sxs-lookup"><span data-stu-id="0db77-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="0db77-284">Le compte utilisé en tant que compte de service doit avoir le droit d’ouvrir une session en tant que service.</span><span class="sxs-lookup"><span data-stu-id="0db77-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="0db77-285">Ce droit peut être accordé à l’aide de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0db77-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="0db77-286">Le compte utilisé en tant que compte de service ne doit pas être membre d’un groupe local, d’un domaine ou d’un groupe administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0db77-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="0db77-287">Chaque instance d’un service doit s’exécuter sous un compte d’utilisateur unique.</span><span class="sxs-lookup"><span data-stu-id="0db77-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="0db77-288">Cela offre une sécurité supplémentaire et permet d’auditer des instances de service individuelles.</span><span class="sxs-lookup"><span data-stu-id="0db77-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="0db77-289">Si le service est interactif, le service doit s’exécuter sous le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="0db77-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="0db77-290">LocalSystem est requis car une seule station Windows (WinSta0) peut être visible et interactive à la fois.</span><span class="sxs-lookup"><span data-stu-id="0db77-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="0db77-291">Si un service s’exécute sous un compte autre que LocalSystem, il s’exécute dans la \\ station Windows par défaut du service 0x03e7, qui est une fenêtre invisible.</span><span class="sxs-lookup"><span data-stu-id="0db77-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="0db77-292">Les services qui s’exécutent dans cette station Windows ne peuvent pas recevoir de sortie d’entrée ou d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0db77-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="0db77-293">Lorsque vous affectez un compte à un service, le SCM requiert le mot de passe correct pour ce compte avant de procéder à l’attribution.</span><span class="sxs-lookup"><span data-stu-id="0db77-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="0db77-294">Si vous fournissez un mot de passe incorrect, le SCM rejette le compte.</span><span class="sxs-lookup"><span data-stu-id="0db77-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="0db77-295">Si vous configurez un compte de service à l’aide du compte LocalSystem, LocalService ou NetworkService, vous n’avez pas besoin de fournir un mot de passe de compte, car ces comptes n’ont pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0db77-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="0db77-296">Le SCM stocke le mot de passe du compte dans la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="0db77-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="0db77-297">Toutefois, une fois le mot de passe affecté, le SCM ne garantit pas que le mot de passe stocké dans la base de données de services et le mot de passe attribué au compte d’utilisateur dans Active Directory continuent de correspondre.</span><span class="sxs-lookup"><span data-stu-id="0db77-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="0db77-298">Par conséquent, une situation semblable à la suivante peut se produire :</span><span class="sxs-lookup"><span data-stu-id="0db77-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="0db77-299">. Vous configurez un service pour qu’il s’exécute sous un compte d’utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="0db77-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="0db77-300">Le service démarre sous ce compte à l’aide du mot de passe du compte actuel.</span><span class="sxs-lookup"><span data-stu-id="0db77-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="0db77-301">Vous modifiez le mot de passe du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0db77-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="0db77-302">Le service continue à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0db77-302">The service continues to run.</span></span> <span data-ttu-id="0db77-303">Toutefois, si le service s’arrête, vous ne pouvez pas le redémarrer, car le SCM continue à utiliser l’ancien mot de passe non valide.</span><span class="sxs-lookup"><span data-stu-id="0db77-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="0db77-304">La modification du mot de passe dans Active Directory ne modifie pas le mot de passe stocké dans la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="0db77-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="0db77-305">Si vous exécutez des services sous des comptes d’utilisateur standard, vous devez mettre à jour ces mots de passe de service chaque fois que le mot de passe du compte d’utilisateur est modifié.</span><span class="sxs-lookup"><span data-stu-id="0db77-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="0db77-306">Cela peut s’avérer particulièrement long si vous ne savez pas quels services s’exécutent sous ce compte ou quels sont les ordinateurs qui exécutent les services sous ce compte.</span><span class="sxs-lookup"><span data-stu-id="0db77-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="0db77-307">Heureusement, vous pouvez utiliser WMI pour vérifier les comptes de service sur tous vos ordinateurs et, si nécessaire, modifier le mot de passe du compte de service.</span><span class="sxs-lookup"><span data-stu-id="0db77-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="0db77-308">Le [**paramètre \_ LoadOrderGroup Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) représente un groupe de services système qui définissent des dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0db77-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="0db77-309">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="0db77-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="0db77-310">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="0db77-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="0db77-311">Pour modifier un service d’un service réseau en système local, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0db77-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="0db77-312">Pour modifier un service d’un service système local sur un réseau, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0db77-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="0db77-313">Exemples</span><span class="sxs-lookup"><span data-stu-id="0db77-313">Examples</span></span>

<span data-ttu-id="0db77-314">Le code VBScript suivant modifie le compte de service pour les services qui s’exécutent sous un compte d’utilisateur spécifié sur LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="0db77-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="0db77-315">Le script VBScript suivant modifie le mot de passe du compte de service pour tous les scripts exécutés sous netsvc</span><span class="sxs-lookup"><span data-stu-id="0db77-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="0db77-316">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0db77-316">Requirements</span></span>



| <span data-ttu-id="0db77-317">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0db77-317">Requirement</span></span> | <span data-ttu-id="0db77-318">Valeur</span><span class="sxs-lookup"><span data-stu-id="0db77-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db77-319">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db77-319">Minimum supported client</span></span><br/> | <span data-ttu-id="0db77-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0db77-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0db77-321">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db77-321">Minimum supported server</span></span><br/> | <span data-ttu-id="0db77-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0db77-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0db77-323">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0db77-323">Namespace</span></span><br/>                | <span data-ttu-id="0db77-324">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0db77-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0db77-325">En-tête</span><span class="sxs-lookup"><span data-stu-id="0db77-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db77-326"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db77-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="0db77-327">MOF</span><span class="sxs-lookup"><span data-stu-id="0db77-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0db77-328"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0db77-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0db77-329">DLL</span><span class="sxs-lookup"><span data-stu-id="0db77-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db77-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db77-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db77-331">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0db77-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db77-332">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="0db77-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="0db77-333">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0db77-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="0db77-334">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="0db77-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0db77-335">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="0db77-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


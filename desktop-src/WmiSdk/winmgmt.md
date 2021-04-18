---
description: Winmgmt est le service WMI dans le processus SVCHOST s’exécutant sous le &\# 0034 ; LocalSystem&\# 0034 ; compte.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: critique
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526282"
---
# <a name="winmgmt"></a><span data-ttu-id="c7c9d-103">critique</span><span class="sxs-lookup"><span data-stu-id="c7c9d-103">winmgmt</span></span>

<span data-ttu-id="c7c9d-104">Winmgmt est le service WMI dans le processus SVCHOST s’exécutant sous le compte « LocalSystem ».</span><span class="sxs-lookup"><span data-stu-id="c7c9d-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="c7c9d-105">Dans tous les cas, le service WMI démarre automatiquement lorsque la première application ou le script de gestion demande une connexion à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="c7c9d-106">Pour plus d’informations, consultez [Démarrage et arrêt du service WMI](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7c9d-107">WMI est un composant fondamental du système d’exploitation Windows qui permet aux développeurs et aux administrateurs informatiques d’écrire des scripts et des applications pour automatiser certaines tâches.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="c7c9d-108">Winmgmt.exe est le service qui permet à WMI de s’exécuter sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="c7c9d-109">Pour plus d’informations sur l’utilisation de WMI, consultez [utilisation de WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="c7c9d-110">Si vous avez reçu un message d’erreur concernant winmgmt.exe, consultez [résolution des problèmes liés à WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="c7c9d-111">Pour plus d’informations sur la Winmgmt.exe, consultez [utilisation des outils de gestion WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="c7c9d-112">Lorsqu’il est exécuté à partir de l’invite de commandes, le service WMI dispose des commutateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="c7c9d-113">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="c7c9d-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="c7c9d-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/Backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="c7c9d-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c9d-115">Permet à WMI de sauvegarder le référentiel dans le nom de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="c7c9d-116">L’argument *filename* doit contenir le chemin d’accès complet à l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="c7c9d-117">Ce processus nécessite un verrou d’écriture sur le référentiel afin que les opérations d’écriture dans le référentiel soient interrompues jusqu’à la fin du processus de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="c7c9d-118">Si vous ne spécifiez pas de chemin d’accès pour le fichier, il est placé dans le répertoire% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="c7c9d-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c9d-120">Restaure manuellement le référentiel WMI à partir du fichier de sauvegarde spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="c7c9d-121">L’argument *filename* doit contenir le chemin d’accès complet à l’emplacement du fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="c7c9d-122">Pour effectuer l’opération de restauration, WMI enregistre le référentiel existant en écriture différée si l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="c7c9d-123">Le référentiel est ensuite restauré à partir du fichier de sauvegarde spécifié dans l’argument de *nom de fichier* .</span><span class="sxs-lookup"><span data-stu-id="c7c9d-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="c7c9d-124">Si l’accès exclusif au référentiel ne peut pas être effectué, les clients existants sont déconnectés de WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="c7c9d-125">L’argument *Flag* doit avoir la valeur 1 (forcer la déconnexion des utilisateurs et la restauration) ou 0 (restauration par défaut si aucun utilisateur n’est connecté) et spécifie le mode de restauration.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<winmgmt-service-process-ID>*</span><span class="sxs-lookup"><span data-stu-id="c7c9d-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c9d-127">Inscrit les bibliothèques de performances de l’ordinateur avec WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="c7c9d-128">PID WMI est l’ID de processus du service WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="c7c9d-129">Nécessaire uniquement si les classes de l’analyseur de performances ne retournent pas de résultats fiables.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="c7c9d-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c9d-131">Déplace le service WinMgmt vers un processus Svchost autonome qui a un point de terminaison DCOM fixe.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="c7c9d-132">Le point de terminaison par défaut est « ncacn \_ IP \_ TCP. 0.24158 ».</span><span class="sxs-lookup"><span data-stu-id="c7c9d-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="c7c9d-133">Toutefois, le point de terminaison peut être modifié en exécutant Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="c7c9d-134">Pour plus d’informations sur la configuration d’un port fixe pour WMI, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="c7c9d-135">L’argument *Level* est le niveau d’authentification pour le processus Svchost.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="c7c9d-136">WMI s’exécute normalement dans le cadre d’un hôte de service partagé et vous ne pouvez pas augmenter le niveau d’authentification pour WMI seul.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="c7c9d-137">Si le *niveau* n’est pas spécifié, la valeur par défaut est 4 (**RPC \_ C \_ Authn \_ niveau \_ PKT** ou **WbemAuthenticationLevelPkt**).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="c7c9d-138">Vous pouvez exécuter WMI de manière plus sécurisée en accroissant le niveau d’authentification à la confidentialité des paquets (RPC-niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité** ou **WbemAuthenticationLevelPktPrivacy**).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="c7c9d-139">Les niveaux d’authentification pour les Visual Basic et les scripts sont décrits dans [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="c7c9d-140">Pour C++, consultez [définition du niveau de sécurité de processus par défaut à l’aide de c++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="c7c9d-141">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="c7c9d-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="c7c9d-143">Déplace le service WinMgmt dans le processus Svchost partagé.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="c7c9d-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c9d-145">Effectue une vérification de cohérence sur le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="c7c9d-146">Lorsque vous ajoutez le commutateur **/verifyrepository** sans l' *<path>* argument, le référentiel Live actuellement utilisé par WMI est vérifié.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="c7c9d-147">Lorsque vous spécifiez l’argument *path* , vous pouvez vérifier toute copie enregistrée du dépôt.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="c7c9d-148">Dans ce cas, l’argument Path doit contenir le chemin d’accès complet à la copie enregistrée du dépôt.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="c7c9d-149">Le référentiel enregistré doit être une copie de l’intégralité du dossier de dépôt.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="c7c9d-150">Pour plus d’informations sur les erreurs retournées par cette commande, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="c7c9d-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="c7c9d-152">Effectue une vérification de cohérence sur le référentiel WMI et, si une incohérence est détectée, reconstruit le référentiel.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="c7c9d-153">Le contenu du référentiel incohérent est fusionné dans le référentiel reconstruit, s’il peut être lu par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="c7c9d-154">L’opération de récupération fonctionne toujours avec le référentiel actuellement utilisé par le service WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="c7c9d-155">Pour plus d’informations sur les erreurs retournées par cette commande, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="c7c9d-156">Les fichiers MOF qui contiennent l’instruction de préprocesseur [**\# pragma AutoRecover**](pragma-autorecover.md) sont restaurés dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="c7c9d-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="c7c9d-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="c7c9d-158">Le référentiel est réinitialisé à l’état initial lors de la première installation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="c7c9d-159">Les fichiers MOF qui contiennent l’instruction de préprocesseur [**\# pragma autoautorecover**](pragma-autorecover.md) sont restaurés dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7c9d-160">Notes</span><span class="sxs-lookup"><span data-stu-id="c7c9d-160">Remarks</span></span>

<span data-ttu-id="c7c9d-161">Cet outil se trouve dans le répertoire% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="c7c9d-162">Pour obtenir la liste des commutateurs disponibles, tapez `WinMgmt /?` à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="c7c9d-163">L’espace de stockage WMI, également connu sous le nom de référentiel CIM, n’est pas un simple fichier, mais une collection de fichiers dans le dossier du référentiel qui fonctionnent ensemble comme une base de données.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="c7c9d-164">Lorsque vous utilisez le commutateur **/Backup** pour sauvegarder le dépôt, la sauvegarde obtenue est un fichier compressé unique.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="c7c9d-165">WMI retourne l’erreur erreur de **\_ \_ \_ défaillance** de la base de donnes (net helpmsg 1358) si une opération de vérification indique que le référentiel n’est pas dans un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="c7c9d-166">Cette erreur peut être retournée à partir de toute commande qui effectue une vérification de référentiel, telle que **/verifyrepository** ou **/salvagerepository**.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="c7c9d-167">Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="c7c9d-168">Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="c7c9d-169">Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="c7c9d-170">Pour plus d’informations sur la source du problème, téléchargez et exécutez l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="c7c9d-171">Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="c7c9d-172">Le rapport aide également les services de support technique Microsoft à vous aider.</span><span class="sxs-lookup"><span data-stu-id="c7c9d-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="c7c9d-173">Vous pouvez télécharger le [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="c7c9d-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7c9d-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7c9d-174">Requirements</span></span>



| <span data-ttu-id="c7c9d-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7c9d-175">Requirement</span></span> | <span data-ttu-id="c7c9d-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7c9d-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c7c9d-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c9d-177">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c9d-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7c9d-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c7c9d-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c9d-179">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c9d-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7c9d-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7c9d-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7c9d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c9d-182">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="c7c9d-182">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="c7c9d-183">Connexion à WMI à distance à partir de Vista</span><span class="sxs-lookup"><span data-stu-id="c7c9d-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 


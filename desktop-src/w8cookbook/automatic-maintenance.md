---
title: Maintenance automatique (Guide de compatibilité pour Windows)
description: Maintenance automatique
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463838"
---
# <a name="automatic-maintenance"></a><span data-ttu-id="d3754-103">Maintenance automatique</span><span class="sxs-lookup"><span data-stu-id="d3754-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="d3754-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="d3754-104">Platforms</span></span>

<span data-ttu-id="d3754-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="d3754-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="d3754-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3754-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="d3754-107">Description</span><span class="sxs-lookup"><span data-stu-id="d3754-107">Description</span></span>

<span data-ttu-id="d3754-108">Windows dépend de l’exécution de la boîte de réception et de l’activité de maintenance d’un tiers pour une grande partie de sa valeur ajoutée, y compris Windows Update et la défragmentation automatique des disques, ainsi que des mises à jour et des analyses antivirus.</span><span class="sxs-lookup"><span data-stu-id="d3754-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="d3754-109">En outre, les entreprises utilisent fréquemment des activités de maintenance telles que l’analyse de la protection d’accès réseau (NAP) pour renforcer l’application des normes de sécurité sur toutes les stations de travail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d3754-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="d3754-110">L’activité de maintenance dans Windows est conçue pour s’exécuter en arrière-plan avec une interaction utilisateur limitée et un impact minimal sur les performances et l’efficacité énergétique.</span><span class="sxs-lookup"><span data-stu-id="d3754-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="d3754-111">Toutefois, dans Windows 7 et les versions antérieures, les performances et l’efficacité énergétique sont toujours affectées en raison de la planification non déterministe et très variée des diverses activités de maintenance dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d3754-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="d3754-112">La réactivité des utilisateurs est réduite lors de l’exécution de l’activité de maintenance pendant que les utilisateurs utilisent l’ordinateur activement.</span><span class="sxs-lookup"><span data-stu-id="d3754-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="d3754-113">Les applications demandent également souvent à l’utilisateur de mettre à jour ses logiciels et d’exécuter une maintenance en arrière-plan, et de diriger les utilisateurs vers plusieurs expériences, notamment le centre de maintenance, le panneau de configuration, Windows Update, Planificateur de tâches composant logiciel enfichable MMC et les contrôles tiers.</span><span class="sxs-lookup"><span data-stu-id="d3754-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="d3754-114">L’objectif de la maintenance automatique consiste à combiner toutes les activités de maintenance en arrière-plan dans Windows et à aider les développeurs tiers à ajouter leur activité de maintenance à Windows sans avoir d’impact négatif sur les performances et l’efficacité énergétique.</span><span class="sxs-lookup"><span data-stu-id="d3754-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="d3754-115">En outre, la maintenance automatique permet aux utilisateurs et aux entreprises de contrôler la planification et la configuration des activités de maintenance.</span><span class="sxs-lookup"><span data-stu-id="d3754-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="d3754-116">**Problèmes clés**</span><span class="sxs-lookup"><span data-stu-id="d3754-116">**Key problems**</span></span>

<span data-ttu-id="d3754-117">La maintenance automatique est conçue pour résoudre ces problèmes liés à l’activité de maintenance dans Windows :</span><span class="sxs-lookup"><span data-stu-id="d3754-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="d3754-118">Planification de l’échéance</span><span class="sxs-lookup"><span data-stu-id="d3754-118">Deadline scheduling</span></span>
-   <span data-ttu-id="d3754-119">Conflits d’utilisation des ressources</span><span class="sxs-lookup"><span data-stu-id="d3754-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="d3754-120">Efficacité énergétique</span><span class="sxs-lookup"><span data-stu-id="d3754-120">Energy efficiency</span></span>
-   <span data-ttu-id="d3754-121">Transparence pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d3754-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="d3754-122">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d3754-122">Functionality</span></span>

<span data-ttu-id="d3754-123">La maintenance automatique facilite l’efficacité inactive et autorise l’exécution de toute l’activité en temps opportun et par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="d3754-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="d3754-124">Il permet également de bénéficier d’une visibilité et d’un contrôle unifiés sur l’activité de maintenance, et permet aux développeurs tiers d’ajouter leur activité de maintenance à Windows sans avoir un impact négatif sur les performances et l’efficacité énergétique.</span><span class="sxs-lookup"><span data-stu-id="d3754-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="d3754-125">Pour ce faire, il fournit un mode entièrement automatique, un mode initié par l’utilisateur, un arrêt automatique, des échéances et des notifications, ainsi qu’un contrôle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d3754-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="d3754-126">Celles-ci sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d3754-126">These are each described below.</span></span>

<span data-ttu-id="d3754-127">**Mode entièrement automatique**</span><span class="sxs-lookup"><span data-stu-id="d3754-127">**Fully automatic mode**</span></span>

<span data-ttu-id="d3754-128">Ce mode par défaut active la planification intelligente pendant le temps d’inactivité de l’ordinateur et à des heures planifiées : l’exécution et la suspension automatique de l’activité de maintenance sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3754-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="d3754-129">L’utilisateur peut définir une planification hebdomadaire ou quotidienne.</span><span class="sxs-lookup"><span data-stu-id="d3754-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="d3754-130">Toutes les activités de maintenance ne sont pas interactives et s’exécutent en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="d3754-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="d3754-131">L’ordinateur est automatiquement repris du mode veille lorsque le système n’est pas susceptible d’être utilisé, en respectant la stratégie de gestion de l’alimentation, qui, dans le cas des ordinateurs portables, autorise par défaut la mise en éveil uniquement si elle se trouve sur secteur.</span><span class="sxs-lookup"><span data-stu-id="d3754-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="d3754-132">Les ressources système complètes à haute puissance sont utilisées pour effectuer l’activité de maintenance le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="d3754-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="d3754-133">Si le système a repris du mode veille pour une maintenance automatique, il est demandé de revenir en mode veille.</span><span class="sxs-lookup"><span data-stu-id="d3754-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="d3754-134">Toutes les interactions utilisateur requises liées à des activités, telles que la configuration, sont effectuées en dehors de l’exécution de maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="d3754-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="d3754-135">**Mode initié par l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3754-135">**User-initiated mode**</span></span>

<span data-ttu-id="d3754-136">Si les utilisateurs doivent se préparer au voyage, s’attendre à avoir une durée prolongée, ou souhaitent optimiser les performances et la réactivité, ils ont la possibilité de lancer une maintenance automatique à la demande.</span><span class="sxs-lookup"><span data-stu-id="d3754-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="d3754-137">Les utilisateurs peuvent configurer des attributs de maintenance automatique, y compris la planification d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="d3754-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="d3754-138">Ils peuvent afficher l’état actuel de l’exécution de maintenance automatique, et ils peuvent arrêter la maintenance automatique si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d3754-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="d3754-139">**Arrêt automatique**</span><span class="sxs-lookup"><span data-stu-id="d3754-139">**Automatic stop**</span></span>

<span data-ttu-id="d3754-140">La maintenance automatique arrête automatiquement les activités de maintenance en cours si l’utilisateur commence à interagir avec l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d3754-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="d3754-141">L’activité de maintenance reprendra lorsque le système revient à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="d3754-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="d3754-142">Toutes les activités de maintenance automatique doivent prendre en charge l’arrêt en moins de 2 secondes.</span><span class="sxs-lookup"><span data-stu-id="d3754-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="d3754-143">L’utilisateur doit être informé que l’activité a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="d3754-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="d3754-144">**Échéances et notification**</span><span class="sxs-lookup"><span data-stu-id="d3754-144">**Deadlines and notification**</span></span>

<span data-ttu-id="d3754-145">L’activité de maintenance critique doit s’exécuter dans une fenêtre de temps prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="d3754-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="d3754-146">Si les tâches critiques n’ont pas pu s’exécuter dans le délai imparti, la maintenance automatique démarrera automatiquement à la prochaine occasion d’inactivité du système disponible.</span><span class="sxs-lookup"><span data-stu-id="d3754-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="d3754-147">Toutefois, si l’état de la tâche reste en retard, la maintenance automatique avertit l’utilisateur de l’activité et fournit une option pour une exécution manuelle de la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="d3754-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="d3754-148">Toutes les tâches planifiées pour la maintenance sont exécutées, bien que les tâches les plus dépendantes soient prioritaires.</span><span class="sxs-lookup"><span data-stu-id="d3754-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="d3754-149">Cette activité peut avoir un impact sur la réactivité et les performances du système ; par conséquent, la maintenance automatique informe l’utilisateur que l’activité de maintenance critique est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d3754-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="d3754-150">**Contrôle d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="d3754-150">**Enterprise control**</span></span>

<span data-ttu-id="d3754-151">Les professionnels de l’informatique d’entreprise doivent être en mesure de déterminer le moment où la maintenance automatique s’exécute sur leurs systèmes Windows, d’appliquer cette planification via des interfaces de gestion standardisées et de récupérer les données d’événement sur l’état des tentatives d’exécution de maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="d3754-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="d3754-152">En outre, les professionnels de l’informatique doivent être en mesure d’appeler une activité de maintenance automatique spécifique à distance via des interfaces de gestion standard.</span><span class="sxs-lookup"><span data-stu-id="d3754-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="d3754-153">Chaque fois que la maintenance automatique s’exécute, rapport d’État, y compris les notifications lorsque la maintenance automatique n’a pas pu être exécutée parce que l’utilisateur a suspendu manuellement l’activité, s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d3754-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="d3754-154">Les professionnels de l’informatique doivent envisager de déplacer les scripts d’ouverture de session vers la maintenance automatique pour faciliter l’expérience d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3754-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="d3754-155">Création d’une tâche de maintenance automatique</span><span class="sxs-lookup"><span data-stu-id="d3754-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="d3754-156">Cette section explique en détail comment les développeurs peuvent créer une tâche à l’aide d’une définition de tâche en langage XML ou C.</span><span class="sxs-lookup"><span data-stu-id="d3754-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="d3754-157">Gardez à l’esprit que l’activité de maintenance ne doit pas lancer une interface utilisateur qui nécessite une interaction de l’utilisateur, car la maintenance automatique est complètement silencieuse et s’exécute lorsque l’utilisateur n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="d3754-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="d3754-158">En effet, si l’utilisateur interagit avec l’ordinateur lors de la maintenance automatique, toutes les tâches en cours seront terminées jusqu’à la période d’inactivité suivante.</span><span class="sxs-lookup"><span data-stu-id="d3754-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="d3754-159">**Utilisation de XML**</span><span class="sxs-lookup"><span data-stu-id="d3754-159">**Using XML**</span></span>

<span data-ttu-id="d3754-160">Planificateur de tâches comprend un outil en ligne de commande intégré, schtasks.exe, qui peut importer une définition de tâche au format XML.</span><span class="sxs-lookup"><span data-stu-id="d3754-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="d3754-161">Le schéma de la définition de tâche est documenté dans https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="d3754-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="d3754-162">Voici un exemple de tâche de maintenance automatique définie dans XML.</span><span class="sxs-lookup"><span data-stu-id="d3754-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



<span data-ttu-id="d3754-163">Pour enregistrer la tâche sur un ordinateur Windows, enregistrez le XML ci-dessus en tant que fichier texte et utilisez la ligne de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d3754-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="d3754-164">**Utilisation de C**</span><span class="sxs-lookup"><span data-stu-id="d3754-164">**Using C**</span></span>

<span data-ttu-id="d3754-165">Vous pouvez également créer une tâche de maintenance automatique à l’aide du code C.</span><span class="sxs-lookup"><span data-stu-id="d3754-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="d3754-166">Vous trouverez ci-dessous un exemple de code qui peut être utilisé pour configurer les paramètres de maintenance automatique d’une tâche :</span><span class="sxs-lookup"><span data-stu-id="d3754-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a><span data-ttu-id="d3754-167">Validation des tâches</span><span class="sxs-lookup"><span data-stu-id="d3754-167">Validating tasks</span></span>

<span data-ttu-id="d3754-168">Vérifiez que la tâche a été créée avec succès et qu’elle s’exécute dans le cadre de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="d3754-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="d3754-169">**Validation de la création de tâches**</span><span class="sxs-lookup"><span data-stu-id="d3754-169">**Validating task creation**</span></span>

<span data-ttu-id="d3754-170">Utilisez cette ligne de commande pour exporter la définition de tâche vers un fichier et vous assurer que la définition de tâche est la même que celle attendue :</span><span class="sxs-lookup"><span data-stu-id="d3754-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="d3754-171">**Validation de l’exécution des tâches**</span><span class="sxs-lookup"><span data-stu-id="d3754-171">**Validating task execution**</span></span>

<span data-ttu-id="d3754-172">Exécutez cette ligne de commande pour lancer la tâche et vérifier que l’interface utilisateur Planificateur de tâches (taskschd. msc) indique que la tâche a été exécutée :</span><span class="sxs-lookup"><span data-stu-id="d3754-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="d3754-173">Ressources</span><span class="sxs-lookup"><span data-stu-id="d3754-173">Resources</span></span>

-   <span data-ttu-id="d3754-174">[Planification de la tâche 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d3754-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 
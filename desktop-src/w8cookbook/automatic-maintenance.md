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
# <a name="automatic-maintenance"></a>Maintenance automatique

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Windows dépend de l’exécution de la boîte de réception et de l’activité de maintenance d’un tiers pour une grande partie de sa valeur ajoutée, y compris Windows Update et la défragmentation automatique des disques, ainsi que des mises à jour et des analyses antivirus. En outre, les entreprises utilisent fréquemment des activités de maintenance telles que l’analyse de la protection d’accès réseau (NAP) pour renforcer l’application des normes de sécurité sur toutes les stations de travail d’entreprise.

L’activité de maintenance dans Windows est conçue pour s’exécuter en arrière-plan avec une interaction utilisateur limitée et un impact minimal sur les performances et l’efficacité énergétique. Toutefois, dans Windows 7 et les versions antérieures, les performances et l’efficacité énergétique sont toujours affectées en raison de la planification non déterministe et très variée des diverses activités de maintenance dans Windows. La réactivité des utilisateurs est réduite lors de l’exécution de l’activité de maintenance pendant que les utilisateurs utilisent l’ordinateur activement. Les applications demandent également souvent à l’utilisateur de mettre à jour ses logiciels et d’exécuter une maintenance en arrière-plan, et de diriger les utilisateurs vers plusieurs expériences, notamment le centre de maintenance, le panneau de configuration, Windows Update, Planificateur de tâches composant logiciel enfichable MMC et les contrôles tiers.

L’objectif de la maintenance automatique consiste à combiner toutes les activités de maintenance en arrière-plan dans Windows et à aider les développeurs tiers à ajouter leur activité de maintenance à Windows sans avoir d’impact négatif sur les performances et l’efficacité énergétique. En outre, la maintenance automatique permet aux utilisateurs et aux entreprises de contrôler la planification et la configuration des activités de maintenance.

**Problèmes clés**

La maintenance automatique est conçue pour résoudre ces problèmes liés à l’activité de maintenance dans Windows :

-   Planification de l’échéance
-   Conflits d’utilisation des ressources
-   Efficacité énergétique
-   Transparence pour l’utilisateur

## <a name="functionality"></a>Fonctionnalités

La maintenance automatique facilite l’efficacité inactive et autorise l’exécution de toute l’activité en temps opportun et par ordre de priorité. Il permet également de bénéficier d’une visibilité et d’un contrôle unifiés sur l’activité de maintenance, et permet aux développeurs tiers d’ajouter leur activité de maintenance à Windows sans avoir un impact négatif sur les performances et l’efficacité énergétique. Pour ce faire, il fournit un mode entièrement automatique, un mode initié par l’utilisateur, un arrêt automatique, des échéances et des notifications, ainsi qu’un contrôle d’entreprise. Celles-ci sont décrites ci-dessous.

**Mode entièrement automatique**

Ce mode par défaut active la planification intelligente pendant le temps d’inactivité de l’ordinateur et à des heures planifiées : l’exécution et la suspension automatique de l’activité de maintenance sans intervention de l’utilisateur. L’utilisateur peut définir une planification hebdomadaire ou quotidienne. Toutes les activités de maintenance ne sont pas interactives et s’exécutent en mode silencieux.

L’ordinateur est automatiquement repris du mode veille lorsque le système n’est pas susceptible d’être utilisé, en respectant la stratégie de gestion de l’alimentation, qui, dans le cas des ordinateurs portables, autorise par défaut la mise en éveil uniquement si elle se trouve sur secteur. Les ressources système complètes à haute puissance sont utilisées pour effectuer l’activité de maintenance le plus rapidement possible. Si le système a repris du mode veille pour une maintenance automatique, il est demandé de revenir en mode veille.

Toutes les interactions utilisateur requises liées à des activités, telles que la configuration, sont effectuées en dehors de l’exécution de maintenance automatique.

**Mode initié par l’utilisateur**

Si les utilisateurs doivent se préparer au voyage, s’attendre à avoir une durée prolongée, ou souhaitent optimiser les performances et la réactivité, ils ont la possibilité de lancer une maintenance automatique à la demande. Les utilisateurs peuvent configurer des attributs de maintenance automatique, y compris la planification d’exécution automatique. Ils peuvent afficher l’état actuel de l’exécution de maintenance automatique, et ils peuvent arrêter la maintenance automatique si nécessaire.

**Arrêt automatique**

La maintenance automatique arrête automatiquement les activités de maintenance en cours si l’utilisateur commence à interagir avec l’ordinateur. L’activité de maintenance reprendra lorsque le système revient à l’état inactif.

> [!Note]  
> Toutes les activités de maintenance automatique doivent prendre en charge l’arrêt en moins de 2 secondes. L’utilisateur doit être informé que l’activité a été arrêtée.

 

**Échéances et notification**

L’activité de maintenance critique doit s’exécuter dans une fenêtre de temps prédéfinie. Si les tâches critiques n’ont pas pu s’exécuter dans le délai imparti, la maintenance automatique démarrera automatiquement à la prochaine occasion d’inactivité du système disponible. Toutefois, si l’état de la tâche reste en retard, la maintenance automatique avertit l’utilisateur de l’activité et fournit une option pour une exécution manuelle de la maintenance automatique. Toutes les tâches planifiées pour la maintenance sont exécutées, bien que les tâches les plus dépendantes soient prioritaires. Cette activité peut avoir un impact sur la réactivité et les performances du système ; par conséquent, la maintenance automatique informe l’utilisateur que l’activité de maintenance critique est en cours d’exécution.

**Contrôle d’entreprise**

Les professionnels de l’informatique d’entreprise doivent être en mesure de déterminer le moment où la maintenance automatique s’exécute sur leurs systèmes Windows, d’appliquer cette planification via des interfaces de gestion standardisées et de récupérer les données d’événement sur l’état des tentatives d’exécution de maintenance automatique. En outre, les professionnels de l’informatique doivent être en mesure d’appeler une activité de maintenance automatique spécifique à distance via des interfaces de gestion standard. Chaque fois que la maintenance automatique s’exécute, rapport d’État, y compris les notifications lorsque la maintenance automatique n’a pas pu être exécutée parce que l’utilisateur a suspendu manuellement l’activité, s’exécute. Les professionnels de l’informatique doivent envisager de déplacer les scripts d’ouverture de session vers la maintenance automatique pour faciliter l’expérience d’ouverture de session de l’utilisateur.

## <a name="creating-an-automatic-maintenance-task"></a>Création d’une tâche de maintenance automatique

Cette section explique en détail comment les développeurs peuvent créer une tâche à l’aide d’une définition de tâche en langage XML ou C. Gardez à l’esprit que l’activité de maintenance ne doit pas lancer une interface utilisateur qui nécessite une interaction de l’utilisateur, car la maintenance automatique est complètement silencieuse et s’exécute lorsque l’utilisateur n’est pas présent. En effet, si l’utilisateur interagit avec l’ordinateur lors de la maintenance automatique, toutes les tâches en cours seront terminées jusqu’à la période d’inactivité suivante.

**Utilisation de XML**

Planificateur de tâches comprend un outil en ligne de commande intégré, schtasks.exe, qui peut importer une définition de tâche au format XML. Le schéma de la définition de tâche est documenté dans https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Voici un exemple de tâche de maintenance automatique définie dans XML.


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



Pour enregistrer la tâche sur un ordinateur Windows, enregistrez le XML ci-dessus en tant que fichier texte et utilisez la ligne de commande suivante :

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Utilisation de C**

Vous pouvez également créer une tâche de maintenance automatique à l’aide du code C. Vous trouverez ci-dessous un exemple de code qui peut être utilisé pour configurer les paramètres de maintenance automatique d’une tâche :


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



## <a name="validating-tasks"></a>Validation des tâches

Vérifiez que la tâche a été créée avec succès et qu’elle s’exécute dans le cadre de la maintenance.

**Validation de la création de tâches**

Utilisez cette ligne de commande pour exporter la définition de tâche vers un fichier et vous assurer que la définition de tâche est la même que celle attendue :

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Validation de l’exécution des tâches**

Exécutez cette ligne de commande pour lancer la tâche et vérifier que l’interface utilisateur Planificateur de tâches (taskschd. msc) indique que la tâche a été exécutée :

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Ressources

-   [Planification de la tâche 2,0](/previous-versions/bb756979(v=msdn.10))

 

 
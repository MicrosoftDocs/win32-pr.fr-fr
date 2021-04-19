---
title: Exemple de déclencheur d’inscription (C++)
description: Cet exemple C++ montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’une tâche est inscrite.
ms.assetid: 5e2e8fa6-66c7-4356-8fd6-22f7974791b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090a690601e24e1245040d0e7b394123afa94b07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509808"
---
# <a name="registration-trigger-example-c"></a><span data-ttu-id="22019-103">Exemple de déclencheur d’inscription (C++)</span><span class="sxs-lookup"><span data-stu-id="22019-103">Registration Trigger Example (C++)</span></span>

<span data-ttu-id="22019-104">Cet exemple C++ montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes lorsqu’une tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="22019-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="22019-105">La tâche contient un déclencheur d’inscription qui spécifie une limite de début et une limite de fin pour la tâche, ainsi qu’un délai pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task and also a delay for the task.</span></span> <span data-ttu-id="22019-106">La limite de début spécifie le moment où le déclencheur est activé, et le délai définit la durée entre le moment où la tâche est inscrite et le moment où elle est démarrée.</span><span class="sxs-lookup"><span data-stu-id="22019-106">The start boundary specifies when the trigger is activated, and the delay sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="22019-107">La tâche contient également une action qui spécifie la tâche d’exécution du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="22019-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="22019-108">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="22019-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="22019-109">La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="22019-109">The following procedure describes how to schedule a task to start an executable when the task is registered.</span></span>

<span data-ttu-id="22019-110">**Pour planifier le démarrage du bloc-notes quand une tâche est inscrite**</span><span class="sxs-lookup"><span data-stu-id="22019-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="22019-111">Initialiser COM et définir la sécurité générale de COM.</span><span class="sxs-lookup"><span data-stu-id="22019-111">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="22019-112">Créez l’objet [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="22019-112">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span> <span data-ttu-id="22019-113">Cet objet vous permet de créer des tâches dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="22019-113">This object allows you to create tasks in a specified folder.</span></span>
3.  <span data-ttu-id="22019-114">Obtient un dossier de tâches dans lequel créer une tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-114">Get a task folder to create a task in.</span></span> <span data-ttu-id="22019-115">Utilisez la méthode [**la :: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) pour récupérer le dossier et la méthode [**la :: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) pour créer l’objet [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="22019-115">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>
4.  <span data-ttu-id="22019-116">Définissez des informations sur la tâche à l’aide de l’objet [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , par exemple les informations d’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-116">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span> <span data-ttu-id="22019-117">Utilisez la [**propriété RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) et d’autres propriétés de l’interface **ITaskDefinition** pour définir les informations sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-117">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the **ITaskDefinition** interface to define the task information.</span></span>
5.  <span data-ttu-id="22019-118">Créez un déclencheur d’inscription à l’aide [**de la propriété déclencheurs de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) pour accéder au [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) de la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-118">Create a registration trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span> <span data-ttu-id="22019-119">Utilisez la méthode [**ITriggerCollection :: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (en spécifiant le type de déclencheur que vous souhaitez créer) pour créer un déclencheur d’inscription.</span><span class="sxs-lookup"><span data-stu-id="22019-119">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method (specifying the type of trigger you want to create) to create a registration trigger.</span></span>
6.  <span data-ttu-id="22019-120">Créez une action à exécuter par la tâche à l’aide [**de la propriété actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) pour accéder à l’interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="22019-121">Utilisez la méthode [**IActionCollection :: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="22019-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="22019-122">Cet exemple utilise un objet [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="22019-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="22019-123">Inscrivez la tâche à l’aide de la méthode [**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="22019-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="22019-124">L’exemple C++ suivant montre comment planifier une tâche pour exécuter le bloc-notes 30 secondes après l’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="22019-124">The following C++ example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start notepad.exe 30 seconds after
 the task is registered. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")
#pragma comment(lib, "credui.lib")

using namespace std;


int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
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
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Registration Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        printf("Failed to create an instance of ITaskService: %x", hr);
        CoUninitialize();
        return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    hr = pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to create a task definition: %x", hr);
        pRootFolder->Release();
        CoUninitialize();
        return 1;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author( L"Author Name" );
    pRegInfo->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task
    IPrincipal *pPrincipal = NULL;
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        printf("\nCannot get principal pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set up principal information: 
    hr = pPrincipal->put_Id( _bstr_t(L"Principal1") ); 
    if( FAILED(hr) )
        printf("\nCannot put the principal ID: %x", hr);

    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
        printf("\nCannot put principal logon type: %x", hr);

    //  Run the task with the least privileges (LUA) 
    hr = pPrincipal->put_RunLevel( TASK_RUNLEVEL_LUA ); 
    pPrincipal->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put principal run level: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
   

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task.
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);    
    pSettings->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the registration trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the registration trigger to the task.
    ITrigger *pTrigger = NULL;    
    hr = pTriggerCollection->Create( TASK_TRIGGER_REGISTRATION, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create a registration trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }     
    
    IRegistrationTrigger *pRegistrationTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IRegistrationTrigger, (void**) &pRegistrationTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed on IRegistrationTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegistrationTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);
    
    //  Define the delay for the registration trigger.
    hr = pRegistrationTrigger->put_Delay( L"PT30S" );
    pRegistrationTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put registration trigger delay: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }   
    

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Create the action, specifying that it is an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) ); 
    pExecAction->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put the action executable path: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    //  Clean up.
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="22019-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22019-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22019-126">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="22019-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 





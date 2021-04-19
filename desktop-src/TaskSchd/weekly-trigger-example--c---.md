---
title: Exemple de déclencheur hebdomadaire (C++)
description: Cet exemple C++ montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes chaque semaine.
ms.assetid: 7c70b743-aff2-4ef5-b65b-ef0b5fdacade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7583384a44224b3642f717d00c8792bcbc163e62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509180"
---
# <a name="weekly-trigger-example-c"></a><span data-ttu-id="fa388-103">Exemple de déclencheur hebdomadaire (C++)</span><span class="sxs-lookup"><span data-stu-id="fa388-103">Weekly Trigger Example (C++)</span></span>

<span data-ttu-id="fa388-104">Cet exemple C++ montre comment créer une tâche qui est planifiée pour exécuter le bloc-notes chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="fa388-104">This C++ example shows how to create a task that is scheduled to execute Notepad on a weekly basis.</span></span> <span data-ttu-id="fa388-105">La tâche contient un déclencheur hebdomadaire qui spécifie une limite de début, un intervalle de semaines et un jour de la semaine où commencer la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-105">The task contains a weekly trigger that specifies a start boundary, a weeks interval, and a day of the week for the task to start on.</span></span> <span data-ttu-id="fa388-106">La tâche contient également une action qui spécifie la tâche d’exécution du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="fa388-106">The task also contains an action that specifies the task to execute Notepad.</span></span>

<span data-ttu-id="fa388-107">La procédure suivante décrit comment planifier une tâche pour démarrer un exécutable sur une base hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="fa388-107">The following procedure describes how to schedule a task to start an executable on a weekly basis.</span></span>

<span data-ttu-id="fa388-108">**Pour planifier le démarrage de Notepad sur une base hebdomadaire**</span><span class="sxs-lookup"><span data-stu-id="fa388-108">**To schedule Notepad to start on a weekly basis**</span></span>

1.  <span data-ttu-id="fa388-109">Initialiser COM et définir la sécurité générale de COM.</span><span class="sxs-lookup"><span data-stu-id="fa388-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="fa388-110">Créez l’objet [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="fa388-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="fa388-111">Cet objet vous permet de créer des tâches dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa388-111">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="fa388-112">Obtient un dossier de tâches dans lequel créer une tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-112">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="fa388-113">Utilisez la méthode [**la :: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) pour récupérer le dossier et la méthode [**la :: newtask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) pour créer l’objet [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="fa388-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="fa388-114">Définissez des informations sur la tâche à l’aide de l’objet [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , par exemple les informations d’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-114">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="fa388-115">Utilisez la [**propriété RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) et d’autres propriétés de l’interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) pour définir les informations sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-115">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="fa388-116">Créez un déclencheur hebdomadaire à l’aide [**de la propriété déclencheurs de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) pour accéder à l’interface [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-116">Create a weekly trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) interface for the task.</span></span>

    <span data-ttu-id="fa388-117">Utilisez la méthode [**ITriggerCollection :: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) pour spécifier que vous souhaitez créer un déclencheur hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="fa388-117">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a weekly trigger.</span></span> <span data-ttu-id="fa388-118">Vous pouvez définir la limite de début, l’intervalle des semaines et le jour de la semaine pour le déclencheur [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) afin que les actions de la tâche soient planifiées pour s’exécuter à un moment donné, à un certain jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="fa388-118">You can set the start boundary, the weeks interval, and the day of the week for the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) trigger so that the task's actions will be scheduled to execute at a specified time on a certain day of the week.</span></span>

6.  <span data-ttu-id="fa388-119">Créez une action à exécuter par la tâche à l’aide [**de la propriété actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) pour accéder à l’interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa388-119">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span>

    <span data-ttu-id="fa388-120">Utilisez la méthode [**IActionCollection :: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) pour spécifier le type d’action que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="fa388-120">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="fa388-121">Cet exemple utilise un objet [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fa388-121">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="fa388-122">Inscrivez la tâche à l’aide de la méthode [**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="fa388-122">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="fa388-123">L’exemple C++ suivant montre comment planifier une tâche pour exécuter le bloc-notes sur une base hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="fa388-123">The following C++ example shows how to schedule a task to execute Notepad on a weekly basis.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start on a weekly basis. 
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


void main(void)
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Weekly Trigger Task";

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
          return;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  
    //  This folder will hold the new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );
    
    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
          printf("Failed to create a task definition: %x", hr);
          pRootFolder->Release();
          CoUninitialize();
          return;
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
        return;
    }
    
    hr = pRegInfo->put_Author( L"Author Name" );
    pRegInfo->Release();  // COM clean up.  Pointer is no longer used.
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    //  ------------------------------------------------------
    //  Get the trigger collection to insert the weekly trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
        
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_WEEKLY, &pTrigger );     
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    IWeeklyTrigger *pWeeklyTrigger = NULL;
    hr = pTrigger->QueryInterface( 
            IID_IWeeklyTrigger, (void**) &pWeeklyTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call for IWeeklyTrigger failed: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    hr = pWeeklyTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);

    //  Set the task to start weekly at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below is January 1st 2005 at
    //  12:05
    hr = pWeeklyTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
        printf("\nCannot put the start boundary: %x", hr);

    //  Set the time when the trigger is deactivated.
    hr = pWeeklyTrigger->put_EndBoundary( _bstr_t(L"2007-01-01T12:05:00") );
    if( FAILED(hr) )
        printf("\nCannot put the end boundary: %x", hr);
    
    
    //  Define the interval for the weekly trigger. 
    //  An interval of 2 produces an
    //  every other week schedule
    hr = pWeeklyTrigger->put_WeeksInterval( (short)2 );
    if( FAILED(hr) )
    {
        printf("\nCannot put weeks interval: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }
    
    hr = pWeeklyTrigger->put_DaysOfWeek( (short)2 );    // Runs on Monday
    pWeeklyTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put days of week interval: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
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
        return;
    }
        
    //  Create the action, specifying that it is an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed on IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot add path for executable action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return;
    }

    //  ------------------------------------------------------
    //  Securely get the user name and password. The task will
    //  be created to run with the credentials from the supplied 
    //  user name and password.
    CREDUI_INFO cui;
    TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH] = "";
    TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH] = "";
    BOOL fSave;
    DWORD dwErr;

    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    //  Ensure that MessageText and CaptionText identify
    //  what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Account information for task registration:");
    cui.pszCaptionText = TEXT("Enter Account Information for Task Registration");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    //  Create the UI asking for the credentials.
    dwErr = CredUIPromptForCredentials(
        &cui,                             //  CREDUI_INFO structure
        TEXT(""),                         //  Target for credentials
        NULL,                             //  Reserved
        0,                                //  Reason
        pszName,                          //  User name
        CREDUI_MAX_USERNAME_LENGTH,       //  Max number for user name
        pszPwd,                           //  Password
        CREDUI_MAX_PASSWORD_LENGTH,       //  Max number for password
        &fSave,                           //  State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |  //  Flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr)
    {
        cout << "Did not get credentials." << endl;    
        CoUninitialize();
        return;      
    }

    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(_bstr_t(pszName)), 
            _variant_t(_bstr_t(pszPwd)), 
            TASK_LOGON_PASSWORD,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        SecureZeroMemory(pszName, sizeof(pszName));
        SecureZeroMemory(pszPwd, sizeof(pszPwd));
        CoUninitialize();
        return;
    }

    printf("\n Success! Task succesfully registered. " );

    //  Clean up
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    CoUninitialize();
    return;
}

```



## <a name="related-topics"></a><span data-ttu-id="fa388-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa388-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa388-125">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="fa388-125">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 





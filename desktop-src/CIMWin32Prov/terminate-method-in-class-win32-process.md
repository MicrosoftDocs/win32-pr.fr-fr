---
description: L'&d’arrêt \# 32 ; La méthode de classe WMI termine un processus et tous ses threads.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Méthode Terminate de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950511"
---
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="e448b-103">Méthode Terminate de la \_ classe Process Win32</span><span class="sxs-lookup"><span data-stu-id="e448b-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="e448b-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Terminate** termine un processus et tous ses threads.</span><span class="sxs-lookup"><span data-stu-id="e448b-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="e448b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e448b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e448b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e448b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e448b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e448b-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="e448b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e448b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e448b-109">*Raison* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e448b-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e448b-110">Code de sortie pour le processus et pour tous les threads terminés à la suite de cet appel.</span><span class="sxs-lookup"><span data-stu-id="e448b-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e448b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e448b-111">Return value</span></span>

<span data-ttu-id="e448b-112">Retourne la valeur 0 (zéro) si le processus a été terminé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="e448b-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="e448b-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e448b-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e448b-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e448b-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e448b-115">**Achèvement réussi** (0)</span><span class="sxs-lookup"><span data-stu-id="e448b-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-116">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="e448b-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-117">**Privilèges insuffisants** (3)</span><span class="sxs-lookup"><span data-stu-id="e448b-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-118">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="e448b-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-119">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="e448b-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-120">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="e448b-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e448b-121">**Autre** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e448b-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e448b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e448b-122">Remarks</span></span>

<span data-ttu-id="e448b-123">**Vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="e448b-123">**Overview**</span></span>

<span data-ttu-id="e448b-124">Les problèmes informatiques sont souvent dus à un processus qui ne fonctionne plus comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e448b-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="e448b-125">Par exemple, le processus peut présenter une fuite de mémoire, ou il peut avoir cessé de répondre aux entrées de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e448b-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="e448b-126">Lorsque des problèmes tels que ceux-ci se produisent, le processus doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="e448b-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="e448b-127">Bien que cela puisse sembler une tâche assez simple, l’arrêt d’un processus peut être compliqué par plusieurs facteurs :</span><span class="sxs-lookup"><span data-stu-id="e448b-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="e448b-128">Le processus peut être bloqué et, par conséquent, ne répond plus aux commandes de menu ou de clavier pour la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="e448b-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="e448b-129">C’est tout, mais impossible pour l’utilisateur standard de faire disparaître l’application et de mettre fin au processus.</span><span class="sxs-lookup"><span data-stu-id="e448b-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="e448b-130">Le processus peut être orphelin.</span><span class="sxs-lookup"><span data-stu-id="e448b-130">The process might be orphaned.</span></span> <span data-ttu-id="e448b-131">Par exemple, un script peut créer une instance de Word, puis quitter sans détruire cette instance.</span><span class="sxs-lookup"><span data-stu-id="e448b-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="e448b-132">En effet, Word reste en cours d’exécution sur l’ordinateur, même si aucune interface utilisateur n’est visible.</span><span class="sxs-lookup"><span data-stu-id="e448b-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="e448b-133">Étant donné qu’il n’y a pas d’interface utilisateur, il n’existe pas de commandes de menu ou de clavier disponibles pour mettre fin au processus.</span><span class="sxs-lookup"><span data-stu-id="e448b-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="e448b-134">Vous ne savez peut-être pas quel processus doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="e448b-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="e448b-135">Par exemple, vous souhaiterez peut-être arrêter tous les programmes qui dépassent une quantité de mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e448b-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="e448b-136">Étant donné que le gestionnaire des tâches vous permet de mettre fin uniquement aux processus que vous avez créés, vous risquez de ne pas pouvoir mettre fin à un processus, même si vous êtes administrateur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e448b-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="e448b-137">Les scripts vous permettent de surmonter tous ces obstacles potentiels, ce qui vous permet de disposer d’un contrôle administratif considérable sur vos ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e448b-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="e448b-138">Par exemple, si vous pensez que les utilisateurs jouent des jeux qui ont été interdits dans votre organisation, vous pouvez facilement écrire un script pour vous connecter à chaque ordinateur, identifier si le jeu est en cours d’exécution et arrêter immédiatement le processus.</span><span class="sxs-lookup"><span data-stu-id="e448b-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="e448b-139">**Utilisation de la méthode Terminate**</span><span class="sxs-lookup"><span data-stu-id="e448b-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="e448b-140">Vous pouvez mettre fin à un processus de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="e448b-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="e448b-141">Arrêt d’un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e448b-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="e448b-142">Par exemple, vous devrez peut-être mettre fin à un programme de diagnostic s’exécutant sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="e448b-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="e448b-143">S’il n’existe aucun moyen de contrôler l’application à distance, il vous suffit de mettre fin au processus de cette application.</span><span class="sxs-lookup"><span data-stu-id="e448b-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="e448b-144">Empêcher l’exécution d’un processus en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="e448b-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="e448b-145">En surveillant en continu la création de processus sur un ordinateur, vous pouvez identifier et arrêter instantanément tout processus dès son démarrage.</span><span class="sxs-lookup"><span data-stu-id="e448b-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="e448b-146">Cela permet de s’assurer que certaines applications (telles que les programmes qui téléchargent des fichiers multimédias volumineux sur Internet) ne sont jamais exécutées sur certains ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e448b-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="e448b-147">Stratégie de groupe peut également être utilisé pour restreindre les programmes qui s’exécutent sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e448b-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="e448b-148">Toutefois, stratégie de groupe pouvez restreindre l’exécution des programmes à l’aide du menu Démarrer ou de l’Explorateur Windows ; elle n’a aucun effet sur les programmes démarrés à l’aide d’autres moyens, tels que la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e448b-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="e448b-149">En revanche, WMI peut empêcher l’exécution d’un processus, quelle que soit la façon dont le processus a été démarré.</span><span class="sxs-lookup"><span data-stu-id="e448b-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="e448b-150">**Arrêt d’un processus dont vous n’êtes pas propriétaire**</span><span class="sxs-lookup"><span data-stu-id="e448b-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="e448b-151">Pour mettre fin à un processus dont vous n’êtes pas propriétaire, activez le privilège **SeDebugPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="e448b-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="e448b-152">Dans VBScript, vous pouvez activer ce privilège avec les lignes de code suivantes :</span><span class="sxs-lookup"><span data-stu-id="e448b-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="e448b-153">Pour plus d’informations sur l’activation de ce privilège en C++, consultez [activation et désactivation des privilèges en c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="e448b-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="e448b-154">Exemples</span><span class="sxs-lookup"><span data-stu-id="e448b-154">Examples</span></span>

<span data-ttu-id="e448b-155">L’exemple de code PowerShell [terminer le processus sur plusieurs serveurs](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) dans la Galerie TechNet met fin à un processus s’exécutant sur un ou plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e448b-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="e448b-156">L’exemple VBScript suivant met fin au processus dans lequel l’application Diagnose.exe est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e448b-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="e448b-157">L’exemple VBScript suivant utilise un consommateur d’événements temporaire pour mettre fin à un processus dès son démarrage.</span><span class="sxs-lookup"><span data-stu-id="e448b-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



<span data-ttu-id="e448b-158">L’exemple de code VBScript suivant se connecte à un ordinateur distant et met fin à Notepad.exe sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e448b-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



<span data-ttu-id="e448b-159">Le code C++ suivant met fin au processus de Notepad.exe sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e448b-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="e448b-160">Spécifiez un handle de processus ou (ID de processus) dans le code pour mettre fin au processus.</span><span class="sxs-lookup"><span data-stu-id="e448b-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="e448b-161">Cette valeur se trouve dans la propriété handle de la classe [**\_ processus Win32**](win32-process.md) (la propriété clé de la classe).</span><span class="sxs-lookup"><span data-stu-id="e448b-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="e448b-162">En spécifiant une valeur pour la propriété Handle, vous fournissez un chemin d’accès à l’instance de la classe que vous souhaitez terminer.</span><span class="sxs-lookup"><span data-stu-id="e448b-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="e448b-163">Pour plus d’informations sur la connexion à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="e448b-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="e448b-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e448b-164">Requirements</span></span>



| <span data-ttu-id="e448b-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e448b-165">Requirement</span></span> | <span data-ttu-id="e448b-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="e448b-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e448b-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e448b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e448b-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e448b-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e448b-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e448b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e448b-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e448b-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e448b-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e448b-171">Namespace</span></span><br/>                | <span data-ttu-id="e448b-172">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e448b-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e448b-173">MOF</span><span class="sxs-lookup"><span data-stu-id="e448b-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e448b-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e448b-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e448b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="e448b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e448b-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e448b-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e448b-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e448b-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="e448b-178">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e448b-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e448b-179">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="e448b-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="e448b-180">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="e448b-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="e448b-181">Tâches WMI : processus</span><span class="sxs-lookup"><span data-stu-id="e448b-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 


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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010190"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Méthode Terminate de la \_ classe Process Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Terminate** termine un processus et tous ses threads.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Raison* \[ dans\]
</dt> <dd>

Code de sortie pour le processus et pour tous les threads terminés à la suite de cet appel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) si le processus a été terminé avec succès, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Achèvement réussi** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Privilèges insuffisants** (3)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Chemin introuvable** (9)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Autre** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

**Vue d'ensemble**

Les problèmes informatiques sont souvent dus à un processus qui ne fonctionne plus comme prévu. Par exemple, le processus peut présenter une fuite de mémoire, ou il peut avoir cessé de répondre aux entrées de l’utilisateur. Lorsque des problèmes tels que ceux-ci se produisent, le processus doit être arrêté. Bien que cela puisse sembler une tâche assez simple, l’arrêt d’un processus peut être compliqué par plusieurs facteurs :

-   Le processus peut être bloqué et, par conséquent, ne répond plus aux commandes de menu ou de clavier pour la fermeture de l’application. C’est tout, mais impossible pour l’utilisateur standard de faire disparaître l’application et de mettre fin au processus.
-   Le processus peut être orphelin. Par exemple, un script peut créer une instance de Word, puis quitter sans détruire cette instance. En effet, Word reste en cours d’exécution sur l’ordinateur, même si aucune interface utilisateur n’est visible. Étant donné qu’il n’y a pas d’interface utilisateur, il n’existe pas de commandes de menu ou de clavier disponibles pour mettre fin au processus.
-   Vous ne savez peut-être pas quel processus doit être arrêté. Par exemple, vous souhaiterez peut-être arrêter tous les programmes qui dépassent une quantité de mémoire spécifiée.
-   Étant donné que le gestionnaire des tâches vous permet de mettre fin uniquement aux processus que vous avez créés, vous risquez de ne pas pouvoir mettre fin à un processus, même si vous êtes administrateur de l’ordinateur.

Les scripts vous permettent de surmonter tous ces obstacles potentiels, ce qui vous permet de disposer d’un contrôle administratif considérable sur vos ordinateurs. Par exemple, si vous pensez que les utilisateurs jouent des jeux qui ont été interdits dans votre organisation, vous pouvez facilement écrire un script pour vous connecter à chaque ordinateur, identifier si le jeu est en cours d’exécution et arrêter immédiatement le processus.

**Utilisation de la méthode Terminate**

Vous pouvez mettre fin à un processus de la façon suivante :

-   Arrêt d’un processus en cours d’exécution. Par exemple, vous devrez peut-être mettre fin à un programme de diagnostic s’exécutant sur un ordinateur distant. S’il n’existe aucun moyen de contrôler l’application à distance, il vous suffit de mettre fin au processus de cette application.
-   Empêcher l’exécution d’un processus en premier lieu. En surveillant en continu la création de processus sur un ordinateur, vous pouvez identifier et arrêter instantanément tout processus dès son démarrage. Cela permet de s’assurer que certaines applications (telles que les programmes qui téléchargent des fichiers multimédias volumineux sur Internet) ne sont jamais exécutées sur certains ordinateurs.

> [!Note]  
> Stratégie de groupe peut également être utilisé pour restreindre les programmes qui s’exécutent sur un ordinateur. toutefois, stratégie de groupe pouvez restreindre l’exécution des programmes à l’aide de l’explorateur de menu Démarrer ou Windows ; elle n’a aucun effet sur les programmes démarrés à l’aide d’autres moyens, tels que la ligne de commande. En revanche, WMI peut empêcher l’exécution d’un processus, quelle que soit la façon dont le processus a été démarré.

 

**Arrêt d’un processus dont vous n’êtes pas propriétaire**

Pour mettre fin à un processus dont vous n’êtes pas propriétaire, activez le privilège **SeDebugPrivilege** . Dans VBScript, vous pouvez activer ce privilège avec les lignes de code suivantes :


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Pour plus d’informations sur l’activation de ce privilège en C++, consultez [activation et désactivation des privilèges en c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Exemples

L’exemple de code PowerShell [terminer le processus sur plusieurs serveurs](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) dans la Galerie TechNet met fin à un processus s’exécutant sur un ou plusieurs ordinateurs.

L’exemple VBScript suivant met fin au processus dans lequel l’application Diagnose.exe est en cours d’exécution.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



L’exemple VBScript suivant utilise un consommateur d’événements temporaire pour mettre fin à un processus dès son démarrage.


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



L’exemple de code VBScript suivant se connecte à un ordinateur distant et met fin à Notepad.exe sur cet ordinateur.


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



Le code C++ suivant met fin au processus de Notepad.exe sur l’ordinateur local. Spécifiez un handle de processus ou (ID de processus) dans le code pour mettre fin au processus. Cette valeur se trouve dans la propriété handle de la classe [**\_ processus Win32**](win32-process.md) (la propriété clé de la classe). En spécifiant une valeur pour la propriété Handle, vous fournissez un chemin d’accès à l’instance de la classe que vous souhaitez terminer. Pour plus d’informations sur la connexion à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> <dt>

[Tâches WMI : analyse des performances](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Tâches WMI : processus](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 


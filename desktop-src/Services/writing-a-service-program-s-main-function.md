---
description: L’exemple suivant peut être utilisé comme point d’entrée pour un programme de service qui prend en charge un seul service.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Écriture d’une fonction principale d’un programme de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120706"
---
# <a name="writing-a-service-programs-main-function"></a>Écriture de la fonction principale d’un programme de service

La fonction **main** d’un [programme de service](service-programs.md) appelle la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) pour se connecter au gestionnaire de [contrôle des services](service-control-manager.md) (SCM) et démarrer le thread répartiteur de contrôle. Le thread du répartiteur effectue une boucle, en attendant les demandes de contrôle entrantes pour les services spécifiés dans la table de dispatch. Ce thread retourne lorsqu’il existe une erreur ou lorsque tous les services du processus sont terminés. Lorsque tous les services du processus sont terminés, le SCM envoie une demande de contrôle au thread de répartiteur en lui indiquant de quitter. Ce thread retourne ensuite à partir de l’appel de **StartServiceCtrlDispatcher** et le processus peut se terminer.

Les définitions globales suivantes sont utilisées dans cet exemple.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



L’exemple suivant peut être utilisé comme point d’entrée pour un programme de service qui prend en charge un seul service. Si votre programme de service prend en charge plusieurs services, ajoutez les noms des services supplémentaires à la table de dispatch afin qu’ils puissent être surveillés par le thread du répartiteur.

La \_ fonction tmain est le point d’entrée. La fonction SvcReportEvent écrit des messages d’information et des erreurs dans le journal des événements. Pour plus d’informations sur l’écriture de la fonction SvcMain, consultez [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md). Pour plus d’informations sur la fonction SvcInstall, consultez [installation d’un service](installing-a-service.md). Pour plus d’informations sur l’écriture de la fonction SvcCtrlHandler, consultez [écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md). Pour obtenir un exemple complet de service, y compris la source de la fonction SvcReportEvent, consultez [SVC. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



Voici un exemple d’exemple. h tel qu’il est généré par le compilateur de message. Pour plus d’informations, consultez [Sample.MC](sample-mc.md).

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Point d’entrée de service](service-entry-point.md)
</dt> <dt>

[Exemple de service complet](the-complete-service-sample.md)
</dt> </dl>

 

 




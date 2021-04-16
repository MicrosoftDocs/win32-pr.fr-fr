---
description: L’exemple suivant peut être utilisé comme point d’entrée pour un programme de service qui prend en charge un seul service.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Écriture d’une fonction principale d’un programme de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525809"
---
# <a name="writing-a-service-programs-main-function"></a><span data-ttu-id="024d7-103">Écriture de la fonction principale d’un programme de service</span><span class="sxs-lookup"><span data-stu-id="024d7-103">Writing a Service Program's main Function</span></span>

<span data-ttu-id="024d7-104">La fonction **main** d’un [programme de service](service-programs.md) appelle la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) pour se connecter au gestionnaire de [contrôle des services](service-control-manager.md) (SCM) et démarrer le thread répartiteur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="024d7-104">The **main** function of a [service program](service-programs.md) calls the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function to connect to the [service control manager](service-control-manager.md) (SCM) and start the control dispatcher thread.</span></span> <span data-ttu-id="024d7-105">Le thread du répartiteur effectue une boucle, en attendant les demandes de contrôle entrantes pour les services spécifiés dans la table de dispatch.</span><span class="sxs-lookup"><span data-stu-id="024d7-105">The dispatcher thread loops, waiting for incoming control requests for the services specified in the dispatch table.</span></span> <span data-ttu-id="024d7-106">Ce thread retourne lorsqu’il existe une erreur ou lorsque tous les services du processus sont terminés.</span><span class="sxs-lookup"><span data-stu-id="024d7-106">This thread returns when there is an error or when all of the services in the process have terminated.</span></span> <span data-ttu-id="024d7-107">Lorsque tous les services du processus sont terminés, le SCM envoie une demande de contrôle au thread de répartiteur en lui indiquant de quitter.</span><span class="sxs-lookup"><span data-stu-id="024d7-107">When all services in the process have terminated, the SCM sends a control request to the dispatcher thread telling it to exit.</span></span> <span data-ttu-id="024d7-108">Ce thread retourne ensuite à partir de l’appel de **StartServiceCtrlDispatcher** et le processus peut se terminer.</span><span class="sxs-lookup"><span data-stu-id="024d7-108">This thread then returns from the **StartServiceCtrlDispatcher** call and the process can terminate.</span></span>

<span data-ttu-id="024d7-109">Les définitions globales suivantes sont utilisées dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="024d7-109">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="024d7-110">L’exemple suivant peut être utilisé comme point d’entrée pour un programme de service qui prend en charge un seul service.</span><span class="sxs-lookup"><span data-stu-id="024d7-110">The following example can be used as the entry point for a service program that supports a single service.</span></span> <span data-ttu-id="024d7-111">Si votre programme de service prend en charge plusieurs services, ajoutez les noms des services supplémentaires à la table de dispatch afin qu’ils puissent être surveillés par le thread du répartiteur.</span><span class="sxs-lookup"><span data-stu-id="024d7-111">If your service program supports multiple services, add the names of the additional services to the dispatch table so they can be monitored by the dispatcher thread.</span></span>

<span data-ttu-id="024d7-112">La \_ fonction tmain est le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="024d7-112">The \_tmain function is the entry point.</span></span> <span data-ttu-id="024d7-113">La fonction SvcReportEvent écrit des messages d’information et des erreurs dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="024d7-113">The SvcReportEvent function writes informational messages and errors to the event log.</span></span> <span data-ttu-id="024d7-114">Pour plus d’informations sur l’écriture de la fonction SvcMain, consultez [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="024d7-114">For information about writing the SvcMain function, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span> <span data-ttu-id="024d7-115">Pour plus d’informations sur la fonction SvcInstall, consultez [installation d’un service](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="024d7-115">For more information about the SvcInstall function, see [Installing a Service](installing-a-service.md).</span></span> <span data-ttu-id="024d7-116">Pour plus d’informations sur l’écriture de la fonction SvcCtrlHandler, consultez [écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="024d7-116">For information about writing the SvcCtrlHandler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span> <span data-ttu-id="024d7-117">Pour obtenir un exemple complet de service, y compris la source de la fonction SvcReportEvent, consultez [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="024d7-117">For the complete example service, including the source for the SvcReportEvent function, see [Svc.cpp](svc-cpp.md).</span></span>


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



<span data-ttu-id="024d7-118">Voici un exemple d’exemple. h tel qu’il est généré par le compilateur de message.</span><span class="sxs-lookup"><span data-stu-id="024d7-118">The following is an example Sample.h as generated by the message compiler.</span></span> <span data-ttu-id="024d7-119">Pour plus d’informations, consultez [Sample.MC](sample-mc.md).</span><span class="sxs-lookup"><span data-stu-id="024d7-119">For more information, see [Sample.mc](sample-mc.md).</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="024d7-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="024d7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="024d7-121">Point d’entrée de service</span><span class="sxs-lookup"><span data-stu-id="024d7-121">Service Entry Point</span></span>](service-entry-point.md)
</dt> <dt>

[<span data-ttu-id="024d7-122">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="024d7-122">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 




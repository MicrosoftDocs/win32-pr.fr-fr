---
description: Quand une fonction de gestionnaire est appelée par le thread du répartiteur, elle gère le code de contrôle passé dans le paramètre OpCode, puis appelle la fonction ReportSvcStatus pour mettre à jour l’état du service.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Écriture d’une fonction de gestionnaire de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517477"
---
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="e6b5d-103">Écriture d’une fonction de gestionnaire de contrôle</span><span class="sxs-lookup"><span data-stu-id="e6b5d-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="e6b5d-104">Quand une fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) est appelée par le thread du répartiteur, elle gère le code de contrôle passé dans le paramètre *opcode* , puis appelle la fonction ReportSvcStatus pour mettre à jour l’état du service.</span><span class="sxs-lookup"><span data-stu-id="e6b5d-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="e6b5d-105">Quand une fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) reçoit un code de contrôle, elle doit signaler l’état du service uniquement si la gestion du code de contrôle entraîne la modification de l’état du service.</span><span class="sxs-lookup"><span data-stu-id="e6b5d-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="e6b5d-106">Si le service n’agit pas sur le contrôle, il ne doit pas signaler l’État au gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="e6b5d-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="e6b5d-107">Pour obtenir le code source de ReportSvcStatus, consultez [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="e6b5d-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="e6b5d-108">Dans l’exemple suivant, la fonction SvcCtrlHandler est un exemple de fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="e6b5d-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="e6b5d-109">Notez que la variable ghSvcStopEvent est une variable globale qui doit être initialisée et utilisée comme illustré dans l' [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="e6b5d-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a><span data-ttu-id="e6b5d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6b5d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b5d-111">Fonction du gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="e6b5d-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="e6b5d-112">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="e6b5d-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 




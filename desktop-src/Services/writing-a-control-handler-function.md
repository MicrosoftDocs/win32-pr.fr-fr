---
description: Quand une fonction de gestionnaire est appelée par le thread du répartiteur, elle gère le code de contrôle passé dans le paramètre OpCode, puis appelle la fonction ReportSvcStatus pour mettre à jour l’état du service.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Écriture d’une fonction de gestionnaire de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888060"
---
# <a name="writing-a-control-handler-function"></a>Écriture d’une fonction de gestionnaire de contrôle

Quand une fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) est appelée par le thread du répartiteur, elle gère le code de contrôle passé dans le paramètre *opcode* , puis appelle la fonction ReportSvcStatus pour mettre à jour l’état du service. Quand une fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) reçoit un code de contrôle, elle doit signaler l’état du service uniquement si la gestion du code de contrôle entraîne la modification de l’état du service. Si le service n’agit pas sur le contrôle, il ne doit pas signaler l’État au gestionnaire de contrôle des services. Pour obtenir le code source de ReportSvcStatus, consultez [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).

Dans l’exemple suivant, la fonction SvcCtrlHandler est un exemple de fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) . Notez que la variable ghSvcStopEvent est une variable globale qui doit être initialisée et utilisée comme illustré dans l' [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonction du gestionnaire de contrôle des services](service-control-handler-function.md)
</dt> <dt>

[Exemple de service complet](the-complete-service-sample.md)
</dt> </dl>

 

 




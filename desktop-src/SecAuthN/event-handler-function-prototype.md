---
description: Les fonctions de prototype du gestionnaire d’événements sont utilisées pour toutes les fonctions qui gèrent les événements de notification Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Fonction de rappel de prototype de fonction du gestionnaire d’événements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: df6670e852ccd12fd2bed1d0c188aa0252c9b3afbcb899cf9480b7011d08625d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008227"
---
# <a name="event-handler-function-prototype-callback-function"></a>Fonction de rappel de prototype de fonction du gestionnaire d’événements

\[les fonctions de Prototype du gestionnaire d’événements ne sont plus utilisables à partir de Windows Server 2008 et Windows Vista. \]

Les fonctions de prototype du gestionnaire d’événements sont utilisées pour toutes les fonctions qui gèrent les événements de notification [*Winlogon*](/windows/desktop/SecGloss/w-gly) . Le nom de la fonction, représenté ci-dessous par le nom de la fonction du gestionnaire d’événements de l’espace réservé, reflète généralement le nom de l’événement géré par la fonction. *\_ \_ \_* Par exemple, la fonction qui gère les événements d’ouverture de session peut être nommée : **WLEventLogon**.

## <a name="syntax"></a>Syntaxe


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ informations de notification wlx**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) qui contient les détails de l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction de rappel ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si votre gestionnaire d’événements doit créer des processus enfants, il doit appeler la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Dans le cas contraire, le nouveau processus sera créé sur le bureau Winlogon, et non sur le Bureau de l’utilisateur.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment implémenter des gestionnaires d’événements pour les événements Winlogon. Par souci de simplicité, seules les implémentations des gestionnaires d’événements Logon et Logoff sont affichées. Vous pouvez implémenter des gestionnaires pour le reste des événements exactement de la même manière.


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 


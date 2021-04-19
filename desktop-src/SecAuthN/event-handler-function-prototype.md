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
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521354"
---
# <a name="event-handler-function-prototype-callback-function"></a>Fonction de rappel de prototype de fonction du gestionnaire d’événements

\[Les fonctions de prototype du gestionnaire d’événements ne sont plus disponibles pour une utilisation à partir de Windows Server 2008 et Windows Vista. \]

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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 


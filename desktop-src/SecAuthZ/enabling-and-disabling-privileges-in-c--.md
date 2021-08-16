---
description: L’activation d’un privilège dans un jeton d’accès permet au processus d’effectuer des actions au niveau du système qu’il ne pouvait pas avoir précédemment.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Activation et désactivation des privilèges en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781725"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Activation et désactivation des privilèges en C++

L’activation d’un privilège dans un jeton d’accès permet au processus d’effectuer des actions au niveau du système qu’il ne pouvait pas avoir précédemment. Votre application doit vérifier minutieusement que le privilège est approprié au type de compte, en particulier pour les privilèges puissants suivants.



| Privilège, constante           | Valeur de chaîne                  | Nom d’affichage                        |
|------------------------------|-------------------------------|-------------------------------------|
| SE \_ nom de ASSIGNPRIMARYTOKEN \_ | SeAssignPrimaryTokenPrivilege | Remplacer un jeton de niveau processus       |
| SE \_ nom de la sauvegarde \_             | SeBackupPrivilege             | Sauvegarder des fichiers et des répertoires       |
| SE \_ nom du débogage \_              | SeDebugPrivilege              | Déboguer les programmes                      |
| SE \_ AUGMENTER \_ le \_ nom du quota    | SeIncreaseQuotaPrivilege      | Ajuster les quotas de mémoire pour un processus  |
| SE \_ \_nom TCB                | SeTcbPrivilege                | Agir en tant que partie du système d'exploitation |



 

Avant d’activer l’un de ces privilèges potentiellement dangereux, déterminez que les fonctions ou opérations de votre code nécessitent réellement les privilèges. Par exemple, très peu de fonctions du système d’exploitation nécessitent en fait le **SeTcbPrivilege**. Pour obtenir la liste de tous les privilèges disponibles, consultez [constantes de privilège](authorization-constants.md).

L’exemple suivant montre comment activer ou désactiver un privilège dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly). L’exemple appelle la fonction [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) pour récupérer l' [*identificateur unique local*](/windows/desktop/SecGloss/l-gly) (LUID) que le système local utilise pour identifier le privilège. L’exemple appelle ensuite la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , qui active ou désactive le privilège qui dépend de la valeur du paramètre *bEnablePrivilege* .


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 


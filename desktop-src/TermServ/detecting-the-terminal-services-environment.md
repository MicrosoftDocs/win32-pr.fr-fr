---
title: Détection de l’environnement de Services Bureau à distance
description: Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507235"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Détection de l’environnement de Services Bureau à distance

Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance. Par exemple, lorsqu’une application s’exécute sur une session à distance, elle doit éliminer les effets graphiques inutiles, comme décrit dans [effets de graphiques](graphic-effects.md). Si l’utilisateur exécute l’application dans un environnement local, il n’est pas aussi essentiel pour l’application d’optimiser son comportement.

L’exemple suivant montre une fonction qui retourne **true** si l’application s’exécute dans une session à distance et **false** si l’application est en cours d’exécution sur la console.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Pour plus d’informations, consultez la page [liaison au moment de l’exécution pour Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Vous ne devez pas utiliser **GetSystemMetrics (SM \_ REMOTESESSION)** pour déterminer si votre application s’exécute dans une session à distance dans Windows 8 et versions ultérieures, ou Windows Server 2012 et versions ultérieures si la session à distance peut également utiliser les améliorations du processeur graphique à distance RemoteFX avec le protocole RDP (Microsoft Remote Display Protocol). Dans ce cas, **GetSystemMetrics (SM \_ REMOTESESSION)** identifie la session à distance en tant que session locale.

Votre application peut vérifier la clé de Registre suivante pour déterminer si la session est une session à distance qui utilise le processeur graphique virtuel RemoteFX. Si une session locale existe, cette clé de Registre fournit l’ID de la session locale.

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Si l’ID de la session active dans laquelle l’application est exécutée est identique à celui de la clé de Registre, l’application s’exécute dans une session locale. Les sessions identifiées comme session à distance de cette façon incluent les sessions à distance qui utilisent le processeur graphique virtuel RemoteFX. C'est ce que montre l'exemple de code suivant.


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 





---
title: Détection de l’environnement de Services Bureau à distance
description: Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f54634112b4a6ac3cc1e981421e4a3e33af5e32bae8ab63ec8690f2df12c7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657989"
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

vous ne devez pas utiliser **GetSystemMetrics (SM \_ REMOTESESSION)** pour déterminer si votre application s’exécute dans une session à distance dans Windows 8 et versions ultérieures, ou Windows Server 2012 et versions ultérieures si la session à distance peut également utiliser le RemoteFX améliorations du processeur graphique à distance (RDP) de Microsoft. Dans ce cas, **GetSystemMetrics (SM \_ REMOTESESSION)** identifie la session à distance en tant que session locale.

votre application peut vérifier la clé de registre suivante pour déterminer si la session est une session à distance qui utilise RemoteFX processeur graphique virtuel. Si une session locale existe, cette clé de Registre fournit l’ID de la session locale.

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Si l’ID de la session active dans laquelle l’application est exécutée est identique à celui de la clé de Registre, l’application s’exécute dans une session locale. les sessions identifiées comme session à distance de cette façon incluent les sessions à distance qui utilisent RemoteFX processeur graphique virtuel. C'est ce que montre l'exemple de code suivant.


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



 

 





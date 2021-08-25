---
description: Décrit comment détecter si un ensemble d’API spécifique est disponible sur l’appareil actuel.
title: Détecter la disponibilité des ensembles d’API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: cc4e26c6e59cfa0af095b297efb72a52d0be30a89a23d42d169e3bf45e72fd13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896529"
---
# <a name="detect-api-set-availability"></a>Détecter la disponibilité des ensembles d’API

dans certains cas, un nom de contrat d’ensemble d’API donné peut être mappé intentionnellement à un nom de module vide sur certains appareils Windows 10. les raisons varient, mais un exemple courant est qu’une fonctionnalité coûteuse en termes de ressources système peut être supprimée du système d’exploitation Windows lorsqu’elle est configurée pour un appareil à ressources restreintes. Cela pose un défi pour que les applications gèrent correctement les fonctionnalités facultatives au niveau de l’API.

L’approche traditionnelle pour tester si une API Win32 est disponible consiste à utiliser [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Toutefois, il ne s’agit pas d’un moyen fiable pour tester les jeux d’API en raison de la prise en charge du [transfert inverse](api-set-loader-operation.md#reverse-forwarding) dans Windows 10. Lorsque le transfert inverse est appliqué à une API donnée, **LoadLibrary** ou **GetProcAddress** peut être résolu en pointeur fonction valide même dans les cas où l’implémentation interne a été supprimée. Dans ce cas, le pointeur de fonction pointe vers une fonction stub qui retourne simplement une erreur.

Pour détecter ce cas, vous pouvez utiliser la fonction [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) pour interroger la disponibilité sous-jacente d’une implémentation d’API donnée. Ce test permet de vérifier que l’appel de cette fonction entraîne l’exécution d’une implémentation fonctionnelle de l’API.

L’exemple de code suivant montre comment utiliser **IsApiSetImplemented** pour déterminer si la fonction [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) est disponible sur l’appareil actuel avant de l’appeler. 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```
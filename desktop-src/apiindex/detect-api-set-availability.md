---
description: Décrit comment détecter si un ensemble d’API spécifique est disponible sur l’appareil actuel.
title: Détecter la disponibilité des ensembles d’API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "104102545"
---
# <a name="detect-api-set-availability"></a><span data-ttu-id="beb01-103">Détecter la disponibilité des ensembles d’API</span><span class="sxs-lookup"><span data-stu-id="beb01-103">Detect API set availability</span></span>

<span data-ttu-id="beb01-104">Dans certains cas, un nom de contrat d’ensemble d’API donné peut être mappé intentionnellement à un nom de module vide sur certains appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="beb01-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="beb01-105">Les raisons de cela varient, mais un exemple courant est qu’une fonctionnalité coûteuse en termes de ressources système peut être supprimée du système d’exploitation Windows lorsqu’elle est configurée pour un appareil à ressources restreintes.</span><span class="sxs-lookup"><span data-stu-id="beb01-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="beb01-106">Cela pose un défi pour que les applications gèrent correctement les fonctionnalités facultatives au niveau de l’API.</span><span class="sxs-lookup"><span data-stu-id="beb01-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="beb01-107">L’approche traditionnelle pour tester si une API Win32 est disponible consiste à utiliser [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="beb01-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="beb01-108">Toutefois, il ne s’agit pas d’un moyen fiable pour tester les jeux d’API en raison de la prise en charge du [transfert inverse](api-set-loader-operation.md#reverse-forwarding) dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="beb01-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="beb01-109">Lorsque le transfert inverse est appliqué à une API donnée, **LoadLibrary** ou **GetProcAddress** peut être résolu en pointeur fonction valide même dans les cas où l’implémentation interne a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="beb01-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="beb01-110">Dans ce cas, le pointeur de fonction pointe vers une fonction stub qui retourne simplement une erreur.</span><span class="sxs-lookup"><span data-stu-id="beb01-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="beb01-111">Pour détecter ce cas, vous pouvez utiliser la fonction [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) pour interroger la disponibilité sous-jacente d’une implémentation d’API donnée.</span><span class="sxs-lookup"><span data-stu-id="beb01-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="beb01-112">Ce test permet de vérifier que l’appel de cette fonction entraîne l’exécution d’une implémentation fonctionnelle de l’API.</span><span class="sxs-lookup"><span data-stu-id="beb01-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="beb01-113">L’exemple de code suivant montre comment utiliser **IsApiSetImplemented** pour déterminer si la fonction [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) est disponible sur l’appareil actuel avant de l’appeler.</span><span class="sxs-lookup"><span data-stu-id="beb01-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

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
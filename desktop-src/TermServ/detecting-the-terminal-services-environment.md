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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="f8412-103">Détection de l’environnement de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f8412-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="f8412-104">Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f8412-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="f8412-105">Par exemple, lorsqu’une application s’exécute sur une session à distance, elle doit éliminer les effets graphiques inutiles, comme décrit dans [effets de graphiques](graphic-effects.md).</span><span class="sxs-lookup"><span data-stu-id="f8412-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="f8412-106">Si l’utilisateur exécute l’application dans un environnement local, il n’est pas aussi essentiel pour l’application d’optimiser son comportement.</span><span class="sxs-lookup"><span data-stu-id="f8412-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="f8412-107">L’exemple suivant montre une fonction qui retourne **true** si l’application s’exécute dans une session à distance et **false** si l’application est en cours d’exécution sur la console.</span><span class="sxs-lookup"><span data-stu-id="f8412-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="f8412-108">Pour plus d’informations, consultez la page [liaison au moment de l’exécution pour Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f8412-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="f8412-109">Vous ne devez pas utiliser **GetSystemMetrics (SM \_ REMOTESESSION)** pour déterminer si votre application s’exécute dans une session à distance dans Windows 8 et versions ultérieures, ou Windows Server 2012 et versions ultérieures si la session à distance peut également utiliser les améliorations du processeur graphique à distance RemoteFX avec le protocole RDP (Microsoft Remote Display Protocol).</span><span class="sxs-lookup"><span data-stu-id="f8412-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="f8412-110">Dans ce cas, **GetSystemMetrics (SM \_ REMOTESESSION)** identifie la session à distance en tant que session locale.</span><span class="sxs-lookup"><span data-stu-id="f8412-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="f8412-111">Votre application peut vérifier la clé de Registre suivante pour déterminer si la session est une session à distance qui utilise le processeur graphique virtuel RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="f8412-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="f8412-112">Si une session locale existe, cette clé de Registre fournit l’ID de la session locale.</span><span class="sxs-lookup"><span data-stu-id="f8412-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="f8412-113">**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**</span><span class="sxs-lookup"><span data-stu-id="f8412-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="f8412-114">Si l’ID de la session active dans laquelle l’application est exécutée est identique à celui de la clé de Registre, l’application s’exécute dans une session locale.</span><span class="sxs-lookup"><span data-stu-id="f8412-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="f8412-115">Les sessions identifiées comme session à distance de cette façon incluent les sessions à distance qui utilisent le processeur graphique virtuel RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="f8412-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="f8412-116">C'est ce que montre l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="f8412-116">The following sample code demonstrates this.</span></span>


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



 

 





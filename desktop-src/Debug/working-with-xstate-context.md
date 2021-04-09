---
description: Ce document contient un exemple qui montre comment utiliser les fonctions de contexte XState pour récupérer et définir des fonctionnalités étendues sur un thread.
ms.assetid: F7937402-1173-4647-B9FF-856C0925C1C3
title: Utilisation du contexte XState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca58a8fadb4404e2f6fc431b7b7d2a9d7f583f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861125"
---
# <a name="working-with-xstate-context"></a><span data-ttu-id="1aa8f-103">Utilisation du contexte XState</span><span class="sxs-lookup"><span data-stu-id="1aa8f-103">Working with XState Context</span></span>

<span data-ttu-id="1aa8f-104">Ce document contient un exemple qui montre comment utiliser les fonctions de contexte XState pour récupérer et définir des fonctionnalités étendues sur un thread.</span><span class="sxs-lookup"><span data-stu-id="1aa8f-104">This document contains an example that demonstrates how to use the XState context functions to retrieve and set extended features on a thread.</span></span> <span data-ttu-id="1aa8f-105">Les exemples suivants manipulent l’état d’Intel Advanced Vector Extensions (AVX) qui est défini par FeatureId 2 (Feature Mask 4).</span><span class="sxs-lookup"><span data-stu-id="1aa8f-105">The following examples manipulate Intel Advanced Vector Extensions (AVX) state which is defined by FeatureId 2 (Feature Mask 4).</span></span> <span data-ttu-id="1aa8f-106">Intel AVX est défini dans la « référence de programmation Intel Advanced Vector Extensions » disponible à partir de <https://go.microsoft.com/fwlink/p/?linkid=212716> .</span><span class="sxs-lookup"><span data-stu-id="1aa8f-106">Intel AVX is defined in the "Intel Advanced Vector Extensions Programming Reference" available from <https://go.microsoft.com/fwlink/p/?linkid=212716>.</span></span>

<span data-ttu-id="1aa8f-107">**Windows 7 avec SP1 :** L' [API AVX](avx-support-portal.md) est tout d’abord implémentée sur Windows 7 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="1aa8f-107">**Windows 7 with SP1:** The [AVX API](avx-support-portal.md) is first implemented on Windows 7 with SP1.</span></span> <span data-ttu-id="1aa8f-108">Étant donné qu’il n’existe aucun kit de développement logiciel (SDK) pour Windows 7 avec SP1, cela signifie qu’il n’y a aucun en-tête et fichier de bibliothèque disponibles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1aa8f-108">Since there is no SDK for Windows 7 with SP1, that means there are no available headers and library files to work with.</span></span> <span data-ttu-id="1aa8f-109">Dans ce cas, un appelant doit déclarer les fonctions nécessaires à partir de cette documentation et y obtenir des pointeurs à l’aide de [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) sur « Kernel32.dll », suivi par des appels à [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="1aa8f-109">In this situation, a caller must declare the needed functions from this documentation and get pointers to them using [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) on "Kernel32.dll", followed by calls to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>


```C++
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <winerror.h>

// Windows 7 SP1 is the first version of Windows to support the AVX API.

// The value for CONTEXT_XSTATE has changed between Windows 7 and
// Windows 7 SP1 and greater.
// While the value will be correct for future SDK headers, we need to set 
// this value manually when building with a Windows 7 SDK for running on 
// Windows 7 SPI OS bits.

#undef CONTEXT_XSTATE

#if defined(_M_X64)
#define CONTEXT_XSTATE                      (0x00100040)
#else
#define CONTEXT_XSTATE                      (0x00010040)
#endif

// Since the AVX API is not declared in the Windows 7 SDK headers and 
// since we don't have the proper libs to work with, we will declare 
// the API as function pointers and get them with GetProcAddress calls 
// from kernel32.dll.  We also need to set some #defines.

#define XSTATE_AVX                          (XSTATE_GSSE)
#define XSTATE_MASK_AVX                     (XSTATE_MASK_GSSE)

typedef DWORD64 (WINAPI *PGETENABLEDXSTATEFEATURES)();
PGETENABLEDXSTATEFEATURES pfnGetEnabledXStateFeatures = NULL;

typedef BOOL (WINAPI *PINITIALIZECONTEXT)(PVOID Buffer, DWORD ContextFlags, PCONTEXT* Context, PDWORD ContextLength);
PINITIALIZECONTEXT pfnInitializeContext = NULL;
    
typedef BOOL (WINAPI *PGETXSTATEFEATURESMASK)(PCONTEXT Context, PDWORD64 FeatureMask);
PGETXSTATEFEATURESMASK pfnGetXStateFeaturesMask = NULL;

typedef PVOID (WINAPI *LOCATEXSTATEFEATURE)(PCONTEXT Context, DWORD FeatureId, PDWORD Length);
LOCATEXSTATEFEATURE pfnLocateXStateFeature = NULL;
    
typedef BOOL (WINAPI *SETXSTATEFEATURESMASK)(PCONTEXT Context, DWORD64 FeatureMask);
SETXSTATEFEATURESMASK pfnSetXStateFeaturesMask = NULL;
    
VOID
PrintThreadAvxState (
    __in HANDLE hThread
    )
{
    PVOID Buffer;
    PCONTEXT Context;
    DWORD ContextSize;
    DWORD64 FeatureMask;
    DWORD FeatureLength;
    ULONG Index;
    BOOL Success;
    PM128A Xmm;
    PM128A Ymm;

    // If this function was called before and we were not running on 
    // at least Windows 7 SP1, then bail.
    if (pfnGetEnabledXStateFeatures == (PGETENABLEDXSTATEFEATURES)-1)
    {
        _tprintf(_T("This needs to run on Windows 7 SP1 or greater.\n"));
        return;
    }

    // Get the addresses of the AVX XState functions.
    if (pfnGetEnabledXStateFeatures == NULL)
    {
        HMODULE hm = GetModuleHandle(_T("kernel32.dll"));
        if (hm == NULL)
        {
            pfnGetEnabledXStateFeatures = (PGETENABLEDXSTATEFEATURES)-1;
            _tprintf(_T("GetModuleHandle failed (error == %d).\n"), GetLastError());
            return;
        }
        
        pfnGetEnabledXStateFeatures = (PGETENABLEDXSTATEFEATURES)GetProcAddress(hm, "GetEnabledXStateFeatures");
        pfnInitializeContext = (PINITIALIZECONTEXT)GetProcAddress(hm, "InitializeContext");
        pfnGetXStateFeaturesMask = (PGETXSTATEFEATURESMASK)GetProcAddress(hm, "GetXStateFeaturesMask");
        pfnLocateXStateFeature = (LOCATEXSTATEFEATURE)GetProcAddress(hm, "LocateXStateFeature");
        pfnSetXStateFeaturesMask = (SETXSTATEFEATURESMASK)GetProcAddress(hm, "SetXStateFeaturesMask");
        
        if (pfnGetEnabledXStateFeatures == NULL
            || pfnInitializeContext == NULL
            || pfnGetXStateFeaturesMask == NULL
            || pfnLocateXStateFeature == NULL
            || pfnSetXStateFeaturesMask == NULL)
        {
            pfnGetEnabledXStateFeatures = (PGETENABLEDXSTATEFEATURES)-1;
            _tprintf(_T("This needs to run on Windows 7 SP1 or greater.\n"));
            return;
        }
    }
    
    FeatureMask = pfnGetEnabledXStateFeatures();
    if ((FeatureMask & XSTATE_MASK_AVX) == 0)
    {
        _tprintf(_T("The AVX feature is not enabled.\n"));
        return;
    }

    ContextSize = 0;
    Success = pfnInitializeContext(NULL,
                                   CONTEXT_ALL | CONTEXT_XSTATE,
                                   NULL,
                                   &ContextSize);

    if ((Success == TRUE) || (GetLastError() != ERROR_INSUFFICIENT_BUFFER))
    {
        _tprintf(_T("Unexpected result from InitializeContext (success == %d, error == %d).\n"),
                 Success,
                 GetLastError());
    }

    Buffer = malloc(ContextSize);
    if (Buffer == NULL)
    {
        _tprintf(_T("Out of memory.\n"));
        return;
    }

    Success = pfnInitializeContext(Buffer,
                                   CONTEXT_ALL | CONTEXT_XSTATE,
                                   &Context,
                                   &ContextSize);

    if (Success == FALSE)
    {
        _tprintf(_T("InitializeContext failed (error == %d).\n"), GetLastError());
        goto Cleanup;
    }

    Success = pfnSetXStateFeaturesMask(Context, XSTATE_MASK_AVX);
    if (Success == FALSE)
    {
        _tprintf(_T("SetXStateFeaturesMask failed (error == %d).\n"), GetLastError());
        goto Cleanup;
    }
    
    Success = GetThreadContext(hThread, Context);
    // Note: Thread state may not be accurate. For best results, suspend 
    // the thread and use the CONTEXT_EXCEPTION_REQUEST flags prior to 
    // calling GetThreadContext.
    if (Success == FALSE)
    {
        _tprintf(_T("GetThreadContext failed (error == %d).\n"), GetLastError());
        goto Cleanup;
    }

    Success = pfnGetXStateFeaturesMask(Context, &FeatureMask);
    if (Success == FALSE)
    {
        _tprintf(_T("GetXStateFeatureMask failed (error == %d).\n"), GetLastError());
        goto Cleanup;
    }

    //
    // The AVX feature consists of 8 (x86) or 16 (x64) 256-bit Ymm registers.
    // The lower 128 bits share storage with the corresponding Xmm (SSE)
    // registers and the high 128 bits are denoted by Ymm_H0 - Ymm_Hn.
    //

    if ((FeatureMask & XSTATE_MASK_AVX) == 0)
    {
        _tprintf(_T("AVX is in the INIT state (YMM_H registers are all zero).\n"));
        goto Cleanup;
    }

    Xmm = (PM128A)pfnLocateXStateFeature(Context, XSTATE_LEGACY_SSE, &FeatureLength);
    Ymm = (PM128A)pfnLocateXStateFeature(Context, XSTATE_AVX, NULL);

    //
    // Print values in the YMM registers.
    //

    for (Index = 0; Index < FeatureLength / sizeof(Xmm[0]); Index += 1)
    {
        _tprintf(_T("Ymm%d: %I64d %I64d %I64d %I64d\n"),
                 Index,
                 Xmm[Index].Low,
                 Xmm[Index].High,
                 Ymm[Index].Low,
                 Ymm[Index].High);
    }

Cleanup:
    free(Buffer);
    return;
} 
```



## <a name="related-topics"></a><span data-ttu-id="1aa8f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1aa8f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aa8f-111">**CopyContext**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-111">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)
</dt> <dt>

[<span data-ttu-id="1aa8f-112">**InitializeContext**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-112">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)
</dt> <dt>

[<span data-ttu-id="1aa8f-113">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-113">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)
</dt> <dt>

[<span data-ttu-id="1aa8f-114">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-114">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)
</dt> <dt>

[<span data-ttu-id="1aa8f-115">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-115">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="1aa8f-116">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="1aa8f-116">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)
</dt> </dl>

 

 

---
title: Créer des applications clientes
description: Comment utiliser l’API Windows Biometric Framework pour créer des applications clientes.
ms.assetid: 7bef37ee-7685-4aaa-8dad-3c5a9c335eca
keywords:
- API Windows Biometric Framework API Windows Biometric Framework, applications clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c2b25df11897a4e5f164c079dc2cd31faa4e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510843"
---
# <a name="create-client-applications"></a>Créer des applications clientes

Les rubriques suivantes expliquent comment utiliser l’API Windows Biometric Framework pour créer des applications clientes qui utilisent des pools de capteurs privés.

## <a name="enroll-biometric-information"></a>Inscrire des informations biométriques

Les exemples de code suivants montrent comment inscrire un modèle biométrique dans le pool système.

### <a name="synchronous-enrollment"></a>Inscription synchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) pour localiser une unité biométrique.
-   Appelle [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) pour démarrer la séquence d’inscription.
-   Appelle [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture) pour traiter plusieurs balayages de doigt sur le capteur.
-   Appelle [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) pour enregistrer le modèle dans le magasin.

Pour compiler cet exemple, liez-le à la bibliothèque statique WinBio. lib et incluez les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT EnrollSysPool(
                      BOOL discardEnrollment, 
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    BOOLEAN isNewTemplate = TRUE;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate a sensor.
    wprintf_s(L"\n Swipe your finger on the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    wprintf_s(L"\n Starting enrollment sequence...\n");
    hr = WinBioEnrollBegin(
            sessionHandle,      // Handle to open biometric session
            subFactor,          // Finger to create template for
            unitId              // Biometric unit ID
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollBegin failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Capture enrollment information by swiping the sensor with
    // the finger identified by the subFactor argument in the 
    // WinBioEnrollBegin function.
    for (int swipeCount = 1;; ++swipeCount)
    {
        wprintf_s(L"\n Swipe the sensor to capture %s sample.",
                 (swipeCount == 1)?L"the first":L"another");

        hr = WinBioEnrollCapture(
                sessionHandle,  // Handle to open biometric session
                &rejectDetail   // [out] Failure information
                );

        wprintf_s(L"\n Sample %d captured from unit number %d.", 
                  swipeCount, 
                  unitId);

        if (hr == WINBIO_I_MORE_DATA)
        {
            wprintf_s(L"\n    More data required.\n");
            continue;
        }
        if (FAILED(hr))
        {
            if (hr == WINBIO_E_BAD_CAPTURE)
            {
                wprintf_s(L"\n  Error: Bad capture; reason: %d", 
                          rejectDetail);
                continue;
            }
            else
            {
                wprintf_s(L"\n WinBioEnrollCapture failed. hr = 0x%x", hr);
                goto e_Exit;
            }
        }
        else
        {
            wprintf_s(L"\n    Template completed.\n");
            break;
        }
    }

    // Discard the enrollment if the appropriate flag is set.
    // Commit the enrollment if it is not discarded.
    if (discardEnrollment == TRUE)
    {
        wprintf_s(L"\n Discarding enrollment...\n\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &identity,          // WINBIO_IDENTITY object for the user
                &isNewTemplate);    // Is this a new template

        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioEnrollCommit failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }


e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L" Press any key to continue...");
    _getch();

    return hr;
}

```



### <a name="asynchronous-enrollment"></a>Inscription asynchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) pour localiser une unité biométrique.
-   Appelle [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) pour démarrer la séquence d’inscription.
-   Appelle [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) pour traiter plusieurs balayages de doigt. Cette fonction est asynchrone et utilise une fonction de rappel personnalisée pour poursuivre le traitement sur un thread séparé. Vous trouverez ci-dessous un exemple de fonction de rappel.
-   Appelle [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) pour attendre que le processus d’inscription asynchrone se termine ou soit annulé.
-   Appelle [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) pour enregistrer le modèle.

Liez à la bibliothèque statique WinBio. lib pour compiler cet exemple.


```C++
//------------------------------------------------------------------------
// EnrollSystemPoolWithCallback.cpp : Entry point for the application.
//
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <winbio.h>


//------------------------------------------------------------------------
// Forward declarations.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor);

VOID CALLBACK EnrollCaptureCallback(
                      __in_opt PVOID EnrollCallbackContext,
                      __in HRESULT OperationStatus,
                      __in WINBIO_REJECT_DETAIL RejectDetail);

typedef struct _ENROLL_CALLBACK_CONTEXT {
    WINBIO_SESSION_HANDLE SessionHandle;
    WINBIO_UNIT_ID UnitId;
    WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} ENROLL_CALLBACK_CONTEXT, *PENROLL_CALLBACK_CONTEXT;

//------------------------------------------------------------------------
int wmain()
{
    HRESULT hr = S_OK;

    hr = EnrollSysPoolWithCallback(
                      FALSE, 
                      FALSE, 
                      WINBIO_ANSI_381_POS_RH_INDEX_FINGER);

    return 0;
}

//------------------------------------------------------------------------
// The following function enrolls a user's fingerprint in the system pool.
// The function calls WinBioEnrollCaptureWithCallback and waits for the
// asynchronous enrollment process to be completed or canceled.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    BOOLEAN isNewTemplate = TRUE;
    ENROLL_CALLBACK_CONTEXT callbackContext = {0};

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the sensor.
    wprintf_s(L"\n Swipe your finger to locate the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    hr = WinBioEnrollBegin(
            sessionHandle,      // Handle to open biometric session
            subFactor,          // Finger to create template for
            unitId              // Biometric unit ID
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollBegin failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Set up the custom callback context structure.
    callbackContext.SessionHandle = sessionHandle;
    callbackContext.UnitId = unitId;
    callbackContext.SubFactor = subFactor;

    // Call WinBioEnrollCaptureWithCallback. This is an asynchronous
    // method that returns immediately.
    hr = WinBioEnrollCaptureWithCallback(
            sessionHandle,          // Handle to open biometric session
            EnrollCaptureCallback,  // Callback function
            &callbackContext        // Pointer to the custom context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollCaptureWithCallback failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor with the appropriate finger...\n");

    // Cancel the enrollment if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous enrollment process to complete
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

    // Discard the enrollment if the bDiscard flag is set.
    // Commit the enrollment if the flag is not set.
    if (bDiscard)
    {
        wprintf_s(L"\n Discarding enrollment...\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &identity,          // WINBIO_IDENTITY object for the user
                &isNewTemplate);    // Is this a new template

        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioEnrollCommit failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for the Windows Biometric
// Framework WinBioEnrollCaptureWithCallback() function. 
//
VOID CALLBACK EnrollCaptureCallback(
    __in_opt PVOID EnrollCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_REJECT_DETAIL RejectDetail
    )
{
    // Declare variables.
    HRESULT hr = S_OK; 
    static SIZE_T swipeCount = 1;

    PENROLL_CALLBACK_CONTEXT callbackContext = 
        (PENROLL_CALLBACK_CONTEXT)EnrollCallbackContext;

    wprintf_s(L"\n EnrollCaptureCallback executing\n");
    wprintf_s(L"\n Sample %d captured", swipeCount++);

    // The capture was not acceptable or the enrollment operation
    // failed.
    if (FAILED(OperationStatus))
    {
        if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
            wprintf_s(L"\n Swipe your finger to capture another sample.\n");

            // Try again.
            hr = WinBioEnrollCaptureWithCallback(
                    callbackContext->SessionHandle, // Open session handle
                    EnrollCaptureCallback,          // Callback function
                    EnrollCallbackContext           // Callback context
                    );
            if (FAILED(hr))
            {
                wprintf_s(L"WinBioEnrollCaptureWithCallback failed.");
                wprintf_s(L"hr = 0x%x\n", hr);
            }
        }
        else
        {
            wprintf_s(L"EnrollCaptureCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus);
        }
        goto e_Exit;
    }

    // The enrollment operation requires more fingerprint swipes.
    // This is normal and depends on your hardware. Typically, at least
    // three swipes are required.
    if (OperationStatus == WINBIO_I_MORE_DATA)
    {
        wprintf_s(L"\n More data required.");
        wprintf_s(L"\n Swipe your finger on the sensor again.");

        hr = WinBioEnrollCaptureWithCallback(
                callbackContext->SessionHandle,
                EnrollCaptureCallback,
                EnrollCallbackContext
                );
        if (FAILED(hr))
        {
            wprintf_s(L"WinBioEnrollCaptureWithCallback failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }

    wprintf_s(L"\n Template completed\n");

e_Exit:

    return;
}

```



## <a name="locate-biometric-units"></a>Localiser les unités biométriques

Les exemples de code suivants montrent comment localiser une unité biométrique installée.

### <a name="locate-biometric-units-synchronously"></a>Localiser des unités biométriques de façon synchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) pour localiser une unité biométrique.

Pour compiler cet exemple, liez-le à la bibliothèque statique WinBio. lib et incluez les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT LocateSensor( )
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the sensor.
    wprintf_s(L"\n Tap the sensor once...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Sensor located successfully. ");
    wprintf_s(L"\n Unit ID = %d \n", unitId);

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to exit...");
    _getch();

    return hr;
}

```



### <a name="locate-biometric-units-asynchronously"></a>Localiser des unités biométriques de façon asynchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) pour localiser un capteur biométrique. Il s’agit d’une fonction asynchrone qui configure le sous-système biométrique pour localiser le capteur sur un autre thread. La sortie du sous-système biométrique est envoyée à une fonction de rappel personnalisée, ici appelée LocateSensorCallback.
-   Appelle [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) pour attendre que le processus asynchrone se termine ou soit annulé.

Pour compiler cet exemple, liez-le à la bibliothèque statique WinBio. lib et incluez les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT LocateSensorWithCallback(BOOL bCancel)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    wprintf_s(L"\n Calling WinBioLocateSensorWithCallback.");
    hr = WinBioLocateSensorWithCallback(
                sessionHandle,          // Open biometric session
                LocateSensorCallback,   // Callback function
                NULL                    // Optional context
                );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensorWithCallback failed.");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous identification process to complete 
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

e_Exit:

    if (sessionHandle != NULL)
    {
       wprintf_s(L"\n Closing the session.\n");

        hr = WinBioCloseSession(sessionHandle);
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCloseSession failed. hr = 0x%x\n", hr);
        }
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for 
// WinBioLocateSensorWithCallback. The function filters the response 
// from the biometric subsystem and writes a result to the console window.
// 
VOID CALLBACK LocateSensorCallback(
    __in_opt PVOID LocateCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_UNIT_ID UnitId
    )
{
    UNREFERENCED_PARAMETER(LocateCallbackContext);

    wprintf_s(L"\n LocateSensorCallback executing.");

    // A sensor could not be located.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n LocateSensorCallback failed.");
        wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus);
    }
    // A sensor was located.
    else
    {
        wprintf_s(L"\n Selected unit ID: %d\n", UnitId);
    }
}

```



## <a name="verify-user-identity"></a>Vérifier l’identité de l’utilisateur

### <a name="synchronous-verification"></a>Vérification synchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify) pour déterminer si un exemple biométrique correspond à l’identité ouverte de l’utilisateur actuel.

Pour compiler cet exemple, liez-le à la bibliothèque statique WinBio. lib et incluez les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT Verify(WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_IDENTITY identity = {0};
    BOOLEAN match = FALSE;

    // Find the identity of the user.
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Verify a biometric sample.
    wprintf_s(L"\n Calling WinBioVerify - Swipe finger on sensor...\n");
    hr = WinBioVerify( 
            sessionHandle, 
            &identity, 
            subFactor, 
            &unitId, 
            &match,
            &rejectDetail
            );
    wprintf_s(L"\n Swipe processed - Unit ID: %d\n", unitId);
    if (FAILED(hr))
    {
        if (hr == WINBIO_E_NO_MATCH)
        {
            wprintf_s(L"\n- NO MATCH - identity verification failed.\n");
        }
        else if (hr == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n- Bad capture; reason: %d\n", rejectDetail);
        }
        else
        {
        wprintf_s(L"\n WinBioVerify failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }
    wprintf_s(L"\n Fingerprint verified:\n", unitId);


e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



### <a name="asynchronous-verification"></a>Vérification asynchrone

L’exemple de code suivant :

-   Appelle [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour ouvrir une session biométrique et se connecter au pool système.
-   Appelle [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) pour déterminer si un exemple biométrique correspond à l’identité ouverte de l’utilisateur actuel. Il s’agit d’une fonction asynchrone qui configure le sous-système biométrique pour vérifier l’utilisateur sur un autre thread. La sortie du sous-système biométrique est envoyée à une fonction de rappel personnalisée, ici appelée VerifyCallback.
-   Appelle [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) pour attendre que le processus asynchrone se termine ou soit annulé.

Pour compiler cet exemple, liez-le à la bibliothèque statique WinBio. lib et incluez les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT VerifyWithCallback(BOOL bCancel, WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_IDENTITY identity = {0};

    // Find the identity of the user.
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Verify a biometric sample asynchronously.
    wprintf_s(L"\n Calling WinBioVerifyWithCallback.\n");
    hr = WinBioVerifyWithCallback(
            sessionHandle,              // Open session handle
            &identity,                  // User SID or GUID
            subFactor,                  // Sample sub-factor
            VerifyCallback,             // Callback function
            NULL                        // Optional context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioVerifyWithCallback failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous identification process to complete 
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to continue...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for WinBioVerifyWithCallback.
// The function filters the response from the biometric subsystem and 
// writes a result to the console window.
// 
VOID CALLBACK VerifyCallback(
  __in_opt PVOID VerifyCallbackContext,
  __in HRESULT OperationStatus,
  __in WINBIO_UNIT_ID UnitId,
  __in BOOLEAN Match,
  __in WINBIO_REJECT_DETAIL RejectDetail
  )
{
    UNREFERENCED_PARAMETER(VerifyCallbackContext);
    UNREFERENCED_PARAMETER(Match);

    wprintf_s(L"\n VerifyCallback executing");
    wprintf_s(L"\n Swipe processed for unit ID %d\n", UnitId);

    // The identity could not be verified.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n Verification failed for the following reason:");
        if (OperationStatus == WINBIO_E_NO_MATCH)
        {
            wprintf_s(L"\n No match.\n");
        }
        else if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture.\n ");
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
        }
        else
        {
            wprintf_s(L"VerifyCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus); 
        }
        goto e_Exit;
    }

    // The user identity was verified.
    wprintf_s(L"\n Fingerprint verified:\n");

e_Exit:
    return;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



## <a name="manage-credentials"></a>Gérer les informations d’identification

Le fournisseur d’informations d’identification et le gestionnaire d’informations d’identification sont des composants de la Windows Biometric Framework. Le fournisseur récupère les informations d’identification de l’utilisateur à partir du magasin sécurisé et répond aux demandes d’élévation de connexion, de déverrouillage, de modification de mot de passe et d’élévation UAC. Il répond également pendant un changement rapide d’utilisateur pour ouvrir une session sur le nouvel utilisateur. Le gestionnaire mappe les informations d’identification d’ouverture de session aux identités biométriques et stocke en toute sécurité les informations d’identification. Les mappages sont généralement créés par des applications d’inscription tierces lors de l’inscription biométrique, mais ils peuvent également être créés par le fournisseur d’informations d’identification biométriques Windows lors de l’ouverture de session si l’utilisateur inscrit tente de s’authentifier de manière biométrique, mais n’est pas inscrit ou les informations d’identification ne correspondent pas à celles de la banque sécurisée.

### <a name="credential-manager-api-guidelines"></a>Instructions pour les API du gestionnaire d’informations d’identification

-   Les informations d’identification ne peuvent pas être stockées, interrogées ou supprimées pour les comptes d’administrateur invités ou intégrés ou pour tous les comptes non interactifs tels que LocalSystem, LocalService ou NetworkService.
-   Toutes les fonctions retournent un code d’erreur **HRESULT** qui peut être un code d’erreur courant comme **e \_ ACCESSDENIED** ou une erreur spécifique au gestionnaire d’informations d’identification, comme **WINBIO \_ e \_ Unknown \_ ID**.
-   Le cas échéant, E \_ ACCESSDENIED est retourné avant les codes d’erreur plus spécifiques tels que s \_ e \_ Logon \_ denied ou WINBIO \_ e \_ Unknown \_ ID sont retournés.
-   Les utilisateurs dont les privilèges n’ont pas été élevés peuvent définir, interroger ou supprimer des informations d’identification uniquement pour leur propre compte. Les appelants avec élévation de privilèges peuvent interroger l’état des informations d’identification et supprimer les informations d’identification d’autres utilisateurs.
-   Toutes les fonctions échouent et retournent WINBIO \_ E \_ cred \_ Prov \_ Disabled :
    -   Pour tous les utilisateurs lorsque le fournisseur d’informations d’identification n’est pas activé à l’ensemble du système.
    -   Pour les utilisateurs de domaine lorsque le fournisseur n’est pas activé pour l’utilisation de domaine.
-   Une notification d’événement est générée lors de l’ajout ou de la suppression d’informations d’identification.

### <a name="set-a-credential"></a>Définir des informations d’identification

L’exemple de code suivant :

-   Appelle GetCurrentUserIdentity pour récupérer un objet d' [**\_ identité WINBIO**](winbio-identity.md) pour l’utilisateur actuel. GetCurrentUserIdentity est une fonction d’assistance qui ne fait pas partie du Windows Biometric Framework.
-   Appelle la fonction d’assistance GetCredentials pour récupérer un tableau d’octets qui contient les informations d’authentification. GetCredentials affiche une boîte de dialogue qui invite l’utilisateur à fournir des informations d’identification.
-   Appelle [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) pour enregistrer les informations d’identification dans le magasin.

Pour compiler ce lien de fonction vers la bibliothèque statique WinBio. lib et inclure les fichiers d’en-tête suivants :

-   Windows. h
-   Wincred. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT SetCredential()
{
    // Declare variables.
    HRESULT hr = S_OK;
    ULONG   ulAuthPackage = 0;
    PVOID   pvAuthBlob = NULL;
    ULONG   cbAuthBlob = 0;
    WINBIO_IDENTITY identity;
    PSID pSid = NULL;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        return hr;
    }

    // Set a pointer to the security descriptor for the user.
    pSid = identity.Value.AccountSid.Data;

    // Retrieve a byte array that contains credential information.
    hr = GetCredentials(pSid, &pvAuthBlob, &cbAuthBlob);
    if (FAILED(hr))
    {
        wprintf_s(L"\n GetCredentials failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Set the credentials.
    hr = WinBioSetCredential(
            WINBIO_CREDENTIAL_PASSWORD,     // Type of credential.
            (PUCHAR)pvAuthBlob,             // Credentials byte array
            cbAuthBlob,                     // Size of credentials
            WINBIO_PASSWORD_PACKED);        // Credentials format

    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioSetCredential failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Credentials successfully set.\n");

e_Exit:
    // Delete the authentication byte array.
    if (NULL != pvAuthBlob)
    {
        SecureZeroMemory(pvAuthBlob, cbAuthBlob);
        CoTaskMemFree(pvAuthBlob);
        pvAuthBlob = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;


}

//------------------------------------------------------------------------
// The following function displays a dialog box to prompt a user
// for credentials.
//
HRESULT GetCredentials(PSID pSid, PVOID* ppvAuthBlob, ULONG* pcbAuthBlob)
{
    HRESULT hr = S_OK;
    DWORD   dwResult;
    WCHAR   szUsername[MAX_PATH] = {0};
    DWORD   cchUsername = ARRAYSIZE(szUsername);
    WCHAR   szPassword[MAX_PATH] = {0};
    WCHAR   szDomain[MAX_PATH] = {0};
    DWORD   cchDomain = ARRAYSIZE(szDomain);
    WCHAR   szDomainAndUser[MAX_PATH] = {0};
    DWORD   cchDomainAndUser = ARRAYSIZE(szDomainAndUser);
    PVOID   pvInAuthBlob = NULL;
    ULONG   cbInAuthBlob = 0;
    PVOID   pvAuthBlob = NULL;
    ULONG   cbAuthBlob = 0;
    CREDUI_INFOW ui;
    ULONG   ulAuthPackage = 0;
    BOOL    fSave = FALSE;

    static const WCHAR WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_MESSAGE[] =
           L"Enter your current password to enable biometric logon.";

    static const WCHAR WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_CAPTION[] =
           L"Biometric Log On Enrollment";

    if (NULL == pSid || NULL == ppvAuthBlob || NULL == pcbAuthBlob)
    {
        return E_INVALIDARG;
    }

    // Retrieve the user name and domain name.
    SID_NAME_USE    SidUse;
    DWORD           cchTmpUsername = cchUsername;
    DWORD           cchTmpDomain = cchDomain;

    if (!LookupAccountSidW(
              NULL,             // Local computer
              pSid,             // Security identifier for user
              szUsername,       // User name
              &cchTmpUsername,  // Size of user name
              szDomain,         // Domain name
              &cchTmpDomain,    // Size of domain name
              &SidUse))         // Account type
    {
        dwResult = GetLastError();
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n LookupAccountSidLocalW failed: hr = 0x%x\n", hr);
        return hr;
    }

    // Combine the domain and user names.
    swprintf_s(
        szDomainAndUser, 
        cchDomainAndUser, 
        L"%s\\%s", 
        szDomain, 
        szUsername);

    // Call CredPackAuthenticationBufferW once to determine the size,
    // in bytes, of the authentication buffer.
    if (!CredPackAuthenticationBufferW(
              0,                // Reserved
              szDomainAndUser,  // Domain\User name
              szPassword,       // User Password
              NULL,             // Packed credentials
              &cbInAuthBlob)    // Size, in bytes, of credentials
        && GetLastError() != ERROR_INSUFFICIENT_BUFFER)
        {
            dwResult = GetLastError();
            hr = HRESULT_FROM_WIN32(dwResult);
            wprintf_s(L"\n CredPackAuthenticationBufferW (1) failed: ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }

    // Allocate memory for the input buffer.
    pvInAuthBlob = CoTaskMemAlloc(cbInAuthBlob);
    if (!pvInAuthBlob)
    {
        cbInAuthBlob = 0;
        wprintf_s(L"\n CoTaskMemAlloc() Out of memory.\n");
        return HRESULT_FROM_WIN32(ERROR_OUTOFMEMORY);
    }

    // Call CredPackAuthenticationBufferW again to retrieve the
    // authentication buffer.
    if (!CredPackAuthenticationBufferW(
              0,
              szDomainAndUser,
              szPassword,
              (PBYTE)pvInAuthBlob,
              &cbInAuthBlob))
    {
        dwResult = GetLastError();
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n CredPackAuthenticationBufferW (2) failed: ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display a dialog box to request credentials.
    ui.cbSize = sizeof(ui);
    ui.hwndParent = GetConsoleWindow();
    ui.pszMessageText = WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_MESSAGE;
    ui.pszCaptionText = WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_CAPTION;
    ui.hbmBanner = NULL;

    dwResult = CredUIPromptForWindowsCredentialsW(
                   &ui,             // Customizing information
                   0,               // Error code to display
                   &ulAuthPackage,  // Authorization package
                   pvInAuthBlob,    // Credential byte array
                   cbInAuthBlob,    // Size of credential input buffer
                   &pvAuthBlob,     // Output credential byte array
                   &cbAuthBlob,     // Size of credential byte array
                   &fSave,          // Select the save check box.
                   CREDUIWIN_IN_CRED_ONLY |
                   CREDUIWIN_ENUMERATE_CURRENT_USER
                   );
    if (dwResult != NO_ERROR)
    {
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n CredUIPromptForWindowsCredentials failed: ");
        wprintf_s(L"0x%08x\n", dwResult);
        goto e_Exit;
    }

    *ppvAuthBlob = pvAuthBlob;
    *pcbAuthBlob = cbAuthBlob;

e_Exit:
    // Delete the input authentication byte array.
    if (pvInAuthBlob)
    {
        SecureZeroMemory(pvInAuthBlob, cbInAuthBlob);
        CoTaskMemFree(pvInAuthBlob);
        pvInAuthBlob = NULL;
    };

    return hr;
}


//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



### <a name="remove-a-credential"></a>Supprimer des informations d’identification

L’exemple de code suivant :

-   Appelle GetCurrentUserIdentity pour récupérer un objet d' [**\_ identité WINBIO**](winbio-identity.md) pour l’utilisateur actuel. GetCurrentUserIdentity est une fonction d’assistance qui ne fait pas partie du Windows Biometric Framework.
-   Appelle [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential) pour supprimer les informations d’identification du magasin.

Pour compiler ce lien de fonction vers la bibliothèque statique WinBio. lib et inclure les fichiers d’en-tête suivants :

-   Windows. h
-   Stdio. h
-   Conio. h
-   WinBio. h


```C++
HRESULT RemoveCredential()
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Remove the user credentials.
    hr = WinBioRemoveCredential(identity, WINBIO_CREDENTIAL_PASSWORD);
    if (FAILED(hr)) 
    {
        wprintf(L"\n WinBioRemoveCredential failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    wprintf_s(L"\n User credentials successfully removed.\n");

e_Exit:

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



 

 





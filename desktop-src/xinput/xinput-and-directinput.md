---
title: XInput et DirectInput
description: XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "103730701"
---
# <a name="xinput-and-directinput"></a>XInput et DirectInput

XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows. Ce document décrit les différences entre les implémentations XInput et [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) du contrôleur Xbox et comment vous pouvez prendre en charge les appareils XInput et les périphériques DirectInput hérités en même temps.

> [!Note]  
> L’utilisation d’un [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérité n’est pas recommandée, et DirectInput n’est pas disponible pour les applications du Windows Store.

## <a name="the-new-standard-xinput"></a>Le nouveau standard : XInput

XInput est désormais disponible pour le développement de jeux. Il s’agit de la nouvelle norme d’entrée pour Xbox et Windows. Les API sont disponibles via le kit de développement logiciel (SDK) DirectX et le pilote est disponible via Windows Update.

L’utilisation de XInput sur [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))présente plusieurs avantages :

-   XInput est plus facile à utiliser et requiert moins d’installation que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   La programmation Xbox et Windows utilise les mêmes jeux d’API de base, ce qui permet de programmer la traduction de plusieurs plateformes plus faciles
-   Il y aura une base installée de contrôleurs Xbox de grande taille
-   Les appareils XInput (autrement dit, les contrôleurs Xbox) auront des fonctionnalités de vibration uniquement lors de l’utilisation des API XInput
-   Les futurs contrôleurs commercialisés pour la console Xbox (autrement dit, les volants) fonctionnent également sur Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Utilisation du contrôleur Xbox avec DirectInput

Le contrôleur Xbox est correctement énuméré sur [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))et peut être utilisé avec DirectInputAPIs. Toutefois, certaines fonctionnalités fournies par XInput seront absentes de l’implémentation de DirectInput :

-   Les boutons de déclenchement de gauche et de droite agiront comme un seul bouton, et non indépendamment
-   Les effets vibratoires ne sont pas disponibles
-   L’interrogation des appareils de casque n’est pas disponible

La combinaison des déclencheurs de gauche et de droite dans [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) est par défaut. Les jeux ont toujours supposé que les axes des appareils DirectInput sont centrés lorsqu’il n’y a aucune interaction de l’utilisateur avec l’appareil. Toutefois, le contrôleur Xbox a été conçu pour inscrire la valeur minimale, et non pas le centre, lorsque les déclencheurs ne sont pas maintenus. Par conséquent, les anciens jeux supposent l’intervention de l’utilisateur.

La solution consistait à combiner les déclencheurs, à définir un déclencheur sur un sens positif et l’autre à une direction négative, de sorte qu’aucune interaction utilisateur n’indique à [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) du « contrôle » au centre.

Pour tester les valeurs de déclencheur séparément, vous devez utiliser XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput et DirectInput côte à côte

En prenant en charge uniquement XInput, votre jeu ne fonctionnera pas avec les appareils [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérités. XInput ne reconnaîtra pas ces appareils.

Si vous souhaitez que votre jeu prenne en charge les périphériques [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérités, vous pouvez utiliser DirectInput et XInput côte à côte. Lors de l’énumération de vos périphériques DirectInput, tous les périphériques DirectInput sont énumérés correctement. Tous les appareils XInput s’affichent en tant qu’appareils XInput et DirectInput, mais ils ne doivent pas être gérés via DirectInput. Vous devez déterminer lequel de vos périphériques DirectInput est un appareil hérité, et qui sont des appareils XInput, et les supprimer de l’énumération des périphériques DirectInput.

Pour ce faire, insérez ce code dans votre rappel d’énumération DirectInput :

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
        }
    }

LCleanup:
    VariantClear(&var);
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a>Rubriques connexes

[Prise en main avec XInput](getting-started-with-xinput.md)

[Guide de référence de programmation](programming-reference.md)

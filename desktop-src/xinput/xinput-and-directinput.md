---
title: XInput et DirectInput
description: XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373185"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="ca014-103">XInput et DirectInput</span><span class="sxs-lookup"><span data-stu-id="ca014-103">XInput and DirectInput</span></span>

<span data-ttu-id="ca014-104">XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows.</span><span class="sxs-lookup"><span data-stu-id="ca014-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="ca014-105">Ce document décrit les différences entre les implémentations XInput et [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) du contrôleur Xbox et comment vous pouvez prendre en charge les appareils XInput et les périphériques DirectInput hérités en même temps.</span><span class="sxs-lookup"><span data-stu-id="ca014-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="ca014-106">l’utilisation d’un [directinput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérité n’est pas recommandée, et directinput n’est pas disponible pour les applications Windows store.</span><span class="sxs-lookup"><span data-stu-id="ca014-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="ca014-107">Le nouveau standard : XInput</span><span class="sxs-lookup"><span data-stu-id="ca014-107">The New Standard: XInput</span></span>

<span data-ttu-id="ca014-108">XInput est désormais disponible pour le développement de jeux.</span><span class="sxs-lookup"><span data-stu-id="ca014-108">XInput is now available for game development.</span></span> <span data-ttu-id="ca014-109">Il s’agit de la nouvelle norme d’entrée pour la Xbox et Windows.</span><span class="sxs-lookup"><span data-stu-id="ca014-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="ca014-110">les api sont disponibles via le kit de développement logiciel (SDK) DirectX et le pilote est disponible via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ca014-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="ca014-111">L’utilisation de XInput sur [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))présente plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="ca014-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="ca014-112">XInput est plus facile à utiliser et requiert moins d’installation que [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca014-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="ca014-113">la programmation Xbox et Windows utilise les mêmes jeux d’api de base, ce qui permet de programmer la traduction de plusieurs plateformes plus faciles</span><span class="sxs-lookup"><span data-stu-id="ca014-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="ca014-114">Il y aura une base installée de contrôleurs Xbox de grande taille</span><span class="sxs-lookup"><span data-stu-id="ca014-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="ca014-115">Les appareils XInput (autrement dit, les contrôleurs Xbox) auront des fonctionnalités de vibration uniquement lors de l’utilisation des API XInput</span><span class="sxs-lookup"><span data-stu-id="ca014-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="ca014-116">Les futurs contrôleurs commercialisés pour la console Xbox (autrement dit, les roues directrices) fonctionnent également sur Windows</span><span class="sxs-lookup"><span data-stu-id="ca014-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="ca014-117">Utilisation du contrôleur Xbox avec DirectInput</span><span class="sxs-lookup"><span data-stu-id="ca014-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="ca014-118">Le contrôleur Xbox est correctement énuméré sur [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))et peut être utilisé avec DirectInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="ca014-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="ca014-119">Toutefois, certaines fonctionnalités fournies par XInput seront absentes de l’implémentation de DirectInput :</span><span class="sxs-lookup"><span data-stu-id="ca014-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="ca014-120">Les boutons de déclenchement de gauche et de droite agiront comme un seul bouton, et non indépendamment</span><span class="sxs-lookup"><span data-stu-id="ca014-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="ca014-121">Les effets vibratoires ne sont pas disponibles</span><span class="sxs-lookup"><span data-stu-id="ca014-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="ca014-122">L’interrogation des appareils de casque n’est pas disponible</span><span class="sxs-lookup"><span data-stu-id="ca014-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="ca014-123">La combinaison des déclencheurs de gauche et de droite dans [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) est par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca014-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="ca014-124">Les jeux ont toujours supposé que les axes des appareils DirectInput sont centrés lorsqu’il n’y a aucune interaction de l’utilisateur avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ca014-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="ca014-125">Toutefois, le contrôleur Xbox a été conçu pour inscrire la valeur minimale, et non pas le centre, lorsque les déclencheurs ne sont pas maintenus.</span><span class="sxs-lookup"><span data-stu-id="ca014-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="ca014-126">Par conséquent, les anciens jeux supposent l’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca014-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="ca014-127">La solution consistait à combiner les déclencheurs, à définir un déclencheur sur un sens positif et l’autre à une direction négative, de sorte qu’aucune interaction utilisateur n’indique à [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) du « contrôle » au centre.</span><span class="sxs-lookup"><span data-stu-id="ca014-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="ca014-128">Pour tester les valeurs de déclencheur séparément, vous devez utiliser XInput.</span><span class="sxs-lookup"><span data-stu-id="ca014-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="ca014-129">XInput et DirectInput côte à côte</span><span class="sxs-lookup"><span data-stu-id="ca014-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="ca014-130">En prenant en charge uniquement XInput, votre jeu ne fonctionnera pas avec les appareils [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérités.</span><span class="sxs-lookup"><span data-stu-id="ca014-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="ca014-131">XInput ne reconnaîtra pas ces appareils.</span><span class="sxs-lookup"><span data-stu-id="ca014-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="ca014-132">Si vous souhaitez que votre jeu prenne en charge les périphériques [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) hérités, vous pouvez utiliser DirectInput et XInput côte à côte.</span><span class="sxs-lookup"><span data-stu-id="ca014-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="ca014-133">Lors de l’énumération de vos périphériques DirectInput, tous les périphériques DirectInput sont énumérés correctement.</span><span class="sxs-lookup"><span data-stu-id="ca014-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="ca014-134">Tous les appareils XInput s’affichent en tant qu’appareils XInput et DirectInput, mais ils ne doivent pas être gérés via DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ca014-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="ca014-135">Vous devez déterminer lequel de vos périphériques DirectInput est un appareil hérité, et qui sont des appareils XInput, et les supprimer de l’énumération des périphériques DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ca014-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="ca014-136">Pour ce faire, insérez ce code dans votre rappel d’énumération DirectInput :</span><span class="sxs-lookup"><span data-stu-id="ca014-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
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
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
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
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> <span data-ttu-id="ca014-137">Une version légèrement améliorée de ce code se trouve dans l’exemple de [manette](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) de jeu DirectInput hérité.</span><span class="sxs-lookup"><span data-stu-id="ca014-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca014-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca014-138">Related topics</span></span>

[<span data-ttu-id="ca014-139">Prise en main avec XInput</span><span class="sxs-lookup"><span data-stu-id="ca014-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="ca014-140">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="ca014-140">Programming Reference</span></span>](programming-reference.md)

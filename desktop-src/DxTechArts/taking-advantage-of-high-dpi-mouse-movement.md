---
title: Tirer parti du High-Definition mouvement de la souris
description: Cet article se concentre sur la meilleure façon d’optimiser les performances de l’entrée de souris haute définition dans un jeu comme un tir de première personne.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007463"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Tirer parti du High-Definition mouvement de la souris

Une souris d’ordinateur standard retourne des données à 400 points par pouce (DPI), tandis qu’une souris haute définition génère des données à 800 ppp ou plus. Cela rend l’entrée d’une souris de haute définition beaucoup plus précise que celle d’une souris standard. Toutefois, les données haute définition ne peuvent pas être obtenues par le biais des messages de la souris inversée WM standard \_ . En général, les jeux tirent parti des périphériques de souris haute définition, mais les jeux qui obtiennent des données de souris à l’aide de WM \_ MOUSEMOVE ne peuvent pas accéder à la résolution complète et non filtrée de la souris.

Plusieurs sociétés fabriquent des périphériques de souris haute définition, tels que Microsoft et Logitech. Avec la popularité croissante des périphériques de souris à haute résolution, il est important que les développeurs sachent comment utiliser les informations générées par ces appareils de manière optimale. Cet article se concentre sur la meilleure façon d’optimiser les performances de l’entrée de souris haute définition dans un jeu comme un tir de première personne.

## <a name="retrieving-mouse-movement-data"></a>Récupération des données de mouvement de la souris

Voici les trois principales méthodes pour récupérer des données de souris :

-   [WM \_ MOUSEMOVE](/windows)
-   [\_entrée WM](/windows)
-   [DirectInput](#directinput)

Chaque méthode présente des avantages et des inconvénients, en fonction de la façon dont les données sont utilisées.

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

La méthode la plus simple pour lire les données de mouvement de la souris consiste à utiliser des \_ messages de désouris WM. L’exemple suivant montre comment lire les données de mouvement de la souris à partir du \_ message WM MOUSEMOVE :

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Le principal inconvénient des données de WM \_ MOUSEMOVE est qu’elles sont limitées à la résolution d’écran. Cela signifie que si vous déplacez légèrement la souris, mais pas assez pour faire passer le pointeur au pixel suivant, aucun \_ message WM MOUSEMOVE n’est généré. Par conséquent, l’utilisation de cette méthode pour lire le mouvement de la souris nie les avantages de l’entrée haute définition.

l’avantage de WM \_ MOUSEMOVE, cependant, est que Windows applique l’accélération de pointeur (également appelée « balistiques ») aux données de souris brutes, ce qui fait que le pointeur de la souris se comporte comme prévu par les clients. Il fait \_ en sorte que WM MOUSEMOVE l’option préférée pour le contrôle de pointeur (sur l' \_ entrée WM ou DirectInput), car il produit un comportement plus naturel pour les utilisateurs. Alors que WM \_ MOUSEMOVE est idéal pour déplacer des pointeurs de souris, ce n’est pas si bon pour déplacer une caméra de première personne, puisque la précision haute définition sera perdue.

Pour plus d’informations sur WM \_ MouseMove, consultez [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>\_entrée WM

La deuxième méthode d’obtention des données de souris consiste à lire les \_ messages d’entrée WM. Le traitement des messages \_ d’entrée WM est plus complexe que le traitement des \_ messages WM MOUSEMOVE, mais les \_ messages d’entrée WM sont lus directement à partir de la pile HID (Human Interface Device) et reflètent les résultats de haute définition.

Pour lire les données de mouvement de la souris à partir du \_ message d’entrée WM, l’appareil doit d’abord être enregistré. le code suivant en fournit un exemple :

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

Le code suivant gère les \_ messages d’entrée WM dans le gestionnaire que winproc de l’application :

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

L’avantage d’utiliser l' \_ entrée WM est que votre jeu reçoit des données brutes de la souris au niveau le plus bas possible.

L’inconvénient est que l' \_ entrée WM n’a pas de balistiques appliquée à ses données. par conséquent, si vous souhaitez diriger un curseur avec ces données, un effort supplémentaire sera nécessaire pour que le curseur se comporte comme dans Windows. pour plus d’informations sur l’application des balistiques de pointeurs, consultez [pointeurs balistiques pour Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Pour plus d’informations sur l' \_ entrée WM, consultez [à propos des entrées brutes](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) est un ensemble d’appels d’API qui soustrait les périphériques d’entrée sur le système. En interne, DirectInput crée un deuxième thread pour lire \_ les données d’entrée WM et l’utilisation des API DirectInput ajoute une charge mémoire supplémentaire par rapport à la simple lecture directe de l' \_ entrée WM. DirectInput est utile uniquement pour lire des données à partir de manettes de manche DirectInput ; toutefois, si vous devez uniquement prendre en charge le contrôleur Xbox 360 pour Windows, utilisez [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) à la place. En général, l’utilisation de DirectInput n’offre aucun avantage lors de la lecture de données à partir de périphériques de souris ou de clavier, et l’utilisation d’DirectInput dans ces scénarios est déconseillée.

Comparez la complexité de l’utilisation de [DirectInput](/windows-hardware/drivers/hid/directinput), illustrée dans le code suivant, aux méthodes décrites précédemment. L’ensemble d’appels suivant est nécessaire pour créer une souris DirectInput :

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

Puis, le périphérique de souris DirectInput peut lire chaque frame :

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Résumé

Globalement, la meilleure méthode pour recevoir les données de déplacement de souris haute définition est l' \_ entrée WM. Si vos utilisateurs déplacent simplement un pointeur de souris, envisagez d’utiliser WM \_ MOUSEMOVE pour éviter d’avoir à effectuer des balistiques de pointeur. Ces deux messages de fenêtre fonctionnent bien même si la souris n’est pas une souris de haute définition. en prenant en charge la haute définition, Windows jeux peuvent offrir un contrôle plus précis aux utilisateurs.
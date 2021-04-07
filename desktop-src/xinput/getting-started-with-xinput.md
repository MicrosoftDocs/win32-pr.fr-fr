---
title: Prise en main avec XInput
description: XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows. Les effets du contrôleur Rumble et l’entrée et la sortie vocales sont pris en charge.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727660"
---
# <a name="getting-started-with-xinput"></a>Prise en main avec XInput

XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows. Les effets du contrôleur Rumble et l’entrée et la sortie vocales sont pris en charge.

Cette rubrique fournit une brève vue d’ensemble des fonctionnalités de XInput et explique comment la configurer dans une application. Les éléments suivants sont abordés :

-   [Présentation de XInput](#introduction-to-xinput)
    -   [Contrôleur Xbox](#the-xbox-controller)
-   [Utilisation de XInput](#using-xinput)
    -   [Plusieurs contrôleurs](#multiple-controllers)
    -   [Obtention de l’état du contrôleur](#getting-controller-state)
    -   [Zone morte](#dead-zone)
    -   [Définition des effets vibratoires](#setting-vibration-effects)
    -   [Obtention des identificateurs de périphérique audio](#getting-audio-device-identifiers)
    -   [Obtention des GUID DirectSound (SDK DirectX hérité uniquement)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Rubriques connexes](#related-topics)

## <a name="introduction-to-xinput"></a>Présentation de XInput

La console Xbox utilise un contrôleur de jeu qui est compatible avec Windows. Les applications peuvent utiliser l’API XInput pour communiquer avec ces contrôleurs lorsqu’elles sont connectées à un PC Windows (jusqu’à quatre contrôleurs uniques peuvent être branchés à la fois).

À l’aide de cette API, tout contrôleur Xbox connecté peut être interrogé pour déterminer son état et les effets vibratoires peuvent être définis. Les contrôleurs qui disposent du casque peuvent également être interrogés pour les périphériques d’entrée et de sortie audio qui peuvent être utilisés avec le casque pour le traitement vocal.

### <a name="the-xbox-controller"></a>Contrôleur Xbox

Le contrôleur Xbox dispose de deux Memory Sticks analogiques, chacun avec un bouton numérique, deux déclencheurs analogiques, un pavé directionnel numérique à quatre directions et huit boutons numériques. Les États de chacune de ces entrées sont retournés dans la structure du [**\_ boîtier de souXINPUTment**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) lorsque la fonction [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) est appelée.

Le contrôleur a également deux moteurs vibrants pour fournir des effets de retour de force à l’utilisateur. Les vitesses de ces moteurs sont spécifiées dans la structure [**\_ vibratoire XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) transmise à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) pour définir des effets vibratoires.

Un casque peut éventuellement être connecté au contrôleur. Le casque a un microphone pour l’entrée vocale et un casque pour la sortie audio. Vous pouvez appeler la fonction [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) ou [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) héritée pour obtenir les identificateurs d’appareil qui correspondent aux appareils du microphone et du casque. Vous pouvez ensuite utiliser les [API audio principales](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) pour recevoir une entrée vocale et envoyer une sortie audio.

## <a name="using-xinput"></a>Utilisation de XInput

L’utilisation de XInput est aussi simple que l’appel des fonctions XInput en fonction des besoins. À l’aide des fonctions XInput, vous pouvez récupérer l’état du contrôleur, obtenir les ID audio du casque et définir les effets du contrôleur Rumble.

### <a name="multiple-controllers"></a>Plusieurs contrôleurs

L’API XInput prend en charge jusqu’à quatre contrôleurs connectés à tout moment. Les fonctions XInput nécessitent toutes un paramètre *dwUserIndex* qui est transmis pour identifier le contrôleur qui est défini ou interrogé. Cet ID se trouve dans la plage 0-3 et est défini automatiquement par XInput. Le nombre correspond au port dans lequel le contrôleur est connecté et n’est pas modifiable.

Chaque contrôleur affiche l’ID qu’il utilise en allumant un quadrant sur la « sonnerie de la lumière » au centre du contrôleur. Une valeur *dwUserIndex* égale à 0 correspond au quadrant supérieur gauche ; la numérotation se poursuit autour de l’anneau dans le sens des aiguilles d’une montre.

Les applications doivent prendre en charge plusieurs contrôleurs.

### <a name="getting-controller-state"></a>Obtention de l’état du contrôleur

Tout au long de la durée d’une application, l’obtention de l’État à partir d’un contrôleur sera probablement effectuée le plus souvent. Du frame au frame dans une application de jeu, l’État doit être récupéré et les informations de jeu mises à jour pour refléter les modifications du contrôleur.

Pour récupérer l’État, utilisez la fonction [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

Notez que la valeur de retour de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) peut être utilisée pour déterminer si le contrôleur est connecté. Les applications doivent définir une structure pour contenir les informations du contrôleur interne ; ces informations doivent être comparées aux résultats de **XInputGetState** pour déterminer quelles modifications, telles que les Appuyez sur les boutons ou les deltas de contrôleur analogique, ont été apportées à ce cadre. Dans l’exemple ci-dessus, *g \_ Controllers* représente une telle structure.

Une fois que l’État a été récupéré dans une structure d' [**\_ État XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , vous pouvez vérifier s’il contient des modifications et obtenir des informations spécifiques sur l’état du contrôleur.

Le membre *dwPacketNumber* de la structure d' [**\_ État XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) peut être utilisé pour vérifier si l’état du contrôleur a changé depuis le dernier appel à [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate). Si *dwPacketNumber* n’est pas modifié entre deux appels séquentiels à **XInputGetState**, cela signifie qu’il n’y a eu aucune modification de l’État. Si elle diffère, l’application doit vérifier le membre de la *manette* de la structure d' **\_ État XInput** pour obtenir des informations d’État plus détaillées.

Pour des raisons de performances, n’appelez pas [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) pour un emplacement utilisateur « vide » à chaque trame. Nous vous recommandons d’utiliser à la place des contrôles de nouveaux contrôleurs à intervalles de quelques secondes.

### <a name="dead-zone"></a>Zone morte

Pour que les utilisateurs bénéficient d’une expérience de jeu cohérente, votre jeu doit implémenter la zone morte correctement. La zone morte est des valeurs de « mouvement » signalées par le contrôleur, même lorsque les Thumbsticks analogiques sont intacts et centrés. Il y a également une zone morte pour les deux déclencheurs analogiques.

> [!Note]  
> Les jeux qui utilisent des XInput qui ne filtrent pas les zones mortes sont confrontés à un mauvais jeu. Notez que certains contrôleurs sont plus sensibles que d’autres, la zone morte peut donc varier d’une unité à l’autre. Il est recommandé de tester vos jeux avec plusieurs contrôleurs Xbox sur différents systèmes.

Les applications doivent utiliser des « zones mortes » sur les entrées analogiques (déclencheurs, bâtons) pour indiquer qu’un mouvement est suffisamment fait sur le bâton ou le déclencheur pour être considéré comme valide.

Votre application doit vérifier les zones mortes et répondre à appopriately, comme dans cet exemple :

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

Cet exemple calcule le vecteur de direction du contrôleur et l’avancement du vecteur que le contrôleur a fait l’objet d’un push. Cela permet l’application d’un deadzone circulaire en vérifiant simplement si l’amplitude du contrôleur est supérieure à la valeur deadzone. En outre, le code normalise l’amplitude du contrôleur, qui peut ensuite être multiplié par un facteur spécifique à un jeu pour convertir la position du contrôleur en unités pertinentes pour le jeu.

Notez que vous pouvez définir vos propres zones mortes pour les bâtons et les déclencheurs (n’importe où à partir de 0-65534), ou vous pouvez utiliser la Deadzones fournie définie en tant que XINPUT du contrôle de point de contrôle \_ \_ gauche \_ \_ DEADZONE, XInput \_ manette \_ droit \_ \_ DEADZONE et XInput \_ \_ de déclencheur de manette XInput \_ dans. h :

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Une fois le deadzone appliqué, il peut s’avérer utile de mettre à l’échelle la plage résultante \[ 0.0.. 1.0 à \] virgule flottante (comme dans l’exemple ci-dessus), et d’appliquer éventuellement une transformation non linéaire.

Par exemple, avec des jeux de conduite, il peut être utile de créer des cubes pour le résultat afin de mieux toucher les voitures à l’aide d’un boîtier de commande, car cubes le résultat vous donne plus de précision dans les plages inférieures, ce qui est souhaitable, car les joueurs appliquent généralement la force logicielle pour obtenir un mouvement subtil ou appliquer une force forcée dans une direction.

### <a name="setting-vibration-effects"></a>Définition des effets vibratoires

Outre l’obtention de l’état du contrôleur, vous pouvez également envoyer des données de vibration au contrôleur pour modifier les commentaires fournis à l’utilisateur du contrôleur. Le contrôleur contient deux moteurs Rumble qui peuvent être contrôlés indépendamment en passant des valeurs à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .

La vitesse de chaque moteur peut être spécifiée à l’aide d’une valeur de mot dans la structure [**\_ vibratoire XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) transmise à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) comme suit :

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Notez que le moteur de droite est le moteur haute fréquence, le moteur gauche est le moteur basse fréquence. Ils n’ont pas toujours besoin d’être définis sur la même quantité, car ils fournissent des effets différents.

### <a name="getting-audio-device-identifiers"></a>Obtention des identificateurs de périphérique audio

Le casque pour un contrôleur Xbox possède les fonctions suivantes :

-   Enregistrer le son à l’aide d’un microphone
-   Lire le son à l’aide d’un casque

Utilisez ce code pour obtenir les identificateurs d’appareil du casque :

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Une fois que vous avez obtenu les identificateurs d’appareil, vous pouvez créer les interfaces appropriées. Par exemple, si vous utilisez XAudio 2,8, utilisez ce code pour créer une voix de mastérisation pour cet appareil :

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Pour plus d’informations sur l’utilisation de l’identificateur d’appareil captureId, consultez [capture d’un flux](/windows/desktop/CoreAudio/capturing-a-stream).

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Obtention des GUID DirectSound (SDK DirectX hérité uniquement)

Le casque qui peut être connecté à un contrôleur Xbox a deux fonctions : il peut enregistrer le son à l’aide d’un microphone et lire le son à l’aide d’un casque. Dans l’API XInput, ces fonctions sont accomplies par le biais de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), à l’aide des interfaces **IDirectSound8** et **IDirectSoundCapture8** .

Pour associer le microphone et le casque du casque à leurs interfaces [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) appropriées, vous devez obtenir le DirectSoundGUIDs pour les appareils de capture et de rendu en appelant [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> L’utilisation de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) héritée n’est pas recommandée et n’est pas disponible dans les applications du Windows Store. Les informations de cette section s’appliquent uniquement à la version du kit de développement logiciel (SDK) DirectX de XInput (XInput 1,3). La version Windows 8 de XInput (XInput 1,4) utilise exclusivement des identificateurs d’appareil de l’API de session audio Windows (WASAPI) obtenus via [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Une fois que vous avez récupéré les GUID, vous pouvez créer les interfaces appropriées en appelant DirectSoundCreate8 et DirectSoundCaptureCreate8 comme suit :

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>Rubriques connexes

[Guide de référence de programmation](programming-reference.md)
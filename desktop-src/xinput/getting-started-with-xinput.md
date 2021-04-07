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
# <a name="getting-started-with-xinput"></a><span data-ttu-id="7238b-104">Prise en main avec XInput</span><span class="sxs-lookup"><span data-stu-id="7238b-104">Getting Started With XInput</span></span>

<span data-ttu-id="7238b-105">XInput est une API qui permet aux applications de recevoir l’entrée du contrôleur Xbox pour Windows.</span><span class="sxs-lookup"><span data-stu-id="7238b-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="7238b-106">Les effets du contrôleur Rumble et l’entrée et la sortie vocales sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7238b-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="7238b-107">Cette rubrique fournit une brève vue d’ensemble des fonctionnalités de XInput et explique comment la configurer dans une application.</span><span class="sxs-lookup"><span data-stu-id="7238b-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="7238b-108">Les éléments suivants sont abordés :</span><span class="sxs-lookup"><span data-stu-id="7238b-108">It includes the following:</span></span>

-   [<span data-ttu-id="7238b-109">Présentation de XInput</span><span class="sxs-lookup"><span data-stu-id="7238b-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="7238b-110">Contrôleur Xbox</span><span class="sxs-lookup"><span data-stu-id="7238b-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="7238b-111">Utilisation de XInput</span><span class="sxs-lookup"><span data-stu-id="7238b-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="7238b-112">Plusieurs contrôleurs</span><span class="sxs-lookup"><span data-stu-id="7238b-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="7238b-113">Obtention de l’état du contrôleur</span><span class="sxs-lookup"><span data-stu-id="7238b-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="7238b-114">Zone morte</span><span class="sxs-lookup"><span data-stu-id="7238b-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="7238b-115">Définition des effets vibratoires</span><span class="sxs-lookup"><span data-stu-id="7238b-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="7238b-116">Obtention des identificateurs de périphérique audio</span><span class="sxs-lookup"><span data-stu-id="7238b-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="7238b-117">Obtention des GUID DirectSound (SDK DirectX hérité uniquement)</span><span class="sxs-lookup"><span data-stu-id="7238b-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="7238b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7238b-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="7238b-119">Présentation de XInput</span><span class="sxs-lookup"><span data-stu-id="7238b-119">Introduction to XInput</span></span>

<span data-ttu-id="7238b-120">La console Xbox utilise un contrôleur de jeu qui est compatible avec Windows.</span><span class="sxs-lookup"><span data-stu-id="7238b-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="7238b-121">Les applications peuvent utiliser l’API XInput pour communiquer avec ces contrôleurs lorsqu’elles sont connectées à un PC Windows (jusqu’à quatre contrôleurs uniques peuvent être branchés à la fois).</span><span class="sxs-lookup"><span data-stu-id="7238b-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="7238b-122">À l’aide de cette API, tout contrôleur Xbox connecté peut être interrogé pour déterminer son état et les effets vibratoires peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="7238b-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="7238b-123">Les contrôleurs qui disposent du casque peuvent également être interrogés pour les périphériques d’entrée et de sortie audio qui peuvent être utilisés avec le casque pour le traitement vocal.</span><span class="sxs-lookup"><span data-stu-id="7238b-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="7238b-124">Contrôleur Xbox</span><span class="sxs-lookup"><span data-stu-id="7238b-124">The Xbox Controller</span></span>

<span data-ttu-id="7238b-125">Le contrôleur Xbox dispose de deux Memory Sticks analogiques, chacun avec un bouton numérique, deux déclencheurs analogiques, un pavé directionnel numérique à quatre directions et huit boutons numériques.</span><span class="sxs-lookup"><span data-stu-id="7238b-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="7238b-126">Les États de chacune de ces entrées sont retournés dans la structure du [**\_ boîtier de souXINPUTment**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) lorsque la fonction [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) est appelée.</span><span class="sxs-lookup"><span data-stu-id="7238b-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="7238b-127">Le contrôleur a également deux moteurs vibrants pour fournir des effets de retour de force à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7238b-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="7238b-128">Les vitesses de ces moteurs sont spécifiées dans la structure [**\_ vibratoire XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) transmise à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) pour définir des effets vibratoires.</span><span class="sxs-lookup"><span data-stu-id="7238b-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="7238b-129">Un casque peut éventuellement être connecté au contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7238b-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="7238b-130">Le casque a un microphone pour l’entrée vocale et un casque pour la sortie audio.</span><span class="sxs-lookup"><span data-stu-id="7238b-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="7238b-131">Vous pouvez appeler la fonction [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) ou [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) héritée pour obtenir les identificateurs d’appareil qui correspondent aux appareils du microphone et du casque.</span><span class="sxs-lookup"><span data-stu-id="7238b-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="7238b-132">Vous pouvez ensuite utiliser les [API audio principales](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) pour recevoir une entrée vocale et envoyer une sortie audio.</span><span class="sxs-lookup"><span data-stu-id="7238b-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="7238b-133">Utilisation de XInput</span><span class="sxs-lookup"><span data-stu-id="7238b-133">Using XInput</span></span>

<span data-ttu-id="7238b-134">L’utilisation de XInput est aussi simple que l’appel des fonctions XInput en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="7238b-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="7238b-135">À l’aide des fonctions XInput, vous pouvez récupérer l’état du contrôleur, obtenir les ID audio du casque et définir les effets du contrôleur Rumble.</span><span class="sxs-lookup"><span data-stu-id="7238b-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="7238b-136">Plusieurs contrôleurs</span><span class="sxs-lookup"><span data-stu-id="7238b-136">Multiple Controllers</span></span>

<span data-ttu-id="7238b-137">L’API XInput prend en charge jusqu’à quatre contrôleurs connectés à tout moment.</span><span class="sxs-lookup"><span data-stu-id="7238b-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="7238b-138">Les fonctions XInput nécessitent toutes un paramètre *dwUserIndex* qui est transmis pour identifier le contrôleur qui est défini ou interrogé.</span><span class="sxs-lookup"><span data-stu-id="7238b-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="7238b-139">Cet ID se trouve dans la plage 0-3 et est défini automatiquement par XInput.</span><span class="sxs-lookup"><span data-stu-id="7238b-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="7238b-140">Le nombre correspond au port dans lequel le contrôleur est connecté et n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="7238b-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="7238b-141">Chaque contrôleur affiche l’ID qu’il utilise en allumant un quadrant sur la « sonnerie de la lumière » au centre du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7238b-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="7238b-142">Une valeur *dwUserIndex* égale à 0 correspond au quadrant supérieur gauche ; la numérotation se poursuit autour de l’anneau dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="7238b-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="7238b-143">Les applications doivent prendre en charge plusieurs contrôleurs.</span><span class="sxs-lookup"><span data-stu-id="7238b-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="7238b-144">Obtention de l’état du contrôleur</span><span class="sxs-lookup"><span data-stu-id="7238b-144">Getting Controller State</span></span>

<span data-ttu-id="7238b-145">Tout au long de la durée d’une application, l’obtention de l’État à partir d’un contrôleur sera probablement effectuée le plus souvent.</span><span class="sxs-lookup"><span data-stu-id="7238b-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="7238b-146">Du frame au frame dans une application de jeu, l’État doit être récupéré et les informations de jeu mises à jour pour refléter les modifications du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7238b-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="7238b-147">Pour récupérer l’État, utilisez la fonction [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :</span><span class="sxs-lookup"><span data-stu-id="7238b-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

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

<span data-ttu-id="7238b-148">Notez que la valeur de retour de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) peut être utilisée pour déterminer si le contrôleur est connecté.</span><span class="sxs-lookup"><span data-stu-id="7238b-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="7238b-149">Les applications doivent définir une structure pour contenir les informations du contrôleur interne ; ces informations doivent être comparées aux résultats de **XInputGetState** pour déterminer quelles modifications, telles que les Appuyez sur les boutons ou les deltas de contrôleur analogique, ont été apportées à ce cadre.</span><span class="sxs-lookup"><span data-stu-id="7238b-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="7238b-150">Dans l’exemple ci-dessus, *g \_ Controllers* représente une telle structure.</span><span class="sxs-lookup"><span data-stu-id="7238b-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="7238b-151">Une fois que l’État a été récupéré dans une structure d' [**\_ État XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , vous pouvez vérifier s’il contient des modifications et obtenir des informations spécifiques sur l’état du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7238b-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="7238b-152">Le membre *dwPacketNumber* de la structure d' [**\_ État XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) peut être utilisé pour vérifier si l’état du contrôleur a changé depuis le dernier appel à [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span><span class="sxs-lookup"><span data-stu-id="7238b-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="7238b-153">Si *dwPacketNumber* n’est pas modifié entre deux appels séquentiels à **XInputGetState**, cela signifie qu’il n’y a eu aucune modification de l’État.</span><span class="sxs-lookup"><span data-stu-id="7238b-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="7238b-154">Si elle diffère, l’application doit vérifier le membre de la *manette* de la structure d' **\_ État XInput** pour obtenir des informations d’État plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="7238b-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="7238b-155">Pour des raisons de performances, n’appelez pas [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) pour un emplacement utilisateur « vide » à chaque trame.</span><span class="sxs-lookup"><span data-stu-id="7238b-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="7238b-156">Nous vous recommandons d’utiliser à la place des contrôles de nouveaux contrôleurs à intervalles de quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="7238b-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="7238b-157">Zone morte</span><span class="sxs-lookup"><span data-stu-id="7238b-157">Dead Zone</span></span>

<span data-ttu-id="7238b-158">Pour que les utilisateurs bénéficient d’une expérience de jeu cohérente, votre jeu doit implémenter la zone morte correctement.</span><span class="sxs-lookup"><span data-stu-id="7238b-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="7238b-159">La zone morte est des valeurs de « mouvement » signalées par le contrôleur, même lorsque les Thumbsticks analogiques sont intacts et centrés.</span><span class="sxs-lookup"><span data-stu-id="7238b-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="7238b-160">Il y a également une zone morte pour les deux déclencheurs analogiques.</span><span class="sxs-lookup"><span data-stu-id="7238b-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="7238b-161">Les jeux qui utilisent des XInput qui ne filtrent pas les zones mortes sont confrontés à un mauvais jeu.</span><span class="sxs-lookup"><span data-stu-id="7238b-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="7238b-162">Notez que certains contrôleurs sont plus sensibles que d’autres, la zone morte peut donc varier d’une unité à l’autre.</span><span class="sxs-lookup"><span data-stu-id="7238b-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="7238b-163">Il est recommandé de tester vos jeux avec plusieurs contrôleurs Xbox sur différents systèmes.</span><span class="sxs-lookup"><span data-stu-id="7238b-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="7238b-164">Les applications doivent utiliser des « zones mortes » sur les entrées analogiques (déclencheurs, bâtons) pour indiquer qu’un mouvement est suffisamment fait sur le bâton ou le déclencheur pour être considéré comme valide.</span><span class="sxs-lookup"><span data-stu-id="7238b-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="7238b-165">Votre application doit vérifier les zones mortes et répondre à appopriately, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="7238b-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

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

<span data-ttu-id="7238b-166">Cet exemple calcule le vecteur de direction du contrôleur et l’avancement du vecteur que le contrôleur a fait l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="7238b-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="7238b-167">Cela permet l’application d’un deadzone circulaire en vérifiant simplement si l’amplitude du contrôleur est supérieure à la valeur deadzone.</span><span class="sxs-lookup"><span data-stu-id="7238b-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="7238b-168">En outre, le code normalise l’amplitude du contrôleur, qui peut ensuite être multiplié par un facteur spécifique à un jeu pour convertir la position du contrôleur en unités pertinentes pour le jeu.</span><span class="sxs-lookup"><span data-stu-id="7238b-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="7238b-169">Notez que vous pouvez définir vos propres zones mortes pour les bâtons et les déclencheurs (n’importe où à partir de 0-65534), ou vous pouvez utiliser la Deadzones fournie définie en tant que XINPUT du contrôle de point de contrôle \_ \_ gauche \_ \_ DEADZONE, XInput \_ manette \_ droit \_ \_ DEADZONE et XInput \_ \_ de déclencheur de manette XInput \_ dans. h :</span><span class="sxs-lookup"><span data-stu-id="7238b-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="7238b-170">Une fois le deadzone appliqué, il peut s’avérer utile de mettre à l’échelle la plage résultante \[ 0.0.. 1.0 à \] virgule flottante (comme dans l’exemple ci-dessus), et d’appliquer éventuellement une transformation non linéaire.</span><span class="sxs-lookup"><span data-stu-id="7238b-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="7238b-171">Par exemple, avec des jeux de conduite, il peut être utile de créer des cubes pour le résultat afin de mieux toucher les voitures à l’aide d’un boîtier de commande, car cubes le résultat vous donne plus de précision dans les plages inférieures, ce qui est souhaitable, car les joueurs appliquent généralement la force logicielle pour obtenir un mouvement subtil ou appliquer une force forcée dans une direction.</span><span class="sxs-lookup"><span data-stu-id="7238b-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="7238b-172">Définition des effets vibratoires</span><span class="sxs-lookup"><span data-stu-id="7238b-172">Setting Vibration Effects</span></span>

<span data-ttu-id="7238b-173">Outre l’obtention de l’état du contrôleur, vous pouvez également envoyer des données de vibration au contrôleur pour modifier les commentaires fournis à l’utilisateur du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7238b-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="7238b-174">Le contrôleur contient deux moteurs Rumble qui peuvent être contrôlés indépendamment en passant des valeurs à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .</span><span class="sxs-lookup"><span data-stu-id="7238b-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="7238b-175">La vitesse de chaque moteur peut être spécifiée à l’aide d’une valeur de mot dans la structure [**\_ vibratoire XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) transmise à la fonction [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) comme suit :</span><span class="sxs-lookup"><span data-stu-id="7238b-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="7238b-176">Notez que le moteur de droite est le moteur haute fréquence, le moteur gauche est le moteur basse fréquence.</span><span class="sxs-lookup"><span data-stu-id="7238b-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="7238b-177">Ils n’ont pas toujours besoin d’être définis sur la même quantité, car ils fournissent des effets différents.</span><span class="sxs-lookup"><span data-stu-id="7238b-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="7238b-178">Obtention des identificateurs de périphérique audio</span><span class="sxs-lookup"><span data-stu-id="7238b-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="7238b-179">Le casque pour un contrôleur Xbox possède les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7238b-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="7238b-180">Enregistrer le son à l’aide d’un microphone</span><span class="sxs-lookup"><span data-stu-id="7238b-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="7238b-181">Lire le son à l’aide d’un casque</span><span class="sxs-lookup"><span data-stu-id="7238b-181">Play back sound using a headphone</span></span>

<span data-ttu-id="7238b-182">Utilisez ce code pour obtenir les identificateurs d’appareil du casque :</span><span class="sxs-lookup"><span data-stu-id="7238b-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="7238b-183">Une fois que vous avez obtenu les identificateurs d’appareil, vous pouvez créer les interfaces appropriées.</span><span class="sxs-lookup"><span data-stu-id="7238b-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="7238b-184">Par exemple, si vous utilisez XAudio 2,8, utilisez ce code pour créer une voix de mastérisation pour cet appareil :</span><span class="sxs-lookup"><span data-stu-id="7238b-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="7238b-185">Pour plus d’informations sur l’utilisation de l’identificateur d’appareil captureId, consultez [capture d’un flux](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="7238b-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="7238b-186">Obtention des GUID DirectSound (SDK DirectX hérité uniquement)</span><span class="sxs-lookup"><span data-stu-id="7238b-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="7238b-187">Le casque qui peut être connecté à un contrôleur Xbox a deux fonctions : il peut enregistrer le son à l’aide d’un microphone et lire le son à l’aide d’un casque.</span><span class="sxs-lookup"><span data-stu-id="7238b-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="7238b-188">Dans l’API XInput, ces fonctions sont accomplies par le biais de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), à l’aide des interfaces **IDirectSound8** et **IDirectSoundCapture8** .</span><span class="sxs-lookup"><span data-stu-id="7238b-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="7238b-189">Pour associer le microphone et le casque du casque à leurs interfaces [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) appropriées, vous devez obtenir le DirectSoundGUIDs pour les appareils de capture et de rendu en appelant [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span><span class="sxs-lookup"><span data-stu-id="7238b-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="7238b-190">L’utilisation de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) héritée n’est pas recommandée et n’est pas disponible dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7238b-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="7238b-191">Les informations de cette section s’appliquent uniquement à la version du kit de développement logiciel (SDK) DirectX de XInput (XInput 1,3).</span><span class="sxs-lookup"><span data-stu-id="7238b-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="7238b-192">La version Windows 8 de XInput (XInput 1,4) utilise exclusivement des identificateurs d’appareil de l’API de session audio Windows (WASAPI) obtenus via [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span><span class="sxs-lookup"><span data-stu-id="7238b-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="7238b-193">Une fois que vous avez récupéré les GUID, vous pouvez créer les interfaces appropriées en appelant DirectSoundCreate8 et DirectSoundCaptureCreate8 comme suit :</span><span class="sxs-lookup"><span data-stu-id="7238b-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7238b-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7238b-194">Related topics</span></span>

[<span data-ttu-id="7238b-195">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="7238b-195">Programming Reference</span></span>](programming-reference.md)
---
title: Jeux de ressources WAVE
description: Jeux de ressources WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- sons Waveform, ressources WAVE de jeu
- audio auxiliaire, lecture des ressources WAVE
- Jeux de ressources WAVE
- PlaySound, fonction, jeux de ressources WAVE
- sndPlaySound fonction)
- Fonction PlaySound, comparée à la fonction sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463119"
---
# <a name="playing-wave-resources"></a><span data-ttu-id="ea390-109">Jeux de ressources WAVE</span><span class="sxs-lookup"><span data-stu-id="ea390-109">Playing WAVE Resources</span></span>

<span data-ttu-id="ea390-110">Vous pouvez utiliser la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) pour lire un son stocké en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="ea390-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="ea390-111">Bien que cela soit également possible à l’aide de la fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** requiert que vous trouviez, chargez, verrouillez, déverrouillez et libérez la ressource. **PlaySound** réalise tout cela avec une seule ligne de code.</span><span class="sxs-lookup"><span data-stu-id="ea390-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="ea390-112">Exemple PlaySound</span><span class="sxs-lookup"><span data-stu-id="ea390-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="ea390-113">Exemple sndPlaySound</span><span class="sxs-lookup"><span data-stu-id="ea390-113">sndPlaySound Example</span></span>

<span data-ttu-id="ea390-114">L' \_ indicateur de mémoire SND indique que le paramètre *lpszSoundName* est un pointeur vers une image en mémoire du fichier wave.</span><span class="sxs-lookup"><span data-stu-id="ea390-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="ea390-115">Pour inclure un fichier WAVE en tant que ressource dans une application, ajoutez l’entrée suivante au script de ressources de l’application (. RC).</span><span class="sxs-lookup"><span data-stu-id="ea390-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="ea390-116">Le nom *soundName* est un espace réservé pour un nom que vous fournissez pour faire référence à cette ressource Wave.</span><span class="sxs-lookup"><span data-stu-id="ea390-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="ea390-117">Les ressources WAVE sont chargées et accessibles comme les autres ressources Windows définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="ea390-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="ea390-118">La fonction PlayResource de l’exemple suivant lit une ressource WAVE spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea390-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



<span data-ttu-id="ea390-119">Pour lire une ressource WAVE à l’aide de cette fonction, transmettez à la fonction un pointeur vers une chaîne contenant le nom de la ressource, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ea390-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 
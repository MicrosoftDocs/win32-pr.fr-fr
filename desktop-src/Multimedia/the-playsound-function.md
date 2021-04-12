---
title: La fonction PlaySound
description: La fonction PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimédia, fonction PlaySound
- audio, PlaySound, fonction
- Wave audio, fonction PlaySound
- PlaySound, fonction, à propos de
- sndPlaySound fonction)
- Fonction PlaySound, comparée à la fonction sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198881"
---
# <a name="the-playsound-function"></a><span data-ttu-id="c0f0c-109">La fonction PlaySound</span><span class="sxs-lookup"><span data-stu-id="c0f0c-109">The PlaySound Function</span></span>

<span data-ttu-id="c0f0c-110">Vous pouvez utiliser la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) pour lire du son de forme d’onde si le son s’ajuste à la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="c0f0c-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="c0f0c-111">(La fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) offre un sous-ensemble des fonctionnalités de PlaySound.</span><span class="sxs-lookup"><span data-stu-id="c0f0c-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="c0f0c-112">Pour optimiser la portabilité de votre application Win32, utilisez **PlaySound**, et non **sndPlaySound**.)</span><span class="sxs-lookup"><span data-stu-id="c0f0c-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="c0f0c-113">La fonction **PlaySound** vous permet de spécifier un son de l’une des trois façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0f0c-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="c0f0c-114">En tant qu’alerte système, à l’aide de l’alias stocké dans le fichier WIN.INI ou le registre</span><span class="sxs-lookup"><span data-stu-id="c0f0c-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="c0f0c-115">En tant que nom de fichier</span><span class="sxs-lookup"><span data-stu-id="c0f0c-115">As a filename</span></span>
-   <span data-ttu-id="c0f0c-116">En tant qu’identificateur de ressource</span><span class="sxs-lookup"><span data-stu-id="c0f0c-116">As a resource identifier</span></span>

<span data-ttu-id="c0f0c-117">La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) vous permet de lire un son dans une boucle continue, en se terminant uniquement quand vous appelez **PlaySound** à nouveau, en spécifiant soit **null** , soit l’identificateur de son d’un autre son pour le paramètre *pszSound* .</span><span class="sxs-lookup"><span data-stu-id="c0f0c-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="c0f0c-118">Vous pouvez utiliser **PlaySound** pour lire le son de façon synchrone ou asynchrone, et pour contrôler le comportement de la fonction d’une autre façon lorsqu’elle doit partager des ressources système.</span><span class="sxs-lookup"><span data-stu-id="c0f0c-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="c0f0c-119">Pour plus d’informations sur l’utilisation de PlaySound, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0f0c-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="c0f0c-120">Utilisation de PlaySound pour lire des fichiers Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="c0f0c-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="c0f0c-121">Utilisation de PlaySound pour boucler des sons</span><span class="sxs-lookup"><span data-stu-id="c0f0c-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="c0f0c-122">Utilisation de PlaySound pour lire des sons système</span><span class="sxs-lookup"><span data-stu-id="c0f0c-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="c0f0c-123">Pour obtenir plus d’exemples sur l’utilisation de **PlaySound** dans vos applications Win32, consultez [Playing Wave Resources](playing-wave-resources.md)(en anglais).</span><span class="sxs-lookup"><span data-stu-id="c0f0c-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 
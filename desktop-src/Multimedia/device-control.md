---
title: Contrôle de périphérique (Windows Multimedia)
description: Contrôle de l’appareil
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032237"
---
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="47025-103">Contrôle de périphérique (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="47025-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="47025-104">Pour contrôler un appareil MCI, ouvrez l’appareil, envoyez-lui les commandes nécessaires, puis fermez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="47025-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="47025-105">Les commandes peuvent être très similaires, même pour les périphériques MCI complètement différents.</span><span class="sxs-lookup"><span data-stu-id="47025-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="47025-106">Par exemple, la série suivante de commandes MCI lit la sixième piste d’un CD audio à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="47025-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="47025-107">L’exemple suivant illustre une série similaire de commandes MCI qui lisent les 10 000 premiers exemples d’un fichier Waveform-Audio :</span><span class="sxs-lookup"><span data-stu-id="47025-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="47025-108">Ces exemples illustrent des informations intéressantes sur les commandes MCI :</span><span class="sxs-lookup"><span data-stu-id="47025-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="47025-109">Les mêmes commandes de base ([**ouvrir**](open.md), [**définir**](set.md), [**lire**](play.md)et [**Fermer**](close.md)) sont utilisées avec les périphériques CD audio et Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="47025-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="47025-110">Les mêmes commandes MCI sont utilisées avec tous les périphériques MCI.</span><span class="sxs-lookup"><span data-stu-id="47025-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="47025-111">La commande ouvrir du périphérique Wave-audio comprend une spécification de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="47025-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="47025-112">Le périphérique Waveform-Audio est un *appareil composé* (l’un associé à un fichier de données), tandis que le périphérique CD audio est un *appareil simple* (un sans fichier de données associé).</span><span class="sxs-lookup"><span data-stu-id="47025-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="47025-113">La commande Set spécifie les formats d’heure dans chaque cas, mais l’indicateur de format d’heure pour le périphérique CD audio spécifie les pistes/minutes/secondes/frames (TMSF), tandis que le format d’heure utilisé avec le périphérique Wave-Audio spécifie « échantillons ».</span><span class="sxs-lookup"><span data-stu-id="47025-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="47025-114">Les variables utilisées avec les indicateurs « from » et « to » sont appropriées au format d’heure respectif.</span><span class="sxs-lookup"><span data-stu-id="47025-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="47025-115">Par exemple, pour le périphérique CD audio, les variables spécifient une plage de pistes, mais pour le périphérique Wave-audio, les variables spécifient une plage d’exemples.</span><span class="sxs-lookup"><span data-stu-id="47025-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 

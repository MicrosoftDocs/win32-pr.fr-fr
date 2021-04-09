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
# <a name="device-control-windows-multimedia"></a>Contrôle de périphérique (Windows Multimedia)

Pour contrôler un appareil MCI, ouvrez l’appareil, envoyez-lui les commandes nécessaires, puis fermez l’appareil. Les commandes peuvent être très similaires, même pour les périphériques MCI complètement différents. Par exemple, la série suivante de commandes MCI lit la sixième piste d’un CD audio à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


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



L’exemple suivant illustre une série similaire de commandes MCI qui lisent les 10 000 premiers exemples d’un fichier Waveform-Audio :


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



Ces exemples illustrent des informations intéressantes sur les commandes MCI :

-   Les mêmes commandes de base ([**ouvrir**](open.md), [**définir**](set.md), [**lire**](play.md)et [**Fermer**](close.md)) sont utilisées avec les périphériques CD audio et Waveform-Audio. Les mêmes commandes MCI sont utilisées avec tous les périphériques MCI.
-   La commande ouvrir du périphérique Wave-audio comprend une spécification de nom de fichier. Le périphérique Waveform-Audio est un *appareil composé* (l’un associé à un fichier de données), tandis que le périphérique CD audio est un *appareil simple* (un sans fichier de données associé).
-   La commande Set spécifie les formats d’heure dans chaque cas, mais l’indicateur de format d’heure pour le périphérique CD audio spécifie les pistes/minutes/secondes/frames (TMSF), tandis que le format d’heure utilisé avec le périphérique Wave-Audio spécifie « échantillons ».
-   Les variables utilisées avec les indicateurs « from » et « to » sont appropriées au format d’heure respectif. Par exemple, pour le périphérique CD audio, les variables spécifient une plage de pistes, mais pour le périphérique Wave-audio, les variables spécifient une plage d’exemples.

 

 

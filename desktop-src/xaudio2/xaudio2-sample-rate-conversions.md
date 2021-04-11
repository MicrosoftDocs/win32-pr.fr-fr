---
description: Les voix XAudio2 peuvent effectuer des conversions automatiques de taux d’échantillonnage si leur taux d’échantillonnage d’entrée diffère du taux d’échantillonnage d’entrée de leurs voix de sortie.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversions de taux d’échantillonnage XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210800"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversions de taux d’échantillonnage XAudio2

Les voix XAudio2 peuvent effectuer des conversions automatiques de taux d’échantillonnage si leur taux d’échantillonnage d’entrée diffère du taux d’échantillonnage d’entrée de leurs voix de sortie.

Les conversions de taux d’échantillonnage suivent les règles suivantes :

-   Le taux d’échantillonnage des entrées vocales est fixe.

    Les voix peuvent uniquement gérer le taux d’échantillonnage d’entrée spécifié lors de leur création. Pour les [**voix de mastérisation**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) et les voix de [**mixage secondaire**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), le taux d’échantillonnage d’entrée est spécifié avec l’argument *InputSampleRate* pour les fonctions [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) et [**IXAudio2 :: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) . Pour les voix source, le taux d’échantillonnage d’entrée de la voix est spécifié par l’argument pSourceFormat à la fonction [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

-   Toutes les voix de sortie de la voix doivent avoir le même taux d’échantillonnage d’entrée.

    Les voix peuvent passer de leur taux d’échantillonnage d’entrée à n’importe quel taux d’échantillonnage de sortie, mais toutes les voix de sortie de la voix doivent avoir le même taux d’échantillonnage d’entrée. Par exemple, une voix peut sortir d’un nombre quelconque de voix, avec un taux d’échantillonnage d’entrée de 22 kHz. Toutefois, si cette même voix avait plusieurs voix de sortie, chacune ayant un taux d’échantillonnage d’entrée différent, le graphique audio n’est pas valide.

-   Le traitement de la conversion de taux d’échantillonnage se produit uniquement lorsque cela est nécessaire.

    La conversion de données audio en un taux d’échantillonnage différent entraîne une charge de traitement plus importante, qu’il est préférable d’éviter. Si le taux d’échantillonnage d’entrée de la voix correspond au taux d’échantillonnage d’entrée de ses voix en sortie, cette conversion n’est pas effectuée et le temps de traitement est raccourci.

-   Le taux d’échantillonnage de sortie peut varier au cours de la vie d’une voix.

    Le taux d’échantillonnage de sortie d’une voix n’est pas fixe. Tant que toutes ses voix en sortie ont le même taux d’échantillonnage d’entrée, le graphique audio est valide. Si une voix est transformée en sortie vers de nouvelles voix avec un taux d’échantillonnage d’entrée différent, la voix est convertie en taux d’échantillonnage des nouvelles voix.

Dans certains scénarios, il est nécessaire d’ajouter une voix de mixage secondaire pour effectuer une conversion de taux d’échantillonnage entre les voix. Si une voix a besoin d’une sortie vers des voix avec différents taux d’échantillonnage d’entrée, une seule des voix peut être une sortie directe de la voix d’origine. Étant donné que toutes les voix de sortie de la voix doivent avoir le même taux d’échantillonnage d’entrée, les autres voix reçoivent indirectement la sortie. Il doit y avoir une voix de mixage secondaire avec la fréquence d’échantillonnage d’entrée appropriée qui est comprise entre la voix d’origine et la voix de sortie prévue.

Par exemple, considérez une voix source avec un taux d’échantillonnage d’entrée de 22 kHz, qui doit sortir sur une voix de mixage secondaire avec un taux d’échantillonnage d’entrée de 11 kHz et une voix de mastérisation avec un taux d’échantillonnage d’entrée de 44,1 kHz. Étant donné que les deux voix de sortie ont des taux d’échantillonnage d’entrée différents, vous devez insérer plus de voix de mixage secondaire entre la voix d’origine et les voix de sortie prévues. Pour préserver la fidélité de la voix source et éviter les conversions coûteuses inutiles vers des taux d’échantillonnage plus élevés, vous devez insérer deux voix de mixage secondaire avec des taux d’entrée d’échantillonnage de 22 kHz dans le graphique. Une voix de mixage secondaire s’affiche à 11 kHz à la voix du mixage secondaire avec l’effet de réverbération, et l’autre voix du mixage secondaire est sortie vers la voix de mastérisation à 44,1 kHz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Exemples de conversion de taux d’échantillonnage dans les graphiques audio

Toutes les voix ont le même taux d’entrée d’échantillonnage ; aucune conversion de taux d’échantillonnage n’est effectuée dans le graphique audio.![aucune conversion de taux d’échantillonnage n’est effectuée dans le graphique audio.](images/xaudio2-sample-rate-conversions-1.png)

Toutes les voix ont le même taux d’entrée d’échantillonnage, à l’exception de la voix de mastérisation ; la conversion de taux d’échantillonnage est effectuée uniquement sur les données qui sont dirigées vers la voix de mastérisation. ![la conversion de taux d’échantillonnage est effectuée uniquement sur les données qui sont dirigées vers la voix de mastérisation.](images/xaudio2-sample-rate-conversions-2.png)

Les voix ont des taux d’entrée différents et nécessitent davantage de voix de mixage secondaire pour effectuer des conversions de taux d’échantillonnage ; la conversion de taux d’échantillonnage est effectuée à plusieurs endroits dans le graphique audio. ![la conversion de taux d’échantillonnage est effectuée à plusieurs endroits dans le graphique audio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Voix](voices.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 

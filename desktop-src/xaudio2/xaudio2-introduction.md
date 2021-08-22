---
description: XAudio2 est une API audio de bas niveau. Il fournit un traitement de signal et une base de mixage pour les jeux similaires à ses prédécesseurs, DirectSound et XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Présentation de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a966e9682a7f605864c0374a588d4b7eb3724036fe284bd6d92c64080e9225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589899"
---
# <a name="xaudio2-introduction"></a>Présentation de XAudio2

XAudio2 est une API audio de bas niveau. Il fournit un traitement de signal et une base de mixage pour les jeux similaires à ses prédécesseurs, DirectSound et XAudio.

XAudio2 est le remplacement attendu long de DirectSound. Il traite plusieurs problèmes et demandes de fonctionnalités en suspens.

## <a name="xaudio2-features"></a>Fonctionnalités de XAudio2

La liste suivante répertorie les fonctionnalités XAudio2 et les nouvelles fonctionnalités qui permettent aux développeurs d’améliorer les performances de leurs jeux.

-   Effets DSP et par filtrage vocal

    Les effets du traitement des signaux numériques (DSP) sont les nuanceurs de pixels de l’audio. Ils gèrent tout ce qui est de la transformation d’un son, en transformant un porc squeal en un petit son effrayant, pour placer des sons dans l’environnement du jeu à l’aide de la réverbération et du filtrage d’occlusion ou d’obstruction. XAudio2 fournit un Framework DSP flexible et puissant. Il fournit également un filtre intégré sur chaque voix, pour des effets de filtrage efficaces faible/élevé/bande.

    Pour plus d’informations sur les effets DSP et le filtrage par voix, consultez [effets audio XAudio2](xaudio2-audio-effects.md) et [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) .

-   Sous-mixage

    La sous-combinaison combine plusieurs sons en un seul flux audio, par exemple un son de moteur constitué de parties composites, qui sont toutes lues simultanément. En outre, vous pouvez utiliser la sous-combinaison pour traiter et combiner des parties similaires d’un jeu. Par exemple, vous pouvez combiner tous les effets sonores du jeu pour permettre l’application d’un paramètre de volume utilisateur alors qu’un paramètre distinct contrôle le volume musical. Combiné à DSP, le sous-mixage offre le type de routage et de traitement des données nécessaire pour les jeux actuels. XAudio2 autorise des niveaux de sous-mixage arbitraires, ce qui permet de créer des sons complexes et des mixages de jeux.

    pour plus d’informations sur le sous-mixage, consultez [XAudio2 Audio Graph](xaudio2-audio-graph.md) et [XAudio2 voices](xaudio2-voices.md) .

-   Prise en charge audio compressée

    L’une des principales demandes de fonctionnalités pour DirectSound concerne la prise en charge de l’audio compressé. XAudio2 prend en charge les formats compressés (ADPCM) en mode natif avec la décompression au moment de l’exécution.

-   Prise en charge améliorée des sons multicanaux et surround

    La prise en charge des sons multicanaux, 3D et surround est développée. les sons 3D et surround sont désormais bien plus flexibles et transparents. XAudio2 supprime la limite de 6 canaux sur les sons multicanaux et prend en charge l’audio multicanal sur toute carte audio compatible multicanal. La carte n’a pas besoin d’être accélérée par le matériel.

-   Traitement multitaux

    Pour réduire l’utilisation du processeur, XAudio2 fournit la technologie permettant de créer plusieurs graphiques de traitement audio à faible débit. Cela peut réduire considérablement l’utilisation de l’UC en permettant à un jeu de traiter l’audio à la vitesse du matériel source si le taux est inférieur à 48 kHz.

-   Modèle d’API de non-blocage

    À quelques exceptions près, un appel de méthode XAudio2 ne bloquera pas le moteur de traitement audio. Cela signifie qu’un client peut effectuer en toute sécurité un ensemble d’appels de méthode à tout moment sans blocage sur les appels de longue durée qui entraînent des retards. Les exceptions sont la méthode [**IXAudio2Voice ::D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (qui peut bloquer le moteur jusqu’à la fin du traitement de la voix) et les méthodes qui terminent le thread audio : [**IXAudio2 :: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) et [**IXAudio2 :: Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Notez que bien que les appels de méthode XAudio2 ne bloquent pas le moteur de traitement audio, les méthodes XAudio2 contiennent des sections critiques et peuvent elles-mêmes être bloquées dans certaines circonstances.

## <a name="when-to-use-xaudio2"></a>Quand utiliser XAudio2

XAudio2 est principalement destiné au développement de moteurs audio hautes performances pour les jeux. Pour les développeurs qui souhaitent ajouter des effets sonores et de la musique de fond dans leurs jeux modernes, XAudio2 propose un moteur de mixage et de graphique audio caractérisé par sa faible latence et sa prise en charge des tampons dynamiques, de la lecture synchrone et précise en échantillonnage, et de la conversion implicite du débit source. Par rapport à WASAPI, XAudio2 nécessite uniquement une quantité minimale de code, même pour les solutions audio complexes. Par rapport au moteur de Media Foundation, XAudio2 est une API C++ de faible latence et de bas niveau, conçue pour être utilisée dans les jeux.

Pour les applications qui ont simplement besoin d’une lecture musicale normale, le moteur de Media Foundation peut être une meilleure correspondance avec les exigences de l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Référence de programmation XAudio2](programming-reference.md)
</dt> </dl>

 

 

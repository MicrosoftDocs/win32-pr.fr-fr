---
description: Cette vue d’ensemble présente des concepts clés pour l’utilisation de XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Concepts clés de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523413"
---
# <a name="xaudio2-key-concepts"></a>Concepts clés de XAudio2

Cette vue d’ensemble présente des concepts clés pour l’utilisation de XAudio2.

-   [Moteur XAudio2](#xaudio2-engine)
-   [Voix](#voices)
-   [Graphique audio](#audio-graph)
-   [Rappels](#callbacks)
-   [Rubriques connexes](#related-topics)

## <a name="xaudio2-engine"></a>Moteur XAudio2

L’interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) est au cœur du moteur XAudio2. La création d’une instance de l’interface **IXAudio2** permet au client d’énumérer les périphériques audio disponibles, de configurer les propriétés de l’API globale, de créer des voix et de surveiller les performances. La fonction d’assistance [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) effectue des tâches d’instanciation et d’initialisation pour XAudio2.

Vous pouvez créer des instances de XAudio2 plusieurs fois dans un même processus. Chaque objet XAudio2 fonctionne de façon indépendante et possède son propre thread de traitement audio. Seuls les paramètres de débogage sont partagés. Cela est important sur Windows où plusieurs composants différents peuvent être chargés dans un même processus. Par exemple, Internet Explorer peut utiliser plusieurs composants XAudio2 simultanément. Bien qu’il soit possible de créer plusieurs objets de moteur XAudio2 dans une même application cliente, vous ne devez pas transmettre des informations entre leurs graphiques respectifs.

Pour obtenir un exemple d’initialisation du moteur XAudio2, consultez [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).

## <a name="voices"></a>Voix

Les voix sont les objets utilisés par XAudio2 pour traiter, manipuler et lire des données audio. Il existe trois types de voix dans XAudio2.

-   [**Voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Les voix source représentent un flux de données audio. Les voix source envoient leurs données à d’autres types de voix.

-   [**Voix de mixage secondaire**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Les voix de mixage secondaire effectuent une manipulation des données audio qu’elles reçoivent. Un exemple de manipulation de données audio peut être une conversion de taux d’échantillonnage. Une fois qu’une voix de mixage a traité des données, elle les transmet à une autre voix de mixage ou à une voix principale.

-   [**Mastérisation des voix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    La maîtrise des voix reçoit des données des voix et des voix de mixage source et envoie ces données au matériel audio.

Pour obtenir une vue d’ensemble des voix XAudio2, consultez [XAudio2 Voices](voices.md) .

## <a name="audio-graph"></a>Graphique audio

Un graphique audio est une collection de voix XAudio2. L’audio commence à un côté d’un graphique audio dans les voix source, passe éventuellement par une ou plusieurs voix de mixage et se termine à une voix de mastérisation. Un graphique audio contient une voix source pour chaque son en cours de lecture, zéro, une ou plusieurs voix de mixage et une voix de mastérisation. Le graphique audio le plus simple, et le minimum nécessaire pour faire un bruit dans XAudio2, est une seule voix source qui s’effectue directement sur une voix de mastérisation. Consultez [Comment : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md) pour obtenir un exemple des étapes minimales nécessaires pour lire un son avec XAudio2.

Pour obtenir une vue d’ensemble des graphiques audio XAudio2, consultez [XAudio2 audio Graph](audio-graphs.md) .

## <a name="callbacks"></a>Rappels

Les rappels sont le mécanisme utilisé par XAudio2 pour signaler au code client qu’un événement s’est produit dans une voix ou dans l’objet moteur. Étant donné que la lecture audio est asynchrone dans le moteur XAudio2, les rappels fournissent le seul moyen de déterminer à quel moment un son est terminé.

Pour obtenir une vue d’ensemble des rappels XAudio2, consultez [rappels XAudio2](callbacks.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Versions de XAudio2](xaudio2-versions.md)
</dt> <dt>

[Procédure : initialiser XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Comment : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 




---
description: L’ensemble de toutes les voix, avec leurs effets contenus et leurs interconnexions, est appelé graphique de traitement audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Graphique audio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210804"
---
# <a name="xaudio2-audio-graph"></a>Graphique audio XAudio2

L’ensemble de toutes les voix, avec leurs effets contenus et leurs interconnexions, est appelé graphique de traitement audio. Le graphique prend un ensemble de flux audio du client comme entrée, les traite et remet le résultat final à un périphérique audio. Tout le traitement audio a lieu dans un thread distinct avec une périodicité définie par le quantum du graphique (actuellement 10 millisecondes sur Microsoft Windows et 5 1/3 millisecondes sur Xbox 360). Chaque Quantum en millisecondes, le thread sort et réitère les millisecondes de quantum des données audio dans le graphique entier. Pour obtenir un exemple de création d’un graphique audio de base, consultez Comment : [générer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md).

Graphique audio simple :

![graphique audio simple](images/xaudio2-audio-graph.png)

Le client peut contrôler l’état du graphique de façon dynamique lorsqu’il est en cours d’exécution. Les actions de contrôle peuvent inclure l’ajout et la suppression d’entrées et de sorties, la modification des effets internes et des interconnexions, la définition de paramètres sur les effets, l’activation et la désactivation des parties du graphique, etc. Pour obtenir un exemple de modification dynamique d’un graphique audio, consultez [Comment : ajouter dynamiquement ou supprimer des voix d’un graphique audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).

## <a name="processing-the-graph"></a>Traitement du graphique

Tout appel de méthode qui affecte un objet dans le graphique est considéré comme un changement d’état de graphique. Les modifications de l’état du graphique sont les suivantes :

-   Création et destruction de voix
-   Démarrage ou arrêt des voix
-   Modification des destinations d’une voix
-   Modification des chaînes d’effets
-   Activation ou désactivation des effets
-   Définition des paramètres sur les effets ou sur les SRCs, filtres, volumes et mixages intégrés

Tout ensemble de modifications d’état de graphique peut être combiné et exécuté comme une transaction atomique. Ces opérations atomiques sont appelées ensembles d’opérations. Elles sont abordées dans la vue d’ensemble des [ensembles d’opérations XAudio2](xaudio2-operation-sets.md) .

## <a name="internal-data-representation"></a>Représentation des données internes

Les données audio dans le graphique XAudio2 sont toujours stockées et traitées dans un formulaire PCM à virgule flottante 32 bits. Toutefois, le nombre de canaux et le taux d’échantillonnage peuvent varier dans le graphique. Le format dans lequel une voix donnée traite les données audio est déterminé par le type de voix et les paramètres utilisés pour créer la voix.



| Type de voix                                                                                                      | Paramètres                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | Nombre de canaux et taux d’échantillonnage des voix auxquelles la voix source envoie de l’audio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) et [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Arguments *InputChannels* et *InputSampleRate* utilisés pour créer la voix de mixage secondaire/de mastérisation. |



 

## <a name="format-conversion"></a>Conversion de format

XAudio2 gère les taux d’échantillonnage ou les conversions de canaux qui sont nécessaires à l’audio transit d’une voix à l’autre, avec les limitations suivantes :

-   Toutes les voix de destination pour une voix particulière doivent s’exécuter au même taux d’échantillonnage
-   Les effets dans une chaîne d’effet peuvent modifier le nombre de canaux audio, mais pas son taux d’échantillonnage
-   Le nombre de canaux de sortie d’une chaîne d’effets doit correspondre à celui des voix qu’il envoie
-   Aucune modification de graphique dynamique ne peut être effectuée, ce qui rompt les règles ci-dessus

Du côté de l’entrée, les voix source peuvent lire les données dans n’importe quel format PCM valide, ou dans n’importe quel format compressé pris en charge par XAudio2. Si les données d’entrée sont compressées, elles sont décodées en PCM à virgule flottante avant tout traitement supplémentaire.

Du côté de la sortie, la maîtrise des voix peut uniquement produire des données PCM. Ces données satisferont toujours les mêmes restrictions que celles décrites ci-dessus pour les données PCM d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Graphiques audio](audio-graphs.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[Procédure : utiliser des voix prémixées](how-to--use-submix-voices.md)
</dt> <dt>

[Procédure : Créer une chaîne d’effets](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 




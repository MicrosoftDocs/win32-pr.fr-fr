---
description: La modulation adaptative du code Pulse (ADPCM) est un format de compression avec perte qui est implémenté pour XAudio2 afin de fournir des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Vue d’ensemble d’ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541849"
---
# <a name="adpcm-overview"></a>Vue d’ensemble d’ADPCM

La modulation adaptative du code Pulse (ADPCM) est un format de compression avec perte qui est implémenté pour XAudio2 afin de fournir des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression. Avec un format de compression avec perte de données, certaines données sont modifiées et perdues pendant la compression. ADPCM peut obtenir des taux de compression allant jusqu’à 4:1.

L’implémentation d’ADPCM pour XAudio2 fournit des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression. ADPCM permet au concepteur audio de choisir un paramètre qui est un compromis approprié parmi la taille, la qualité et la résolution (pour placer des points de boucle).

XAudio2 utilise une version modifiée du codec Microsoft ADPCM qui prend en charge la mise en forme des données étendues requise pour fournir des exemples personnalisés de tailles de bloc. Pour cette raison, les données audio XAudio2 ne peuvent pas être lues par des moteurs audio qui ne prennent pas en charge cette version du codec ADPCM.

> [!Note]  
> Actuellement, la compression ADPCM est uniquement disponible pour Windows, y compris les déploiements de XNA Game Studio Express pour Windows.

 

## <a name="adpcm-encoding"></a>Encodage ADPCM

Les données audio sont encodées dans ADPCM à l’aide de l’outil en ligne de commande AdpcmEncode.

-   AdpcmEncode

    Pour encoder des fichiers audio comme ADPCM pour une utilisation avec XAudio2, utilisez l’outil de ligne de commande **AdpcmEncode** .

## <a name="adpcm-decoding"></a>Décodage ADPCM

Le décodage logiciel d’ADPCM est pris en charge dans XAudio2.

-   XAudio2

    Pour utiliser des données encodées ADPCM dans XAudio2, vous devez initialiser une structure **ADPCMWAVEFORMAT** avec des valeurs spécifiques à ADPCM et la passer en tant qu’argument à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) lorsque vous créez une voix source. Pour obtenir un exemple de chargement et de lecture d’un son dans XAudio2, consultez [Comment : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>SamplesPerBlock

La compression ADPCM fonctionne en séparant la forme d’onde par des blocs et en prédisant la variation des échantillons de forme d’onde dans chaque bloc. La taille des blocs est mesurée en échantillons. La plus petite taille de bloc est 32 exemples et le plus élevé est 512 échantillons.

Les blocs plus grands permettent une meilleure compression, ce qui se traduit par des fichiers de plus petite taille, mais au détriment de la qualité du son et de la résolution de l’alignement des points de boucle.

En général, la modification de la valeur SamplesPerBlock entraîne ces compromis :



| Si SamplesPerBlock...      | Compression de fichier | Qualité du son | Résolution des points de boucle |
|----------------------------|------------------|---------------|-----------------------|
| Augmentation (jusqu’à 512 max.)  | Augmente        | Réduis     | Réduis             |
| Diminue (jusqu’à min 32) | Réduis        | Augmente     | Augmente             |



 

## <a name="restrictions"></a>Restrictions

Comme ADPCM utilise des blocs d’exemple qui sont alignés l’un après l’autre, une vague compressée avec ADPCM peut avoir un bloc partiel non terminé à sa fin. Le décodeur ADPCM génère un silence pour le reste de ce bloc partiel, ce qui empêche l’onde de s’exécuter en boucle en toute transparence.

La valeur du paramètre *SamplesPerBlock* affecte la résolution avec laquelle vous pouvez aligner les données Wave et les points de boucle.

Si vous essayez d’appliquer la compression à une vague non alignée, vous obtiendrez une erreur ou un avertissement selon que l’onde est utilisée dans les événements de lecture en boucle. Vous ne pouvez pas compresser une vague utilisée dans des événements de lecture en boucle. Supprimez-le des événements de lecture en boucle et réappliquez la compression.

Si vous utilisez l’onde exclusivement en mode non-bouclage, la restriction d’alignement de bloc de l’exemple ne s’applique pas.

## <a name="adpcm-file-structure"></a>Structure de fichiers ADPCM

Un fichier ADPCM est un fichier RIFF standard avec les types de blocs suivants.



| Bloc FCC     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Bloc RIFF standard contenant un type de fichier avec la valeur WAVE dans les quatre premiers octets de sa section de données et les autres segments du fichier dans le reste de sa section de données.                                                                                                                                                                                                                                                                 |
| fmt           | Contient l’en-tête format pour le fichier ADPCM. Les données de ce segment correspondent à une structure **ADPCMWAVEFORMAT** .                                                                                                                                                                                                                                                                                                                             |
| data          | Contient les données audio ADPCM encodées. Quand vous utilisez ADPCM dans XAudio2, vous devez lire le contenu du segment de données dans une mémoire tampon et le transmettre à une voix source en tant que membre **pAudioData** d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Vous n’avez pas besoin d’échanger par octet le contenu du bloc de données.                                                                                                                            |
| SMPL et wsmp | Types de blocs facultatifs contenant les informations de bouclage pour le fichier ADPCM. Lorsque vous utilisez ADPCM dans XAudio2, les valeurs contenues dans les segments SMPL ou wsmp sont utilisées pour remplir les membres **LoopBeginLoopLength** et **LoopCount** de la structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Sur la Xbox 360, vous devez échanger par octet les données chargées à partir d’un bloc SMPL pour tenir compte de la différence endianness entre Windows et Xbox 360. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 

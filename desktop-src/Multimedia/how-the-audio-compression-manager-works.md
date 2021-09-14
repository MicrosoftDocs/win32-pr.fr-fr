---
title: Fonctionnement du gestionnaire de compression audio
description: Fonctionnement du gestionnaire de compression audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimédia, gestionnaire de compression audio (ACM)
- audio, gestionnaire de compression audio (ACM)
- Audio Compression Manager (ACM), à propos de
- ACM (gestionnaire de compression audio), à propos de
- Audio Compression Manager (ACM), pilotes de codec
- ACM (gestionnaire de compression audio), pilotes de codec
- Audio Compression Manager (ACM), pilotes de convertisseur de format
- ACM (gestionnaire de compression audio), pilotes de convertisseur de format
- Gestionnaire de compression audio (ACM), pilotes de filtre
- ACM (gestionnaire de compression audio), pilotes de filtre
- Gestionnaire de compression audio (ACM), pilotes de compresseur
- ACM (gestionnaire de compression audio), pilotes de compresseur
- le gestionnaire de compression audio (ACM), les pilotes de décompresseur
- ACM (gestionnaire de compression audio), pilotes de décompresseur
- pilotes de codec
- mettre en forme les pilotes de convertisseur
- filtrer les pilotes
- pilotes de compresseur
- pilotes de décompresseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007197"
---
# <a name="how-the-audio-compression-manager-works"></a>Fonctionnement du gestionnaire de compression audio

L’ACM utilise des hooks d’interface de pilote existants pour remplacer l’algorithme de mappage par défaut pour les périphériques audio Waveform. Cela permet à l’ACM d’intercepter les appels d’appareils ouverts. Une fois qu’un appel a été intercepté, l’ACM peut effectuer diverses tâches pour traiter les données audio, telles que l’insertion d’un compresseur externe ou d’un décompresseur dans la séquence.

L’ACM gère les types de pilotes suivants :

-   Pilotes de compresseur et décompresseur (codec)
-   Mettre en forme les pilotes de convertisseur
-   Filtrer les pilotes

Les compresseurs et les décompresseurs modifient un type de format. Par exemple, un compresseur ou un décompresseur peut modifier un fichier PCM (modulation d’impulsions de code) en un fichier ADPCM (adaptative différentielle Pulse Code Modulation). Les convertisseurs de format modifient le format, mais pas le type de données. Par exemple, un convertisseur peut modifier les données 44-kHz, 16 bits en données de 44 kHz, 8 bits. Les filtres ne changent pas du tout le format des données, mais ils modifient les données Waveform-Audio d’une certaine manière. Par exemple, un filtre peut combiner un flux de données et un écho de lui-même. Un pilote ACM unique, ou une balise de filtre ou de format dans un pilote, peut également prendre en charge des combinaisons des types précédents.

Pour la sortie Waveform-Audio, l’ACM passe chaque mémoire tampon de données au convertisseur à mesure qu’elle arrive. Le convertisseur décompresse les données et retourne les données décompressées à l’ACM dans une mémoire tampon « Shadow ». L’ACM transmet ensuite le tampon d’ombre décompressé au pilote Wave-audio. L’ACM alloue les mémoires tampons d’ombre à chaque fois qu’il reçoit un message de préparation.

Pour une entrée Waveform-Audio, l’ACM transmet des tampons d’ombre vides au pilote. Elle utilise une tâche en arrière-plan pour recevoir une notification après que le pilote a rempli le tampon d’ombre. L’ACM transmet ensuite les tampons au pilote pour la compression. Une fois la compression terminée, le pilote transmet les données à l’application.

 

 





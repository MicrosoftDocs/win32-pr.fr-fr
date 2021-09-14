---
title: Traitement des données audio
description: Traitement des données audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- plug-ins Lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, données audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013249"
---
# <a name="processing-the-audio-data"></a>Traitement des données audio

L’implémentation par défaut de **DoProcessOutput** commence par la récupération d’un pointeur vers une structure **WAVEFORMATEX** valide, exactement comme cela a été fait dans **AllocateStreamingResources**. Il utilise ensuite les informations de cette structure pour calculer le nombre d’échantillons dans la mémoire tampon d’entrée en attente de traitement. Le code suivant provient de l’implémentation par défaut :


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Ensuite, le code inspecte le membre **wBitsPerSample** pour déterminer la profondeur de bits de l’audio. Cette valeur est utilisée dans une instruction switch pour fournir un traitement distinct pour les données audio 8 bits et 16 bits.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Différences entre les données audio 8 bits et 16 bits

Il existe des différences importantes entre les fichiers audio 8 bits et 16 bits. Par conséquent, les routines de traitement pour créer l’effet ECHO sont différentes. Les deux formats diffèrent des façons suivantes :

-   Chaque format a une taille d’échantillonnage différente : les échantillons 8 bits occupent chacun un octet de mémoire, tandis que les échantillons 16 bits occupent chacun deux octets.
-   Chaque format représente l’amplitude audio différemment. l’audio 8 bits est représenté par un entier non signé avec une plage comprise entre 0 et 255 ; la valeur 128 représente un silence. les données audio 16 bits sont représentées par un entier signé compris entre-32768 et 32767. la valeur zéro représente un silence.

Alors que le processus de création de l’effet ECHO est fondamentalement identique pour chaque format, les détails doivent différer légèrement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CEcho ::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





---
description: Définition des propriétés de capture audio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Définition des propriétés de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078809"
---
# <a name="setting-audio-capture-properties"></a>Définition des propriétés de capture audio

Chaque broche d’entrée sur le filtre de capture audio expose l’interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) . Utilisez cette interface pour activer ou désactiver une entrée particulière, en appelant la méthode [**IAMAudioInputMixer ::p ut \_ Enable**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) sur le code confidentiel. Utilisez également cette interface pour définir les propriétés d’une entrée, telles que les basses, les aigus et les niveaux de volume. Si vous capturez plusieurs entrées à la fois, vous pouvez contrôler les basses, les aigus et les niveaux de volume globaux via l’interface **IAMAudioInputMixer** sur le filtre lui-même.

Les taux d’échantillonnage et les formats audio disponibles pour la capture sont déterminés par le pilote. Utilisez l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sur la broche de sortie du filtre de capture audio pour énumérer les taux d’échantillonnage et les formats disponibles et définir le format souhaité. Le filtre peut se connecter en aval à n’importe quel filtre qui accepte le type de média de la broche de sortie.

Le filtre de capture audio expose également l’interface [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) . Cette interface est utile pour contrôler la quantité de latence dans la version préliminaire audio. Par défaut, le filtre de capture audio utilise une taille de mémoire tampon de demi-seconde. Cette taille de mémoire tampon est optimale pour la capture, mais entraîne un délai d’aperçu de demi-seconde. Pour réduire la latence, appelez la méthode [**IAMBufferNegotiation :: SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) avant de connecter la broche de sortie du filtre de capture audio. Cette méthode prend un pointeur vers la structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) . Utilisez le membre **cbBuffer** pour spécifier la taille de la mémoire tampon, en octets. Une mémoire tampon de 80 millisecondes est généralement sûre, mais les tampons de 30 ou 40 millisecondes peuvent être suffisants. Si les tampons sont trop petits, la qualité du son est détériorée.

 

 




---
description: Fonctionnalités audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Fonctionnalités audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112177"
---
# <a name="audio-capabilities"></a>Fonctionnalités audio

Pour les fonctionnalités audio, [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retourne un tableau de paires de structures de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) et d' [**\_ \_ \_ embouts de configuration de flux audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) . Comme avec la vidéo, vous pouvez l’utiliser pour exposer toutes sortes de fonctionnalités audio sur le code confidentiel, telles que le débit de données et la prise en charge de mono ou stéréo.

Pour obtenir des exemples relatifs à la vidéo relatifs à GetStreamCaps, consultez [Video Capabilities](video-capabilities.md).

Supposons que vous prenez en charge le format Wave PCM (Pulse Code Modulation) (tel que représenté par la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ) aux taux d’échantillonnage de 11 025, 22 050 et 44 100 échantillons par seconde, tous à 8 ou 16 bits mono ou stéréo. Dans ce cas, vous pouvez proposer deux paires de structures. La première paire aurait une structure de capacité de **\_ configuration de flux \_ \_ audio** , indiquant que vous pouvez prendre en charge un minimum de 11 025 à 22 050 par seconde avec une granularité de 11 025 échantillons par seconde (la granularité est la différence entre les valeurs prises en charge); un minimum de 8 bits à un nombre maximal de bits de 16 bits par échantillon, avec une granularité de 8 bits par échantillon et une valeur minimale de 1 canal et un maximum de deux canaux. Le type de média de la première paire correspond à votre format PCM par défaut dans cette plage, peut-être 22 kilohertz (kHz), stéréo 16 bits. Votre deuxième paire est une fonctionnalité qui indique 44 100 pour les échantillons minimaux et maximaux par seconde. 8 bits (minimum) et 16 bits (maximum) bits par échantillon, avec une granularité de 8 bits par échantillon ; et les valeurs minimale et maximale à un canal. Le type de média est le format 44 kHz par défaut, peut-être une stéréo de 44 kHz 16 bits.

Si vous prenez en charge des formats wave non-PCM, le type de média renvoyé par cette méthode peut indiquer les formats non-PCM que vous prenez en charge (avec un taux d’échantillonnage, une vitesse de transmission et des canaux par défaut) et la structure des fonctionnalités accompagnant ce type de média peut décrire les autres taux d’échantillonnage, les vitesses de transmission et les canaux pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exposition des formats de capture et de compression](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 

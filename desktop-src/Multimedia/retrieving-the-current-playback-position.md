---
title: Récupération de la position de lecture actuelle
description: Récupération de la position de lecture actuelle
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio de forme d’onde, position de lecture actuelle
- Waveform-interface audio, position de lecture actuelle
- lecture des fichiers Waveform-Audio, position de lecture actuelle
- waveOutGetPosition fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314675"
---
# <a name="retrieving-the-current-playback-position"></a>Récupération de la position de lecture actuelle

Vous pouvez surveiller la position de lecture actuelle dans le fichier lors de la lecture de l’audio Wave à l’aide de la fonction [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .

Pour les périphériques audio Waveform, les exemples sont le format d’heure par défaut dans lequel représenter la position actuelle. Ainsi, la position actuelle d’un périphérique audio Waveform est spécifiée comme le nombre d’échantillons pour un canal à partir du début du fichier Waveform-Audio. Pour interroger la position actuelle d’un périphérique audio Waveform, définissez le membre **wType** de la structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) sur des échantillons de temps \_ et transmettez cette structure à **waveOutGetPosition**.

La structure **MMTIME** peut représenter le temps dans un ou plusieurs formats différents, y compris les millisecondes, les échantillons, les ingénieurs de la société de motion et les formats de pointeur de chanson midi. Le membre **wType** spécifie le format utilisé pour représenter l’heure. Avant d’appeler une fonction qui utilise la structure **MMTIME** , vous devez définir **wType** pour indiquer le format d’heure demandé. Veillez à vérifier **wType** après l’appel pour voir si le format d’heure demandé est pris en charge. Si le format d’heure demandé n’est pas pris en charge, le pilote de périphérique spécifie l’heure dans un autre format d’heure et remplace le membre **wType** par le format d’heure sélectionné.

Pour plus d’informations sur la structure **MMTIME** , consultez [minuteries multimédias](multimedia-timers.md).

 

 
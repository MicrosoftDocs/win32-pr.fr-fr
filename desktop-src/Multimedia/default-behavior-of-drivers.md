---
title: Comportement par défaut des pilotes
description: Comportement par défaut des pilotes
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144522"
---
# <a name="default-behavior-of-drivers"></a>Comportement par défaut des pilotes

Dans de nombreux cas, les spécifications de commande MCI définissent les valeurs et le comportement par défaut des pilotes d’un type d’appareil particulier. Étant donné que les périphériques multimédias peuvent avoir un large éventail de fonctionnalités (et limitations), il peut y avoir des zones de comportement non définies. En outre, les pilotes peuvent gérer les exceptions différemment, en fonction des fonctionnalités de l’appareil.

Par exemple, considérez les commandes suivantes envoyées à un pilote Wave-audio à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



La commande d' [**enregistrement**](record.md) renvoie une valeur « paramètre hors limites » et arrête la lecture démarrée par la commande de [**lecture**](play.md) précédente. On peut s’attendre à ce que le pilote valide la commande d’enregistrement avant d’arrêter la lecture, mais le pilote arrête d’abord la lecture.

 

 
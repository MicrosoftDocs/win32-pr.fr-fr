---
title: L’indicateur d’attente
description: L’indicateur d’attente
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Indicateur de MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368087"
---
# <a name="the-wait-flag"></a>L’indicateur d’attente

Les commandes MCI sont généralement renvoyées immédiatement à l’utilisateur, même s’il faut quelques minutes pour effectuer l’action initiée par la commande. Vous pouvez utiliser l' \_ indicateur d’attente MCI pour indiquer à l’appareil d’attendre que l’action demandée soit terminée avant de retourner le contrôle à l’application.

Par exemple, la commande [**Play**](play.md) suivante ne retourne pas de contrôle à l’application tant que la lecture n’est pas terminée :


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> L’utilisateur peut annuler une opération d’attente en appuyant sur une touche d’arrêt. Par défaut, cette clé est CTRL + ATTN. Les applications peuvent redéfinir cette clé à l’aide de la commande [**break**](break.md) ([**\_ Pause MCI**](mci-break.md)). (**L' \_ interruption MCI** utilise la structure de l' [**\_ interruption \_ MCI**](mci-break-parms.md) .) Quand une opération d’attente est annulée, MCI tente de retourner le contrôle à l’application sans interrompre la commande associée à l’indicateur « WAIT ».

 

 

 





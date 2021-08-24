---
title: Communication avec les périphériques MCI
description: Communication avec les périphériques MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString macro)
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3def53cda9374ba50dfea8252918f073d961410092a977c8779f3a29d6b36204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807839"
---
# <a name="communicating-with-mci-devices"></a>Communication avec les périphériques MCI

Le pilote de chaque périphérique MCI gère une liste de ses paramètres et capacités actuels. il peut donc émettre une réponse exacte lorsqu’il est interrogé pour obtenir des informations.

Lorsque vous souhaitez communiquer avec un périphérique MCI, vous pouvez utiliser des macros et des fonctions MCIWnd. La plupart des commandes et requêtes MCI les plus courantes sont définies en tant que macros. Toutefois, si la tâche que vous voulez effectuer n’est pas disponible en tant que fonction ou macro, vous pouvez envoyer des commandes MCI directement au pilote de périphérique à l’aide de la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) ou en utilisant la forme message ou chaîne des commandes MCI. L’utilisation de la macro **MCIWndSendString** revient à utiliser la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) comme suit :


```C++
mciSendString(sz, Null, 0, Null) 
```



Les paramètres de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) incluent uniquement le handle de fenêtre et la forme de chaîne de la commande. Pour récupérer les informations retournées par une commande de chaîne, utilisez la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .

Pour plus d’informations sur MCI, consultez [MCI](mci.md).

> [!Note]  
> Vous devez exclure l’alias d’appareil de la commande MCI quand vous utilisez **MCIWndSendString**. La bibliothèque MCIWnd ajoute cet alias lors de l’envoi de la commande à l’appareil MCI.

 

 

 
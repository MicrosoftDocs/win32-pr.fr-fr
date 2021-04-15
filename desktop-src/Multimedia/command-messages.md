---
title: Messages de commande
description: Messages de commande
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Messages de commande MCI, à propos de
- Messages de commande MCI, syntaxe
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507866"
---
# <a name="command-messages"></a>Messages de commande

L’interface de message de commande est conçue pour être utilisée par les applications qui requièrent une interface en langage C pour contrôler les appareils multimédias. Il utilise un paradigme de transmission de messages pour communiquer avec les périphériques MCI. Vous pouvez envoyer une commande à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

La fonction **mciSendCommand** retourne la valeur zéro en cas de réussite. Si la fonction échoue, le mot de poids faible de la valeur de retour contient un code d’erreur. Vous pouvez transmettre ce code d’erreur à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.

## <a name="syntax-of-command-messages"></a>Syntaxe des messages de commande

Les messages de commande MCI sont constitués des éléments suivants :

-   Valeur de message constante
-   Structure contenant les paramètres de la commande
-   Ensemble d’indicateurs spécifiant des options pour la commande et des champs de validation dans le bloc de paramètres

L’exemple suivant utilise la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour envoyer la commande de [**\_ lecture MCI**](mci-play.md) à l’appareil identifié par un identificateur d’appareil.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



L’identificateur d’appareil indiqué dans le premier paramètre est récupéré lorsque l’appareil est ouvert à l’aide de la commande [**MCI \_ Open**](mci-open.md) . Le dernier paramètre est l’adresse d’une structure de [**\_ lecture MCI \_**](mci-play-parms.md) , qui peut contenir des informations sur le début et la fin de la lecture. De nombreux messages de commande MCI utilisent une structure pour contenir des paramètres de ce genre. Le premier membre de chacune de ces structures identifie la fenêtre qui reçoit un [**message \_ MCINOTIFY mm**](mm-mcinotify.md) lorsque l’opération se termine.

 

 
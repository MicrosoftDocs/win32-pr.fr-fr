---
title: IAgentCharacterEx écouter
description: IAgentCharacterEx écouter
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee221de03fe0a0e908e1fc3c10f05d48c26dd9fd264edd20ee2e4d78d73fb91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105497"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx :: Listen

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Active ou désactive le mode d’écoute (entrée de reconnaissance vocale).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Indicateur du mode d’écoute. Si ce paramètre a la **valeur true**, le mode d’écoute est activé ; Si la **valeur est false**, le mode d’écoute est désactivé.

</dd> </dl>

L’affectation de la **valeur true** à cette méthode active le mode d’écoute (active la reconnaissance vocale) pendant une période de temps fixe. Bien que vous ne puissiez pas définir la valeur du délai d’attente, vous pouvez désactiver le mode d’écoute avant l’expiration du délai d’attente. En outre, si le mode d’écoute est déjà activé parce que vous (ou un autre client) avez correctement défini la méthode sur **true** avant l’expiration du délai d’attente, la méthode réussit et réinitialise le délai d’attente. Toutefois, si le mode d’écoute est déjà activé parce que l’utilisateur appuie sur la touche d’écoute, la méthode aboutit, mais le délai d’attente est ignoré et le mode d’écoute se termine en fonction de l’interaction de l’utilisateur avec la clé d’écoute.

Cette méthode ne fonctionnera que lorsqu’elle est appelée par le client d’entrée-actif. Par conséquent, la méthode échoue si votre client n’est pas le client actif du premier caractère. La méthode échouera également si vous tentez de définir la méthode sur **false** et que l’utilisateur appuie sur la touche d’écoute. Elle peut également échouer si aucun moteur vocal compatible ne correspond au paramètre ID de langue du caractère ou si l’utilisateur a désactivé l’entrée vocale à l’aide de la feuille de propriétés de l’agent Microsoft. Toutefois, la méthode n’échouera pas si le périphérique audio est occupé.

Lorsque vous avez correctement défini cette méthode sur **true**, le serveur déclenche l’événement [**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md) . Le serveur envoie également **IAgentNotifySinkEx :: ListeningState** lorsque le délai d’attente du mode d’écoute est terminé ou lorsque vous définissez [**IAgentCharacterEx :: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) sur **false**.

Cette méthode n’appelle pas automatiquement [**IAgentCharacter :: stopAll**](iagentcharacter--stopall.md) et joue une animation d’état d’écoute du caractère tel qu’il se produit lorsque l’utilisateur appuie sur la touche d’écoute. Cela vous permet d’utiliser l’événement [**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md) pour déterminer si vous souhaitez arrêter l’animation actuelle et lire votre propre animation appropriée. Toutefois, une fois qu’un énoncé utilisateur est détecté, le serveur appelle automatiquement **IAgentCharacter :: stopAll** et émet une animation d’État auditif.

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 





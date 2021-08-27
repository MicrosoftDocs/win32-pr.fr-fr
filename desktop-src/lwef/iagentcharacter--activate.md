---
title: IAgentCharacter activer
description: IAgentCharacter activer
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7256b1d155b051985c72120283e60896026218ea81d8b2b9c37dc94fb52bb63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750995"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter :: Activate

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Définit si un client est actif ou si un caractère est le plus haut.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.
-   Retourne S \_ false pour indiquer que l’opération a échoué.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Vous pouvez spécifier les valeurs suivantes pour ce paramètre :



| Valeur | Description                   |
|-------|-------------------------------|
| 0     | Défini comme n’étant pas le client actif. |
| 1     | Défini en tant que client actif.     |
| 2     | Créez le premier caractère.   |



 

</dd> </dl>

Lorsque plusieurs caractères sont visibles, un seul des caractères reçoit les entrées vocales à la fois. De même, lorsque plusieurs applications clientes partagent le même caractère, un seul des clients reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent) à la fois. Le jeu de caractères pour recevoir l’entrée de la souris et de la parole est le caractère le plus élevé et le client qui reçoit l’entrée est le client actif du caractère. (La fenêtre du caractère supérieur s’affiche également en haut de l’ordre de plan de la fenêtre de caractères.) En règle générale, l’utilisateur détermine le caractère le plus élevé en le sélectionnant explicitement. Toutefois, l’activation de niveau supérieur change également lorsqu’un caractère est affiché ou masqué (le caractère devient ou n’est plus le premier niveau, respectivement).

Vous pouvez également utiliser cette méthode pour gérer explicitement quand votre client reçoit une entrée dirigée vers le caractère, par exemple quand votre application est elle-même active. Par exemple, la définition de l' **État** sur 2 rend le caractère le plus haut, et votre client reçoit tous les événements d’entrée de la souris et de la parole générés par l’interaction de l’utilisateur avec le caractère. Par conséquent, il rend également votre client le client d’entrée-actif du caractère. Toutefois, vous pouvez également définir le client actif pour un caractère sans rendre le caractère le plus haut, en définissant l' **État** sur 1. Cela permet à votre client de recevoir l’entrée dirigée vers ce caractère lorsque le caractère devient le plus haut. De même, vous pouvez configurer votre client pour qu’il ne soit pas le client actif (pour ne pas recevoir d’entrée) lorsque le caractère est le plus haut, en définissant l' **État** sur 0. Vous pouvez déterminer si un caractère a d’autres clients actuels à l’aide de [**IAgentCharacter :: HasOtherClients**](iagentcharacter--hasotherclients.md).

Évitez d’appeler cette méthode directement après une méthode [**Show**](iagentcharacter--show.md) . **Afficher** définit automatiquement le client d’entrée-actif. Lorsque le caractère est masqué, l’appel d' **activation** peut échouer s’il est traité avant la fin de la méthode **Show** .

Toute tentative d’appel à cette méthode avec le paramètre d' **État** défini sur 2 (lorsque le caractère spécifié est masqué) échoue. De même, si vous affectez à l' **État** la valeur 0 et que votre application est le seul client, cet appel échoue. Un caractère doit toujours avoir un client de niveau supérieur.

> [!Note]  
> L’appel de cette méthode avec un **État** défini sur 1 ne génère généralement pas d’événement [**AgentNotifySink :: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) , sauf si aucun autre caractère n’est chargé ou si votre application est déjà en entrée-active.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 





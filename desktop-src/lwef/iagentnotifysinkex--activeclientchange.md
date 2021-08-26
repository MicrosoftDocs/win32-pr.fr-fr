---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961499"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Avertit une application cliente si son client actif n’est plus le client actif d’un caractère.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère pour lequel l’état du client actif a été modifié.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Changement d’état actif du client, qui peut être une combinaison de l’une des valeurs suivantes :



| Valeur                                                              | Description                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const non signed Short** **ACTIVATe \_ notactive = 0 ;**<br/>   | Votre client n’est pas le client actif du caractère.                |
| **const non signé Short** **Activate \_ active = 1 ;**<br/>      | Votre client est le client actif du caractère.                    |
| **const non signed Short** **Activate \_ INPUTACTIVE = 2 ;**<br/> | Votre client est en entrée-actif (client actif du premier caractère). |



 

</dd> </dl>

Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent). De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

Lorsque le client actif d’un caractère change, cet événement transmet l’ID de ce caractère et la **valeur true** si votre application est devenue le client actif du caractère ou **false** si elle n’est plus le client actif du caractère.

Une application cliente peut recevoir cet événement lorsque l’utilisateur sélectionne une autre entrée de l’application cliente dans le menu contextuel du caractère ou à l’aide de la commande vocale, que l’application cliente modifie son état actif ou qu’une autre application cliente quitte sa connexion à Microsoft Agent. Agent envoie cet événement uniquement aux applications clientes directement affectées, c’est-à-dire celles qui deviennent le client actif ou qui cessent d’être le client actif.

Vous pouvez utiliser la méthode [**Activate**](iagentcharacter--activate.md) pour définir si votre application est le client actif du caractère ou pour faire de votre application le client d’entrée-actif (qui rend également le caractère le plus haut).

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx :: GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 






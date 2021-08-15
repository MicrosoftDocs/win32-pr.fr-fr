---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f9cb05143d4948fbcae1f8d9ed74a7216c5a2520b28f4c299321bcbac4272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478026"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Récupère les valeur indiquant si votre application cliente est le client actif du caractère et si le caractère est le plus haut.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Adresse d’une variable qui reçoit l’une des valeurs suivantes pour le paramètre d’État :



| Valeur                                                              | Description                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const non signed Short** **ACTIVATe \_ notactive = 0 ;**<br/>   | Votre client n’est pas le client actif du caractère.                |
| **const non signé Short** **Activate \_ active = 1 ;**<br/>      | Votre client est le client actif du caractère.                    |
| **const non signed Short** **Activate \_ INPUTACTIVE = 2 ;**<br/> | Votre client est en entrée-actif (client actif du premier caractère). |



 

</dd> </dl>

Ce paramètre vous permet de savoir si vous êtes le client actif du caractère ou si votre caractère est le caractère actif d’entrée. Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent). De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

Utilisez la méthode [**Activate**](iagentcharacter--activate.md) pour définir si votre application est le client actif du personnage ou pour faire de votre application le client actif d’entrée (ce qui rend également le premier caractère).

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx :: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 






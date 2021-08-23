---
title: IAgentCommand SetCaption
description: IAgentCommand SetCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976359"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand::SetCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Définit le texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR qui spécifie le texte de la propriété [**Caption**](caption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

La définition de la propriété [**Caption**](caption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) définit son mode d’affichage dans le menu contextuel du caractère lorsque sa propriété [**visible**](visible-property.md) a la valeur **true** et que votre application n’est pas le client d’entrée-actif. Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère. Pour qu’elle soit sélectionnable, sa propriété [**Enabled**](enabled-property.md) doit avoir la valeur **true**.

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 
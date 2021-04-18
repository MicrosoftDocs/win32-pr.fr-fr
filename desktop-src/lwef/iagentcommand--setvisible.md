---
title: IAgentCommand SetVisible
description: IAgentCommand SetVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512311"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand :: SetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Définit la valeur de la propriété [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valeur booléenne qui détermine la propriété [**visible**](visible-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object). **True** affiche la **commande**; **False** le masque.

</dd> </dl>

La propriété [**visible**](visible-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object) doit être définie sur **true** et sa propriété [**Caption**](caption-property.md) définie sur s’afficher dans le menu contextuel du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: getVisible**](iagentcommand--getvisible.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 
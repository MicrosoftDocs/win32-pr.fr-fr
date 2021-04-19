---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511484"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands :: SetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Définit la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valeur booléenne qui détermine la propriété [**visible**](visible-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . **True** définit la [**légende**](caption-property.md) de la collection **Commands** pour qu’elle soit visible lorsque le menu contextuel du caractère s’affiche ; *False* ne l’affiche pas.

</dd> </dl>

Une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) doit avoir sa propriété [**Caption**](caption-property.md) définie et sa propriété [**visible**](visible-property.md) définie sur **true** pour apparaître dans le menu contextuel du caractère. La propriété **visible** doit également avoir la valeur **true** pour que les commandes de la collection s’affichent lorsque votre application cliente est active en entrée.

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: getVisible**](iagentcommands--getvisible.md), [ **IAgentCommand :: SetCaption**](iagentcommand--setcaption.md)


 

 
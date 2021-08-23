---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665469"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Définit le texte de [**légende**](caption-property.md) affiché pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR qui spécifie la valeur de la propriété [**Caption**](caption-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

La définition de la propriété [**Caption**](caption-property.md) pour une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) définit son mode d’affichage dans le menu contextuel du caractère lorsque sa propriété [**visible**](visible-property.md) a la valeur **true** et que votre application n’est pas le client d’entrée-actif. Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.

Si vous définissez des commandes pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) dont la [**légende**](caption-property.md) est définie, vous définissez généralement une **légende** pour la collection **Commands** .

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands :: setVisible**](iagentcommands--setvisible.md), [**IAgentCommands :: SetVoice**](iagentcommands--setvoice.md)


 

 
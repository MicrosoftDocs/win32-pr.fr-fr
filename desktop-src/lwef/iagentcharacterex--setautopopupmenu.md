---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477957"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Définit si le serveur affiche automatiquement le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

Indicateur d’affichage automatique du menu contextuel. Si ce paramètre est défini sur **true**, Microsoft Agent affiche automatiquement le menu contextuel du caractère lorsque l’utilisateur clique avec le bouton droit sur l’icône de barre des tâches caractère ou caractère.

</dd> </dl>

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

En affectant à cette propriété la **valeur false**, vous pouvez créer votre propre comportement de gestion de menus. Pour afficher le menu après avoir défini cette propriété sur **false**, utilisez la méthode [**IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 





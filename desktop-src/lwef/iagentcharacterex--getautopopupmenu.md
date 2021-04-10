---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940166"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>IAgentCharacterEx::GetAutoPopupMenu

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

Récupère si le serveur affiche automatiquement le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si le serveur Microsoft Agent gère automatiquement l’affichage du menu contextuel du caractère et la **valeur false** dans le cas contraire.

</dd> </dl>

Quand cette propriété a la valeur **false**, votre application doit afficher le menu contextuel à l’aide de la méthode [**IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [ **IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 





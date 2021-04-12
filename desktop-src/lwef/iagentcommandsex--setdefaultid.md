---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381858"
---
# <a name="iagentcommandsexsetdefaultid"></a>IAgentCommandsEx::SetDefaultID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Définit l’ID de la commande par défaut dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

ID de la [**commande**](/windows/desktop/lwef/the-command-object) à définir comme valeur par défaut.

</dd> </dl>

Cette propriété définit le jeu d’objets de [**commande**](/windows/desktop/lwef/the-command-object) par défaut dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . La commande par défaut est en gras dans le menu contextuel du caractère. Toutefois, la définition de la commande par défaut ne modifie pas réellement les événements de gestion des commandes ou de double-clic.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::GetDefaultID**](iagentcommandsex--getdefaultid.md)


 

 
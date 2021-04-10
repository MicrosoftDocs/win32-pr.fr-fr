---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197284"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Récupère une valeur indiquant si le mode d’aide contextuelle est activé pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Adresse d’une variable qui reçoit **true** si le mode d’aide est activé pour le caractère et **false** dans le cas contraire.

</dd> </dl>

Lorsque cette propriété est définie sur **true**, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère. Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**IAgentNotifySinkEx :: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) et quitte le mode d’aide.

En mode d’aide, le serveur n’envoie pas les événements [**IAgentNotifySink :: Click**](iagentnotifysink--click.md), [**IAgentNotifySink ::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink ::D Ragcomplete**](iagentnotifysink--dragcomplete.md)et [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) , sauf si la propriété [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) retourne la **valeur true**. Dans ce cas, le serveur enverra l’événement **IAgentNotifySink :: Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris pour vous permettre d’afficher le menu contextuel.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 





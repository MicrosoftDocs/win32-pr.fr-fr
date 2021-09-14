---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012372"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Définit le mode d’aide contextuelle pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Indicateur du mode d’aide. Si ce paramètre a la **valeur true**, Microsoft Agent active le mode d’aide pour le caractère.

</dd> </dl>

Lorsque vous affectez la valeur **true** à cette propriété, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère. Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**IAgentNotifySinkEx :: HelpComplete**](iagentnotifysinkex--helpcomplete.md) et quitte le mode d’aide.

Dans le mode d’aide, le serveur n’envoie pas les événements [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)et [**Command**](command-event.md) , sauf si la propriété [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) retourne la **valeur true**. Dans ce cas, le serveur enverra l’événement **Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris afin que vous puissiez afficher le menu contextuel.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx :: HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 
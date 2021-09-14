---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292291"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx ::D efaultCharacterChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Avertit une application cliente lorsque le caractère par défaut change.

-   Pas de valeur de retour.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

Identificateur unique du caractère.

</dd> </dl>

Lorsque l’utilisateur modifie le caractère affecté comme caractère par défaut de l’utilisateur, le serveur envoie cet événement aux clients qui ont chargé le caractère par défaut. L’événement retourne l’identificateur unique (GUID) du caractère mis en forme à l’aide d’accolades et de tirets, qui est défini lorsque le caractère est généré avec l’éditeur de caractères Microsoft Agent.

Lorsque le nouveau caractère apparaît, il suppose la même taille que toute instance déjà chargée du caractère ou le caractère par défaut précédent (dans cet ordre).

## <a name="see-also"></a>Voir aussi

[**IAgent :: Load**](iagent--load.md)


 

 





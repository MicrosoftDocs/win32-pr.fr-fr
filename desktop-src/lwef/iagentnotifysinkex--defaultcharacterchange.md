---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aea2a310e55228f6e9f15ec14f9ed9ac6e20374f8c8ecb12e016d60f1809b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961469"
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


 

 





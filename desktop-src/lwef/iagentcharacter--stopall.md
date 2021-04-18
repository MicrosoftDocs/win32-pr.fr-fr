---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509611"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter :: StopAll

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Arrête toutes les animations (requêtes) et les supprime de la file d’attente d’animation du caractère.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Champ de type de code qui indique les types de demandes à arrêter (et à supprimer de la file d’attente du caractère), constitué des éléments suivants :



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const type d’arrêt long non signé** **\_ \_ = 0xFFFFFFFF ;**<br/>              | Arrête toutes les demandes d’animation, y compris les demandes de [**préparation**](iagentcharacter--prepare.md) non mises en file d’attente. |
| **const type d’arrêt long non signé** **\_ \_ lu = 0x00000001 ;**<br/>             | Arrête toutes les demandes de lecture.                                                                                 |
| **const type d’arrêt long non signé** **\_ \_ Move = 0x00000002 ;**<br/>             | Arrête toutes les demandes de [**déplacement**](https://www.bing.com/search?q=**Move**) .                                               |
| **const type d’arrêt long non signé** **\_ \_ Speak = 0x00000004 ;**<br/>            | Arrête toutes les demandes [**Speak**](iagentcharacter--speak.md) .                                              |
| **const unsigned long** **Stop \_ type \_ Prepare = 0x00000008 ;**<br/>          | Arrête toutes les demandes de [**préparation**](iagentcharacter--prepare.md) mises en file d’attente.                                   |
| **const, unsigned long** **Stop \_ \_ , type NONQUEUEDPREPARE = 0x00000010 ;**<br/> | Arrête toutes les demandes de [**préparation**](iagentcharacter--prepare.md) non mises en file d’attente.                               |
| type d’arrêt **long non signé const** **\_ \_ visible = 0x00000020 ;**<br/>          | Arrête toutes les demandes d' [**affichage**](iagentcharacter--show.md) ou de [**masquage**](iagentcharacter--hide.md) .       |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Stop**](iagentcharacter--stop.md)


 

 






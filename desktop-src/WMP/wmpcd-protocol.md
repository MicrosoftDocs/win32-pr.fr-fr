---
title: Protocole WMPCD
description: Protocole WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Lecteur Windows Media, protocoles
- Lecteur Windows Media modèle objet, protocoles
- modèle objet, protocoles
- Lecteur Windows Media ActiveX contrôle, protocoles pour le modèle objet
- contrôle ActiveX, protocoles pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, protocoles pour le modèle objet
- Lecteur Windows Media Mobile, protocoles pour le modèle objet
- protocoles, Lecteur Windows Media modèle objet
- protocoles, WMPCD
- Protocole WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b1359d22b792587f7cceeb46f0f9e621585dfba296422a227e9012077df7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900139"
---
# <a name="wmpcd-protocol"></a>Protocole WMPCD

Le protocole WMPCD vous permet de spécifier des pistes sur un disque compact à l’aide de la syntaxe d’URL. Il s’agit de la syntaxe générale du protocole :


```C++
wmpcd://drive/track
```



Le segment de *lecteur* est l’index du lecteur de CD. Le segment de *suivi* est le numéro de la piste. L’exemple suivant illustre l’utilisation du protocole WMPCD.


```C++
player.url = "wmpcd://0/4";
```



L’exemple lit la quatrième piste sur le disque dans le premier lecteur de CD (le lecteur dont l’index est 0).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Protocoles et types de fichiers pris en charge**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 





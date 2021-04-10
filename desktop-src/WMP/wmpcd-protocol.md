---
title: Protocole WMPCD
description: Protocole WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Lecteur Windows Media, protocoles
- Modèle d’objet du lecteur Windows Media, protocoles
- modèle objet, protocoles
- Contrôle ActiveX du lecteur Windows Media, protocoles pour le modèle objet
- Contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, protocoles pour le modèle objet
- Windows Media Player Mobile, protocoles pour le modèle objet
- protocoles, modèle objet du lecteur Windows Media
- protocoles, WMPCD
- Protocole WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196723"
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

 

 





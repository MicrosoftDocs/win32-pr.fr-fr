---
title: Protocole WMPDVD
description: Protocole WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Lecteur Windows Media, protocoles
- Lecteur Windows Media modèle objet, protocoles
- modèle objet, protocoles
- Lecteur Windows Media ActiveX contrôle, protocoles pour le modèle objet
- contrôle ActiveX, protocoles pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, protocoles pour le modèle objet
- Lecteur Windows Media Mobile, protocoles pour le modèle objet
- protocoles, Lecteur Windows Media modèle objet
- protocoles, WMPDVD
- Protocole WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530232"
---
# <a name="wmpdvd-protocol"></a>Protocole WMPDVD

Le protocole WMPDVD vous permet de spécifier un média à partir d’un DVD à l’aide de la syntaxe d’URL. Il s’agit de la forme générale du protocole :


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



Le segment de *lecteur* est la lettre du lecteur de DVD ; elle n’inclut pas les deux-points généralement utilisés avec les spécificateurs de lecteur. Ce segment est toujours requis.

Le segment de *titre* est le numéro du titre à lire. Ce n’est pas obligatoire, sauf si vous souhaitez commencer la lecture à un titre spécifique ou à un chapitre spécifique d’un titre spécifique.

Le segment de *chapitre* est le numéro du chapitre à lire. Ce n’est pas obligatoire, sauf si vous souhaitez démarrer la lecture dans un chapitre spécifique d’un titre spécifique.

L’argument contentdir est le chemin d’accès à une vidéo \_ TS. Fichier IFO, qui peut être dans un stockage local ou sur un partage réseau. Si vous incluez ce segment, le segment de *lecteur* est ignoré, même s’il est toujours requis. Si vous incluez également le segment de *titre* ou les segments de *titre* et de *chapitre* , ils sont relatifs au contenu de DVD spécifié dans le segment contentdir, et non au segment de *disque* .

L’exemple suivant utilise le protocole WMPDVD pour lire le DVD depuis le début, comme s’il démarrait automatiquement.


```C++
player.url = "wmpdvd://F";
```



L’exemple suivant utilise le protocole WMPDVD pour lire le DVD à partir du début du titre spécifié.


```C++
player.url = "wmpdvd://F/2";
```



L’exemple suivant utilise le protocole WMPDVD pour lire le DVD à partir du chapitre spécifié.


```C++
player.url = "wmpdvd://F/2/4";
```



L’exemple suivant utilise le protocole WMPDVD pour lire du contenu DVD à partir du stockage local. La chaîne de *chemin d’accès* se termine par le dossier qui contient la vidéo \_ TS. Fichier IFO ; elle n’inclut pas le nom de fichier. Dans cet exemple, la valeur du segment de *lecteur* n’a aucun effet, bien qu’elle soit requise, et la lecture commence au chapitre 4 du titre 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



l’attribution d’une chaîne WMPDVD à la propriété **url** requiert Lecteur Windows Media série 9 ou une version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Protocoles et types de fichiers pris en charge**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 





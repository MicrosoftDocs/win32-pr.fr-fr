---
title: Reference, élément (déconseillé)
description: Reference, élément (déconseillé)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Fichiers Windows Media, élément Reference
- fichiers de rapport, élément de référence
- Reference, élément
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512056"
---
# <a name="reference-element-deprecated"></a>Reference, élément (déconseillé)

Cette rubrique documente une fonctionnalité qui n’est plus utilisée dans la version actuelle des fichiers Windows Media.

L’élément **Reference** contient une liste de références aux URL. Chaque élément de la liste a le formulaire Ref *XX*  =  *URL*, où *XX* est un entier et *URL* est l’URL d’un fichier ASF (Advanced Systems Format).

**Syntaxe**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



Les entiers représentés par *XX* doivent être dans l’ordre croissant. Autrement dit, l’entier de chaque ligne doit être supérieur à l’entier de la ligne précédente.

Lorsqu’un programme client lit un élément de référence, il tente de se connecter au fichier multimédia représenté par la première URL de la liste. En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL suivante dans la liste. Le programme client continue la liste jusqu’à ce qu’il établisse une connexion réussie ou qu’il atteigne la fin de la liste. Notez que si le programme client effectue une connexion réussie, il ne lit aucune des URL suivantes dans la liste.

**Exemple de code**

Dans l’exemple suivant, le programme client tente d’abord de se connecter au fichier représenté par l’URL MMS. En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL http.


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>Notes

Le format de fichier ASF englobe un large éventail de types de médias, tels que l’audio et la vidéo. Les fichiers ASF utilisent également plusieurs extensions de nom de fichier différentes, y compris. WMA et. wmv.

Les entiers représentés par *XX* doivent être dans l’ordre croissant. Autrement dit, l’entier de chaque ligne doit être supérieur à l’entier de la ligne précédente.

Lorsqu’un programme client lit un élément de référence, il tente de se connecter au fichier multimédia représenté par la première URL de la liste. En cas d’échec, le programme client tente de se connecter au fichier représenté par l’URL suivante dans la liste. Le programme client continue la liste jusqu’à ce qu’il établisse une connexion réussie ou qu’il atteigne la fin de la liste. Notez que si le programme client effectue une connexion réussie, il ne lit aucune des URL suivantes dans la liste.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Versions précédentes des fichiers Windows Media (déconseillés)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 





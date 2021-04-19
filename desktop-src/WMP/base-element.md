---
title: Élément de BASE
description: L’élément BASE définit une chaîne d’URL ajoutée au début des URL envoyées au lecteur Windows Media.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Élément de BASE lecteur Windows Media
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529944"
---
# <a name="base-element"></a>Élément de BASE

L’élément **base** définit une chaîne d’URL ajoutée au début des URL envoyées au lecteur Windows Media.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

Chaîne ajoutée au début des URL envoyées au lecteur Windows Media. La valeur par défaut est la chaîne null ("").

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

Cet élément définit une chaîne d’URL ajoutée au début des URL-Flip URL envoyées au lecteur Windows Media. Le basculement d’URL est un mécanisme de script qui amène le lecteur Windows Media à ouvrir une nouvelle URL dans un navigateur ou un cadre de navigateur lorsqu’il reçoit une commande de script.

L’élément de **base** est similaire à un répertoire de base pour les liens relatifs. Il affecte uniquement les URL envoyées à l’aide de commandes de script dans le cadre du flux de contenu qui est lu dans le lecteur Windows Media.

Un élément de **base** défini en tant qu’enfant d’un élément **ASX** devient la valeur par défaut pour l’ensemble du métafichier. Un élément de **base** défini dans un élément d' **entrée** remplace tout élément de **base** dans l’élément **ASX** parent (pour cet élément d' **entrée** uniquement).

> [!Note]  
> Si l’attribut **href** ne se termine pas par un caractère/, le lecteur Windows Media ajoute l’un à la fin de la chaîne.

 

## <a name="examples"></a>Exemples


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






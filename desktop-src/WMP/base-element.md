---
title: Élément de BASE
description: l’élément BASE définit une chaîne d’url ajoutée au début des url envoyées à Lecteur Windows Media.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Lecteur Windows Media de l’élément de BASE
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855891"
---
# <a name="base-element"></a>Élément de BASE

l’élément **BASE** définit une chaîne d’url ajoutée au début des url envoyées à Lecteur Windows Media.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

chaîne ajoutée au début des url envoyées à Lecteur Windows Media. La valeur par défaut est la chaîne null ("").

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Notes

cet élément définit une chaîne d’url ajoutée au début des url-flip url envoyées à Lecteur Windows Media. l’inversion d’url est un mécanisme de script qui amène Lecteur Windows Media à ouvrir une nouvelle URL dans un navigateur ou un cadre de navigateur lorsqu’il reçoit une commande de script.

L’élément de **base** est similaire à un répertoire de base pour les liens relatifs. il affecte uniquement les url envoyées à l’aide de commandes de script dans le cadre du flux de contenu qui est lu dans Lecteur Windows Media.

Un élément de **base** défini en tant qu’enfant d’un élément **ASX** devient la valeur par défaut pour l’ensemble du métafichier. Un élément de **base** défini dans un élément d' **entrée** remplace tout élément de **base** dans l’élément **ASX** parent (pour cet élément d' **entrée** uniquement).

> [!Note]  
> si l’attribut **HREF** ne se termine pas par un caractère/, Lecteur Windows Media en ajoute un à la fin de la chaîne.

 

## <a name="examples"></a>Exemples


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






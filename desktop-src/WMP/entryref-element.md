---
title: Élément ENTRYREF
description: L’élément ENTRYREF pointe vers les éléments d’entrée dans un métafichier externe.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- élément ENTRYREF Lecteur Windows Media
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193283"
---
# <a name="entryref-element"></a>Élément ENTRYREF

L’élément **ENTRYREF** pointe vers les éléments d' **entrée** dans un métafichier externe.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un métafichier référencé.

**CLIENTBIND**

Cet attribut n'est plus pris en charge.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                       |
|-----------------|--------------------------------|
| Éléments parents | **ASX**, **événement**, **répéter** |
| Éléments enfants  | None                           |



 

## <a name="remarks"></a>Notes

Cet élément pointe vers le contenu d’un métafichier externe. Lecteur Windows Media traite les éléments d' **entrée** du métafichier référencé comme s’ils étaient inclus dans le métafichier principal à la position de l’élément **ENTRYREF** . Toutefois, elle ignore tous les éléments d' **entrée** dans le métafichier référencé dont l’attribut **SKIPIFREF** a la valeur Yes.

Lecteur Windows Media 7,0, 7,1 et Lecteur Windows Media pour Windows XP ignorent tous les éléments **ENTRYREF** dans le métafichier référencé. Par conséquent, les fichiers de conversions peuvent être imbriqués un niveau de profondeur uniquement lors de l’utilisation de ces versions du lecteur. Lecteur Windows Media ignore également l’élément **ASX** dans le fichier référencé avec ses attributs. Lecteur Windows Media série 9 ou version ultérieure prend en charge l’imbrication de fichiers de conversions jusqu’à cinq niveaux.

L’URL spécifiée dans l’attribut **href** devient l’URL de base pour toutes les URL relatives dans le métafichier externe. Cette URL est utilisée lorsqu’une entrée du métafichier externe est lue et que l’utilisateur l’ajoute à la bibliothèque.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






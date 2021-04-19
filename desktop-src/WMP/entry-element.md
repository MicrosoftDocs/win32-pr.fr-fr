---
title: Élément ENTRy
description: L’élément ENTRy spécifie un fichier Windows Media à afficher sous forme de clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Élément d’entrée Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537686"
---
# <a name="entry-element"></a>Élément ENTRy

L’élément **entry** spécifie un fichier Windows Media à afficher sous forme de clip.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Attributs

**CLIENTSKIP**

Valeur indiquant si l’utilisateur peut avancer au-delà du clip.

Les valeurs possibles sont les suivantes.



| Valeur | Description                                   |
|-------|-----------------------------------------------|
| YES   | Par défaut. L’utilisateur peut avancer au-delà du clip. |
| Non    | L’utilisateur ne peut pas avancer au-delà du clip.       |



 

**SKIPIFREF**

Valeur indiquant si le lecteur Windows Media doit ignorer ce clip lorsque l’élément d' **entrée** est inclus dans un deuxième métafichier par le biais de l’utilisation d’un élément **ENTRYREF** .

Les valeurs possibles sont les suivantes.



| Valeur | Description                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | Le lecteur Windows Media ignore cette entrée, si elle est référencée par l’intermédiaire d’un élément **ENTRYREF** . |
| Non    | Par défaut. Le lecteur Windows Media n’ignore pas cette entrée.                                   |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents | **ASX**, **événement**, **répéter**                                                                                                                                                               |
| Éléments enfants  | **abstrait**, **auteur**, **bannière**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title** |



 

## <a name="remarks"></a>Notes

Cet élément est la construction fondamentale dans un métafichier Windows Media. L’élément **entry** et ses attributs associés définissent des méta-informations pour une seule pièce logique de contenu, appelée clip. Les éléments enfants dans la portée d’un élément d' **entrée** définissent le contenu multimédia pour que le lecteur Windows Media ouvre (**ref**), des informations sur le clip que le lecteur Windows Media affiche sous forme de texte (**auteur**, **Copyright**, **titre**) et d’autres paramètres liés au clip. L’élément enfant **ref** lie le contenu à diffuser en continu pour l’élément d' **entrée** parent. Bien que le script ne s’arrête pas, l' **entrée** n’a pas de sens sans un enfant **ref** .

Si la valeur de l’attribut **CLIENTSKIP** est non, l’utilisateur ne peut pas avancer au-delà de la partie de contenu définie par l’élément **entry** . Cela ne fonctionne pas si l’élément **ref** enfant fait référence à un autre métafichier. Les sous-fichiers imbriqués doivent être référencés à l’aide de l’élément **ENTRYREF** .

L’attribut **SKIPIFREF** se rapporte uniquement aux éléments d' **entrée** inclus dans un deuxième métafichier par le biais de l’utilisation d’un élément **ENTRYREF** . L’élément **ENTRYREF** référence un autre métafichier pour l’inclusion logique dans le fichier actuel. Si la valeur de l’attribut **SKIPIFREF** pour un élément d' **entrée** du fichier de métafichier référencé est oui, le lecteur Windows Media ignore cette entrée extraite et passe à l’élément d' **entrée** suivant, le cas échéant. L’élément d' **entrée** suivant peut être l’entrée suivante dans le fichier d’origine, ou l’entrée suivante dans le métafichier référencé dans l’élément **ENTRYREF** .

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






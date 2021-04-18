---
title: Commentaires (msfeeds. h)
description: Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML). Les commentaires commencent par \ 0034 ; --\ 0034 ; et se terminent par \ 0034 ;--\ 0034 ;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Commentaires sur le lecteur Windows Media
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529029"
---
# <a name="comments-msfeedsh"></a>Commentaires (msfeeds. h)

Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML). Les commentaires commencent par « &lt; !-- » et se terminent par « -- &gt; ».

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Notes

Les commentaires peuvent apparaître n’importe où, à l’exception du contenu de l’élément (entre les balises d’ouverture et de fermeture d’élément,  < >). Elles ne font pas partie des données caractères du document et sont ignorées lorsque le métafichier est analysé.

## <a name="examples"></a>Exemples


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 






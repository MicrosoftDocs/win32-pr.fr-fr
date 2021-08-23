---
title: Commentaires (msfeeds. h)
description: Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML). Les commentaires commencent par \ 0034 ; --\ 0034 ; et se terminent par \ 0034 ;--\ 0034 ;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- commentaires Lecteur Windows Media
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
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135782"
---
# <a name="comments-msfeedsh"></a>Commentaires (msfeeds. h)

Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML). Les commentaires commencent par « &lt; !-- » et se terminent par « -- &gt; ».

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Remarques

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 






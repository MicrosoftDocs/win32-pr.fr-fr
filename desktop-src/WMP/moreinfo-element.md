---
title: Élément MOREINFO
description: L’élément MOREINFO spécifie une URL vers un site Web, une adresse de messagerie ou une commande de script associée à un affichage, un clip ou une bannière.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- élément MOREINFO Lecteur Windows Media
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 925783b6bd48fbc8b944d7b8fd2a2b94a9954c7036114145b99b015b90cbb6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134952"
---
# <a name="moreinfo-element"></a>Élément MOREINFO

L’élément **moreinfo** spécifie une URL vers un site Web, une adresse de messagerie ou une commande de script associée à un affichage, un clip ou une bannière.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un site Web, d’une adresse de messagerie ou d’une commande de script.

**Indicatif**

Valeur définissant le frame ou la fenêtre dans laquelle le navigateur ouvre la page définie par l’attribut **href** .

Il peut s’agir d’une chaîne contenant un nom de fenêtre ou de l’une des valeurs suivantes.



| Valeur    | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_Occult  | Le document se charge dans une nouvelle fenêtre de navigateur.                                                                              |
| \_self   | le document se charge dans le même frame que le document actif contenant le contrôle Lecteur Windows Media.                |
| \_parent | Le document se charge dans le frame parent immédiat du frame actuel, ou le frame actuel s’il n’y a pas de frame parent. |
| \_top    | Le document se charge dans la fenêtre de navigateur complète, en remplaçant tous les autres frames ou documents.                                  |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                       |
|-----------------|--------------------------------|
| Éléments parents | **ASX**, **entrée**, **bannière** |
| Éléments enfants  | None                           |



 

## <a name="remarks"></a>Remarques

Cet élément spécifie une URL vers un site Web, une adresse de messagerie **ou une commande de script. L’utilisateur peut accéder à la cible de l’URL en cliquant sur le graphique ou le texte associé à l’élément MOREINFO** . Les détails dépendent de l’élément parent de l’élément **moreinfo** :

-   Si l’élément **moreinfo** est l’enfant d’un élément **ASX** , l’utilisateur peut accéder à l’URL en cliquant sur le titre afficher.
-   Si l’élément **moreinfo** est l’enfant d’un élément **entry** , l’utilisateur peut accéder à l’URL en cliquant sur le titre du clip.
-   Si l’élément **moreinfo** est l’enfant d’un élément **Banner** , l’utilisateur peut accéder à l’URL en cliquant sur le graphique de la bannière.

Si l’attribut **href** spécifie une URL vers un site Web, le navigateur s’ouvre et accède à l’URL. Si l’attribut **href** spécifie une adresse e-mail, l’application de messagerie de l’utilisateur démarre. Si l’attribut **href** spécifie une commande de script, la commande de script s’exécute dans le navigateur.

**Remarque**

si l’élément **MOREINFO** apparaît dans un élément **asx** ou un élément d' **entrée** , lorsque le curseur de la souris est maintenu sur le titre de l’élément d’affichage (pour un élément **asx** ) ou du clip (pour un élément d' **entrée** ), l’URL définie dans l’attribut **HREF** peut être sélectionnée et accessible par Lecteur Windows Media.

L’attribut **target** définit le frame ou la fenêtre dans lequel le navigateur ouvre la page définie par l’attribut **href** . Les valeurs de cet attribut suivent la syntaxe et les définitions HTML standard. Dans le cas d’un contrôle incorporé dans une page Web, si aucun attribut **cible** n’est défini, l’URL charge la fenêtre de navigateur actuelle et remplace la page existante, ce qui signifie que le contenu s’arrête. par conséquent, il est recommandé de toujours spécifier un attribut **cible** lors de l’incorporation du contrôle Lecteur Windows Media dans une page web.

si le métafichier est ouvert dans le Lecteur Windows Media autonome, l’attribut **cible** est ignoré et l’URL est chargée dans une fenêtre de navigateur existante. Si aucune fenêtre de navigateur n’est actuellement ouverte, l’URL est chargée dans une nouvelle fenêtre de navigateur.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






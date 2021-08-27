---
title: ClosedCaption.SAMIStyle
description: La propriété SAMIStyle spécifie ou récupère le style de sous-titrage.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIStyle Lecteur Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bd45977e3d433239e74aee21def913b640fad12
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882176"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

La propriété **SAMIStyle** spécifie ou récupère le style de sous-titrage.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Un fichier SAMI peut contenir plusieurs définitions de style de format. Les styles SAMI sont définis entre le &lt; style &gt; et les </STYLE> balises dans le fichier sami. Un style est défini avec une chaîne de texte précédée d’un \# caractère. Par exemple :


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Cela spécifie un style qui produit une police particulière.

Si aucun style SAMI n’est spécifié, le premier style défini dans le fichier SAMI est utilisé par défaut.

**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant crée un élément SELECT HTML qui utilise *closedCaption*. **SAMIStyle** pour modifier l’apparence du texte de la légende fermée. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 






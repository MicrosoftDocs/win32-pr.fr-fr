---
title: ClosedCaption.SAMILang
description: La propriété SAMILang spécifie ou récupère la langue affichée pour le sous-titrage.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Lecteur Windows Media ClosedCaption. SAMILang
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537970"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

La propriété **SAMILang** spécifie ou récupère la langue affichée pour le sous-titrage.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Un fichier SAMI peut contenir du texte pour une ou plusieurs langues. Les langues disponibles pour le sous-titrage sont définies entre les balises <STYLE> et </STYLE> dans le fichier sami. Un identificateur de langue est spécifié avec une chaîne alphanumérique unique précédée d’un point (.). Le nom spécifié pour une langue peut être n’importe quelle chaîne. Par exemple, les éléments suivants peuvent être utilisés pour définir l’anglais des États-Unis :


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Si aucune langue SAMI n’est spécifiée, la première langue définie dans le fichier SAMI est utilisée par défaut.

Valeur que vous transmettez à l’aide de *ClosedCaption*. **SAMILang** doit correspondre à l’attribut **Name** dans le spécificateur de langage.

**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *ClosedCaption*. **SAMILang** dans un élément Select HTML pour spécifier la langue de la légende fermée. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>Configuration requise



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

 

 






---
description: 'En savoir plus sur : structure JET_TUPLELIMITS'
title: Structure JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953111"
---
# <a name="jet_tuplelimits-structure"></a>Structure JET_TUPLELIMITS


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_tuplelimits-structure"></a>Structure JET_TUPLELIMITS

La structure **JET_TUPLELIMITS** permet de personnaliser les caractéristiques de l’index de tuples par index, plutôt qu’une base par instance, à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003 :** La structure **JET_TUPLELIMITS** est introduite dans Windows Server 2003.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Membres

**chLengthMin**

Longueur minimale d’un tuple. La valeur par défaut est 3.

**chLengthMax**

Longueur maximale d’un tuple. La valeur par défaut est 10.

**chToIndexMax**

Longueur maximale d’une chaîne à indexer. Par exemple, si une colonne a une longueur de 100 caractères et que **chToIndexMax** est défini sur 60, seuls les 60 premiers caractères de la colonne seront indexés. La valeur par défaut est 32767.

**cchIncrement**

Cela permet de configurer le Stride sur une base par index.

**Windows Vista :** Le membre **cchIncrement** est introduit dans Windows Vista. Avant Windows Vista, la quantité de décalage de la fenêtre (« Stride ») était toujours de 1, comme indiqué dans l’exemple de la section Notes.

**ichStart**

Offset dans la valeur pour commencer à récupérer des tuples à partir de la valeur.

**Windows Vista :** Le membre **ichStart** est introduit dans Windows Vista.

### <a name="remarks"></a>Notes

Un index de tuple parcourt une chaîne et indexe toutes ses sous-chaînes possibles de **chLengthMax**. À la fin de la chaîne (ou à la position **chToIndexMax**, selon ce qui se produit en premier), les sous-chaînes d’au moins **chLengthMin** seront indexées.

Un index de tuple peut être utilisé pour rechercher des chaînes avec des caractères génériques de début et de fin.

En supposant une ligne avec un champ de texte « pluie en Espagne \! », si un index de tuple est créé avec les paramètres **chLengthMin**= 2 et **chLengthMax**= 3, les entrées suivantes sont créées dans l’index :

"RAI"  
Ayn  
DANS  
« N I »  
DANS  
DANS  
« N S »  
SR  
Spa  
"PAI"  
Ayn  
« IN \! »  
« N \! »

Notez que « IN » se produit deux fois, et que la dernière entrée (« N \! ») est plus petite que 3 (**chLengthMax**). Notez également que l’algorithme de fractionnement ne tient pas compte des espaces ou des mots et traite tous les caractères de la même façon.

**Windows XP :** Windows XP prend en charge les index de tuple, mais n’a pas de **JET_TUPLELIMITS**. Le moteur de base de données utilisera les valeurs par défaut (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767). Il est toujours possible de modifier ces valeurs, mais elles sont définies en fonction de l’instance à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)et [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

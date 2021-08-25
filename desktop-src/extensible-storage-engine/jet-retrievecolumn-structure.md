---
description: 'En savoir plus sur : structure JET_RETRIEVECOLUMN'
title: Structure JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 4f29f3c6a9ca3262b3cd09d726634afd70db9c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471455"
---
# <a name="jet_retrievecolumn-structure"></a>Structure JET_RETRIEVECOLUMN


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_retrievecolumn-structure"></a>Structure JET_RETRIEVECOLUMN

La structure **JET_RETRIEVECOLUMN** contient des paramètres d’entrée et de sortie pour [JetRetrieveColumns](./jetretrievecolumns-function.md). Les champs de la structure décrivent la valeur de colonne à récupérer, la méthode de récupération et l’emplacement d’enregistrement des résultats.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Membres

**ColumnID**

Identificateur de colonne pour la colonne à récupérer.

**pvData**

Pointeur pour commencer à stocker des données récupérées à partir de la valeur de colonne.

**cbData**

Taille de l’allocation en commençant à **pvData**, en octets. L’opération de récupération de colonne ne stocke pas plus de données sur **pvData** que **cbData**.

**cbActual**

Taille, en octets, des données récupérées par une opération de récupération de colonne.

**grbit**

Groupe de bits qui contient les options de récupération de colonne, qui incluent zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Récupère la valeur modifiée au lieu de la valeur d’origine. Si la valeur n’a pas été modifiée, la valeur d’origine est récupérée. De cette façon, une valeur qui n’a pas encore été insérée ou mise à jour peut être récupérée lorsqu’un enregistrement est inséré ou mis à jour.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Récupère les valeurs de colonne de l’index sans accéder à l’enregistrement, si possible. De cette façon, le chargement inutile d’enregistrements peut être évité lorsque les données nécessaires sont disponibles à partir d’entrées d’index. Dans les cas où la valeur de colonne d’origine ne peut pas être récupérée à partir de l’index, en raison des transformations irréversibles ou de la troncation des données, l’enregistrement est accessible et les données sont récupérées comme normales. Il s’agit d’une option de performance qui doit être spécifiée uniquement lorsqu’il est probable que la valeur de colonne puisse être récupérée à partir de l’index. Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster, étant donné que les entrées d’index de l’index cluster ou principal sont les enregistrements eux-mêmes. Ce bit ne peut pas être défini si JET_bitRetrieveFromPrimaryBookmark est également défini.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Récupère les valeurs de colonne du signet d’index et peut différer de la valeur d’index lorsqu’une colonne apparaît à la fois dans l’index primaire et dans l’index actuel. Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster ou principal. Ce bit ne peut pas être défini si JET_bitRetrieveFromIndex est également défini.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Récupère le numéro de séquence d’une valeur de colonne à valeurs multiples dans pretinfo- &gt; itagSequence. Le champ itagSequence est souvent utilisé pour récupérer des valeurs de colonnes à valeurs multiples à partir d’un enregistrement. Toutefois, lorsque vous récupérez des valeurs à partir d’un index, il est également possible d’associer l’entrée d’index à un numéro de séquence particulier et de récupérer également ce numéro de séquence. La récupération du numéro de séquence peut être une opération coûteuse et ne doit être effectuée que si nécessaire.</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>Récupère des valeurs NULL de colonne à valeurs multiples. Si cette option n’est pas spécifiée, les valeurs NULL de la colonne à valeurs multiples sont automatiquement ignorées.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Entraîne le renvoi d’une valeur NULL lorsque le numéro de séquence demandé est 1 et qu’il n’y a aucune valeur définie pour la colonne dans l’enregistrement. Cette option affecte uniquement les colonnes à valeurs multiples.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</p> | 



**ibLongValue**

Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Numéro de séquence des valeurs contenues dans une colonne à valeurs multiples. **itagSequence** ici dans le **JET_RETRIEVECOLUMN** peut avoir la valeur 0. Si **itagSequence** est égal à 0, le nombre d’instances d’une colonne à valeurs multiples est retourné à la place des données de colonne. Une valeur **itagSequence** de 0 ne peut pas être utilisée dans les appels à [JetRetrieveColumn](./jetretrievecolumn-function.md).

**columnidNextTagged**

**ColumnID** de la colonne balisée, à valeurs multiples ou épars lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme **ColumnID** à [JetRetrieveColumn](./jetretrievecolumn-function.md).

**Raise**

Codes d’erreur et avertissements retournés par la récupération de la colonne.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)

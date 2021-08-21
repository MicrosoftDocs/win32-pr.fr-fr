---
description: 'En savoir plus sur : structure JET_SETCOLUMN'
title: Structure JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: ffdcd2ea11fad6c9ec2baae1a37bdd1965acb852
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466366"
---
# <a name="jet_setcolumn-structure"></a>Structure JET_SETCOLUMN


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_setcolumn-structure"></a>Structure JET_SETCOLUMN

La structure **JET_SETCOLUMN** contient des paramètres d’entrée et de sortie pour [JetSetColumns](./jetsetcolumns-function.md). Les champs de la structure décrivent la valeur de colonne à définir, comment la définir et où récupérer les données du jeu de colonnes.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Membres

**ColumnID**

Identificateur de colonne pour une colonne à définir.

**pvData**

Pointeur vers les données à définir dans une colonne.

**cbData**

Taille de l’allocation, en octets, à partir de **pvData** en octets.

**grbit**

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Ajoute des données à une colonne de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant <strong>ibLongValue</strong> dans <strong>psetinfo</strong>. Toutefois, il est plus simple d’utiliser ce <em>Grbit</em>, car la connaissance de la taille de la valeur de colonne existante n’est pas nécessaire.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Remplace la valeur de type long existante par les nouvelles données. Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Interprète la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le ColumnID donné et, si elle est fournie, le numéro de séquence dans psetinfo- &gt; itagSequence. Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0. Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Affecte une longueur nulle à une valeur. Normalement, une valeur de colonne est définie sur NULL en passant un cbMax de 0. Toutefois, pour certains types, comme <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, une valeur de colonne peut être de longueur 0 et non null, et cette option est utilisée pour différencier les valeurs NULL et 0.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Force une valeur long, les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>à être stockées séparément du reste des données d’enregistrement. Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes. Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long. Notez que les valeurs longues d’une taille de 4 octets ou plus petite ne peuvent pas être forcées à être séparées. Dans ce cas, l’option est ignorée.</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Applique des valeurs distinctes dans une colonne à valeurs multiples. Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, JET_bitSetAppendLv, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Applique des valeurs distinctes dans une colonne à valeurs multiples. Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, JET_bitSetAppendLv, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes. Toutes les valeurs de colonnes existantes sont supprimées. Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Conserve la valeur long, les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou JET_coltypeLongBinary, stockées avec les données d’enregistrement restantes, si possible. Normalement, les colonnes de type long sont stockées séparément quand leur longueur dépasse 1024 octets ou si la longueur de l’enregistrement dépasse la limite de taille associée à la taille de la page. Toutefois, si cette option est définie, l’opération de définition de colonne échoue avec l’erreur JET_errColumnTooBig au lieu de stocker cette valeur de colonne séparément des données d’enregistrement restantes.</p> | 



**ibLongValue**

Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples. Un **itagSequence** de 0 indique que la valeur de colonne définie doit être ajoutée en tant que nouvelle instance d’une colonne à valeurs multiples.

**Raise**

Codes d’erreur et avertissements retournés par l’opération de définition de colonne.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)

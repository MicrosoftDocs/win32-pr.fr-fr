---
description: 'En savoir plus sur : structure JET_ENUMCOLUMNVALUE'
title: Structure JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: 3a4d9500980434c21f9dfa6584db666418605de8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988612"
---
# <a name="jet_enumcolumnvalue-structure"></a>Structure JET_ENUMCOLUMNVALUE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_enumcolumnvalue-structure"></a>Structure JET_ENUMCOLUMNVALUE

La structure **JET_ENUMCOLUMNVALUE** énumère les valeurs de colonne d’un enregistrement à l’aide de la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMNVALUE** . Le tableau est retourné dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible qui a été fourni à cette fonction.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Membres

**itagSequence**

Valeur de colonne (par index de base un) qui a été énumérée.

**Raise**

Code d’état de colonne résultant de l’énumération de la valeur de colonne.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>La valeur de la colonne demandée est NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>Le <em>itagSequence</em> spécifié dans l’élément du tableau <em>rgtagSequence</em> dans le struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> qui correspond à ce <strong>JET_ENUMCOLUMNVALUE</strong> struct était égal à zéro.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>La valeur de colonne demandée a été tronquée à la taille spécifiée avant d’être retournée.</p><p>Cette troncation se produit uniquement pour les colonnes de texte long et les colonnes binaires longues contenant de grandes quantités de données.</p> | 



**cbData**

Valeur de colonne qui a été énumérée pour la colonne.

La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

Valeur de colonne qui a été énumérée pour la colonne.

La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)

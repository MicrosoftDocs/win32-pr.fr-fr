---
description: 'En savoir plus sur : structure JET_UNICODEINDEX'
title: Structure JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: cb2779c75d525e45e9140d8f70665a09fe202b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294955"
---
# <a name="jet_unicodeindex-structure"></a>Structure JET_UNICODEINDEX


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_unicodeindex-structure"></a>Structure JET_UNICODEINDEX

La structure **JET_UNICODEINDEX** personnalise la manière dont les données Unicode sont normalisées lorsqu’un index est créé sur une colonne Unicode.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Membres

**lcid**

ID de paramètres régionaux à utiliser lors de la normalisation des données. Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur. La seule exception est que les paramètres régionaux de langue neutre (LCID de zéro) ne sont pas conformes.

**dwMapFlags**

Ces indicateurs sont passés à [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) lorsque les données Unicode sont normalisées en une clé, ce qui permet aux indicateurs définis par l’utilisateur de remplacer la valeur par défaut.

**Windows 2000**: les deux seules valeurs autorisées pour **dwFlags** sont :

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)

<!-- end list -->

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)

**dwMapFlags** présente les restrictions suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>facultatif.</p> | 
| <p>NORM_IGNORECASE</p> | <p>facultatif.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>Optionnel.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>Optionnel.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>Optionnel.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>Optionnel.</p> | 
| <p>SORT_STRINGSORT</p> | <p>Optionnel.</p> | 



### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)

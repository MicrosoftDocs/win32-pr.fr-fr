---
description: 'En savoir plus sur : paramètres d’index'
title: Paramètres d’index
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 3d322334d5a14439461f903a583e11e78a7b829863c2b55dbf653dc13aa4d22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604479"
---
# <a name="index-parameters"></a>Paramètres d’index


_**S’applique à :** Windows | Windows Serveurs_

## <a name="index-parameters"></a>Paramètres d’index

Cette rubrique contient des paramètres qui sont utilisés pour l’index.

*JET_paramIndexTupleIncrement*  
132  

Ce paramètre spécifie la valeur par défaut pour l’incrément de décalage utilisé pour parcourir la valeur de la colonne source lors de la génération de chaque tuple. Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Entier</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows Versions Vista et ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTupleStart*  
133  

Ce paramètre spécifie la valeur par défaut pour le décalage dans la valeur de colonne source au niveau de laquelle la génération de tuple démarrera. Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Entier</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows Versions Vista et ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMax*  
111  

Ce paramètre spécifie la valeur par défaut de la longueur maximale du tuple dans un index de Tuple. Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista :**  avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut. pour Windows Vista, ce n’est plus pris en charge.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Entier</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 0, 2-255</p>
<p><strong>Windows Vista :</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Ce paramètre spécifie la valeur par défaut pour la longueur minimale du tuple dans un index de Tuple. Pour plus d’informations, consultez [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista :**  avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut. pour Windows Vista, ce n’est plus pris en charge.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Entier</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 0, 2-255</p>
<p><strong>Windows Vista :</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Ce paramètre spécifie la valeur par défaut pour la longueur maximale d’une chaîne source à décomposer en tuples pour un index de Tuple. Pour plus d’informations, consultez [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista :**  avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut. pour Windows Vista, ce n’est plus pris en charge.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Entier</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 0 – 32767</p>
<p><strong>Windows Vista :</strong> 1 – 32767</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Ce paramètre contrôle les paramètres Unicode par défaut utilisés par n’importe quel index sur une colonne de clé Unicode. Le type de ce paramètre est [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) et est passé en fait à l’aide d’un pointeur de mémoire tampon stocké dans le paramètre entier de [JetGetSystemParameter](./jetgetsystemparameter-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md). La taille de la mémoire tampon doit être égale à la taille de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) et doit être passée à [JetGetSystemParameter](./jetgetsystemparameter-function.md) à l’aide du paramètre de taille de mémoire tampon de chaîne. Cela est clairement incohérent, mais il s’agit du comportement de ce paramètre.

La valeur par défaut de ce paramètre contient un LCID pour les paramètres régionaux anglais (États-Unis) et les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)suivants : LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.

**Windows 2000 :**  Le SORTID dans le LCID est ignoré. Un SORTID de SORT_DEFAULT est toujours utilisé.

**Windows 2000 :**  Les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) doivent contenir les indicateurs suivants : LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH. En outre, les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)peuvent contenir les indicateurs suivants : NORM_IGNORENONSPACE.

**Remarque**  Si votre application souhaite stocker des données Unicode, il est vivement recommandé de ne pas compter sur les paramètres Unicode par défaut de vos index. L’utilisation de l’anglais des États-Unis est équivaut à l’utilisation des paramètres régionaux invariants et les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)par défaut sont connus pour interférer sérieusement avec certaines langues. Vous devez toujours spécifier vos propres paramètres pour les paramètres Unicode à JetCreateIndex2 à l’aide de [JET_INDEXCREATE](./jet-indexcreate-structure.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

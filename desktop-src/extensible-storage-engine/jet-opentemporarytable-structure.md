---
description: 'En savoir plus sur : structure JET_OPENTEMPORARYTABLE'
title: Structure JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: ee2f2ab2fca7a849f889d46badcc86a8a5438fa8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478505"
---
# <a name="jet_opentemporarytable-structure"></a>Structure JET_OPENTEMPORARYTABLE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_opentemporarytable-structure"></a>Structure JET_OPENTEMPORARYTABLE

La structure **JET_OPENTEMPORARYTABLE** contient une collection de paramètres facilement extensible pour la fonction **JET_OPENTEMPORARYTABLE** . Cette structure est l’équivalent de la table temporaire de la structure [JET_TABLECREATE](./jet-tablecreate-structure.md) .

**Windows Vista :** la structure **JET_OPENTEMPORARYTABLE** est introduite dans Windows Vista.

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de cette structure en octets (pour une extension future). Elle doit être définie sur sizeof (JET_TABLECREATE) en octets.

**prgcolumndef**

Définitions de colonne pour les colonnes créées dans la table temporaire.

Il existe des limitations **importantes** pour les options de définition de colonne utilisées avec une table temporaire. Pour plus d'informations, consultez la section Notes.

Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant. Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La colonne est une colonne clé pour la table temporaire.</p><p>L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire. La première définition de colonne dans le tableau qui a cette option est définie sur la colonne clé la plus significative, et ainsi de suite. Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</p> | 



**ccolumn**

Consultez *prgcolumndef*.

**pidxunicode**

Indicateurs de normalisation et d’ID de paramètres régionaux à utiliser pour comparer des données de colonne de clé Unicode dans la table temporaire.

Lorsque ce paramètre n’est pas présent et que le paramètre *LCID* n’est pas présent, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire. Le LCID par défaut est le paramètre régional anglais (États-Unis).

Lorsque ce paramètre n’est pas présent, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire. Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.

**grbit**

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTUnique</p> | <p>Demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</p><p>avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques. à partir de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</p><p>Il n’est pas possible de savoir quel doublon va être effectué et quels doublons seront ignorés, en général. Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire sera toujours correctement effectué.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</p><p>Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Demande que les valeurs de colonne clé <strong>null</strong> soient plus proches de la fin de l’index que les valeurs de colonne clé non null.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Force le gestionnaire de tables temporaires à abandonner la recherche de la meilleure stratégie pour utiliser la gestion de la table temporaire qui entraîne des performances améliorées.</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec JET_errKeyDuplicate. Si cette option n’est pas demandée, un doublon est détecté immédiatement et échoue, ou est supprimé en mode silencieux ultérieurement, en fonction de la stratégie choisie par le moteur de base de données pour implémenter la table temporaire, en fonction de la fonctionnalité demandée.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>La table temporaire est créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation qui est optimisée pour les résultats de requête intermédiaires. Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</p><p>L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées. Pour plus d’informations, consultez JET_bitTTUnique.</p><p><strong>Windows Server 2003 :</strong> cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</p> | 



**prgcolumnid**

Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.

Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.

**cbKeyMost**

Taille maximale d’une clé représentant une ligne donnée.

La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées. La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes.

si ce paramètre a la valeur 0 ou JET_cbKeyMostMin (255), la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003 et les versions antérieures. Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données de l’instance (JET_paramDatabasePageSize). Pour plus d’informations, consultez JET_paramKeyMost.

**cbVarSegMac**

Quantité maximale de données qui seront utilisées à partir d’une colonne de longueur variable pour construire une clé pour une ligne donnée.

Ce paramètre peut être utilisé pour contrôler la quantité d’espace clé consommée par une colonne clé donnée. Cette limite est en octets. Si ce paramètre est égal à zéro ou est identique au paramètre *cbKeyMost* , aucune limite n’est appliquée.

**TableID**

Descripteur de table pour la table temporaire créée à la suite d’un appel réussi à [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[paramètres système du moteur de Stockage Extensible](./extensible-storage-engine-system-parameters.md)

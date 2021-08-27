---
description: 'En savoir plus sur : fonction JetMakeKey'
title: Fonction JetMakeKey
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a642a103d67b023fdf42aa532cc328964c7734a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482845"
---
# <a name="jetmakekey-function"></a>Fonction JetMakeKey


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetmakekey-function"></a>Fonction JetMakeKey

La fonction **JetMakeKey** construit des clés de recherche qui peuvent ensuite être utilisées pour rechercher un ensemble d’entrées dans un index par certains critères de recherche simples sur les valeurs de leurs colonnes clés. Une clé de recherche est également l’une des propriétés intrinsèques d’un curseur et est utilisée par les opérations [JetSeek](./jetseek-function.md) et [JetSetIndexRange](./jetsetindexrange-function.md) pour localiser les entrées d’index correspondant à ces critères de recherche sur l’index actuel de ce curseur. Une clé de recherche complète est créée dans une série d’appels **JetMakeKey** où chaque appel est utilisé pour charger la valeur de colonne pour la colonne clé suivante de l’index actuel d’un curseur. Il est également possible de charger une clé de recherche précédemment construite qui a été récupérée à partir du curseur à l’aide de [JetRetrieveKey](./jetretrievekey-function.md).

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvData*

Mémoire tampon d’entrée contenant les données de colonne pour la colonne clé actuelle de l’index actuel du curseur pour lequel la clé de recherche est construite.

Le type de données des données de colonne dans la mémoire tampon d’entrée doit correspondre exactement au type de données et à d’autres propriétés de la définition de colonne de la colonne clé actuelle. Aucune contrainte de type n’est effectuée sur les données de colonne.

Si JET_bitNormalizedKey est spécifié dans le paramètre *Grbit* , la mémoire tampon d’entrée doit contenir une clé de recherche précédemment construite. Ces clés sont obtenues à l’aide d’un appel à [JetRetrieveKey](./jetretrievekey-function.md).

*cbData*

Taille en octets des données de colonne fournies dans la mémoire tampon d’entrée.

Si JET_bitNormalizedKey est spécifié dans le paramètre *Grbit* , il s’agit de la taille de la clé de recherche fournie dans la mémoire tampon d’entrée.

Si la taille des données de la colonne est égale à zéro, le contenu de la mémoire tampon d’entrée est ignoré. Si JET_bitKeyDataZeroLength est spécifié dans le paramètre *Grbit* et que la colonne clé actuelle de l’index actuel du curseur est une colonne de longueur variable, les données de la colonne d’entrée sont supposées être une valeur de longueur nulle. Dans le cas contraire, les données de la colonne d’entrée sont supposées être une valeur NULL.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour cette colonne clé et toutes les colonnes clés précédentes.</p></li><li><p>Toutes les valeurs de colonne nécessaires pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches de la fin d’un index. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>cette option est disponible uniquement sur Windows XP et versions ultérieures.</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour cette colonne clé et toutes les colonnes clés précédentes.</p></li><li><p>Toutes les valeurs de colonne nécessaires pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches du début d’un index. Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index. Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>cette option est disponible uniquement sur Windows XP et versions ultérieures.</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>Si la taille de la mémoire tampon d’entrée est égale à zéro et que la colonne clé actuelle est une colonne de longueur variable, cette option indique que la mémoire tampon d’entrée contient une valeur de longueur égale à zéro. Dans le cas contraire, une taille de mémoire tampon d’entrée égale à zéro indiquerait une valeur NULL.</p> | 
| <p>JET_bitNewKey</p> | <p>Une nouvelle clé de recherche doit être construite. Toute clé de recherche existante est ignorée.</p> | 
| <p>JET_bitNormalizedKey</p> | <p>Quand cette option est spécifiée, toutes les autres options sont ignorées, toute clé de recherche précédemment existante est ignorée et le contenu de la mémoire tampon d’entrée est chargé en tant que nouvelle clé de recherche.</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>La clé de recherche doit être construite de telle sorte que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour cette colonne clé et toutes les colonnes clés précédentes.</p></li><li><p>Toutes les valeurs de colonne nécessaires pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches de la fin d’un index. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>Cette option ne peut pas être utilisée lorsque la colonne clé actuelle n’est pas une colonne de texte ou une colonne binaire de variable. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p><p>cette option est disponible uniquement sur Windows XP et versions ultérieures.</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>Cette option indique que la clé de recherche doit être construite de manière à ce que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour cette colonne clé et toutes les colonnes clés précédentes.</p></li><li><p>Toutes les valeurs de colonne nécessaires pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches du début d’un index. Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index. Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>Cette option ne peut pas être utilisée lorsque la colonne clé actuelle n’est pas une colonne de texte ou une colonne binaire de variable. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p><p>cette option est disponible uniquement sur Windows XP et versions ultérieures.</p> | 
| <p>JET_bitStrLimit</p> | <p>Cette option indique que la clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour cette colonne clé et toutes les colonnes clés précédentes.</p></li><li><p>Toutes les valeurs de colonne nécessaires pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches de la fin d’un index. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>Quand cette option est spécifiée en combinaison avec JET_bitSubStrLimit et que la colonne clé actuelle est une colonne de texte, cette option est ignorée. Ce comportement est destiné à permettre au type de la colonne clé actuelle d’être déduit lors de la génération de la clé de recherche.</p><p>Si vous souhaitez créer une clé de recherche similaire pour le début d’un index, un appel similaire à <strong>JetMakeKey</strong> doit être effectué pour la dernière colonne clé qui n’est pas un caractère générique, mais sans options génériques spécifiées. La clé de recherche est alors dans un état approprié à utiliser pour une telle recherche. Cela est similaire à l’utilisation de JET_bitFullColumnStartLimit, à la différence que la clé de recherche n’est pas correctement terminée, car elle est effectuée après l’utilisation d’une option de caractère générique.</p><p>cette option est dépréciée pour les versions Windows XP et versions ultérieures afin de résoudre cette sémantique maladroite. JET_bitFullColumnStartLimit et JET_bitFullColumnEndLimit doivent être utilisés à la place, dans la mesure du possible.</p> | 
| <p>JET_bitSubStrLimit</p> | <p>Cette option indique que la clé de recherche doit être construite de manière à ce que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques. Cela signifie que la clé de recherche construite peut être utilisée pour mettre en correspondance les entrées d’index qui présentent les éléments suivants :</p><ul><li><p>Valeurs de colonne exactes fournies pour toutes les colonnes clés précédentes.</p></li><li><p>Données de la colonne spécifiée en tant que préfixe de la valeur de leur colonne pour la colonne clé actuelle.</p></li><li><p>Toutes les valeurs de colonne pour les colonnes clés suivantes.</p></li></ul><p>Cette option doit être utilisée lors de la création de clés de recherche de caractères génériques à utiliser pour rechercher les entrées d’index les plus proches de la fin d’un index. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p><p>Quand cette option est spécifiée en combinaison avec JET_bitStrLimit et que la colonne clé actuelle est une colonne de texte, cette option est prioritaire. Cette option est ignorée lorsque la colonne clé actuelle n’est pas une colonne de texte. Ce comportement est destiné à permettre au type de la colonne clé actuelle d’être déduit lors de la génération de la clé de recherche.</p><p>Si vous souhaitez créer une clé de recherche similaire pour le début d’un index, un appel similaire à <strong>JetMakeKey</strong> doit être effectué pour la colonne clé qui doit être le caractère générique de préfixe, mais sans aucune option générique spécifiée. La clé de recherche est alors dans un état approprié à utiliser pour une telle recherche. Cela est similaire à l’utilisation de JET_bitPartialColumnStartLimit, à la différence que la clé de recherche n’est pas correctement terminée, car elle est effectuée après l’utilisation d’une option de caractère générique.</p><p>cette option est dépréciée pour les versions Windows XP et versions ultérieures afin de résoudre cette sémantique maladroite. JET_bitPartialColumnStartLimit et JET_bitPartialColumnEndLimit doivent être utilisés à la place, lorsque cela est possible.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>Les données de la colonne fournie sont insuffisantes pour créer une clé valide pour l’index actuel, car cet index est un index de tuple et la taille minimale du tuple était supérieure aux données de la colonne fournie. Pour plus d’informations sur les index de tuple, consultez <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> . cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Les données de colonne fournies ne correspondent pas à la taille requise par la définition de colonne. Cela peut se produire si le type de données de la colonne est intrinsèquement une certaine taille. Cela peut également se produire si le type de données de la colonne n’est pas intrinsèquement une certaine taille, mais que la définition de la colonne le déclare comme étant de longueur fixe. La seule exception à cela est que cette erreur ne se produira pas quand un trop petit nombre de données est fourni pour une colonne de texte de longueur fixe parce que les données manquantes sont automatiquement complétées par des espaces. Une deuxième exception à cela est que cette erreur ne se produit pas quand un trop petit nombre de données est fourni pour une colonne binaire de longueur fixe, car les données manquantes sont automatiquement complétées par des zéros.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>L’une des options demandées n’est pas valide, utilisée de manière non conforme ou non implémentée. Cela peut se produire pour <strong>JetMakeKey</strong> dans les cas suivants :</p><ul><li><p>JET_bitPartialColumnStartLimit ou JET_bitPartialColumnEndLimit sont spécifiés et la colonne clé correspondante n’est pas une colonne de texte et n’est pas une colonne binaire de longueur variable. ce cas se produit uniquement sur Windows XP et les versions ultérieures.</p></li><li><p>Une tentative d’utilisation conjointe de plusieurs des options suivantes est effectuée : JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit et JET_bitFullColumnEndLimit. ce cas se produit uniquement sur Windows XP et les versions ultérieures.</p></li><li><p>Une tentative est faite pour utiliser JET_bitStrLimit ou JET_bitSubStrLimit lorsque l’une des options suivantes est utilisée : JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit et JET_bitFullColumnEndLimit. ce cas se produit uniquement sur Windows XP et les versions ultérieures.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</p><p>Cela peut se produire pour <strong>JetMakeKey</strong> lorsque JET_bitNormalizedKey a été spécifié et que la valeur fournie dans la mémoire tampon d’entrée est trop grande pour être une clé de recherche valide.</p> | 
| <p>JET_errKeyIsMade</p> | <p>Les données de colonne fournies à <strong>JetMakeKey</strong> ont été rejetées, car des données de colonne ont déjà été fournies pour toutes les colonnes clés de l’index actuel. Cela peut se produire de trois manières. La première consiste à faire en sorte que les données de colonne soient fournies pour chaque colonne clé de l’index actuel. La seconde méthode est si des données de colonne ont été fournies pour au moins une colonne clé et qu’une option de caractère générique a été choisie pour le dernier appel. La troisième méthode consiste à fournir une clé de recherche précédemment construite à l’aide de JET_bitNormalizedKey, qui couvre toutes les colonnes clés.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Il n’existe pas de clé de recherche pour le curseur. Cela se produit pour <strong>JetMakeKey</strong> si JET_bitNewKey n’est pas spécifié et qu’une clé de recherche n’a pas été construite pour ce curseur à l’aide d’un appel antérieur à <strong>JetMakeKey</strong>. La clé de recherche sera supprimée par un appel précédent à n’importe quelle API de navigation sur le curseur autre que <a href="gg294117(v=exchg.10).md">JetMove</a>.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Il n’y a pas d’index actuel pour le curseur. Cela se produit pour <strong>JetMakeKey</strong> si le curseur se trouve sur l’index cluster d’une table, qu’un index primaire n’a pas été défini et que JET_bitNormalizedKey n’a pas été spécifié. Il n’est pas possible de construire une clé de recherche si le curseur se trouve sur un index qui n’a pas de colonnes clés, sauf si une clé de recherche précédemment construite est fournie.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, si JET_bitNormalizedKey et JET_bitNewKey n’ont pas été spécifiés, la clé de recherche est générée par les critères de recherche pour une colonne clé supplémentaire dans l’index actuel. Si JET_bitNormalizedKey n’a pas été spécifié et que JET_bitNewKey a été spécifié, toute clé de recherche précédemment existante était ignorée et une nouvelle a été créée par les critères de recherche de la première colonne clé de l’index actuel. Si JET_bitNormalizedKey a été spécifié, toute clé de recherche précédemment existante était ignorée et une nouvelle est chargée à partir de la mémoire tampon d’entrée. Dans tous les cas, aucune modification de l’état de la base de données ne se produit.

En cas d’échec, si JET_bitNormalizedKey ou JET_bitNewKey a été spécifié, l’état de la clé de recherche n’est pas défini. Si ni JET_bitNormalizedKey ni JET_bitNewKey n’ont été spécifiés, aucune modification de l’état de la clé de recherche ne se produit. Dans tous les cas, aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Les clés doivent être traitées comme des blocs de données opaques. Aucune tentative n’est faite pour exploiter la structure interne de ces données. Toutefois, les éléments suivants sont connus de toutes les clés ESENT :

  - Les clés peuvent être comparées les unes aux autres à l’aide de [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur ordre relatif dans l’index d’origine sur la table des entrées d’index source.

  - Il est inutile de comparer les clés des entrées d’index de différents index.

  - la longueur d’une clé est toujours inférieure ou égale à JET_cbKeyMost (255) octets avant Windows Vista. sur Windows Vista et les versions ultérieures, les clés peuvent être plus volumineuses. La taille maximale d’une clé est égale à la valeur actuelle de JET_paramKeyMost.

Les clés de recherche peuvent prendre plus d’un octet si une option générique a été utilisée. dans ce cas, la clé de recherche sera jusqu’à JET_cbLimitKeyMost (256) octets pour les versions antérieures à Windows vista et JET_paramKeyMost + 1 octets pour Windows vista et les versions ultérieures.

Il existe une ramification très importante pour cette taille de clé maximale. Lorsqu’il existe une entrée d’index qui a des valeurs de colonne suffisamment grandes pour provoquer la génération d’une clé pour cet index qui, autrement, serait plus grande que cette taille maximale, cette clé est tronquée en silence à cette taille maximale. Cela entraîne deux effets :

  - Pour les entrées dans un index unique, les entrées qui, autrement, seraient uniques sont déclarées en tant que doublons.

  - Pour les entrées dans tous les index, la troncation de clé entraînera la déclaration des entrées d’index qui, autrement, ne correspondent pas aux critères de recherche d’une clé de recherche donnée à déclarer comme correspondances.

Les applications doivent anticiper cette troncation et l’éviter ou compenser ses effets. dans Windows Vista, un nouvel indicateur d’index, JET_bitIndexDisallowTruncation, a été ajouté pour faciliter la tâche des applications afin d’éviter les troncations de clé. Pour plus d’informations sur cette option d’indexation, consultez la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)

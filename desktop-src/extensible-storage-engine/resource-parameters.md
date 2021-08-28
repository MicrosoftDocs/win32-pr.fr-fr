---
description: 'En savoir plus sur : paramètres de ressource'
title: Paramètres de ressource
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: a2575f6b6cbdd49380422cb955ad64e246bf6ccf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984212"
---
# <a name="resource-parameters"></a>Paramètres de ressource


_**S’applique à :** Windows | Windows Serveurs_

## <a name="resource-parameters"></a>Paramètres de ressource

Cette rubrique contient des paramètres qui sont utilisés pour les ressources.

*JET_paramCachedClosedTables*  
125  

Ce paramètre contrôle le nombre de ressources de l’arborescence B + mises en cache par l’instance une fois que les tables qu’elles représentent ont été fermées par l’application.

Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application. Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>64</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows Versions Vista et ultérieures</p> | 



*JET_paramDisablePerfmon*  
107  

Ce paramètre peut être utilisé pour empêcher le moteur de base de données de publier des données sur ses performances dans Windows. Cela peut être fait pour réduire l’activité de thread de service du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Faux</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows Versions Vista et ultérieures</p> | 



*JET_paramGlobalMinVerPages*  
81  

Ce paramètre permet aux applications qui fonctionnent en mode multi-instance de préallouer de la mémoire pour les pages de version dans un pool global afin d’émuler l’ancien comportement. Cela est utile si l’application souhaite garantir que les transactions d’une certaine taille peuvent être effectuées plus tard, même si la mémoire devient rare.

**Windows 2000 :**  Une quantité suffisante de mémoire pour sauvegarder toutes les pages de version est toujours réservée à l’heure [JetInit](./jetinit-function.md) .

**Windows XP :**  à partir de Windows XP, cela est toujours vrai en mode d’instance unique. Toutefois, la mémoire de page de version est allouée dynamiquement en mode multi-instance.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>64</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>Yes</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramMaxCursors*  
8  

Ce paramètre réserve le nombre demandé de ressources de curseur pour une utilisation par une instance. Une ressource de curseur correspond directement à un type de données [JET_TABLEID](./jet-tableid.md) . Ce paramètre affecte le nombre de curseurs qui peuvent être utilisés en même temps. Une ressource de curseur ne peut pas être partagée par différentes sessions, de sorte que ce paramètre doit être défini sur une valeur suffisamment élevée afin que chaque session puisse utiliser autant de curseurs que nécessaire.

**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>1 024</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramMaxInstances*  
104  

Ce paramètre contrôle le nombre maximal d’instances qui peuvent être créées dans un processus unique.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>16</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1-1024</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramMaxOpenTables*  
6  

Ce paramètre réserve le nombre demandé de ressources de l’arborescence B + pour une utilisation par une instance. Ce paramètre affecte le nombre de tables qui peuvent être utilisées en même temps. Ce paramètre doit être défini par rapport au schéma physique des bases de données utilisées par le moteur de base de données. par conséquent, ce paramètre n’est pas aussi simple que possible.

En général, vous avez besoin de deux ressources, plus une ressource par index secondaire par table, dans l’utilisation simultanée par l’application.

**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>300</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramMaxSessions*  
5  

Ce paramètre réserve le nombre demandé de ressources de session pour une utilisation par une instance. Une ressource de session correspond directement à un type de données [JET_SESID](./jet-sesid.md) . Ce paramètre affecte le nombre de sessions qui peuvent être utilisées en même temps.

**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>16</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 30000</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramMaxTemporaryTables*  
10  

Ce paramètre réserve le nombre demandé de ressources de table temporaire pour une utilisation par une instance. Ce paramètre affecte le nombre de tables temporaires qui peuvent être utilisées en même temps.

**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.

**Windows XP et versions ultérieures :**  Si ce paramètre système est défini à zéro, aucune base de données temporaire n’est créée et toute activité nécessitant l’utilisation de la base de données temporaire échoue. Ce paramètre peut être utile pour éviter les e/s nécessaires à la création de la base de données temporaire si elle est connue qu’elle ne sera pas utilisée.

**Remarque**  L’utilisation d’une table temporaire requiert également une ressource curseur.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>20</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>Yes</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramMaxVerPages*  
9  

Ce paramètre réserve le nombre demandé de pages du magasin de versions pour une utilisation par une instance. La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives. Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané. Ce paramètre affecte le nombre de mises à jour qui peuvent être conservées en mémoire à la fois. Cela affecte à son tour le nombre maximal de mises à jour qu’une seule transaction peut effectuer, la durée maximale pendant laquelle une transaction peut être ouverte, la charge simultanée maximale de transactions de mise à jour sur le système ou une combinaison de ces opérations.

Chaque page de la Banque des versions telle que configurée par ce paramètre a une taille de 16 Ko sur les ordinateurs 32 bits, et 32 Ko sur des ordinateurs 64 bits.

**Windows Vista et versions ultérieures :**  La taille de page de la Banque des versions peut être lue et modifiée via JET_paramVerPageSize.

**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.

**Remarque**  Il s’agit de la ressource la plus couramment épuisée par le moteur de base de données. Une attention particulière doit être accordée au paramètre du système et au chargement transactionnel de l’application afin d’éviter l’épuisement de cette ressource en fonctionnement normal. Lorsque cette ressource est épuisée, les mises à jour de la base de données seront rejetées avec JET_errVersionStoreOutOfMemory. Pour libérer certaines de ces ressources, la plus ancienne transaction en suspens doit être abandonnée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>64</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>Yes</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramPageHintCacheSize*  
101  

Ce paramètre contrôle la taille d’un cache spécial utilisé pour accélérer la recherche de pointeurs de page enfant B + d’arborescence dans le cache de la page de base de données. La taille du cache est en octets.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>262 144</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

Ce paramètre tente de conserver le nombre de ressources de l’arborescence B + en cours d’utilisation en deçà du seuil spécifié.

Si ce paramètre a la valeur zéro, la valeur par défaut est 100% de **JET_paramMaxOpenTables**.

**Windows Vista et versions ultérieures :**  Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données. Les applications doivent utiliser JET_paramMaxCachedClosedTables à la place.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>0 (100% de <strong>JET_paramMaxOpenTables</strong>)</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramPreferredVerPages*  
63  

Ce paramètre représente un seuil relatif à **JET_paramMaxVerPages** qui contrôle l’utilisation discrétionnaire des pages de version par le moteur de base de données. Si la taille de la Banque des versions dépasse ce seuil, toutes les informations qui sont utilisées uniquement pour les tâches en arrière-plan facultatives, telles que la récupération de l’espace supprimé dans la base de données, sont sacrifiées pour conserver de l’espace pour les informations transactionnelles.

**Windows 2000, Windows XP et Windows Server 2003 :**  Si vous affectez la valeur zéro à ce paramètre, le seuil est de 90% de **JET_paramMaxVerPages**.

**Windows Vista et versions ultérieures :**  Cela n’est plus pris en charge et la valeur par défaut de ce paramètre a été modifiée pour clarifier son comportement.

Chaque page de la Banque des versions telle que configurée par ce paramètre a une taille de 16 Ko sur les ordinateurs 32 bits, et 32 Ko sur des ordinateurs 64 bits.

**Windows Vista et versions ultérieures :**  La taille de page de la Banque des versions peut être lue et modifiée via JET_paramVerPageSize.

**Remarque**  Si le moteur de base de données fonctionne trop souvent au-dessus de ce seuil, il est possible que la base de données se dégrade en performances. Cela se produit parce que les processus d’arrière-plan qui nettoient la base de données ne peuvent pas fonctionner sans les informations facultatives qui sont rejetées dans ce scénario. La défragmentation en ligne ou hors connexion contrecarre cet effet.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 0 (90% de JET_paramMaxVerPages)</p><p><strong>Windows Vista :</strong> 58</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>Yes</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramVerPageSize*  
128  

Ce paramètre contrôle la taille des pages de la Banque des versions utilisées par le moteur de base de données pour stocker les informations transactionnelles. La valeur de ce paramètre est la taille d’unité pour tous les autres paramètres système en termes de pages de version (par exemple, JET_paramMaxVerPages).

Le moteur de base de données peut choisir d’utiliser une plus grande taille de page de la Banque des versions que celle demandée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>16384</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows Vista et versions ultérieures</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

Ce paramètre contrôle le nombre d’éléments de travail de nettoyage en arrière-plan qui peuvent être mis en file d’attente dans le pool de threads du moteur de base de données à un moment donné.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>32</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p><strong>Windows XP et Windows Server 2003 :</strong> 1 – 63</p><p><strong>Windows Vista :</strong> 1 – 127</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows XP et Windows Server 2003 :</strong>  º</p><p><strong>Windows Vista :</strong>  Oui</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

---
description: 'En savoir plus sur : paramètres de base de données'
title: Paramètres de base de données
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: cdccfca7e7a68ea997c9b564939f89799634e344
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471835"
---
# <a name="database-parameters"></a>Paramètres de base de données


_**S’applique à :** Windows | Windows Serveurs_

## <a name="database-parameters"></a>Paramètres de base de données

Cette rubrique contient les paramètres utilisés pour la base de données.

*JET_paramCheckFormatWhenOpenFail*  
44  

Quand ce paramètre est défini, [JetInit](./jetinit-function.md) renvoie une erreur spéciale lorsqu’une base de données ou un journal des transactions d’une version précédente du moteur de base de données est ouvert. Ces erreurs sont les suivantes :


| <p>Erreur</p> | <p>Description</p> | 
|--------------|--------------------|
| <p>JET_errDatabase200Format</p> | <p>La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans Windows NT 3,51.</p> | 
| <p>JET_errDatabase400Format</p> | <p>La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans une version de test antérieure à Windows NT Server 4,0.</p> | 
| <p>JET_errDatabase500Format</p> | <p>La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans Windows NT Server 4,0.</p> | 



**Windows Vista :**  pour Windows Vista et versions ultérieures, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.


| | | <p>Valeur par défaut :</p> | <p>Vrai</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramDatabasePageSize*  
64  

Ce paramètre configure la taille de page pour la base de données. La taille de la page est la plus petite unité d’allocation d’espace possible pour un fichier de base de données. La taille de la page de base de données est également très importante, car elle définit la limite supérieure de la taille d’un enregistrement individuel dans la base de données.

**Remarque** Une seule taille de page de base de données est prise en charge par processus pour l’instant. Cela signifie que si vous êtes dans un processus unique qui contient des applications qui utilisent le moteur de base de données, elles doivent toutes accepter sur une taille de page de base de données.


| | | <p>Valeur par défaut :</p> | <p>4096</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>2048, 4096, 8192</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>Yes</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>Yes</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramDbExtensionSize*  
18  

Ce paramètre contrôle la quantité d’espace qui est ajoutée à un fichier de base de données chaque fois qu’il doit croître pour accueillir davantage de données. La taille est dans les pages de base de données.


| | | <p>Valeur par défaut :</p> | <p>256</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>1 – 2147483647</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p><p><strong>Windows Vista :</strong>  pour Windows Vista et versions ultérieures : oui</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>Yes</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramEnableIndexChecking*  
45  

Lorsque ce paramètre a la valeur true, chaque base de données est vérifiée au moment de la [JetAttachDatabase](./jetattachdatabase-function.md) pour les index sur les colonnes clés Unicode qui ont été créées à l’aide d’une version antérieure de la bibliothèque NLS dans le système d’exploitation. Cela doit être fait parce que le moteur de base de données conserve les clés de tri générées par [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) et que la valeur de ces clés de tri passe de Release à Release.

Si un index principal est détecté comme étant dans cet État, [JetAttachDatabase](./jetattachdatabase-function.md) échouera toujours avec JET_errPrimaryIndexCorrupted.

Si des index secondaires sont détectés comme étant dans cet État, il existe deux résultats possibles. Si JET_bitDbDeleteCorruptIndexes a été passé à [JetAttachDatabase](./jetattachdatabase-function.md) , ces index seront supprimés et JET_wrnCorruptIndexDeleted sera retourné à partir de [JetAttachDatabase](./jetattachdatabase-function.md). Ces index doivent être recréés par votre application. Si JET_bitDbDeleteCorruptIndexes n’a pas été passé à [JetAttachDatabase](./jetattachdatabase-function.md) , l’appel échoue avec JET_errSecondaryIndexCorrupted.

**Remarque** Il est fortement recommandé de définir ce paramètre sur true par votre application.

**Remarque** Il est fortement recommandé que les applications évitent l’utilisation de colonnes clés Unicode dans leurs index de clé primaire (en cluster).


| | | <p>Valeur par défaut :</p> | <p>Faux</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Global</p><p><strong>Windows Vista :</strong>  pour Windows Vista et versions ultérieures : Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>Yes</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramEnableIndexCleanup*  
54  

Lorsque ce paramètre est défini sur true, le moteur de base de données peut nettoyer automatiquement les index sur les colonnes de clés Unicode au moment [JetInit](./jetinit-function.md) pour éviter les modifications de format de base de données provoquées par les modifications apportées à la bibliothèque NLS dans Windows. Ces modifications sont régulièrement apportées à la bibliothèque NLS pour ajouter la prise en charge de nouvelles langues, pour ajouter des caractères manquants à une langue, pour ajouter un ordre de classement à une langue ou pour corriger les bogues dans l’ordre de classement d’une langue. Ces modifications affectent les clés de tri produites par [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) qui sont rendues persistantes par le moteur de base de données en tant que composants des clés d’index.

Il est important de comprendre qu’il est possible que les modifications apportées à l’index soient tellement importantes qu’un nettoyage incrémentiel n’est pas possible. Dans ce cas, l’index sera géré conformément aux indications de **JET_paramEnableIndexChecking**.

**Remarque** Il est fortement recommandé de définir ce paramètre et d' **JET_paramEnableIndexChecking** avoir la valeur **true** par votre application.


| | | <p>Valeur par défaut :</p> | <p>Vrai</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p><p><strong>Windows Vista :</strong>  pour Windows Vista et versions ultérieures : oui</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows Versions 2003 et ultérieures du serveur</p> | 



*JET_paramOneDatabasePerSession*  
102  

Lorsque ce paramètre a la valeur true, une seule base de données peut être ouverte à l’aide de [JetOpenDatabase](./jetopendatabase-function.md) par une session donnée à un moment donné. La base de données temporaire est exclue de cette restriction.

**Windows XP et Windows Server 2003 :**  ce paramètre est écrit uniquement sur Windows XP et Windows Server 2003.

**Windows Vista :**  ce paramètre se comporte normalement à partir de Windows Vista.

**Remarque**  Ce paramètre est en écriture seule.


| | | <p>Valeur par défaut :</p> | <p>Faux</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p><p><strong>Windows Vista :</strong>  pour Windows Vista et versions ultérieures : oui</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramEnableOnlineDefrag*  
35  

Ce paramètre contrôle le comportement de la défragmentation en ligne lorsqu’elle est lancée à l’aide de [JetDefragment](./jetdefragment-function.md). Pour plus d’informations, consultez [JetDefragment](./jetdefragment-function.md) .

Windows 2000 : sur Windows 2000, ce paramètre était un booléen simple qui porterait sur la défragmentation en ligne lors de son lancement par [JetDefragment](./jetdefragment-function.md). Lorsque la valeur est **true**, la défragmentation en ligne est effectuée sur les enregistrements de chaque table de la base de données.

**Windows XP :**  sur Windows XP et les versions ultérieures, ce paramètre peut être défini sur une ou plusieurs des options suivantes :


| <p>Option</p> | <p>Description</p> | 
|---------------|--------------------|
| <p>JET_OnlineDefragDisable</p> | <p>N’effectuez pas de défragmentation en ligne. il s’agit du binaire équivalent au paramètre Windows 2000 de la valeur false pour ce paramètre.</p> | 
| <p>JET_OnlineDefragAllOBSOLETE</p> | <p>Effectuez une défragmentation en ligne complète. il s’agit du binaire équivalent au paramètre Windows 2000 de True pour ce paramètre.</p> | 
| <p>JET_OnlineDefragDatabases</p> | <p>Effectuez une défragmentation en ligne des enregistrements de chaque table dans la base de données.</p> | 
| <p>JET_OnlineDefragSpaceTrees</p> | <p>Effectuez une défragmentation en ligne des arborescences d’espaces de chaque table dans la base de données.</p> | 
| <p>JET_OnlineDefragStreamingFiles</p> | <p>ce paramètre est utilisé pour prendre en charge l’infrastructure Microsoft Exchange et n’est pas destiné à être utilisé dans votre application.</p> | 
| <p>JET_OnlineDefragAll</p> | <p>Effectuez une défragmentation en ligne complète. il s’agit du concept conceptuel équivalent au paramètre Windows 2000 de True pour ce paramètre.</p> | 




| | | <p>Valeur par défaut :</p> | <p><strong>Windows 2000 :</strong>  :</p><p><strong>Windows xp : pour Windows xp et versions ultérieures :</strong> JET_OnlineDefragAll</p> | | <p>Tapez :</p> | <p><strong>Windows 2000 :</strong>  Expression</p><p><strong>Windows XP et versions ultérieures :</strong>  JET_GRBIT (entier)</p> | | <p>Plage valide :</p> | <p><strong>Windows 2000 :</strong>  False, true</p><p><strong>Windows XP et versions ultérieures :</strong> 0 – JET_OnlineDefragAll</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>Yes</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramPageFragment*  
20  

Ce paramètre correspond au seuil utilisé par le moteur de base de données pour contrôler la fragmentation de l’espace libre. La taille est dans les pages de base de données.


| | | <p>Valeur par défaut :</p> | <p>8</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0 – 2147483647</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>Yes</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramRecordUpgradeDirtyLevel*  
78

Ce paramètre contrôle la manière dont le gestionnaire de cache de la page de base de données écrira une page de base de données qui a subi une conversion de format en place. ces conversions de format se produisent à la volée lorsque les pages sont chargées à partir d’une base de données qui a été créée avec le moteur de base de données Windows 2000, mais utilisée par une version Windows XP ou ultérieure du moteur de base de données.


| | | <p>Valeur par défaut :</p> | <p>1</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0-3</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | | <p>Affecte la disposition physique :</p> | <p>Yes</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramWaypointLatency*  
153  

Latence (dans les journaux) en arrière-plan des vidages de pages de la page de base de données pour différer le vidage. L’activation de cette latence peut permettre la récupération de la base de données en cas de perte irrémédiable du fichier journal le plus récent. Consultez JET_bitReplayIgnoreLostLogs.


| | | <p>Valeur par défaut :</p> | <p>0</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0-1023</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>Yes</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTrees*  
160  

Activez/désactivez la défragmentation séquentielle automatique de l’arbre B.


| | | <p>Valeur par défaut :</p> | <p>1</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>0-1</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>Yes</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Détermine la fréquence de vérification de la densité de l’arbre B.


| | | <p>Valeur par défaut :</p> | <p>10</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0-entier maximal</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>Yes</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramIOThrottlingTimeQuanta*  
162  

Durée maximale, en millisecondes, pendant laquelle le mécanisme de limitation des e/s permet à une tâche de s’exécuter pour qu’elle soit considérée comme « terminée ».


| | | <p>Valeur par défaut :</p> | <p>125</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0-10000</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>Yes</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)

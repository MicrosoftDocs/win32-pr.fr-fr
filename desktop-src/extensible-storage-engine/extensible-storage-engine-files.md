---
description: 'en savoir plus sur : fichiers de moteur d’Stockage Extensible'
title: fichiers de moteur d’Stockage Extensible
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: d06773526048ed819f0f855b44644e9d7738ca77
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983172"
---
# <a name="extensible-storage-engine-files"></a>fichiers de moteur d’Stockage Extensible


_**S’applique à :** Windows | Windows Serveurs_

## <a name="extensible-storage-engine-files"></a>fichiers de moteur d’Stockage Extensible

le moteur de Stockage Extensible utilise les types de fichiers suivants :

- [Fichiers du journal des transactions](#transaction-log-files)

- [Fichiers journaux des transactions temporaires](#temporary-transaction-log-files)

- [Fichiers journaux des transactions réservés](#reserved-transaction-log-files)

- [Fichiers de point de contrôle](#checkpoint-files)

- [Fichiers de base de données](#database-files)

- [Bases de données temporaires](#temporary-databases)

- [Vider les fichiers de mappage](#flush-map-files)

Ce tableau contient une vue d’ensemble des noms de fichiers de données qui sont gérés par ESE. pour Windows Vista et versions ultérieures, le paramètre JET_paramLegacyNames a un impact sur les noms de fichiers utilisés.


| Étiquette | Valeur |
|--------|-------|
|  | 



### <a name="transaction-log-files"></a>Fichiers du journal des transactions

Les fichiers journaux des transactions contiennent des opérations sur les fichiers de base de données. Ils contiennent suffisamment d’informations pour amener une base de données à un État logiquement cohérent après un arrêt inattendu du processus ou un arrêt du système.

Les noms des fichiers journaux sont dépendants d’un nom de base à trois lettres, qui peut être défini avec [JET_paramBaseName](./transaction-log-parameters.md). Les exemples ci-dessous utilisent le nom de base « edb », car il s’agit du nom de base par défaut. L’extension pour les fichiers journaux des transactions est. log ou. JTX selon que la JET_bitESE98FileNames est définie dans le paramètre JET_paramLegacyFileNames. pour plus d’informations, consultez [paramètres système du moteur de Stockage Extensible](./extensible-storage-engine-system-parameters.md).

Les fichiers journaux des transactions sont nommés \<base\> \<generation-number\> . log, en commençant par 1. Le numéro de génération de journal est au format hexadécimal. Par exemple, edb00001. log est le premier journal et edb000ff. log est le journal 255th. Les fichiers journaux comportent cinq chiffres hexadécimaux dans le nom du fichier journal, jusqu’à ce que le fichier journal 1048576th, à partir duquel les fichiers journaux commencent à être nommés dans un format 11,3 (par exemple, edb00100000. log). \<base\>. log est toujours le fichier journal en cours d’utilisation. Si le moteur de base de données n’est pas actif, la génération du fichier Edb. log peut être identifiée à l’aide de la commande suivante : **esentutl.exe-ml edb. log**.

Bien que les fichiers journaux des transactions aient le. L’extension de journal est couramment associée à des fichiers texte, les fichiers journaux de transactions sont au format binaire et ne doivent jamais être modifiés par un utilisateur. Les opérations de base de données sont écrites en premier dans le journal. Les données peuvent être écrites dans le fichier de base de données ultérieurement ; peut-être immédiatement, potentiellement plus tard. En cas de processus inattendu ou d’arrêt du système, les opérations sont toujours présentes dans les fichiers journaux, et les transactions incomplètes peuvent être annulées. La relecture des fichiers journaux de transactions est appelée *récupération conditionnelle* et est effectuée automatiquement quand [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md) est appelé. La récupération logicielle peut également être effectuée manuellement avec l’option « -r » du programme Esentutl.exe. La relecture des fichiers journaux des transactions sur une base de données restaurée à partir d’une sauvegarde est appelée *récupération matérielle*.

Les fichiers journaux ont une taille fixe et peuvent être personnalisés avec [JET_paramLogFileSize](./transaction-log-parameters.md). Lorsque le fichier journal actuel (c’est-à-dire edb. log) est rempli, il est renommé en \<base\> \<generation-number\> . log et un nouveau fichier journal des transactions est nécessaire dans le flux du journal des transactions.

Chaque instance de base de données est associée à une seule séquence de fichier journal. Windows XP a introduit [JetCreateInstance](./jetcreateinstance-function.md), ce qui permet à plusieurs séquences de fichiers du journal des transactions d’être utilisées par un processus unique. Toutefois, plusieurs séquences de fichiers du journal des transactions ne peuvent pas exister dans le même répertoire.

Les fichiers du journal des transactions ne doivent jamais être manipulés manuellement, renommés, déplacés ou supprimés, car l’altération des données peut en résulter.

Les fichiers journaux des transactions seront supprimés par le moteur de base de données lors d’une sauvegarde complète (consultez [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) ou pendant des opérations normales, si l’enregistrement circulaire est activé.

Une fois qu’un fichier journal de transactions est plein, le moteur de base de données doit créer un nouveau fichier journal. La journalisation circulaire est un moyen par lequel les fichiers journaux peuvent être automatiquement nettoyés par le moteur de base de données lorsqu’ils ne sont plus nécessaires pour la récupération après incident. Ce processus est une alternative à la suppression des fichiers journaux en tant que produit par le biais d’une sauvegarde. La journalisation circulaire peut être contrôlée à l’aide du paramètre système [JET_paramCircularLog](./transaction-log-parameters.md) . Les fichiers journaux des transactions ne doivent pas être supprimés à l’aide d’une autre méthode.

### <a name="temporary-transaction-log-files"></a>Fichiers journaux des transactions temporaires

Lorsque edb. log se remplit, ESE doit créer un nouveau fichier. Le nouveau fichier de transaction de journal est connu sous le nom de fichier journal temporaire des transactions, avant son utilisation par ESE.

Lorsqu’un nouveau fichier journal est créé et sa taille étendue, il s’appelle \<base\> tmp. log. La création d’un nouveau fichier peut être une opération potentiellement coûteuse, de sorte que le moteur ESE crée le prochain fichier journal de manière proactive en tant que tâche en arrière-plan.

Étant donné que le fichier journal temporaire des transactions est créé en prévision de la nécessité d’un nouveau fichier journal des transactions, il ne contient aucune information utile.

### <a name="reserved-transaction-log-files"></a>Fichiers journaux des transactions réservés

Les fichiers journaux de transactions réservés sont créés lorsque le moteur commence à autoriser la journalisation des opérations importantes pour obtenir un arrêt correct.

**Windows Vista :** dans Windows Vista et versions ultérieures, les fichiers journaux de transactions réservés sont nommés \<base\> RESXXXXX. jrs.

**Windows Server 2003 :** dans Windows Server 2003 et versions antérieures, les fichiers journaux de transactions réservés sont nommés res1. log et res2. log.

Lorsque le moteur de base de données ne dispose plus de suffisamment d’espace disque, il ne peut pas créer de nouveau fichier journal. La chose la plus sûre consiste à arrêter correctement, mais certaines opérations (telles que les opérations de restauration) doivent toujours être enregistrées. La plupart des opérations de base de données échoueront au cours de cette phase.

Étant donné que les fichiers journaux de transactions réservés sont créés en prévision des besoins en matière de fichiers journaux de transactions dans un scénario hors disque, ils ne contiennent pas d’informations utiles.

### <a name="checkpoint-files"></a>fichiers de point de contrôle

Le fichier de point de contrôle stocke le point de contrôle pour une séquence particulière de fichier journal des transactions. Le fichier de point de contrôle se nomme \<base\> . chk ou \<base\> . JCP, selon que la JET_bitESE98FileNames est définie dans le paramètre JET_paramLegacyFileNames, et que son emplacement est donné par [JET_paramSystemPath](./transaction-log-parameters.md).

Les opérations de base de données sont d’abord écrites dans les fichiers journaux, puis mises en cache en mémoire. À un moment ultérieur, les opérations sont écrites dans le fichier de base de données, mais pour des raisons de performances, l’ordre dans lequel les opérations sont écrites dans le fichier de base de données peut ne pas correspondre à l’ordre dans lequel elles ont été journalisées à l’origine. Les opérations écrites dans le fichier journal des transactions sont dans l’un des deux États suivants :

  - Écrit dans le fichier journal des transactions et dans le fichier de base de données.

  - Écrit dans le fichier journal des transactions et n’est pas encore écrit dans le fichier de base de données.

De nombreuses opérations de base de données peuvent être stockées dans un seul fichier journal des transactions. Un fichier journal donné peut comporter les éléments suivants :

  - Toutes les opérations écrites dans le fichier de base de données.

  - Aucune opération n’est écrite dans le fichier de base de données

  - Une combinaison d’opérations écrites dans le fichier de base de données et les opérations qui n’ont pas encore été écrites dans le fichier de base de données.

Le point de contrôle fait référence au point dans le temps dans le flux du journal des transactions où toutes les opérations antérieures au point de contrôle ont été écrites dans le fichier de base de données. Il n’existe aucune garantie quant aux opérations qui se produisent après le point de contrôle ; certains peuvent être en mémoire et d’autres peuvent être écrits dans la base de données.

Étant donné que toutes les opérations dans les fichiers journaux avant le point de contrôle sont représentées dans le fichier de base de données, seuls les fichiers journaux des transactions situés après le point de contrôle sont nécessaires à la récupération logicielle afin d’amener une base de données particulière dans un état propre.

### <a name="database-files"></a>Fichiers de base de données

Le fichier de base de données contient le schéma de toutes les tables de la base de données, les enregistrements de toutes les tables de la base de données et les index sur les tables. Son emplacement est fourni à l’aide de [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)ou [JetAttachDatabase2](./jetattachdatabase2-function.md).

Une base de données est arrêtée proprement uniquement après un appel réussi à [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).

Le programme Esentutl.exe peut détecter si une base de données est arrêtée proprement avec l’option « -MH ». Par exemple, « esentutl.exe-MH Sample. edb » lira l’en-tête de base de données d’une base de données nommée Sample. edb et imprime l’état de Sample. edb. Il peut imprimer « État : arrêt correct » ou « État : arrêt intempestif ».

Une base de données qui n’a pas été correctement arrêtée est dans un état d’arrêt intempestif. avant Windows XP, cet état était appelé *incohérent*. Une base de données incorrecte (incohérente) peut être placée dans un état propre avec la récupération logicielle. Une base de données endommagée n’est pas la même chose qu’une base de données modifiée (« incohérente »).

Une base de données endommagée fait référence à une altération physique ou logique, et ne peut pas être corrigée avec la récupération logicielle. Les altérations physiques peuvent être des retournements de bits, qui sont souvent détectés par les sommes de contrôle sur les pages de la base de données. Un checksum en échec dans un fichier de base de données se manifeste comme une erreur de JET_errReadVerifyFailure.

Seules les bases de données correctement arrêtées peuvent être déplacées ou renommées en toute sécurité. Si une base de données n’a pas été arrêtée proprement, elle ne peut pas être déplacée ou renommée automatiquement en toute sécurité.

Plusieurs bases de données peuvent être associées à une seule séquence de fichiers du journal des transactions.

### <a name="temporary-databases"></a>Bases de données temporaires

La base de données temporaire est utilisée comme magasin de stockage pour temptables et elle est également utilisée lors de la création d’index.

Le nom et l’emplacement sont configurés avec [JET_paramTempPath](./temporary-database-parameters.md).

Les Temptables sont créés avec [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md). Elles sont également créées par certains appels d’API et utilisées pour retourner les informations de schéma (par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Vider les fichiers de mappage

à partir de la Windows 10 mise à jour anniversaire (client) et Windows Server 2016 (serveur), ESE a ajouté un niveau supplémentaire de protection contre les écritures perdues (ou les vidages perdus) 1, ce qui lui permet de détecter de tels événements interprocessus initialization2. Cette fonctionnalité requiert la conservation des métadonnées dans un fichier distinct appelé « vidage du mappage ».

Un fichier de mappage de vidage est créé pour chaque fichier de base de données et se trouve dans le même répertoire. Le fichier est nommé de la même façon que le fichier de base de données, mais avec une extension différente. Par exemple, si l’application cliente crée une base de données avec le chemin d’accès complet C : \\ mydirectory \\ MyDabatase. edb, son fichier de mappage de vidage correspondant est c : \\ mydirectory \\ MyDabatase. jfm.

Cette amélioration introduit deux conditions requises pour le nom des fichiers de base de données :

  - Deux bases de données dans le même répertoire ne doivent pas avoir le même nom de fichier avec des extensions différentes. Par exemple : C : \\ mydirectory \\ MyDabatase. DB1 et c : \\ mydirectory \\ MyDabatase. DB2.

  - 2 \. Une base de données ne doit pas avoir une extension. jfm.

Lorsque vous copiez ou déplacez manuellement un fichier de base de données, le fichier de mappage de vidage correspondant doit également être copié ou déplacé vers le même répertoire de destination. Si un fichier de mappage de vidage n’est pas présent au moment d’une nouvelle pièce jointe de base de données (par le biais de [JetAttachDatabase](./jetattachdatabase-function.md), un nouveau fichier est créé et rempli à la demande à mesure que des pages sont lues à partir de la base de données. La combinaison d’une base de données incompatible et de fichiers de mappage de vidage est gérée par ESE et force la suppression et la recréation de la carte de vidage incompatible.

La taille d’un fichier de mappage de vidage est directement proportionnelle à son fichier de base de données associé et approximativement égale à (toutes les tailles en octets, le résultat doit être arrondi au multiple suivant de 8 192) :

`8,192 + ((<database file size> / <database page size>) / 4)`

Par exemple : pour une base de données de 1,5 Go utilisant une taille de page de 32 Ko, la taille approximative du mappage de vidage est de 24 576 octets (ou 24KB).

Le fichier de mappage de vidage doit être actualisé au fur et à mesure que les pages de la base de données sont vidées. Si la journalisation transactionnelle est activée (par exemple, [JET_paramRecovery](./transaction-log-parameters.md) définie sur « on », valeur par défaut), l’actualisation du mappage de vidage est effectuée lorsque l’application cliente modifie la base de données. En moyenne, l’ensemble du mappage de vidage est écrit sur le support non volatile une fois tous les 20% des [JET_paramCheckpointDepthMax](./database-cache-parameters.md) de la valeur (en octets) des journaux transactionnels générés. Le nombre d’opérations d’écriture dépend de la répartition des modifications dans l’ensemble de la base de données. Mais elle est au plus approximative (toutes les tailles en octets) :

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Si la journalisation transactionnelle est désactivée (par exemple, [JET_paramRecovery](./transaction-log-parameters.md) défini sur « désactivé »), le mappage de vidage est actualisé une seule fois lorsque la base de données est explicitement détachée proprement (via [JetDetachDatabase](./jetdetachdatabase-function.md), ou détaché de manière implicite en mettant fin à l’instance ESE associée (via l’une des fonctions [JetTerm](./jetterm-function.md) , tant que [JET_bitTermDirty](./jetterm2-function.md) n’est pas passé).

1 une perte d’écriture (ou un vidage perdu) est définie comme une opération d’écriture qui renvoie correctement depuis le système d’exploitation vers le moteur de base de données ESE, mais les données réelles ne sont jamais conservées dans le fichier de base de données du média non volatile. Cela est généralement dû à une pile de stockage défectueuse ou mal configurée (logiciel ou matériel). Les applications clientes peuvent recevoir une erreur [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) des fonctions ESE qui nécessitent la lecture des données de la base de données si les données se trouvent dans une région qui a subi un événement d’écriture perdu.

2 la possibilité de détecter les écritures perdues au cours de la durée de vie d’un processus est présente depuis Windows 8 (client) et Windows Server 2012 (serveur).

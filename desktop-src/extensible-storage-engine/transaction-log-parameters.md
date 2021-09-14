---
description: 'En savoir plus sur : paramètres du journal des transactions'
title: Paramètres du journal des transactions
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 1d8f3ed19d01eece0b22e22b4a2a16d8d985751a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236514"
---
# <a name="transaction-log-parameters"></a>Paramètres du journal des transactions


_**S’applique à :** Windows | Windows Serveurs_

**Dans cet article**  
Paramètres du journal des transactions  
Spécifications  
Voir aussi  

## <a name="transaction-log-parameters"></a>Paramètres du journal des transactions

Cette rubrique contient des paramètres qui sont utilisés pour les journaux des transactions.

*JET_paramBaseName*  
3  

Ce paramètre définit le préfixe à trois lettres utilisé pour la plupart des fichiers utilisés par le moteur de base de données. Par exemple, le fichier de point de contrôle est appelé EDB. CHK par défaut, car EDB est le nom de base par défaut. Le nom de base peut être utilisé pour distinguer facilement les ensembles de fichiers qui appartiennent à différentes instances ou à différentes applications.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>EDB</p> | 
| <p>Tapez :</p> | <p>String</p> | 
| <p>Plage valide :</p> | <p>3 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramCircularLog*  
17  

Ce paramètre configure la façon dont les fichiers journaux des transactions sont gérés par le moteur de base de données.

Lorsque la journalisation circulaire est désactivée, tous les fichiers journaux des transactions générés sont conservés sur le disque jusqu’à ce qu’ils ne soient plus nécessaires, car une sauvegarde complète de la base de données a été effectuée. Dans ce mode, il est possible de restaurer à partir d’une sauvegarde plus ancienne et de lire par progression tous les fichiers journaux de transactions conservés de sorte qu’aucune donnée ne soit perdue à la suite de l’incident qui a forcé la restauration. Des sauvegardes complètes régulières sont nécessaires pour empêcher le disque de se remplir avec les fichiers journaux des transactions.

Lorsque la journalisation circulaire est activée, seuls les fichiers journaux des transactions qui sont plus récents que le point de contrôle actuel sont conservés sur le disque. L’avantage de ce mode est que les sauvegardes ne sont pas nécessaires pour supprimer les anciens fichiers du journal des transactions. Le compromis est qu’il n’est plus possible de restaurer une perte de données nulle.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>False</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramCommitDefault*  
16  

Ce paramètre contrôle l’action par défaut entreprise lorsque la transaction la plus à l’extérieur est validée sur une session. Toute option valide pouvant être passée à [JetCommitTransaction](./jetcommittransaction-function.md) peut également être définie comme étant la valeur par défaut pour toutes les sessions dans une instance et/ou pour une session spécifique. Pour plus d’informations sur ces options, consultez [JetCommitTransaction](./jetcommittransaction-function.md) .

Ce paramètre a un impact sur la fiabilité et les performances des transactions. Pour plus d’informations, consultez [JetCommitTransaction](./jetcommittransaction-function.md) .


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>0</p> | 
| <p>Tapez :</p> | <p>JET_GRBIT (entier)</p> | 
| <p>Plage valide :</p> | <p>Une option valide pour JetCommitTransaction</p> | 
| <p>Étendue :</p> | <p>Instance ou session</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Oui</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramDeleteOldLogs*  
48  

Lorsque ce paramètre a la valeur true et que les fichiers journaux des transactions désignés par le chemin d’accès au fichier journal (**JET_paramLogFilePath**) sont tous des versions obsolètes, ces fichiers journaux des transactions sont automatiquement supprimés.

**Windows 2000 :**  vous devez veiller à utiliser ce paramètre lors de la mise à niveau d’une base de données de Windows NT vers Windows 2000. Si la base de données n’est pas dans un état cohérent et que les anciens fichiers journaux sont supprimés, le contenu de la base de données sera perdu.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p><strong>Windows 2000 :</strong>  Fausses</p><p><strong>Windows XP :</strong>  :</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramIgnoreLogVersion*  
47  

Si ce paramètre a la valeur true, le moteur de base de données ne valide pas le numéro de version du fichier journal des transactions pendant la [JetInit](./jetinit-function.md).

**Windows XP :**  à partir de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>False</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLegacyFileNames*  
136  

Ce paramètre offre une compatibilité descendante avec les conventions d’affectation des noms de fichiers des versions antérieures du moteur de base de données.

Les options suivantes sont actuellement prises en charge :

JET_bitESE98FileNames

Lorsque cette option est présente, le moteur de base de données utilise les conventions d’affectation de noms suivantes pour ses fichiers :

  - Les fichiers journaux des transactions vont utiliser. Journal pour l’extension de fichier

  - Les fichiers de point de contrôle seront utilisés. CHK pour leur extension de fichier


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Tapez :</p> | <p>JET_GRBIT (entier)</p> | 
| <p>Plage valide :</p> | <p>0, JET_bitESE98FileNames</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows Versions Vista et ultérieures</p> | 



*JET_paramLogBuffers*  
12  

Ce paramètre permet de configurer la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions. L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions. La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité.

Ce paramètre a un impact sur les performances. Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide. Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée. La valeur par défaut est trop petite pour ce cas.

**Windows XP et Windows 2000 :**  dans Windows XP et les versions antérieures, il n’est pas recommandé de définir ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 80</p><p><strong>Windows Vista :</strong> 126</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 80 – 2147483647</p><p><strong>Windows Vista :</strong> 1 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLogCheckpointPeriod*  
14  

Ce paramètre configure le moteur de base de données pour qu’il prenne un point de contrôle lorsque le nombre spécifié de secteurs de fichier journal a été généré.

**Windows XP :**  à partir de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>1 024</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLogFileCreateAsynch*  
69  

Lorsque ce paramètre est défini sur true, le moteur de base de données crée le prochain fichier journal des transactions, car le fichier journal des transactions en cours est consommé. L’objectif est de réduire le temps passé à passer d’un fichier journal de transactions à l’autre sous une charge de mise à jour importante.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Vrai</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramLogFilePath*  
2 

Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra les journaux des transactions pour l’instance. Le chemin d’accès doit se terminer par une barre oblique inverse, ce qui indique que le chemin d’accès cible est un dossier. Les fichiers journaux des transactions contiennent les informations requises pour ramener les fichiers de base de données à un état cohérent après un incident. Ils sont généralement nommés EDB \* . Sign. Le contenu des fichiers du journal des transactions est tout aussi important (si ce n’est pas le cas) que les fichiers de base de données eux-mêmes. Chaque effort doit être effectué pour les protéger.

Il y aura également des fichiers journaux de réserve supplémentaires nommés RES1. LOG et RES2. JOURNAL stocké avec les fichiers journaux ordinaires. Le contenu de ces fichiers n’est pas important car leur seul objectif est de réserver de l’espace disque pour permettre au moteur de s’arrêter correctement dans un scénario à faible disque. Il s’agit également d’un fichier journal temporaire appelé EDBTMP. Connectez-vous au même dossier. Le contenu de ce fichier n’a pas d’importance. Ce fichier est un nouveau fichier journal préparé pour être utilisé.

Les propriétés du volume hôte des fichiers journaux des transactions et leur emplacement par rapport aux autres fichiers utilisés par le moteur de base de données peuvent avoir un impact considérable sur les performances.

**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>".\"</p> | 
| <p>Tapez :</p> | <p>Chemin d’accès au dossier (String)</p> | 
| <p>Plage valide :</p> | <p>0 – 246 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLogFileSize*  
11  

Ce paramètre permet de configurer la taille des fichiers du journal des transactions. Chaque fichier journal de transactions a une taille fixe. La taille est égale à la valeur de ce paramètre système, en unités de 1024 octets.

Ce paramètre a un impact sur la fiabilité. Si le paramètre est trop petit, le nombre maximal de fichiers journaux (1048575) sera atteint beaucoup plus rapidement. Dans ce cas, l’instance doit être arrêtée correctement, les fichiers journaux existants doivent être supprimés et l’instance doit être redémarrée. Cette action permet non seulement de réduire la disponibilité de l’application, mais également d’invalider les sauvegardes précédentes de la base de données de l’application.

Ce paramètre a un impact sur les performances. Si le paramètre est très important, [JetInit](./jetinit-function.md) est lent, car le moteur de base de données doit lire le fichier journal le plus récent (au minimum) au moment de l’initialisation. Si le paramètre est très volumineux, le basculement entre les fichiers journaux prendra également plus de temps. Si le paramètre est très petit, vous devrez créer des fichiers journaux pour un nombre donné de mises à jour, ce qui entraînera une surcharge supplémentaire.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>5120</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> 128 – 32768</p><p><strong>Windows Vista :</strong> 64 – 32768</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLogWaitingUserMax*  
15  

Ce paramètre tente d’optimiser le vidage du tampon du journal provoqué par une validation durable en attendant qu’un nombre spécifié de sessions attendent une validation durable avant de forcer un vidage à se produire dans l’espoir qu’une autre transaction partage le vidage.

**Windows XP :**  à partir de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>3</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramRecovery*  
34  

Ce paramètre est le commutateur maître qui contrôle la récupération après incident pour une instance. Si ce paramètre a la valeur « on », la récupération de type ARIES sera utilisée pour ramener toutes les bases de données de l’instance dans un état cohérent en cas de panne d’un processus ou d’un ordinateur. Si ce paramètre est défini sur « désactivé », toutes les bases de données de l’instance seront gérées sans l’avantage de la récupération après incident. Autrement dit, si l’instance n’est pas fermée correctement à l’aide de [JetTerm](./jetterm-function.md) avant la sortie du processus ou de l’arrêt de l’ordinateur, le contenu de toutes les bases de données de cette instance est endommagé.

La désactivation de la récupération est utile dans des circonstances particulières où l’on sait que le contenu d’une base de données n’est pas utile en cas de panne. La récupération doit être activée pour tous les autres cas.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Sur</p> | 
| <p>Tapez :</p> | <p>String</p> | 
| <p>Plage valide :</p> | <p>0 – 259 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramSystemPath*  
0  

Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra le fichier de point de contrôle de l’instance. Le chemin d’accès doit se terminer par une barre oblique inverse, ce qui indique que le chemin d’accès cible est un dossier. Le fichier de point de contrôle est un fichier simple géré par instance qui mémorise le fichier journal des transactions le plus ancien qui doit être relu pour ramener toutes les bases de données de cette instance à un état cohérent après un incident. Le fichier de point de contrôle est généralement nommé EDB. CHK.

**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>".\"</p> | 
| <p>Tapez :</p> | <p>Chemin d’accès au dossier (String)</p> | 
| <p>Plage valide :</p> | <p>0 – 246 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramWaitLogFlush*  
13 

Ce paramètre tente d’optimiser le vidage du tampon du journal provoqué par une validation durable en attendant une période spécifiée avant de forcer un vidage à se produire dans l’espoir qu’une autre transaction partage le vidage.

**Windows XP :**  à partir de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>0</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance ou session</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Oui</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramLegacyFileNames*  
136  

ce paramètre est utilisé pour spécifier les fonctionnalités de compatibilité des noms de fichiers à gérer avec le Windows Server 2003 et le schéma d’attribution de noms de fichier précédent. pour plus d’informations sur les différents fichiers et leur nom, consultez [Extensible Stockage Engine files](./extensible-storage-engine-files.md).

la JET_bitESE98FileNames garantit que l’extension de fichier utilisée dans les fichiers journaux de transactions et le fichier de point de contrôle sont les mêmes que ceux utilisés dans Windows Server 2003. remarque : si vous effectuez une mise à niveau à partir de Windows Server 2003, ce bit n’a toujours pas besoin d’être spécifié, car le moteur met automatiquement à niveau les extensions de fichier si JET_paramCircularLog a la valeur **true** ou conserve l’ancienne extension de journal si JET_paramCircularLog a la **valeur false**.

**Remarque**  Pour définir un bit, la valeur doit d’abord être récupérée, puis « ou » dans le bit de compatibilité souhaité.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Tapez :</p> | <p>JET_GRBIT (entier)</p> | 
| <p>Plage valide :</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>à compter de Windows Server 2008 et Windows Vista</p> | 



## <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



## <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)

---
description: En savoir plus sur les paramètres d’e/s
title: Paramètres d’e/s
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 62cc1183f14e3de113ff5f34eaf6367bc2ff0f9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519144"
---
# <a name="io-parameters"></a>Paramètres d’e/s


_**S’applique à :** Windows | Windows Serveurs_

## <a name="io-parameters"></a>Paramètres d’e/s

Cette rubrique contient des paramètres qui sont utilisés pour l’entrée et la sortie (e/s).

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP et versions ultérieures :**  Ce paramètre configure la durée (en millisecondes) pendant laquelle le moteur de base de données utilisera pour accéder à un fichier verrouillé avant l’échec avec JET_errFileAccessDenied. Ce délai est conçu pour contourner les logiciels antivirus qui peuvent contenir certains des fichiers du moteur de base de données ouverts brièvement après leur fermeture.

**Remarque**  En raison de la logique de nouvelle tentative ci-dessus, toute tentative d’attachement à une base de données ou d’utilisation d’un fichier journal qui est déjà utilisé par le moteur de base de données entraîne un délai de cette taille avant que l’appel d’API ne retourne un échec (légitime). Ce paramètre peut être utilisé pour désactiver ce délai au cas où il s’agit d’un scénario courant.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>10000</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 – 4294967295</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Oui</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Lorsque ce paramètre est défini sur true, tout dossier manquant dans un chemin d’accès du système de fichiers utilisé par le moteur de base de données sera créé sans assistance. Dans le cas contraire, l’opération qui utilise le chemin d’accès au système de fichiers manquant échouera avec JET_errInvalidPath.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>False</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramEnableFileCache*  
126  

lorsque ce paramètre a la **valeur True**, le moteur de base de données utilise le cache de fichiers Windows en tant que cache de lecture pour tous ses différents fichiers. Il l’utilise également comme cache d’écriture pour la base de données temporaire ou pour les bases de données ouvertes avec la récupération désactivée. Le moteur de base de données doit désactiver le cache d’écriture pour les bases de données ordinaires, les fichiers journaux des transactions et les fichiers de point de contrôle pour protéger l’intégrité transactionnelle des bases de données.

il est important de noter que l’utilisation du cache de fichiers Windows ajoute une deuxième superposition de la mise en cache des fichiers de base de données. Le cache de base de données utilisera toujours sa propre mémoire pour mettre en cache les fichiers de base de données. l’objectif de ce mode est de permettre à l’application de configurer le moteur de base de données avec un petit cache dédié et de permettre à Windows de faire don de mémoire spare pour améliorer la mise en cache des données de la base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>False</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Non</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Windows Vista et versions ultérieures</p> | 



*JET_paramIOPriority*  
152  

Ce paramètre contrôle la manière dont ESE gère les opérations d’e/s. Les valeurs peuvent être définies sur 0 (JET_IOPriorityNormal) pour une opération normale, ou sur 1 (JET_IOPriorityLow) pour une opération de faible priorité. lorsque la priorité est définie sur JET_IOPriorityLow, le moteur ESE utilise la nouvelle fonctionnalité de priorité d’e/s de thread disponible dans Windows Vista pour réduire la priorité d’e/s sur le thread afin que les opérations d’e/s ultérieures soient émises au niveau de la nouvelle priorité basse.

**Windows Vista :**  JET_paramIOPriority est introduite dans Windows Vista.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>0</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 - 1</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Oui</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Ce paramètre contrôle le nombre d’e/s de fichier de base de données qui peuvent être mises en file d’attente dans le système d’exploitation hôte à un moment donné.

Une valeur plus élevée pour ce paramètre peut améliorer considérablement les performances d’une application de base de données volumineuse.

**Windows XP et Windows Server 2003 :**  ce paramètre est ignoré sur Windows XP et Windows Server 2003 et n’affecte pas le fonctionnement du moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p><strong>Windows 2000 :</strong> 64</p><p><strong>Windows Vista :</strong> 1024</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p><strong>Windows 2000 :</strong> 8 – 2147483647</p><p><strong>Windows Vista :</strong> 0 – 65536</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Non</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Nombre maximal d’octets pouvant être regroupés pour une opération de lecture fusionnée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>262 144</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0-1073741824</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Nombre maximal d’octets pouvant être regroupés pour une opération d’écriture fusionnée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>393216</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0-1073741824</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Nombre maximal d’octets pouvant être utilisé pour une opération d’e/s d’écriture fusionnée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>262 144</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0-1073741824</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Nombre maximal d’octets pouvant être utilisé pour une opération d’e/s de lecture fusionnée.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>393216</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0-1073741824</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

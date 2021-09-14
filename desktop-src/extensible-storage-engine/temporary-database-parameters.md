---
description: En savoir plus sur les paramètres de base de données temporaires
title: Paramètres de base de données temporaires
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920620"
---
# <a name="temporary-database-parameters"></a>Paramètres de base de données temporaires


_**S’applique à :** Windows | Windows Serveurs_

## <a name="temporary-database-parameters"></a>Paramètres de base de données temporaires

Cette rubrique contient les paramètres utilisés pour la base de données temporaire.

*JET_paramEnableTempTableVersioning*  
46  

Ce paramètre contrôle l’utilisation des transactions dans les tables temporaires. Lorsque ce paramètre a la valeur false, les tables temporaires sont plus rapides, mais il n’est pas possible de restaurer les mises à jour effectuées dans une transaction.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Vrai</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Non</p> | 
| <p>Affecte la fiabilité :</p> | <p>Oui</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramPageTempDBMin*  
19  

Ce paramètre contrôle la taille initiale de la base de données temporaire. La taille est dans les pages de base de données. Une taille de zéro indique que la taille par défaut d’une base de données ordinaire doit être utilisée.

Il est souvent souhaitable que les petites applications configurent la base de données temporaire aussi petite que possible. L’affectation de la valeur 14 à ce paramètre permet d’obtenir la plus petite base de données temporaire possible. Notez qu’il est également possible d’éliminer entièrement la base de données temporaire en affectant à **JET_paramMaxTemporaryTables** la valeur zéro.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>0</p> | 
| <p>Tapez :</p> | <p>Integer</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Oui</p> | 
| <p>Affecte les ressources :</p> | <p>Oui</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramTempPath*  
1  

Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier ou du fichier qui contiendra la base de données temporaire de l’instance. Si le chemin d’accès correspond à un dossier qui contiendra la base de données temporaire, il doit se terminer par une barre oblique inverse. La base de données temporaire est utilisée pour stocker les données volatiles générées dans le processus de gestion des appels d’informations de l’API ESE, de création d’index ou de stockage du contenu d’une table temporaire.

**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>« tmp. edb »</p> | 
| <p>Tapez :</p> | <p>Path (chaîne)</p> | 
| <p>Plage valide :</p> | <p>0 – 247 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Oui</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Non</p> | 
| <p>Affecte la disposition physique :</p> | <p>Oui</p> | 
| <p>Affecte la fiabilité :</p> | <p>Non</p> | 
| <p>Affecte les performances :</p> | <p>Non</p> | 
| <p>Affecte les ressources :</p> | <p>Non</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

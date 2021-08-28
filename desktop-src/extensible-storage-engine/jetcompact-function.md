---
description: 'En savoir plus sur : fonction JetCompact'
title: JetCompact fonction)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14e79ceda56658bf8b214fff923c2df17fe8f786
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480465"
---
# <a name="jetcompact-function"></a>JetCompact fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcompact-function"></a>JetCompact fonction)

La fonction **JetCompact** effectue une copie d’une base de données existante. La copie est compactée dans un état optimal pour l’utilisation. Les données dans les données copiées seront empaquetées en fonction des mesures choisies pour les index lors de la création de l’index. De cette façon, les données compactées peuvent être stockées aussi denses que possible. Les données compactées peuvent également réserver de l’espace pour la croissance des enregistrements ou les insertions d’index suivantes.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*szDatabaseSrc*

Base de données source qui sera compactée.

*szDatabaseDest*

Nom à utiliser pour la base de données compactée.

*pfnStatus*

Fonction de rappel qui peut être appelée régulièrement via l’opération de compactage de la base de données pour signaler la progression.

*pconvert*

Pointeur utilisé pour désigner une autre DLL ESE pouvant être utilisée pour lire la base de données source et pour fournir des paramètres facultatifs pour une opération **JetCompact** qui convertit une base de données d’un format antérieur à un format de version ultérieure. cette fonctionnalité a été supprimée dans Windows Server 2003.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitCompactRepair</p> | <p>Utilisé lorsque la base de données source est endommagée. Il active un ensemble complet de nouveaux comportements destinés à récupérer autant de données que possible à partir de la base de données source. <strong>JetCompact</strong> avec ce groupe d’options peut retourner JET_errSuccess mais pas copier toutes les données créées dans la base de données source. Les données qui étaient dans des parties endommagées de la base de données source seront ignorées.</p> | 
| <p>JET_bitCompactStats</p> | <p>Fait en sorte que <strong>JetCompact</strong> vide les statistiques de la base de données source vers un fichier nommé DFRGINFO.TXT. Les statistiques incluent le nom de chaque table dans la base de données source, le nombre de lignes dans chaque table, la taille totale, en octets, de toutes les lignes de chaque table, la taille totale en octets de toutes les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> qui étaient suffisamment volumineuses pour être stockées séparément de l’enregistrement, le nombre de pages de feuilles d’index cluster et le nombre de pages de En outre, les statistiques récapitulatives, y compris la taille de la base de données source, la base de données de destination, le temps requis pour le compactage de base de données, l’espace temporaire de la base de données sont également vidées.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Un pointeur <em>pconvert</em> non null a été fourni, mais la version de ESE utilisée ne prend pas en charge la fonctionnalité de conversion. cette fonctionnalité a été supprimée de la version 2003 du serveur Windows de ESE.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInTransaction</p> | <p>La session appelante est dans une transaction. <strong>JetCompact</strong> doit être appelé par une session en dehors d’une transaction.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, la base de données source est copiée dans la base de données de destination. La base de données de destination est dans un état optimal, par exemple, tous les index de table se trouvent dans l’espace disque logique adjacent. Chaque page d’index est remplie à la quantité configurée lorsque les index ont été créés à l’origine dans la base de données source. Tous les paramètres de données et de métadonnées sont copiés avec une fidélité complète, sauf si l’option de réparation a été spécifiée. Si l’option de réparation a été spécifiée, certaines données de la base de données source n’ont peut-être pas été copiées.

En cas d’échec, la base de données de destination peut exister, mais n’est pas une copie complète de la base de données source.

#### <a name="remarks"></a>Remarques

Le compactage d’une base de données est également utilisé pour mettre à niveau une base de données d’un format de version antérieure vers une version plus moderne. Un paramètre facultatif est *pconvert*, qui contient une structure qui peut contenir une description d’une dll de version antérieure à utiliser pour la lecture du format de base de données source. cette fonctionnalité a été supprimée dans Windows Server 2003. à la suite de Windows Server 2003, les nouvelles versions de ESE sont toujours en mesure de lire les anciennes versions du format de base de données. par conséquent, cette fonctionnalité n’est pas nécessaire.

La densité de données souhaitée après une opération compact est spécifiée lors de la création de tables et d’index. La densité doit être comprise entre 20% et 100%. Si une base de données est principalement lue et non mise à jour, les applications définissent la densité à 100% pour réduire le nombre d’opérations d’e/s lors du traitement des requêtes. Toutefois, si les données sont fréquemment mises à jour avec des opérations qui augmentent la taille des données stockées avec l’enregistrement, ou si de nouvelles données sont fréquemment insérées, l’application choisit une densité inférieure afin que les mises à jour trouvent les ressources nécessaires disponibles. Le fait de compacter la base de données rend la base de données idéalement imposée en fonction du remplissage choisi par l’application.

Le compactage de base de données est une opération hors connexion. Elle ne peut pas être effectuée tant que la base de données est en cours d’utilisation. En conséquence, elle est généralement effectuée dans le cadre d’un processus de génération de développement d’une application qui remet un jeu de données dans le cadre d’elle-même.

La compression de la base de données hors connexion touche chaque bit de données dans une base de données et peut être utilisée pour vérifier la cohérence d’une base de données. Si une base de données est suspecte, elle peut être compactée. Si aucune erreur n’est détectée dans le compactage, il est connu que la base de données est dans un état valide pour ESE.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetCompactW</strong> (Unicode) et <strong>JetCompactA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)

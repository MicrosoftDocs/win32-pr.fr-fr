---
description: L’action RemoveODBC supprime les sources de données, les traducteurs et les pilotes qui sont indiqués pour la suppression au cours de l’installation.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Action RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580429"
---
# <a name="removeodbc-action"></a>Action RemoveODBC

L’action RemoveODBC supprime les sources de données, les traducteurs et les pilotes qui sont indiqués pour la suppression au cours de l’installation. Cette action interroge la table [ODBCDataSource](odbcdatasource-table.md), la table [ODBCTranslator](odbctranslator-table.md)et la [table ODBCDriver](odbcdriver-table.md) pour chaque source de données, traducteur ou pilote dont la suppression est planifiée.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Pour chaque pilote installé.



| Champ | Description des données d’action               |
|-------|------------------------------------------|
| \[1\] | Description du pilote. Clé du pilote ODBC. |
| \[2\] | ComponentId                              |



 

Pour chaque traducteur installé.



| Champ | Description des données d’action               |
|-------|------------------------------------------|
| \[1\] | Description du pilote. Clé du pilote ODBC. |
| \[2\] | ComponentId                              |



 

Pour chaque source de données installée.



| Champ | Description des données d’action                              |
|-------|---------------------------------------------------------|
| \[1\] | Description du pilote. Clé du pilote ODBC.                |
| \[2\] | ComponentId                                             |
| \[3\] | inscription : SQL \_ supprimer le \_ dsn ou SQL \_ supprimer le \_ \_ dsn SYS |



 

## <a name="remarks"></a>Remarques

Si le nombre d’utilisations ODBC et le nombre d’utilisations de fichiers deviennent nuls, le fichier est supprimé. L’inscription dépend du nombre d’utilisations ODBC et la suppression des fichiers est basée sur les nombres de références de clé dll partagés.

 

 




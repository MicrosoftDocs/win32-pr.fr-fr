---
description: L’action RemoveODBC supprime les sources de données, les traducteurs et les pilotes qui sont indiqués pour la suppression au cours de l’installation.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Action RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524661"
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
| \[3\] | Inscription : SQL \_ Remove \_ DSN ou SQL \_ Remove \_ sys \_ DSN |



 

## <a name="remarks"></a>Notes

Si le nombre d’utilisations ODBC et le nombre d’utilisations de fichiers deviennent nuls, le fichier est supprimé. L’inscription dépend du nombre d’utilisations ODBC et la suppression des fichiers est basée sur les nombres de références de clé dll partagés.

 

 




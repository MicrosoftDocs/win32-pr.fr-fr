---
description: L’action SetODBCFolders recherche les pilotes ODBC existants sur le système et définit le répertoire cible de chaque nouveau pilote à l’emplacement d’un pilote existant.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Action SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628639"
---
# <a name="setodbcfolders-action"></a>Action SetODBCFolders

L’action SetODBCFolders recherche les pilotes ODBC existants sur le système et définit le répertoire cible de chaque nouveau pilote à l’emplacement d’un pilote existant.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action SetODBCFolders doit venir après l' [action CostFinalize](costfinalize-action.md) et avant l' [action InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Description du pilote. Clé du pilote ODBC.                                            |
| \[2\] | Emplacement du dossier d’origine du nouveau pilote.                                         |
| \[3\] | Nouvel emplacement du dossier pour le nouveau pilote. Il s’agit de l’emplacement d’un pilote existant. |



 

## <a name="remarks"></a>Remarques

Cette action place un nouveau pilote dans le même répertoire que le pilote existant en cours de remplacement. L’action SetODBCFolders utilise la [table Directory](directory-table.md) pour définir les emplacements des pilotes existants à remplacer.

 

 




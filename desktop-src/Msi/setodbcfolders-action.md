---
description: L’action SetODBCFolders recherche les pilotes ODBC existants sur le système et définit le répertoire cible de chaque nouveau pilote à l’emplacement d’un pilote existant.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Action SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238637"
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



 

## <a name="remarks"></a>Notes

Cette action place un nouveau pilote dans le même répertoire que le pilote existant en cours de remplacement. L’action SetODBCFolders utilise la [table Directory](directory-table.md) pour définir les emplacements des pilotes existants à remplacer.

 

 




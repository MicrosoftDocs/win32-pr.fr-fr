---
description: Entrez les enregistrements des cinq exemples d’actions personnalisées créés dans la section précédente dans la table CustomAction. Pour plus d’informations sur la façon de remplir la table CustomAction pour ce type d’action personnalisée, consultez action personnalisée type 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Création de la table CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951757"
---
# <a name="authoring-the-customaction-table"></a>Création de la table CustomAction

Entrez les enregistrements des cinq exemples d’actions personnalisées créés dans la section précédente dans la [table CustomAction](customaction-table.md). Pour plus d’informations sur la façon de remplir la table CustomAction pour ce type d’action personnalisée, consultez [action personnalisée type 1](custom-action-type-1.md).

[Table CustomAction](customaction-table.md)



| Action            | Type  | Source      | Cible                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

Le code source C++ pour les bibliothèques de liens dynamiques est fourni dans le kit de développement logiciel (SDK) Windows Installer. Utilisez Process. cpp pour créer le fichier Process.dll. Utilisez CREATE. cpp pour créer le fichier Create.dll. Utilisez Remove. cpp pour créer Remove.dll. Ajoutez ces fichiers de bibliothèque de liens dynamiques à la table binaire.

[Table binaire](binary-table.md)



| Nom        | Données            |
|-------------|-----------------|
| Process.dll | {*données binaires*} |
| Create.dll  | {*données binaires*} |
| Remove.dll  | {*données binaires*} |



 

Continuez à [Ajouter une table CustomUserAccounts personnalisée](adding-a-custom-customuseraccounts-table.md).

 

 




---
description: Entrez les enregistrements des cinq exemples d’actions personnalisées créés dans la section précédente dans la table CustomAction. Pour plus d’informations sur la façon de remplir la table CustomAction pour ce type d’action personnalisée, consultez action personnalisée type 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Création de la table CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b618da6e88718aa59483b3b25c007ff0b41eb89f6e1dc18a7eb31563632dc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066079"
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



 

le code source C++ pour les bibliothèques de liens dynamiques est fourni dans le kit de développement logiciel (SDK) Windows Installer. Utilisez Process. cpp pour créer le fichier Process.dll. Utilisez CREATE. cpp pour créer le fichier Create.dll. Utilisez Remove. cpp pour créer Remove.dll. Ajoutez ces fichiers de bibliothèque de liens dynamiques à la table binaire.

[Table binaire](binary-table.md)



| Nom        | Données            |
|-------------|-----------------|
| Process.dll | {*données binaires*} |
| Create.dll  | {*données binaires*} |
| Remove.dll  | {*données binaires*} |



 

Continuez à [Ajouter une table CustomUserAccounts personnalisée](adding-a-custom-customuseraccounts-table.md).

 

 




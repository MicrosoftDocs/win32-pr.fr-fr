---
description: Ajoutez toutes les propriétés de mot de passe de la table CustomUserAccounts à la propriété MsiHiddenProperties dans la table des propriétés.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sécurisation de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953168"
---
# <a name="securing-the-installation"></a>Sécurisation de l’installation

Ajoutez toutes les propriétés de mot de passe de la table CustomUserAccounts à la propriété [**MsiHiddenProperties**](msihiddenproperties.md) dans la [table des propriétés](property-table.md). Ajoutez également les noms des actions personnalisées différées à la propriété **MsiHiddenProperties** . Cela empêche le programme d’installation d’écrire les valeurs de propriété sensibles (les mots de passe) dans le journal et s’assure que ces valeurs ne sont pas journalisées lorsque les actions personnalisées différées utilisent les valeurs comme propriété CustomActionData.

Pour que le mot de passe de l’utilisateur soit disponible dans le service Windows Installer, la propriété de mot de passe doit être ajoutée à la propriété [**SecureCustomProperties**](securecustomproperties.md) .

[Table de propriétés](property-table.md)



| Propriété                                                 | Valeur                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Cela conclut l’exemple.

 

 




---
description: Windows Le programme d’installation fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Niveaux d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbe932ea10b62d20ca06a027b935ff04289cdef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478065"
---
# <a name="user-interface-levels"></a>Niveaux d’interface utilisateur

Windows Le programme d’installation fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité. Étant donné que l’interface utilisateur interne doit être créée par l’auteur du package, le comportement de l’interface utilisateur complète, de l’interface utilisateur réduite, de l’interface utilisateur de base et des niveaux aucun dépend du package d’installation. Le tableau suivant décrit les fonctionnalités généralement attribuées aux niveaux de l’interface utilisateur.




| Niveau d’interface utilisateur | Description | 
|----------|-------------|
| Interface utilisateur complète | Affiche les boîtes de dialogue modales et non modales qui ont été créées dans l’interface utilisateur interne. Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées.<blockquote>[!Note]<br />Les boîtes de dialogue modales nécessitent une entrée d’utilisateur pour que l’installation puisse continuer et sont spécifiées en définissant le <a href="modal-dialog-style-bit.md">bit de style de boîte de dialogue modale</a> dans la colonne attributs de la table de <a href="dialog-table.md">boîtes de dialogue</a> . Une boîte de dialogue non modale ne nécessite pas d’entrée d’utilisateur pour que l’installation se poursuive.</blockquote><br /> Une interface utilisateur complète présente généralement le comportement de l' <a href="user-interface-wizard-behavior.md">Assistant interface utilisateur</a>.<br /> | 
| Interface utilisateur réduite | Affiche toutes les boîtes de dialogue non modales qui ont été créées dans l’interface utilisateur. N’affiche pas de boîtes de dialogue modales créées. Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées. Affiche des messages d' <a href="authoring-disk-prompt-messages.md">invite de disque</a> . Affiche les boîtes de <a href="filesinuse-dialog.md">dialogue FilesInUse</a> . | 
| Interface utilisateur de base | Affiche les boîtes de dialogue non modales intégrées qui affichent les messages de progression. Affiche des boîtes de dialogue d’erreur intégrées. N’affiche pas de boîtes de dialogue créées. Invite les utilisateurs à insérer un disque en affichant une boîte de dialogue contenant la valeur de la propriété <a href="diskprompt.md"><strong>DiskPrompt</strong></a> . | 
| Aucun | None signifie une installation sans assistance qui n’affiche aucune interface utilisateur. | 




 

Le niveau de l’interface utilisateur interne peut être défini à l’aide de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Le programme d’installation définit la propriété [**UILevel**](uilevel.md) sur le niveau actuel de l’interface utilisateur.

Si la propriété [**LIMITUI**](limitui.md) est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.

Pour obtenir un exemple de création d’interface utilisateur, consultez [un exemple d’installation](an-installation-example.md).

 

 





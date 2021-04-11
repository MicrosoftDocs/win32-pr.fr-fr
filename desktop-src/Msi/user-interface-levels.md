---
description: Windows Installer fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Niveaux d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210764"
---
# <a name="user-interface-levels"></a>Niveaux d’interface utilisateur

Windows Installer fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité. Étant donné que l’interface utilisateur interne doit être créée par l’auteur du package, le comportement de l’interface utilisateur complète, de l’interface utilisateur réduite, de l’interface utilisateur de base et des niveaux aucun dépend du package d’installation. Le tableau suivant décrit les fonctionnalités généralement attribuées aux niveaux de l’interface utilisateur.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Niveau d’interface utilisateur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interface utilisateur complète</td>
<td>Affiche les boîtes de dialogue modales et non modales qui ont été créées dans l’interface utilisateur interne. Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées.
<blockquote>
[!Note]<br />
Les boîtes de dialogue modales nécessitent une entrée d’utilisateur pour que l’installation puisse continuer et sont spécifiées en définissant le <a href="modal-dialog-style-bit.md">bit de style de boîte de dialogue modale</a> dans la colonne attributs de la table de <a href="dialog-table.md">boîtes de dialogue</a> . Une boîte de dialogue non modale ne nécessite pas d’entrée d’utilisateur pour que l’installation se poursuive.
</blockquote>
<br/> Une interface utilisateur complète présente généralement le comportement de l' <a href="user-interface-wizard-behavior.md">Assistant interface utilisateur</a>.<br/></td>
</tr>
<tr class="even">
<td>Interface utilisateur réduite</td>
<td>Affiche toutes les boîtes de dialogue non modales qui ont été créées dans l’interface utilisateur. N’affiche pas de boîtes de dialogue modales créées. Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées. Affiche des messages d' <a href="authoring-disk-prompt-messages.md">invite de disque</a> . Affiche les boîtes de <a href="filesinuse-dialog.md">dialogue FilesInUse</a> .</td>
</tr>
<tr class="odd">
<td>Interface utilisateur de base</td>
<td>Affiche les boîtes de dialogue non modales intégrées qui affichent les messages de progression. Affiche des boîtes de dialogue d’erreur intégrées. N’affiche pas de boîtes de dialogue créées. Invite les utilisateurs à insérer un disque en affichant une boîte de dialogue contenant la valeur de la propriété <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</td>
</tr>
<tr class="even">
<td>Aucun</td>
<td>None signifie une installation sans assistance qui n’affiche aucune interface utilisateur.</td>
</tr>
</tbody>
</table>



 

Le niveau de l’interface utilisateur interne peut être défini à l’aide de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Le programme d’installation définit la propriété [**UILevel**](uilevel.md) sur le niveau actuel de l’interface utilisateur.

Si la propriété [**LIMITUI**](limitui.md) est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.

Pour obtenir un exemple de création d’interface utilisateur, consultez [un exemple d’installation](an-installation-example.md).

 

 





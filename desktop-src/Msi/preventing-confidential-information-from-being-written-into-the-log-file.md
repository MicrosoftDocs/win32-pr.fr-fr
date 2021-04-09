---
description: Les développeurs peuvent empêcher la saisie d’informations confidentielles, telles que les mots de passe, dans le fichier journal au cours d’une installation Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Empêcher l’écriture d’informations confidentielles dans le fichier journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034392"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Empêcher l’écriture d’informations confidentielles dans le fichier journal

Lorsque vous utilisez l’Windows Installer, vous pouvez empêcher que des informations confidentielles, par exemple des mots de passe, soient entrées dans le fichier journal et soient rendues visibles.

-   Le programme d’installation n’écrit jamais les informations de la colonne Password de la [table ServiceInstall](serviceinstall-table.md) dans le journal.
-   Vous pouvez empêcher le programme d’installation d’écrire la propriété associée à un [contrôle d’édition](edit-control.md) dans le journal en définissant l' [attribut de contrôle de mot de passe](password-control-attribute.md). La propriété associée à un contrôle d’édition avec l’attribut de contrôle de mot de passe est masquée même si la stratégie de [débogage](debug.md) est définie sur la valeur 7.
-   Vous pouvez empêcher le programme d’installation d’écrire une propriété privée dans le journal en incluant la propriété dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) .
    > [!Note]  
    > Cette méthode peut rendre les informations confidentielles entrées sur une ligne de commande visibles dans le journal. Lorsque la stratégie de [débogage](debug.md) est définie sur 7, le programme d’installation écrit les informations entrées sur une ligne de commande dans le journal. Cela rend la propriété entrée sur une ligne de commande visible, même si la propriété est incluse dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) .

     

-   Vous pouvez empêcher l’écriture dans le journal des informations contenues dans la colonne cible de la table [CustomAction](customaction-table.md) en incluant l’indicateur de bit HideTarget dans le champ type de la table CustomAction. La valeur de cet indicateur est 8192 (0x2000). Pour plus d’informations, consultez [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md).

 

 




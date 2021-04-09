---
description: Outre les informations abordées dans les sections précédentes, uisample.msi contient également des données pour un exemple d’interface utilisateur.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importation de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863038"
---
# <a name="importing-the-user-interface"></a>Importation de l’interface utilisateur

Outre les informations abordées dans les sections précédentes, uisample.msi contient également des données pour un exemple d’interface utilisateur. Si vous avez fusionné uisample.msi dans MNP2000.msi dans la section [importation d’une base de données vide](importing-a-blank-database.md), ces informations sont également présentes dans MNP2000.msi. Les informations de l’exemple d’interface utilisateur se trouvent dans les tableaux suivants.

-   [Table ActionText](actiontext-table.md)
-   [Table binaire](binary-table.md)
-   [Table de contrôle](control-table.md)
-   [Table ControlEvent,](controlevent-table.md)
-   [Table de boîtes de dialogue](dialog-table.md)
-   [Table des erreurs](error-table.md)
-   [Table EventMapping](eventmapping-table.md)
-   [Table RadioButton](radiobutton-table.md)
-   [Table TextStyle](textstyle-table.md)
-   [Table UIText](uitext-table.md)

L’éditeur de base de données Orca fourni avec le programme d’installation comprend une option d’aperçu de boîte de dialogue que vous pouvez utiliser pour afficher un aperçu des dialogues de l’interface utilisateur spécifiés par les données dans les tables ci-dessus.

L’exemple de package d’installation MNP2000.msi est maintenant prêt pour la validation du package. Exécutez toujours la validation sur un nouveau package avant d’essayer d’installer le package pour la première fois. Cela est décrit dans validation de l’exemple d’installation.

Si vous ne souhaitez pas inclure l’interface utilisateur dans l’exemple de package, omettez ou supprimez toutes les informations figurant dans les tableaux ci-dessus, à l’exception de la [table TextStyle](textstyle-table.md) (qui est nécessaire pour définir la propriété [**DefaultUIFont**](defaultuifont.md) ). Vous devez également supprimer les propriétés de l’interface utilisateur de la [table des propriétés](property-table.md). Un exemple de table de propriétés pour l’exemple Notepad, sans interface utilisateur, est illustré ci-dessous. Ne réutilisez pas les GUID indiqués dans le tableau si vous copiez cet exemple.

[Table de propriétés](property-table.md)



| Propriété                                   | Valeur                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Fabricant**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1033                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Un package sans interface utilisateur peut être installé à partir de la ligne de commande ou d’un programme. Pour installer un package à partir de la ligne de commande, utilisez les méthodes décrites dans [options de ligne de commande](command-line-options.md). Pour installer un package à partir d’un programme, utilisez les méthodes décrites dans [utilisation des fonctions de programme d’installation](using-installer-functions.md). Exécutez toujours la validation sur un nouveau package avant de tenter d’installer un nouveau package pour la première fois.

[Continuer](validating-an-installation-database.md)

 

 




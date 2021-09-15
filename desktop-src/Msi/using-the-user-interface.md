---
description: Cette section s’intéresse principalement à la façon dont les développeurs de packages d’installation créent une interface utilisateur d’installation à l’aide de la base de données du programme d’installation et de l’interface utilisateur interne.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Utilisation de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413916"
---
# <a name="using-the-user-interface"></a>Utilisation de l’interface utilisateur

Cette section s’intéresse principalement à la façon dont les développeurs de packages d’installation créent une interface utilisateur d’installation à l’aide de la base de données du programme d’installation et de l’interface utilisateur interne. Pour plus d’informations sur la différence entre une interface utilisateur interne et une interface utilisateur externe, consultez [à propos de l’interface utilisateur](about-the-user-interface.md).

Pour afficher une séquence de boîte de dialogue ou un panneau d’affichage au cours de l’installation, le nom de la boîte de dialogue doit être entré dans la colonne action de la table séquence d’action appropriée. Le nom de la boîte de dialogue doit apparaître dans la [table](adminuisequence-table.md) [InstallUISequence](installuisequence-table.md) ou AdminUISequence, selon que l’interface utilisateur est planifiée pour s’exécuter sous l’action d' [installation](install-action.md), de [publication](advertise-action.md)ou d' [administration](admin-action.md).

Bien que le programme d’installation prenne en charge la création de boîtes de dialogue et de panneaux personnalisés, il existe également un certain nombre de noms réservés pour certaines séquences de boîte de dialogue. Étant donné que le programme d’installation utilise ces noms lors de l’exécution de certaines actions, ces noms doivent uniquement être utilisés avec les types de boîtes de dialogue pour lesquels ils sont réservés. Une liste de ces noms réservés et une description de chacune des séquences de boîte de dialogue spéciales sont indiquées dans les [boîtes de dialogue](dialog-boxes.md).

Les propriétés de chaque boîte de dialogue ou de tous les panneaux de l’interface utilisateur doivent être spécifiés respectivement dans les tables [boîte de dialogue](dialog-table.md) et tableau [blanc](billboard-table.md) . Le style de chaque boîte de dialogue doit également être spécifié dans la table de boîte de dialogue en définissant l’indicateur [de bit de style de la boîte de dialogue](dialog-style-bits.md) .

Les contrôles et le texte doivent être ajoutés à la boîte de dialogue. ceux-ci doivent être liés à [ControlEvents](controlevent-overview.md)pour permettre à l’utilisateur d’interagir avec le processus d’installation. Pour plus d’informations sur l’ajout de contrôles à une boîte de dialogue [, consultez Ajout de contrôles et de texte](adding-controls-and-text.md) .

Windows Le gestionnaire d’interface utilisateur interne du programme d’installation peut afficher ou masquer des boîtes de dialogue de manière sélective pour contrôler le niveau d’interactivité de l’utilisateur final au cours de l’installation. Ces niveaux d’interactivité de l’utilisateur final sont appelés Full, Reduced, Basic et None. Consultez [niveaux d’interface utilisateur](user-interface-levels.md). pour obtenir une description complète de ces UIlevels.

Il existe deux méthodes pour définir le niveau de l’interface utilisateur. Le niveau de l’interface utilisateur peut être défini par programme avec un appel à [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui), et le premier paramètre de **MsiSetInternalUI** spécifie le niveau de l’interface utilisateur. Les développeurs de packages peuvent également définir le niveau d’interface utilisateur à l’aide de l' [option de ligne de commande](command-line-options.md) « /q ».

Le comportement de chaque niveau d’interface utilisateur est déterminé par la création du fichier de .msi par le développeur du package. L’auteur d’une interface utilisateur interne offre une grande flexibilité dans la façon dont ces niveaux se comportent pour un package. La disponibilité de ces niveaux dépend de la création du package d’installation. L’auteur doit spécifier toutes les boîtes de dialogue et tous les contrôles de l’interface utilisateur dans les tables de dialogue et de contrôle.

-   Une interface utilisateur complète présente généralement le comportement de l' [Assistant interface utilisateur](user-interface-wizard-behavior.md), comme chaque boîte de dialogue dans une séquence contenant un bouton **>>suivant** . Cette forme d’interface utilisateur est familière à de nombreux utilisateurs et est le type d’interface utilisateur le plus courant qu’un auteur peut créer. Le programme d’installation présente une séquence logique de boîtes de dialogue et invite l’utilisateur à interagir avec les contrôles situés dans chaque boîte de dialogue.
-   Une interface utilisateur réduite supprime généralement l’affichage du comportement de l’Assistant.
-   En général, une interface utilisateur de base affiche uniquement les messages de progression à l’utilisateur.
-   Le niveau d’interface utilisateur None signifie une installation sans assistance.

Windows Le programme d’installation fournit un indicateur de barre de progression unique dans le [contrôle ProgressBar](progressbar-control.md) qui affiche à l’utilisateur une estimation de la durée totale restante jusqu’à ce que l’installation soit terminée. Pour plus d’informations sur la barre de progression, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md).

Les auteurs de l’interface utilisateur doivent faciliter l’accessibilité de leur application ou de leur produit pour tous les utilisateurs. pour en savoir plus sur les Active Accessibility et les Windows Installer, consultez [accessibilité](accessibility.md).

Pour plus d’informations sur la création d’une interface utilisateur, consultez [Ajout de contrôles et de texte](adding-controls-and-text.md), [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md), [création de messages d’invite de disque](authoring-disk-prompt-messages.md), [création d’un conditionnel « Veuillez patienter... » MessageBox et en](authoring-a-conditional-please-wait-------message-box.md) [prévisualisation de l’interface utilisateur](previewing-the-user-interface.md). Pour plus d’informations sur les panneaux de création, consultez [affichage des panneaux dans une boîte de dialogue non modale](displaying-billboards-on-a-modeless-dialog.md)

à partir de Windows Installer 4,5, une interface utilisateur personnalisée peut être incorporée dans le package Windows Installer. Pour obtenir un exemple d’interface utilisateur personnalisée incorporée, consultez [utilisation d’une interface utilisateur incorporée](using-an-embedded-ui.md).

 

 




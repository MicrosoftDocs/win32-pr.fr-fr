---
description: Windows Le programme d’installation peut réparer, remplacer et vérifier les fichiers contenus dans une application. Une réinstallation partielle ou complète de l’application peut être nécessaire si des fichiers ou des entrées de Registre associés à une fonctionnalité sont manquants ou endommagés.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Réinstallation d’une fonctionnalité ou d’une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009672"
---
# <a name="reinstalling-a-feature-or-application"></a>Réinstallation d’une fonctionnalité ou d’une application

Windows Le programme d’installation peut réparer, remplacer et vérifier les fichiers contenus dans une application. Une réinstallation partielle ou complète de l’application peut être nécessaire si des fichiers ou des entrées de Registre associés à une fonctionnalité sont manquants ou endommagés.

Quand une fonctionnalité ou une application est réinstallée, tous les services, les variables d’environnement et les actions personnalisées appartenant à la fonctionnalité ou à l’application sont également réinstallés. Notez que cela signifie que toutes les modifications apportées aux variables d’environnement entre l’installation d’origine et la réinstallation sont perdues.

La liste suivante contient les méthodes de réinstallation d’une fonctionnalité ou d’un produit. Les deux premières méthodes ont été automatisées par le programme d’installation :

-   Réparez, remplacez ou vérifiez les fichiers en appelant la fonction [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) .
-   Réinstallez l’intégralité du produit en appelant la fonction [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) .
-   Réinstallez, remplacez ou vérifiez les fichiers avec un bouton de contrôle de l’interface utilisateur du programme d’installation via le [ControlEvent, réinstaller](reinstall-controlevent.md).
-   Réinstallez, remplacez ou vérifiez les fichiers à partir d’une ligne de commande en définissant les propriétés [**REINSTALL**](reinstall.md) et [**REINSTALLMODE**](reinstallmode.md) .

Pour plus d’informations sur la réinstallation d’une fonctionnalité ou d’une application, consultez [résilience](resiliency.md).

**Pour réinstaller un produit à l’aide du programme d’installation**

-   Appelez [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Pour réinstaller une fonctionnalité à l’aide du programme d’installation**

-   Appelez [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

**Pour réinstaller un produit ou une fonctionnalité à l’aide d’une interface utilisateur du programme d’installation**

1.  Ajoutez un bouton à la boîte de dialogue spécifiée en ajoutant une entrée à la [table de contrôle](control-table.md).
2.  Ajoutez un [ControlEvent, ReinstallMode](reinstallmode-controlevent.md) à la table ControlEvent,, avec les champs de boîte de dialogue \_ et de contrôle qui \_ référencent le contrôle Button créé à l’étape 1. Dans le champ argument, entrez une chaîne contenant les lettres correspondant aux modes de réinstallation souhaités (les valeurs acceptables pour ce champ sont identiques à celles acceptées pour la propriété [**REINSTALLMODE**](reinstallmode.md) ). La valeur dans la colonne classement de cet événement doit être 1.
3.  Ajoutez un événement de [réinstallation ControlEvent,](reinstall-controlevent.md) à la [table ControlEvent,](controlevent-table.md), en référençant à nouveau le même contrôle bouton. Le champ argument de cet événement est normalement ALL, pour forcer la réinstallation de toutes les fonctionnalités, mais vous pouvez placer le nom d’une fonctionnalité spécifique ici. La valeur dans la colonne classement de cet événement doit être 2.
4.  Ajoutez un événement supplémentaire lié au même contrôle de bouton pour lancer la réinstallation. Il peut s’agir d’un événement EndDialog (avec un argument Return). En général, toutefois, un événement NewDialog serait utilisé ici pour accéder à une boîte de dialogue **voulez-vous vraiment réinstaller ?** confirmer. La valeur dans la colonne classement de cet événement doit être 3.

    Si vous le souhaitez, plusieurs boutons de [**réinstallation**](reinstall.md) peuvent être créés pour une seule boîte de dialogue, ce qui permet à l’utilisateur de sélectionner le type de réinstallation effectué. Dans ce cas, chaque bouton est créé comme indiqué dans la procédure précédente, avec un autre paramètre [ControlEvent, ReinstallMode](reinstallmode-controlevent.md) pour chaque bouton.

Une fois qu’un produit particulier a été installé (avec une partie ou la totalité des fonctionnalités du produit), une réinstallation peut être effectuée à partir de la ligne de commande :

**Pour réinstaller un produit ou une fonctionnalité à partir d’une ligne de commande**

1.  À partir de l’invite de commandes, spécifiez la propriété [**réinstaller**](reinstall.md) .
2.  À partir de l’invite de commandes, spécifiez la propriété [**REINSTALLMODE**](reinstallmode.md) .

    La spécification de ces propriétés permet à l’utilisateur de réinstaller tout ou partie des fonctionnalités du produit. Le type de réinstallation peut également être spécifié. Par exemple, vous pouvez spécifier que seuls les fichiers qui sont complètement manquants doivent être réinstallés, ou que seuls les fichiers endommagés (par exemple, tout fichier exécutable dont le checksum ne correspond pas au contenu réel du fichier) soient remplacés.

 

 




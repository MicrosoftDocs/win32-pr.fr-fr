---
description: lorsque des privilèges élevés ne sont pas nécessaires pour installer un package Windows Installer, l’auteur du package peut supprimer la boîte de dialogue que le contrôle de compte d’utilisateur affiche pour inviter les utilisateurs à autoriser les utilisateurs à effectuer des autorisations d’administrateur.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Création de packages sans la boîte de dialogue UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064589a49327db263158b10ff9377e0f7b69232b0e3679d5bd86c7bd2f2e3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066089"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Création de packages sans la boîte de dialogue UAC

lorsque des privilèges élevés ne sont pas nécessaires pour installer un package Windows Installer, l’auteur du package peut supprimer la boîte de dialogue que le [*contrôle de compte d’utilisateur*](u-gly.md) affiche pour inviter les utilisateurs à autoriser les utilisateurs à effectuer des autorisations d’administrateur.

Pour supprimer l’affichage de la boîte de dialogue contrôle de compte d’utilisateur lors de l’installation de l’application, l’auteur du package doit effectuer les opérations suivantes :

-   installez l’application à l’aide du programme d’installation de windows 4,0 ou version ultérieure sur Windows Vista.
-   Ne dépendez pas de l’utilisation de privilèges système élevés pour installer l’application sur l’ordinateur.
-   Installez l’application dans le contexte par utilisateur et faites-en le contexte d’installation par défaut du package. Si la propriété [**ALLUSERS**](allusers.md) n’est pas définie, le programme d’installation installe le package dans le contexte par utilisateur. Si vous n’incluez pas la propriété **ALLUSERS** dans la [table de propriétés](property-table.md), le programme d’installation ne définit pas cette propriété et, par conséquent, l’installation par utilisateur devient le contexte d’installation par défaut. Vous pouvez remplacer cette valeur par défaut en définissant la propriété **ALLUSERS** sur la ligne de commande.
-   Définissez le bit 3 dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) pour indiquer que les privilèges élevés ne sont pas nécessaires pour installer l’application.

 

 




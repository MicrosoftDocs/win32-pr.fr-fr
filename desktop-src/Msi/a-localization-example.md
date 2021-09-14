---
description: cet exemple montre comment localiser le package Windows Installer décrit dans un exemple d’Installation. Le package d’installation d’origine passe d’une version anglaise à une version en langue française.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Exemple de localisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092974"
---
# <a name="a-localization-example"></a>Exemple de localisation

cet exemple montre comment localiser le package Windows Installer décrit dans [un exemple d’Installation](an-installation-example.md). Le package d’installation d’origine passe d’une version anglaise à une version en langue française.

L’exemple Localization présente les spécifications suivantes :

-   L’interface utilisateur d’installation de l’application MNP2000 doit passer de l’anglais au français.
-   La version française de MNP2000 comprend des fichiers Readme.txt et Help.txt écrits en français.
-   La version française comprend une liste d’agents de voyage en France qui peuvent fournir des tickets à la place de parc rouge. Cette liste (fournie sous la forme d’un nouveau fichier, Fre.txt) ne fait pas partie de la version anglaise.

la procédure générale pour la localisation d’une installation est décrite dans la section [localizing a Windows Installer Package](localizing-a-windows-installer-package.md).

Copiez la version anglaise de MNP2000.msi et tous les fichiers sources décrits dans [planification de l’installation](planning-the-installation.md) dans un nouveau dossier. Remplacez le nom de l' MNP2000.msi dans le dossier par MNPFren.msi. Dans les sections suivantes, vous allez modifier cette copie pour localiser l’application en français.

[Continuer](checking-the-installation-database-code-page.md)

 

 




---
description: La section d’installation d’un fichier INF définit les étapes de la procédure d’installation.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Exemple de section d’installation INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543728"
---
# <a name="inf-install-section-example"></a>Exemple de section d’installation INF

La **section d’installation d'** un fichier INF définit les étapes de la procédure d’installation. Chaque ligne d’une section d' **installation** comporte deux parties. À gauche du signe égal (=) est la clé. Sur le côté droit, est une liste d’un ou plusieurs titres de section. La clé spécifie le type des sections répertoriées à droite. Pour obtenir une description du format de cette section, consultez les sections et les directives du fichier INF du kit de développement de pilotes Microsoft Windows 2000.

Voici un exemple de section d' **installation** .

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

Dans cet exemple, la clé **CopyFiles** est définie sur les valeurs « fichiers de fichiers » et « ProgramFiles ». Cela spécifie deux sections de **fichiers de copie** dans le fichier INF qui contiennent les noms des fichiers sources utilisés par les opérations de copie. La destination des fichiers copiés est spécifiée dans une section **DestinationDirs** dans le fichier INF.

La clé **DelFiles** reçoit la valeur « OldFiles ». Cela spécifie une section de **Suppression de fichiers** qui contient des informations relatives aux opérations de suppression de fichiers.

La clé **UpdateInis** spécifie la **mise à jour** des sections du fichier ini qui contiennent des informations sur la mise à jour des entrées dans le fichier ini.

Les clés **AddReg** et **DelReg** spécifient des sections **Add Registry** et **Delete Registry** qui contiennent des informations sur l’ajout ou la suppression d’informations de registre.

 

 




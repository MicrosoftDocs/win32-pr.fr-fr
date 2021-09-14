---
description: si un seul des fichiers a un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Un fichier a une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218932"
---
# <a name="one-file-has-a-version"></a>Un fichier a une version

Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.

Si un seul des fichiers a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de déroulement suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant. Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.

Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) . La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

![règles de contrôle de version de fichier par défaut lorsqu’un seul fichier a un numéro de version](images/waiflow3.png)

Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).

-   [Les deux fichiers ont une version](both-files-have-a-version.md)
-   [Aucun fichier n’a une version](neither-file-has-a-version.md)
-   [Aucun fichier n’a une version avec contrôle de hachage de fichier](neither-file-has-a-version-with-file-hash-check.md)

 

 




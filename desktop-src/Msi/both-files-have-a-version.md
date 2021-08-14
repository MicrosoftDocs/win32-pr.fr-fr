---
description: si les deux fichiers ont un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Les deux fichiers ont une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380800"
---
# <a name="both-files-have-a-version"></a>Les deux fichiers ont une version

Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version et la langue des deux fichiers.

Si les deux fichiers ont un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant. Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.

Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) . La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

![règles de contrôle de version des fichiers par défaut lorsque les deux fichiers portent le même nom ou le même numéro de version](images/waiflow1.png)

Le diagramme précédent peut également être utilisé avec des fichiers sans langue spécifiée. Si Copy-a a un langage spécifié et que Copy-B n’a pas de langue spécifiée, Copy-B est remplacé par Copy-A. Si Copy-A et Copy-B n’ont aucune langue spécifiée, Copy-B n’est pas remplacé.

Consultez des exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).

-   [Aucun fichier n’a une version](neither-file-has-a-version.md)
-   [Aucun fichier n’a une version avec contrôle de hachage de fichier](neither-file-has-a-version-with-file-hash-check.md)
-   [Un fichier a une version](one-file-has-a-version.md)

 

 




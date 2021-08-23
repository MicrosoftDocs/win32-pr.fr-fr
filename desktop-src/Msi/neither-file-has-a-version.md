---
description: si aucun fichier n’a un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Aucun fichier n’a une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065932"
---
# <a name="neither-file-has-a-version"></a>Aucun fichier n’a une version

Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.

Si aucun fichier n’a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant. Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.

Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) . La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

![règles de contrôle de version des fichiers par défaut lorsque aucun fichier ne possède un numéro de version](images/waiflow2.png)

Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).

-   [Les deux fichiers ont une version](both-files-have-a-version.md)
-   [Aucun fichier n’a une version avec contrôle de hachage de fichier](neither-file-has-a-version-with-file-hash-check.md)
-   [Un fichier a une version](one-file-has-a-version.md)

 

 




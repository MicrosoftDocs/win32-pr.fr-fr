---
description: le hachage de fichier est disponible avec Windows Installer. Pour plus d’informations, consultez MsiGetFileHash et la table MsiFileHash. La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Aucun fichier n’a une version avec contrôle de hachage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869193"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Aucun fichier n’a une version avec contrôle de hachage de fichier

le hachage de fichier est disponible avec Windows Installer. Pour plus d’informations, consultez [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) et la [table MsiFileHash](msifilehash-table.md). La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.

Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.

Si aucun fichier n’a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant. Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.

Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) . La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

![règles de contrôle de version des fichiers par défaut en cas de substitution par le paramètre de propriété REINSTALLMODE](images/waiflow2b.png)

Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).

-   [Les deux fichiers ont une version](both-files-have-a-version.md)
-   [Aucun fichier n’a une version](neither-file-has-a-version.md)
-   [Un fichier a une version](one-file-has-a-version.md)

 

 




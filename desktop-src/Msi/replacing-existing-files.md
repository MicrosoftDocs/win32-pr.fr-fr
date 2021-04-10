---
description: Étant donné que la copie de fichiers inutile ralentit une installation, le Windows Installer détermine si le fichier de clé du composant est déjà installé avant de tenter d’installer les fichiers de n’importe quel composant.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Remplacement des fichiers existants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866073"
---
# <a name="replacing-existing-files"></a>Remplacement des fichiers existants

Étant donné que la copie de fichiers inutile ralentit une installation, le Windows Installer détermine si le fichier de clé du composant est déjà installé avant de tenter d’installer les fichiers de n’importe quel composant. Si le programme d’installation trouve un fichier portant le même nom que le fichier de clé du composant installé à l’emplacement cible, il compare la version, la date et la langue des deux fichiers de clé et utilise des règles de contrôle de version de fichier pour déterminer s’il faut installer le composant fourni par le package. Si le programme d’installation détermine qu’il doit remplacer la base de composants sur le fichier de clé, il utilise les règles de contrôle de version de fichier sur chaque fichier installé pour déterminer s’il faut remplacer le fichier.

Notez que lorsque vous créez un package d’installation avec des fichiers avec version, la chaîne de version dans la colonne version de la [table file](file-table.md) doit toujours être identique à la version du fichier inclus dans le package.

Les règles de contrôle de version de fichier par défaut peuvent être remplacées ou modifiées à l’aide de la propriété [**REINSTALLMODE**](reinstallmode.md) . Le programme d’installation utilise les règles de contrôle de version de fichier spécifiées par la propriété **REINSTALLMODE** lors de l’installation, de la réinstallation ou de la réparation d’un fichier. L’exemple suivant montre comment le programme d’installation applique les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut. La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

Les fichiers de clé de composant suivants sont installés sur le système avant la réinstallation du composant.



| Fichier                                    | Version  | Date de création | Date de modification | Language    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| Filea                                   | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| Classer                                   | 1.0.0000 | 1/1/99      | 1/2/99        | FR         |
| Fichier                                   | aucun     | 1/1/99      | 1/1/99        | aucun        |
| FileF (modifié > créer)<br/> | aucun     | 1/1/99      | 1/2/99        | aucun        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Fichier                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

Les fichiers de clé de composant suivants sont inclus dans le package d’installation.



| Fichier                               | Version  | Date de création | Date de modification | Language    |
|------------------------------------|----------|-------------|---------------|-------------|
| Filea (marquée comme identique)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileB (version antérieure)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileC (version ultérieure)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | FR         |
| Archivé (version ultérieure)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Fichier (identique)<br/>     | aucun     | 1/1/99      | 1/1/99        | aucun        |
| FileF (nouveau fichier)<br/>        | aucun     | 1/3/99      | 1/3/99        | aucun        |
| FileG (nouveau langage)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (nouveau langage)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, GER |
| Fichieri (plus de langues)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (moins de langues)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | Windows ger         |



 

Les fichiers de clé de composant suivants restent sur le système une fois le composant réinstallé. L’état du fichier de clé détermine l’état de tous les autres fichiers du composant.



| Fichier                | Version  | Date de création | Date de modification | Language    |
|---------------------|----------|-------------|---------------|-------------|
| Fichier (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileB (original)    | 2.0.0000 | 1/1/99      | 1/1/99        | FR         |
| FileC (remplacement) | 2.0.0000 | 1/1/99      | 1/1/99        | FR         |
| Archivé (remplacement) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Fichier (remplacement) | aucun     | 1/1/99      | 1/1/99        | aucun        |
| FileF (original)    | aucun     | 1/1/99      | 1/2/99        | aucun        |
| FileG (remplacement) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (remplacement) | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, GER |
| Fichieri (remplacement) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérification des CRC au cours d’une installation](crc-checking-during-an-installation.md)
</dt> </dl>

 

 





---
description: Les diagrammes de flow des sections suivantes illustrent les règles de contrôle de version de fichier par défaut utilisées lorsque le fichier de clé d’un composant en cours d’installation a le même nom qu’un fichier déjà installé à l’emplacement cible.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Contrôle de version de fichier par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866361"
---
# <a name="default-file-versioning"></a>Contrôle de version de fichier par défaut

Les diagrammes de flow des sections suivantes illustrent les règles de contrôle de version de fichier par défaut utilisées lorsque le fichier de clé d’un composant en cours d’installation a le même nom qu’un fichier déjà installé à l’emplacement cible. Le contrôle de version de fichier par défaut est également illustré dans le [remplacement de fichiers existants](replacing-existing-files.md).

Notez qu’avec Windows Installer, le hachage de fichier est disponible pour optimiser la copie des fichiers. Pour plus d’informations, consultez [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) et la [table MsiFileHash](msifilehash-table.md). La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.

-   [Les deux fichiers ont une version](both-files-have-a-version.md)
-   [Aucun fichier n’a une version](neither-file-has-a-version.md)
-   [Aucun fichier n’a une version avec contrôle de hachage de fichier](neither-file-has-a-version-with-file-hash-check.md)
-   [Un fichier a une version](one-file-has-a-version.md)

 

 




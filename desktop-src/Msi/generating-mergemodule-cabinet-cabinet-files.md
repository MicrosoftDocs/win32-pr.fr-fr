---
description: Chaque fichier qui est remis au package d’installation cible par le module de fusion doit être stocké dans un fichier CAB incorporé en tant que flux à l’intérieur du fichier. msm. Le nom de ce fichier cab est toujours MergeModule. cab.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Génération de fichiers CAB MergeModule. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021686"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Génération de fichiers CAB MergeModule. cab

Chaque fichier qui est remis au package d’installation cible par le module de fusion doit être stocké dans un fichier CAB incorporé en tant que flux à l’intérieur du fichier. msm. Le nom de ce fichier cab est toujours MergeModule. cab.

Les noms des fichiers dans MergeModule. cab doivent correspondre aux clés primaires utilisées dans la [table de fichiers](file-table.md) du module de fusion et doivent respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).

Le programme d’installation ignore les fichiers supplémentaires inclus dans MergeModule. cab qui ne sont pas répertoriés dans la [table de fichiers](file-table.md)du module de fusion. Les numéros de séquence des fichiers spécifiés dans la table de fichiers n’ont pas besoin d’être consécutifs, mais ils doivent suivre la même séquence que les fichiers stockés dans MergeModule. cab. Pour plus d’informations, consultez [création de tables de fichiers de module de fusion](authoring-merge-module-file-tables.md).

Cela signifie qu’un seul fichier CAB peut contenir tous les fichiers nécessaires à un module de fusion pour prendre en charge plusieurs langues. Tous les fichiers de langue peuvent recevoir des numéros séquentiels uniques dans le fichier CAB, puis une transformation de langue peut être utilisée pour ajouter ou supprimer des fichiers dans la table file afin d’obtenir un module de fusion pour une langue particulière. Pour plus d’informations, consultez [création de modules de fusion multilingues](authoring-multiple-language-merge-modules.md).

MergeModule. cab peut être ajouté au module de fusion en ouvrant une [ \_ Table de Flux](-streams-table.md)temporaire. par exemple, l’outil Msidb.exe fourni avec le kit de développement logiciel (SDK) Windows Installer peut être utilisé pour ajouter MergeModule. CABinet au module de fusion. Pour plus d’informations, consultez [inclusion d’un fichier cab dans une installation](including-a-cabinet-file-in-an-installation.md).

 

 




---
description: Une table de fichiers est requise dans chaque module de fusion et doit avoir un enregistrement pour chaque fichier qui est remis au package d’installation cible par le module de fusion.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Création de tables de fichier de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092493"
---
# <a name="authoring-merge-module-file-tables"></a>Création de tables de fichier de module de fusion

Une [table de fichiers](file-table.md) est requise dans chaque module de fusion et doit avoir un enregistrement pour chaque fichier qui est remis au package d’installation cible par le module de fusion. Lorsque le module de fusion est fusionné dans un fichier .msi, chaque fichier de la table de fichier de module de fusion est stocké dans un [*fichier CAB*](c-gly.md) dans le fichier. msm. Le nom du fichier cab dans un module de fusion est toujours le suivant : MergeModule. CABinet.

Pour plus d’informations, consultez [génération de fichiers CAB MergeModule. cab](generating-mergemodule-cabinet-cabinet-files.md).

-   Étant donné que les fichiers d’un module de fusion sont toujours stockés dans un fichier CAB, il n’est pas nécessaire de définir les indicateurs de bits **msidbFileAttributesNoncompressed** ou **msidbFileAttributesCompressed** dans la colonne attributs de la [table file](file-table.md).
-   Les noms des fichiers dans MergeModule. cab doivent correspondre à la clé primaire de la table de [fichiers](file-table.md)du module de fusion.

    La colonne de fichier est la clé primaire de la [table de fichiers](file-table.md) et les entrées de ce champ doivent respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).

-   Les numéros de séquence de fichiers sont spécifiés dans la colonne séquence de la [table file](file-table.md).

    Les fichiers doivent être répertoriés dans la [table de fichiers](file-table.md) du module de fusion dans l’ordre dans lequel ils sont stockés dans MergeModule. cab. Les numéros de séquence des fichiers n’ont pas besoin d’être consécutifs, mais ils doivent suivre la même séquence que les fichiers qui sont stockés dans le fichier CAB. Par exemple, les premier, deuxième et troisième fichiers stockés dans le fichier CAB peuvent avoir les numéros de séquence 100, 200 et 300.

-   Le programme d’installation ignore les fichiers supplémentaires inclus dans MergeModule. cab qui ne sont pas répertoriés dans la [table de fichiers](file-table.md).

    Un fichier CAB peut contenir tous les fichiers nécessaires pour un module de fusion qui prend en charge plusieurs langues à l’aide de transformations. Tous les fichiers de langue peuvent recevoir un numéro de séquence unique dans le fichier CAB, puis une transformation peut ajouter ou supprimer des fichiers dans la [table de fichiers](file-table.md) si nécessaire pour une langue spécifique. Pour plus d’informations, consultez [création de modules de fusion multilingues](authoring-multiple-language-merge-modules.md).

Pour plus d’informations, consultez [table file](file-table.md).

 

 




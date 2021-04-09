---
description: Un module de fusion peut être appliqué à un fichier. msi pour ajouter des répertoires à l’installation, mais il ne peut pas remplacer ou supprimer des répertoires existants.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Création de tables de répertoires de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98332f2c0bda10a5cc076f0ec80df3bf4b2e05aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864457"
---
# <a name="authoring-merge-module-directory-tables"></a>Création de tables de répertoires de module de fusion

Un module de fusion peut être appliqué à un fichier. msi pour ajouter des répertoires à l’installation, mais il ne peut pas remplacer ou supprimer des répertoires existants. La [table Directory](directory-table.md) spécifie la disposition des répertoires fournis par le module de fusion à l’installation cible. Une table de répertoire est requise dans chaque module de fusion.

Utilisez les instructions suivantes lors de la création de la table de répertoires dans un module de fusion. Pour plus d’informations, consultez la [table Directory](directory-table.md) et l' [utilisation de la table Directory](using-the-directory-table.md).

-   La structure de répertoire ajoutée par le module de fusion doit avoir un répertoire racine unique. La racine doit être nommée TARGETDIR. L’utilisateur peut modifier la valeur de TARGETDIR pendant la fusion pour spécifier l’emplacement d’attachement de la structure de répertoire du module dans l’arborescence de répertoires de la cible.
-   Les tables de module de fusion autres que la table de répertoire ne doivent pas référencer directement les emplacements de répertoires à TARGETDIR. L’emplacement d’une telle référence change si la valeur de TARGETDIR est modifiée par l’utilisateur.
-   Les tables du module de fusion doivent référencer l’emplacement d’un répertoire enfant de TARGETDIR, ou un autre répertoire de l’arborescence du module de fusion. Procédez comme suit pour spécifier TARGETDIR comme parent d’un répertoire dans le module de fusion. Entrez le répertoire dans la colonne répertoire et entrez TARGETDIR dans la \_ colonne parent du répertoire. Utilisez la notation « . » dans la colonne DefaultDir pour indiquer que ce répertoire se trouve dans TARGETDIR sans sous-répertoire. Pour plus d’informations, consultez [utilisation de la table des répertoires](using-the-directory-table.md).
-   Les noms des répertoires ajoutés par le module de fusion doivent utiliser les conventions d’affectation des noms décrites dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md). Cela comprend les répertoires prédéfinis par des propriétés telles que la propriété [**SystemFolder**](systemfolder.md) et la propriété [**ProgramFilesFolder**](programfilesfolder.md) .
-   Ajoutez un [*GUID*](g-gly.md) à chaque entrée de la table Directory (sauf TARGETDIR.) Cela comprend les entrées de table de répertoire qui spécifient Windows Installer propriétés [**SystemFolder**](systemfolder.md) , par exemple, SystemFolder. 00000000 0000 0000 0000 \_ \_ \_ \_ 000000000000. La bibliothèque Mergemod.dll ajoute des actions personnalisées pour définir la propriété **SystemFolder** .
-   Lorsqu’un répertoire prédéfini est inclus dans un module de fusion, l’outil de fusion ajoute automatiquement un [type d’action personnalisé 51](custom-action-type-51.md) à la base de données cible. L’auteur du module de fusion doit s’assurer qu’une [table CustomAction](customaction-table.md) est également incluse. La table CustomAction peut être vide, mais cette table doit exister dans la base de données cible et s’assurer que les répertoires prédéfinis modifiés sont écrits dans les emplacements appropriés. Par exemple, lorsqu’un répertoire système est inclus dans un module de fusion, l’auteur du module de fusion doit s’assurer qu’il existe une table d’actions personnalisée.

    Notez que l’algorithme correspondant pour la génération de ces types d’actions personnalisées 51 vérifie uniquement que le nom du répertoire commence par l’une des propriétés [**SystemFolder**](systemfolder.md) prédéfinies. Il ne vérifie pas que le nom du répertoire est exactement égal à la propriété Directory. Tout répertoire commençant par l’un de ces noms de dossiers standard obtient une action personnalisée de type 51, même si le reste du nom n’est pas un GUID. Les auteurs doivent veiller à ce que cela ne génère pas de correspondances de faux positifs, ni de génération d’actions personnalisées imprévues, sur les clés primaires dérivées qui commencent par l’une des propriétés **SystemFolder** .

Voici un exemple de table de répertoire dans un module de fusion et des répertoires résolus attendus.



| Répertoire                                              | Répertoire \_ parent                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | TARGETDIR                                        | . : Programme \_ MMM |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | TARGETDIR                                        | Système \_ MMM    |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848 \_ 006097ABDE17 | \_ocx MFC    |



 

Un module de fusion avec la table de répertoire ci-dessus est censé générer la structure de répertoire suivante.



| Répertoire                                              | Cible                                     | Source                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[Point d’installation du module de fusion\]\\         | \[Programme MMM de point source du module de fusion \] \\ \_           |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[Point source du module de fusion \] \\ MMM \_ sys            |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[\] \\ MFC ocx du point d’installation du module de fusion \_ | \[Point source du module de fusion de l' \] \\ \_ \\ ocx MFC PROG \_ |



 

 

 




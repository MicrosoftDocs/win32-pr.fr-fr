---
description: Le type de données mis en forme est une chaîne de texte qui est traitée pour résoudre les noms de propriétés incorporées, les clés de table, les références de variable d’environnement et d’autres sous-chaînes spéciales.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Mis en forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952301"
---
# <a name="formatted"></a>Mis en forme

Le type de données mis en forme est une chaîne de texte qui est traitée pour résoudre les noms de propriétés incorporées, les clés de table, les références de variable d’environnement et d’autres sous-chaînes spéciales. Les conventions suivantes sont reconnues pour résoudre la chaîne :

-   Les crochets ( \[ \] ) ou les accolades ({}) sans paire correspondante restent dans le texte.
-   Si une sous-chaîne du formulaire \[ *PropertyName* \] est rencontrée, elle est remplacée par la valeur de la propriété. Si *PropertyName* n’est pas un nom de propriété valide, la sous-chaîne se résout comme vide. Par exemple, la colonne Description de la [table LaunchCondition](launchcondition-table.md) prend une chaîne mise en forme. Si ERRORTXT a été défini sur « veuillez contacter votre service de support technique ». le texte affiché pour l’échec de la condition de lancement inclut cette chaîne. Si ERRORTXT n’est pas défini, le texte affiché pour l’échec de la condition de lancement est simplement « le système ne répond pas à la configuration requise pour l’installation. »

    

    | Condition | Description                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | Le système ne répond pas à la configuration requise pour l’installation. \[ERRORTXT\] |

    

     

-   Les crochets peuvent être itérés et les noms de propriété sont résolus de l’intérieur vers l’extérieur. Par exemple, supposons que la propriété SUBSTRING est \[ \[ \] \] affichée dans le texte. Tout d’abord, la valeur de Property PropertyA est récupérée. Si la valeur est un nom de propriété valide, tel que PropertyB, la valeur de PropertyB est récupérée, et la propriété de la sous-chaîne entière \[ \[ \] \] est remplacée par la valeur de PropertyB. Si PropertyA n’est pas un nom de propriété valide, ou si la valeur de PropertyA n’est pas un nom de propriété valide, la sous-chaîne est vide.
-   Si une sous-chaîne du formulaire \[ % *EnvironmentVariable* \] est trouvée, la valeur de la variable d’environnement est substituée à la sous-chaîne.
-   Si une sous-chaîne du formulaire \[ \\ *x* \] est trouvée, elle est remplacée par le caractère *x* , où *x* est un caractère, sans traitement supplémentaire. Seul le premier caractère après la barre oblique inverse est conservé ; tout le reste est supprimé. Par exemple, pour inclure un crochet gauche littéral ( \[ ), utilisez \[ \\ \[ \] . Le \[ \\ \[ \] texte du crochet de texte est \[ \\ \] \] résolu en \[ texte entre crochets \] .
-   Si une sous-chaîne est entourée d’accolades ({}) et qu’elle ne contient pas de noms de propriété entre crochets ( \[ \] ), la sous-chaîne reste inchangée, y compris les accolades.
-   Si une sous-chaîne est placée entre accolades ({}) et qu’elle contient un ou plusieurs noms de propriété entre crochets ( \[ \] ), si tous les noms de propriétés sont valides, le texte (avec les substitutions résolues) s’affiche sans les accolades.
-   Si une sous-chaîne du formulaire \[ ~ \] est trouvée, elle est remplacée par le caractère null. Il est utilisé pour créer des chaînes de caractères **\_ \_ multiszs reg** dans la [table du Registre](registry-table.md). Notez que \[ ~ \] est également utilisé pour ajouter ou préfixer des valeurs à des variables d’environnement à l’aide de la [table d’environnement](environment-table.md).
-   Si une sous-chaîne du formulaire \[ \# *filekey* \] est trouvée, elle est remplacée par le chemin d’accès complet du fichier, avec la valeur *filekey* utilisée comme clé dans la [table de fichiers](file-table.md). La valeur de \[ \# *filekey* \] reste vide et n’est pas remplacée par un chemin d’accès jusqu’à ce que le programme d’installation exécute l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md). La valeur de \[ \# *filekey* \] dépend de l’état d’installation du composant auquel le fichier appartient. Si le composant est exécuté à partir de la source, la valeur est le chemin d’accès à l’emplacement source du fichier. Si le composant est exécuté localement, la valeur est le chemin d’accès à l’emplacement cible du fichier après l’installation. Si l’état d’action du composant est absent, l’état installé du composant est utilisé pour déterminer le \[ \) .
-   Si une sous-chaîne du formulaire \[ $ *componentkey* \] est trouvée, elle est remplacée par le répertoire d’installation du composant, avec la valeur *componentkey* utilisée comme clé dans la [table des composants](component-table.md). La valeur de \[ $ *componentkey* \] reste vide et n’est pas remplacée par un répertoire tant que le programme d’installation n’a pas exécuté l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md). La valeur de \[ $ *componentkey* \] dépend de l’état d’installation du composant et de l’emplacement où il se produit. Dans la colonne valeur de la [table du Registre](registry-table.md), cette sous-chaîne peut faire référence à l’état de l’action ou à l’état d’action demandé du composant. Dans tous les autres cas, cette sous-chaîne fait référence à l’état d’action du composant. Par exemple, si le composant est exécuté à partir de la source, la valeur est le répertoire source du fichier. Si le composant est exécuté localement, la valeur est le répertoire cible après l’installation. Si le composant est absent, la valeur est laissée vide. Windows Installer effectue le suivi des États de l’action et de l’installation demandée des composants. Par exemple, si un composant est déjà installé, il peut avoir l’état local demandé et un état d’action null. Pour plus d’informations sur la vérification de l’état d’installation des composants, consultez [vérification de l’installation de fonctionnalités, de composants et de fichiers](checking-the-installation-of-features-components-files.md).
-   Notez que si un composant est déjà installé et qu’il n’est pas réinstallé, supprimé ou déplacé au cours de l’installation actuelle, l’état d’action du composant est null et la chaîne \[ $ *componentkey* \] prend la valeur null.
-   Si une sous-chaîne du formulaire \[ !*filekey* \] est trouvé, il est remplacé par le chemin d’accès complet du fichier, avec la valeur *filekey* utilisée comme clé dans la [table de fichiers](file-table.md).

    Cette syntaxe est valide uniquement lorsqu’elle est utilisée dans la colonne valeur du registre ou dans les tables IniFile. En cas d’utilisation dans d’autres colonnes, cette syntaxe est traitée de la même façon que \[ \# *filekey* \] .

 

 




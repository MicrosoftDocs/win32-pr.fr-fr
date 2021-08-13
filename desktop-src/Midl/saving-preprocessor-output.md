---
title: Enregistrement de la sortie du préprocesseur
description: L’affichage de la sortie du préprocesseur peut être une méthode de résolution des problèmes efficace, par exemple quand une syntaxe de préprocesseur IDL, C ou C non valide se produit, ou lorsque des valeurs factices-D sur la ligne de commande MIDL génèrent des erreurs obscures de création de rapports.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL du compilateur MIDL, enregistrement de la sortie du préprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f016885ac4d669d7b62eaf3ff1d5ee3154f03d5eae64fca5f63c6111dff4c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641374"
---
# <a name="saving-preprocessor-output"></a>Enregistrement de la sortie du préprocesseur

L’affichage de la sortie du préprocesseur peut être une méthode de résolution des problèmes efficace, par exemple quand une syntaxe de préprocesseur IDL, C ou C non valide se produit, ou lorsque des valeurs factices-D sur la ligne de commande MIDL génèrent des erreurs obscures de création de rapports. Les développeurs peuvent également examiner la sortie du préprocesseur pour déterminer les fichiers et définitions qui étaient présents dans le flux d’entrée du compilateur, par exemple lorsqu’une casse difficile de conflit de redéfinition de type doit être résolue. Ou moins souvent, certains développeurs peuvent vouloir forcer des commutateurs privés sur le préprocesseur avec [**/CPP \_ OPT**](-cpp-opt.md), ou peuvent souhaiter voir le fonctionnement des commutateurs.

Le moyen le plus simple et le moins gênant d’obtenir les fichiers prétraités à partir d’une exécution de compilation MIDL consiste à utiliser le commutateur [**-savePP**](-savepp.md) . Le commutateur **-savePP** empêche simplement MIDL de supprimer les fichiers temporaires que le préprocesseur renvoie à MIDL. Tenez compte des éléments suivants :

**MIDL-savePP-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**

Cette directive compile stub. idl tout en préservant tous les fichiers de préprocesseur.

> [!Note]  
> MIDL génère des exécutions distinctes du préprocesseur pour les fichiers IDL et ACF (le cas échéant), ainsi que pour chaque fichier importé.

 

Pour une compilation DCOM, plusieurs fichiers de préprocesseur sont généralement générés, même s’ils sont traités par MIDL comme un flux d’entrée contigu virtuel. dans un environnement de programmation Windows classique, les fichiers temporaires se trouvent dans le répertoire Temp sous la forme de noms de fichiers tels que MID \* . tmp. En cas de préservation de la sortie du préprocesseur, il est recommandé de surveiller les fichiers récents dans le répertoire Temp pour identifier les fichiers qui sont associés à l’exécution du préprocesseur.

Dans les cas simples, par exemple lorsque le fichier IDL compilé n’importe pas d’autres fichiers directement ou indirectement, ou lorsque vous examinez le fichier de niveau supérieur, le préprocesseur peut être appelé directement. L’exécution directe du préprocesseur C/C++ peut révéler des erreurs masquées ou confuses par MIDL. Par exemple, les deux lignes de commande de préprocesseur suivantes peuvent être utilisées pour la ligne MIDL précédemment citée :

**CL/E/nologo-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. pp**

**CL/E/P-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl**

Dans le premier de ces deux exemples, **/e** [**/nologo**](-nologo.md) sont les commutateurs ajoutés par MIDL lors de l’appel du préprocesseur. La sortie du préprocesseur est envoyée à stdout (l’écran) et nécessite donc une redirection vers un fichier à des fins d’examen. Dans le deuxième exemple, **/p** indique au préprocesseur de rediriger la sortie vers un \* fichier. i. dans ce cas, un fichier stub. i serait créé dans le répertoire actif.

Le commutateur [**/CPP \_ OPT**](-cpp-opt.md) peut également être utilisé pour obtenir un fichier prétraité, mais il est difficile et inférieur aux méthodes mentionnées précédemment. L’exemple suivant génère également un fichier stub. i, comme le faisait l’exemple précédent. Les guillemets dans l’exemple suivant sont essentiels :

**MIDL-Oicf-Win32-CPP \_ OPT "/E/p-ID : \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1" stub. idl**

 

 





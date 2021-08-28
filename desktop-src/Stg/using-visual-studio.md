---
title: Utilisation de Visual Studio
description: pour plus de commodité, Microsoft Visual Studio 6,0 fournit un fichier projet pour chaque exemple.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee6edc1b19cb0e56495c8af6f96d28e4d255e40d53161671f52a1a7d27939f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796849"
---
# <a name="using-visual-studio"></a>Utilisation de Visual Studio

pour plus de commodité, Microsoft Visual Studio 6,0 fournit un fichier projet pour chaque exemple. Ce fichier possède l’extension DSP. Un fichier d’espace de travail Allsamp. dsw est également fourni dans le répertoire principal afin que vous puissiez Compiler tous les échantillons à la fois à partir de Visual Studio.

> [!Note]  
> les instructions suivantes sont écrites pour Microsoft Visual Studio 6,0. Les commandes peuvent différer dans les versions antérieures et ultérieures de Visual Studio.

 

pour charger le projet approprié pour un exemple, vous pouvez exécuter Visual Studio à l’invite de commandes dans le répertoire de l’exemple, comme indiqué dans l’exemple suivant. Vous devez substituer l’exemple de nom de projet à **<project name>** .

**msdev <project name> . DSP**

vous pouvez également simplement double-cliquer sur le fichier. dsp dans l’explorateur de Windows pour charger l’espace de travail d’un exemple dans Visual Studio. à partir de Visual Studio vous pouvez parcourir les classes C++ de l’exemple de source et effectuer généralement les autres opérations de modification-compilation-débogage.

dans le cadre du kit de développement logiciel (SDK) de la plateforme, la compilation de ces exemples à partir de Visual Studio requiert le paramètre approprié des chemins d’accès aux répertoires dans Visual Studio. Pour définir les chemins d’accès aux répertoires, procédez comme suit :

-   exécutez Microsoft Visual Studio (Visual C++).
-   Dans le menu **Outils** , choisissez **options..** ..
-   Choisissez l’onglet **répertoires** dans la boîte de dialogue **options** .
-   Dans la liste déroulante **afficher les répertoires pour** , sélectionnez **fichiers exécutables** , puis entrez le chemin d’accès au répertoire bin de votre plateforme SDK installée (par exemple, C : \\ Program Files \\ Microsoft SDK \\ bin). Cliquez sur le bouton fléché vers le haut pour déplacer le chemin d’accès que vous venez d’entrer afin qu’il corresponde à la première entrée de la liste des **répertoires** .
-   Dans la liste déroulante **afficher les répertoires pour** , sélectionnez **inclure les fichiers** , puis entrez le chemin d’accès du répertoire include pour le kit de développement logiciel (SDK) de plateforme installé (par exemple, C : \\ Program Files \\ Microsoft \\ include). Cliquez sur le bouton fléché vers le haut pour déplacer le chemin d’accès que vous venez d’entrer afin qu’il corresponde à la première entrée de la liste des **répertoires** .
-   Dans la liste déroulante **afficher les répertoires pour** , sélectionnez **fichiers de bibliothèque** , puis entrez le chemin d’accès au répertoire lib pour votre kit de développement logiciel (SDK) de plateforme installé (par exemple, C : \\ Program Files \\ Microsoft SDK \\ lib). Cliquez sur les flèches vers le haut pour déplacer ce chemin d’accès qui vient d’être entré afin qu’il corresponde à la première entrée de la liste des **répertoires** .
-   Cliquez sur le bouton OK dans la boîte de dialogue **options** pour terminer les paramètres.

À partir de là, vous pouvez utiliser l’éditeur, le débogueur et les fonctionnalités de projet pour modifier, compiler, lier et déboguer.

D’autres IDE visuels peuvent également générer facilement l’un de leurs makefiles de projet natifs, en fonction des fichiers source existants d’un exemple de code. Si vous utilisez un tel IDE, la génération de ce type de Makefile de projet natif peut s’avérer très utile, car il offre un moyen de parcourir les classes C++ du programme. Pour plus d’informations sur l’utilisation de makefiles externes ou la création d’un Makefile de projet natif à l’aide d’un ensemble de fichiers sources existants, consultez la documentation de votre IDE.

Outre la dépendance vis-à-vis du code commun dans les répertoires APPUTIL, INC et LIB frères, de nombreux exemples de code sont autonomes. Générez APPUTIL avant de générer d’autres exemples de code. Certains exemples plus loin dans la séquence peuvent fonctionner avec les résultats compilés d’exemples précédents. Ces interdépendances d’exemples de code sont les suivantes :

-   Any : la génération d’un exemple de code nécessite une version antérieure de APPUTIL.
-   DLLUSER : la génération ou l’exécution a besoin d’une version antérieure de DLLSKEL.
-   Comuser : la génération ou l’exécution a besoin d’une version antérieure de COMOBJ.
-   DLLSERVE : la Build a besoin d’une version antérieure du Registre.
-   DLLCLIEN : l’exécution nécessite une build antérieure de DLLSERVE.
-   LICSERVE : la Build a besoin d’une version antérieure du Registre.
-   LICCLIEN : l’exécution nécessite une build antérieure de LICSERVE et DLLSERVE.
-   MARSHAL : la Build a besoin d’une version antérieure du Registre.
-   LOCSERVE : la génération ou l’exécution a besoin d’une version antérieure du Registre et du MARSHAL.
-   LOCCLIEN : l’exécution nécessite une build antérieure de LOCSERVE.
-   APTSERVE : la génération ou l’exécution a besoin d’une version antérieure du Registre et du MARSHAL.
-   APTCLIEN : l’exécution nécessite une build antérieure de APTSERVE.
-   REMCLIEN : la génération ou l’exécution a besoin d’une version antérieure du Registre et du MARSHAL sur l’ordinateur local (client). L’exécution a besoin d’une version antérieure de REGISTER, MARSHAL et APTSERVE sur l’ordinateur distant (serveur).
-   FRESERVE : la Build a besoin d’une version antérieure du Registre.
-   FRECLIEN : l’exécution nécessite une build antérieure de FRESERVE.
-   CONSERVER : la Build a besoin d’une version antérieure du Registre.
-   CONCLIEN : l’exécution nécessite une build antérieure de la conservation.
-   STOSERVE : la Build a besoin d’une version antérieure du Registre.
-   STOCLIEN : l’exécution nécessite une build antérieure de STOSERVE.
-   CONSERVATION : la Build a besoin d’une version antérieure du Registre.
-   Pertext : la génération a besoin d’une version antérieure du Registre.
-   Pertirage : la Build a besoin d’une version antérieure du Registre.
-   PERCLIEN : l’exécution nécessite la génération antérieure des perservices, du pertext et du pertirage.
-   DCDMARSH : la Build a besoin d’une version antérieure du Registre.
-   DCDSERVE : la génération ou l’exécution a besoin d’une version antérieure de REGISTER et DCDMARSH.
-   DCOMDRAW : la génération ou l’exécution a besoin d’une version antérieure de REGISTER et DCDMARSH sur l’ordinateur local (client). L’exécution a besoin d’une version antérieure de REGISTER, DCDMARSH et DCOMDRAW sur l’ordinateur distant (serveur).

 

 





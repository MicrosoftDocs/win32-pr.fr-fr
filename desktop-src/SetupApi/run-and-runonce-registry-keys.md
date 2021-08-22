---
description: Les clés de Registre Run et RunOnce provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Clés de Registre Run et RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665239"
---
# <a name="run-and-runonce-registry-keys"></a>Clés de Registre Run et RunOnce

Les clés de Registre Run et RunOnce provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session. La valeur de données pour une clé est une ligne de commande ne dépassant pas 260 caractères. Inscrivez les programmes à exécuter en ajoutant des entrées de la chaîne Description de la *Description* de la ligne de commande -  = . Vous pouvez écrire plusieurs entrées sous une clé. Si plusieurs programmes sont inscrits sous une clé particulière, l’ordre dans lequel ces programmes s’exécutent est indéterminé.

le registre de Windows comprend les quatre clés Run et RunOnce suivantes :

-   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Par défaut, la valeur d’une clé RunOnce est supprimée avant l’exécution de la ligne de commande. Vous pouvez faire précéder un nom de valeur RunOnce d’un point d’exclamation ( !) pour différer la suppression de la valeur jusqu’à ce que la commande s’exécute. Sans le préfixe du point d’exclamation, si l’opération RunOnce échoue, le programme associé ne sera pas invité à s’exécuter la prochaine fois que vous démarrerez l’ordinateur.

par défaut, ces clés sont ignorées lorsque l’ordinateur est démarré en Mode Coffre. le nom de la valeur des clés RunOnce peut être préfixé par un astérisque ( \* ) pour forcer l’exécution du programme même en mode Coffre.

Un programme exécuté à partir de l’une de ces clés ne doit pas écrire dans la clé pendant son exécution, car cela interfère avec l’exécution d’autres programmes enregistrés sous la clé. Les applications doivent utiliser la clé RunOnce uniquement pour les conditions temporaires, par exemple pour terminer l’installation de l’application. une application ne doit pas recréer continuellement des entrées sous RunOnce, car cela interfère avec installation de Windows.

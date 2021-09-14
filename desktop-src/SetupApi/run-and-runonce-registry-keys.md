---
description: Les clés de Registre Run et RunOnce provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Clés de Registre Run et RunOnce
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 024d04ad535fc85022a6076b3fbc260e52f7488d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127175197"
---
# <a name="run-and-runonce-registry-keys"></a>Clés de Registre Run et RunOnce

`Run` et les `RunOnce` clés de Registre provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session. La valeur de données pour une clé est une ligne de commande ne dépassant pas 260 caractères. Inscrivez les programmes à exécuter en ajoutant des entrées de la chaîne Description de la *Description* de la ligne de commande -  = . Vous pouvez écrire plusieurs entrées sous une clé. Si plusieurs programmes sont inscrits sous une clé particulière, l’ordre dans lequel ces programmes s’exécutent est indéterminé.

le registre de Windows comprend les quatre `Run` clés et suivantes `RunOnce` :

-   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Par défaut, la valeur d’une `RunOnce` clé est supprimée avant l’exécution de la ligne de commande. Vous pouvez préfixer un `RunOnce` nom de valeur avec un point d’exclamation ( !) pour différer la suppression de la valeur jusqu’à ce que la commande s’exécute. Sans le préfixe du point d’exclamation, si l' `RunOnce` opération échoue, le programme associé ne sera pas invité à s’exécuter la prochaine fois que vous démarrerez l’ordinateur.

par défaut, ces clés sont ignorées lorsque l’ordinateur est démarré en Mode Coffre. le nom de la valeur des `RunOnce` clés peut être précédé d’un astérisque ( \* ) pour forcer l’exécution du programme même en Mode Coffre.

Un programme exécuté à partir de l’une de ces clés ne doit pas écrire dans la clé pendant son exécution, car cela interfère avec l’exécution d’autres programmes enregistrés sous la clé. Les applications doivent utiliser la `RunOnce` clé uniquement pour les conditions temporaires, par exemple pour terminer l’installation de l’application. une application ne doit pas recréer continuellement des entrées sous `RunOnce` , car cela interfère avec installation de Windows.

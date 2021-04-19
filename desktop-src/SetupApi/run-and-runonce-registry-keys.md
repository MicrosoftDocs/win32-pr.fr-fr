---
description: Les clés de Registre Run et RunOnce provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Clés de Registre Run et RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530256"
---
# <a name="run-and-runonce-registry-keys"></a>Clés de Registre Run et RunOnce

Les clés de Registre Run et RunOnce provoquent l’exécution des programmes chaque fois qu’un utilisateur ouvre une session. La valeur de données pour une clé est une ligne de commande ne dépassant pas 260 caractères. Inscrivez les programmes à exécuter en ajoutant des entrées de la chaîne Description de la *Description* de la ligne de commande -  = . Vous pouvez écrire plusieurs entrées sous une clé. Si plusieurs programmes sont inscrits sous une clé particulière, l’ordre dans lequel ces programmes s’exécutent est indéterminé.

Le Registre Windows comprend les quatre clés Run et RunOnce suivantes :

-   **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Par défaut, la valeur d’une clé RunOnce est supprimée avant l’exécution de la ligne de commande. Vous pouvez faire précéder un nom de valeur RunOnce d’un point d’exclamation ( !) pour différer la suppression de la valeur jusqu’à ce que la commande s’exécute. Sans le préfixe du point d’exclamation, si l’opération RunOnce échoue, le programme associé ne sera pas invité à s’exécuter la prochaine fois que vous démarrerez l’ordinateur.

Par défaut, ces clés sont ignorées lorsque l’ordinateur est démarré en mode sans échec. Le nom de la valeur des clés RunOnce peut être précédé d’un astérisque ( \* ) pour forcer l’exécution du programme même en mode sans échec.

Un programme exécuté à partir de l’une de ces clés ne doit pas écrire dans la clé pendant son exécution, car cela interfère avec l’exécution d’autres programmes enregistrés sous la clé. Les applications doivent utiliser la clé RunOnce uniquement pour les conditions temporaires, par exemple pour terminer l’installation de l’application. Une application ne doit pas recréer continuellement des entrées sous RunOnce, car cela interfère avec installation de Windows.

---
description: Les applications peuvent gérer un contexte d’activation en appelant directement les fonctions de contexte d’activation.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Utilisation de l’API de contexte d’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112694"
---
# <a name="using-the-activation-context-api"></a>Utilisation de l’API de contexte d’activation

Les applications peuvent gérer un [contexte d’activation](activation-contexts.md) en appelant directement les fonctions de contexte d’activation. Les contextes d’activation sont des structures de données en mémoire. Le système peut utiliser les informations du contexte d’activation pour rediriger une application afin de charger une version de DLL particulière, une instance d’objet COM ou une version de fenêtre personnalisée. Pour plus d’informations, consultez [Référence du contexte d’activation](activation-context-reference.md).

L’interface de programmation d’applications (API) peut être utilisée pour gérer le contexte d’activation et créer des objets de nom de version avec des [manifestes](manifests.md). Les deux scénarios suivants illustrent comment une application peut gérer un contexte d’activation en appelant directement les fonctions de contexte d’activation. Toutefois, dans la plupart des cas, le contexte d’activation est géré par le système. Les développeurs d’applications et les fournisseurs d’assemblys n’ont généralement pas besoin d’effectuer des appels à la pile pour gérer le contexte d’activation.

-   Processus et applications qui implémentent des couches d’indirection ou de répartition.

    Par exemple, un utilisateur qui gère les contextes d’activation dans la boucle d’événements. Chaque fois que vous accédez à la fenêtre, par exemple en déplaçant la souris sur la fenêtre, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) est appelé, ce qui active le contexte d’activation actuel pour la ressource, comme indiqué dans le fragment de code suivant.

    <dl> HANDLE hActCtx ;  
    CreateWindow ();  
    ...  
    GetCurrentActCtx (&ActCtx);  
    ...  
    ReleaseActCtx (&ActCtx);  
    </dl>

    Dans le fragment de code suivant, la fonction API active les contextes d’activation appropriés avant d’appeler [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). Quand **CallWindowProc** est appelé, il utilise ce contexte pour transmettre un message à Windows. Lorsque toutes les opérations de ressource sont terminées, la fonction désactive le contexte.

    <dl> ULONG \_ ptr ulpCookie ;  
    HANDLE hActCtx ;  
    if (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc(...);  
    ...  
    DeactivateActCtx (0, ulpCookie);  
    }  
    </dl>

-   Couche de répartition de délégation.

    Ce scénario s’applique aux responsables qui gèrent plusieurs entités avec une couche API commune, telle qu’un gestionnaire de pilotes. Bien qu’il n’ait pas encore été implémenté, il s’agit d’un exemple de pilote ODBC.

    Dans ce scénario, la couche intermédiaire prend en charge le traitement des liaisons d’assembly. Pour obtenir le pilote de liaison spécifique à la version, les éditeurs doivent fournir un manifeste et spécifier des dépendances sur des composants spécifiques dans ce manifeste. L’application de base ne crée pas de liaison dynamique avec les composants ; au moment de l’exécution, le gestionnaire de pilotes gère les appels. Lorsque le pilote ODBC est appelé en fonction de la chaîne de connexion, il charge le pilote approprié. Il crée ensuite le contexte d’activation à l’aide des informations contenues dans le fichier manifeste de l’assembly.

    Sans le manifeste, l’action par défaut pour le pilote consiste à utiliser le même contexte que celui spécifié par l’application (dans cet exemple, la version 2 de MSVCRT). Étant donné qu’un manifeste existe, un contexte d’activation distinct est établi. Lorsque le pilote ODBC s’exécute, il est lié à la version 1 de l’assembly MSVCRT.

    Chaque fois que le gestionnaire de pilotes appelle la couche de répartition (par exemple, pour obtenir le jeu de données suivant), il utilise les assemblys appropriés en fonction du contexte d’activation. Le fragment de code suivant illustre cela.

    <dl> HANDLE hActCtx ;  
    ULONG \_ ptr ulpCookie ;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx (&ActCtxToCreate);  
    ...;  
    if (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx (0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 

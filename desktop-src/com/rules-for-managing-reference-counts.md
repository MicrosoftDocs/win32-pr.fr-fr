---
title: Règles pour la gestion des nombres de références
description: L’utilisation d’un décompte de références pour gérer la durée de vie d’un objet permet à plusieurs clients d’obtenir et de libérer l’accès à un objet unique sans avoir à coordonner l’un avec l’autre pour gérer la durée de vie de l’objet.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363640"
---
# <a name="rules-for-managing-reference-counts"></a>Règles pour la gestion des nombres de références

L’utilisation d’un décompte de références pour gérer la durée de vie d’un objet permet à plusieurs clients d’obtenir et de libérer l’accès à un objet unique sans avoir à coordonner l’un avec l’autre pour gérer la durée de vie de l’objet. Tant que l’objet client est conforme à certaines règles d’utilisation, l’objet, en vigueur, fournit cette gestion. Ces règles spécifient comment gérer les références entre les objets. (COM ne spécifie pas les implémentations internes d’objets, bien que ces règles soient un point de départ raisonnable pour une stratégie dans un objet.)

D’un point de vue conceptuel, les pointeurs d’interface peuvent être considérés comme résidant dans des variables de pointeur qui incluent tous les États de calcul internes qui contiennent un pointeur d’interface. Cela inclut les variables dans les emplacements de mémoire, dans les registres internes du processeur, ainsi que les variables générées par le programmeur et générées par le compilateur. L’assignation ou l’initialisation d’une variable pointeur implique la création d’une nouvelle copie d’un pointeur déjà existant. Lorsqu’il y avait une copie du pointeur dans une variable (la valeur utilisée dans l’assignation/initialisation), il y en a maintenant deux. Une assignation à une variable pointeur détruit la copie du pointeur actuellement dans la variable, tout comme la destruction de la variable elle-même. (Autrement dit, l’étendue dans laquelle la variable est trouvée, telle que le frame de pile, est détruite.)

Du point de vue du client COM, le décompte de références est toujours effectué pour chaque interface. Les clients ne doivent jamais supposer qu’un objet utilise le même compteur pour toutes les interfaces.

Le cas par défaut est que [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) doit être appelé pour chaque nouvelle copie d’un pointeur d’interface et que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) doit être appelé pour chaque destruction d’un pointeur d’interface, sauf si les règles suivantes l’autorisent autrement :

-   **Paramètres d’extraction aux fonctions.** L’appelant doit appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur le paramètre, car il sera libéré (avec un appel à [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) dans le code d’implémentation lorsque la valeur out est stockée au-dessus.
-   **Récupération d’une variable globale.** Lors de la création d’une copie locale d’un pointeur d’interface à partir d’une copie existante du pointeur dans une variable globale, vous devez appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur la copie locale, car une autre fonction peut détruire la copie dans la variable globale lorsque la copie locale est toujours valide.
-   **Nouveaux pointeurs synthétisés à partir de « l’air mince ».** Une fonction qui synthétise un pointeur d’interface à l’aide d’une connaissance interne spéciale plutôt que de l’obtenir à partir d’une autre source doit appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) initialement sur le pointeur récemment synthétisé. Les exemples importants de telles routines incluent les routines de création d’instance, les implémentations de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), etc.
-   **Récupération d’une copie d’un pointeur stocké en interne.** Lorsqu’une fonction récupère une copie d’un pointeur stocké en interne par l’objet appelé, le code de cet objet doit appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur le pointeur avant le retour de la fonction. Une fois le pointeur récupéré, l’objet d’origine n’a aucun autre moyen de déterminer la façon dont sa durée de vie est associée à celle de la copie stockée en interne du pointeur.

La seule exception au cas par défaut exige que le code de gestion connaisse les relations des durées de vie de deux ou plusieurs copies d’un pointeur vers la même interface sur un objet et qu’il vérifie simplement que l’objet n’est pas détruit en permettant à son décompte de références de passer à zéro. Il y a généralement deux cas, comme suit :

-   Lorsqu’une copie d’un pointeur existe déjà et qu’une deuxième est créée par la suite, puis est détruite alors que la première copie existe toujours, les appels à [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)pour la deuxième copie peuvent être omis.
-   Lorsqu’il existe une copie d’un pointeur et qu’une deuxième est créée, puis que la première est détruite avant la seconde, les appels à [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)pour la deuxième copie et à [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour la première copie peuvent être omis.

Voici des exemples spécifiques de ces situations, les deux premières étant particulièrement courantes :

-   **Dans les paramètres de fonctions.** La durée de vie de la copie d’un pointeur d’interface passé comme paramètre à une fonction est imbriquée dans celle du pointeur utilisé pour initialiser la valeur. il n’est donc pas nécessaire de disposer d’un décompte de références distinct sur le paramètre.
-   **Les paramètres out des fonctions, y compris les valeurs de retour.** Pour définir le paramètre out, la fonction doit avoir une copie stable du pointeur d’interface. Au retour, l’appelant est chargé de libérer le pointeur. Par conséquent, le paramètre out n’a pas besoin d’un nombre de références distinct.
-   **Variables locales.** Une implémentation de méthode contrôle les durées de vie de chacune des variables de pointeur allouées sur le frame de pile et peut l’utiliser pour déterminer comment omettre les paires de versions de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)redondantes / [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .
-   **Points de soulignement.** Certaines structures de données contiennent deux objets, chacun avec un pointeur vers l’autre. Si la durée de vie du premier objet est connue pour contenir la durée de vie de la seconde, il n’est pas nécessaire de disposer d’un décompte de références sur le deuxième pointeur de l’objet vers le premier objet. Souvent, il est important d’éviter ce cycle pour maintenir le comportement de désallocation approprié. Toutefois, les pointeurs non comptés doivent être utilisés avec une extrême prudence, car la partie du système d’exploitation qui gère le traitement à distance n’a aucun moyen de connaître cette relation. Par conséquent, dans la plupart des cas, le fait de faire en sorte que le point de présence du point de présence est un deuxième objet « Friend » du premier pointeur (ce qui évite la circularité) est la solution recommandée. L’architecture des objets connectables de COM, par exemple, utilise cette approche.

Lors de l’implémentation ou de l’utilisation d’objets comptés par référence, il peut être utile d’appliquer des *nombres de références artificielles*, ce qui garantit la stabilité des objets pendant le traitement d’une fonction. Lors de l’implémentation d’une méthode d’interface, vous pouvez appeler des fonctions qui ont la possibilité de décrémenter le décompte de références à un objet, provoquant une version prématurée de l’objet et l’échec de l’implémentation. Un moyen fiable d’éviter cela consiste à insérer un appel à [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) au début de l’implémentation de la méthode et à le coupler avec un appel à [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) juste avant le retour de la méthode.

Dans certains cas, les valeurs de retour de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) peuvent être instables et ne doivent pas être réutilisables ; elles doivent être utilisées uniquement à des fins de débogage ou de diagnostic.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des durées de vie des objets via le décompte de références](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 
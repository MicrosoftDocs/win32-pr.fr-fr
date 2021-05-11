---
title: Minutage des jeux et processeurs multicœurs.
description: Cet article propose une solution plus précise et fiable pour obtenir des minutages processeur haute résolution à l’aide des API Windows QueryPerformanceCounter et QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a6d9d65ccb79c7b496b4d02b1bed132bdc2d3f
ms.sourcegitcommit: 998a611c97d5e20ac0c45e3bda768ae67d8c2cca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "109725008"
---
# <a name="game-timing-and-multicore-processors"></a>Minutage des jeux et processeurs multicœurs.

Les technologies de gestion de l’alimentation devenant de plus en plus répandues sur les ordinateurs d’aujourd’hui, une méthode couramment utilisée pour obtenir des minutages UC haute résolution, l’instruction RDTSC, peut ne plus fonctionner comme prévu. Cet article propose une solution plus précise et fiable pour obtenir des minutages processeur haute résolution à l’aide des API Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Contexte](#background)
-   [Recommandations](#recommendations)
-   [Compatibilité des applications](#application-compatibility)

## <a name="background"></a>Arrière-plan

Depuis l’introduction du jeu d’instructions x86 P5, de nombreux développeurs de jeux ont utilisé le compteur d’horodatage de lecture, l’instruction RDTSC, pour effectuer un minutage haute résolution. Les minuteurs Windows Media sont suffisamment précis pour le traitement des sons et des vidéos, mais avec des temps d’image d’une douzaine de millisecondes ou moins, ils n’ont pas suffisamment de résolution pour fournir des informations sur le delta. De nombreux jeux utilisent toujours un minuteur multimédia au démarrage pour établir la fréquence de l’UC, et ils utilisent cette valeur de fréquence pour mettre à l’échelle les résultats de RDTSC pour obtenir un temps précis. En raison des limitations de RDTSC, l’API Windows expose la manière la plus correcte d’accéder à cette fonctionnalité via les routines de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Cette utilisation de RDTSC pour la synchronisation souffre de ces problèmes fondamentaux :

-   Valeurs discontinues. L’utilisation directe de RDTSC suppose que le thread est toujours en cours d’exécution sur le même processeur. Les systèmes multiprocesseurs et à double cœur ne garantissent pas la synchronisation de leurs compteurs de cycles entre les cœurs. Cela est aggravé lorsqu’il est associé à des technologies de gestion de l’alimentation modernes qui inactivent et restaurent différents cœurs à des moments différents, ce qui entraîne généralement une désynchronisation des cœurs. Pour une application, cela entraîne généralement des problèmes ou des pannes potentielles à mesure que le thread saute entre les processeurs et obtient des valeurs de minutage qui entraînent des deltas de grande taille, des deltas négatifs ou une interruption du minutage.
-   Disponibilité du matériel dédié. RDTSC verrouille les informations de minutage que l’application demande au compteur de cycle du processeur. Pendant de nombreuses années, il s’agissait de la meilleure façon d’obtenir des informations de temporisation de haute précision, mais les cartes mères plus récentes incluent maintenant des appareils de synchronisation dédiés qui fournissent des informations de minutage haute résolution sans les inconvénients de RDTSC.
-   Variabilité de la fréquence du processeur. L’hypothèse est souvent faite que la fréquence du processeur est fixée pour la durée de vie du programme. Toutefois, avec les technologies de gestion de l’alimentation modernes, il s’agit d’une hypothèse incorrecte. S’il est initialement limité aux ordinateurs portables et aux autres appareils mobiles, la technologie qui modifie la fréquence de l’UC est utilisée sur de nombreux ordinateurs de bureau haut de gamme. la désactivation de sa fonction pour maintenir une fréquence cohérente n’est généralement pas acceptable pour les utilisateurs.

## <a name="recommendations"></a>Recommandations

Les jeux ont besoin d’informations de temporisation précises, mais vous devez également implémenter le code de minutage de manière à éviter les problèmes associés à l’utilisation de RDTSC. Lorsque vous implémentez le minutage haute résolution, procédez comme suit :

1.  Utilisez [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) au lieu de RDTSC. Ces API peuvent utiliser RDTSC, mais peuvent utiliser à la place des périphériques de minuterie sur la carte mère ou d’autres services système qui fournissent des informations de minutage haute résolution haute qualité. Bien que RDTSC soit beaucoup plus rapide que **QueryPerformanceCounter**, puisque ce dernier est un appel d’API, il s’agit d’une API qui peut être appelée plusieurs centaines de fois par trame sans aucun impact notable. (Toutefois, les développeurs doivent tenter d’appeler **QueryPerformanceCounter** le moins possible pour éviter toute altération des performances.)
2.  Lors du calcul des deltas, les valeurs doivent être ancrées pour garantir que tous les bogues dans les valeurs de minutage ne provoquent pas de blocages ou des calculs liés à l’heure instables. La plage de brides doit être comprise entre 0 (pour empêcher les valeurs Delta négatives) et une valeur raisonnable en fonction de votre fréquence de cadence la plus faible attendue. Le verrouillage est susceptible d’être utile dans tout débogage de votre application, mais veillez à garder l’esprit en cas d’analyse des performances ou d’exécution du jeu en mode non optimisé.
3.  Calculez tout le minutage sur un thread unique. Le calcul du minutage sur plusieurs threads, par exemple, avec chaque thread associé à un processeur spécifique, réduit considérablement les performances des systèmes multicœurs.
4.  Définissez ce thread unique de façon à ce qu’il reste sur un processeur unique à l’aide de l’API Windows [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). En règle générale, il s’agit du thread de jeu principal. Alors que [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) s’ajustent généralement pour plusieurs processeurs, les bogues dans le BIOS ou les pilotes peuvent entraîner le retour de valeurs différentes par les routines à mesure que le thread passe d’un processeur à un autre. Par conséquent, il est préférable de conserver le thread sur un processeur unique.

    Tous les autres threads doivent fonctionner sans collecter leurs propres données de minuteur. Nous vous déconseillons d’utiliser un thread de travail pour calculer la durée, car cela deviendra un goulot d’étranglement de synchronisation. Au lieu de cela, les threads de travail doivent lire les horodateurs du thread principal, et comme les threads de travail lisent uniquement les horodateurs, il n’est pas nécessaire d’utiliser des sections critiques.

5.  Appelez [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) une seule fois, car la fréquence ne change pas pendant l’exécution du système.

## <a name="application-compatibility"></a>Compatibilité des applications

De nombreux développeurs ont fait des suppositions sur le comportement de RDTSC sur de nombreuses années. il est donc très probable que certaines applications existantes présenteront des problèmes lorsqu’ils s’exécuteront sur un système avec plusieurs processeurs ou cœurs en raison de l’implémentation du minutage. Ces problèmes se manifestent généralement comme un problème ou un mouvement lent. Il n’existe pas de solution facile pour les applications qui ne sont pas informées de la gestion de l’alimentation, mais il existe un shim pour forcer une application à toujours s’exécuter sur un processeur unique dans un système multiprocesseur.

Pour créer ce shim, téléchargez Microsoft Application Compatibility Toolkit à partir de la [compatibilité des applications Windows](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

À l’aide de l’administrateur de compatibilité, qui fait partie de la boîte à outils, créez une base de données de votre application et les correctifs associés. Créez un nouveau mode de compatibilité pour cette base de données et sélectionnez le correctif de compatibilité **SingleProcAffinity** pour forcer tous les threads de l’application à s’exécuter sur un seul processeur/cœur. À l’aide de l’outil de ligne de commande Fixpack.exe (également inclus dans la boîte à outils), vous pouvez convertir cette base de données en package installable pour l’installation, le test et la distribution.

Pour obtenir des instructions sur l’utilisation de l’administrateur de compatibilité, consultez la documentation de la boîte à outils. Pour obtenir la syntaxe des et des exemples d’utilisation de Fixpack.exe, consultez l’aide de la ligne de commande.

Pour obtenir des informations sur les clients, consultez les articles suivants de la base de connaissances de la rubrique aide et support Microsoft :

-   [Les programmes qui utilisent la fonction QueryPerformanceCounter peuvent fonctionner mal dans Windows Server 2003 et Windows XP](https://support.microsoft.com/kb/895980) (article 895980)
-   [Les performances du jeu peuvent être médiocres sur un ordinateur Windows XP qui utilise un processeur double cœur](https://support.microsoft.com/kb/909944) (article 909944)

 

 

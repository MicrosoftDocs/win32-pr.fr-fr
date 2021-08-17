---
title: principaux problèmes pour les titres de Windows
description: Cet article présente un grand nombre des problèmes courants que nous avons rencontrés dans les jeux de PC actuels.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396504"
---
# <a name="top-issues-for-windows-titles"></a>principaux problèmes pour les titres de Windows

le groupe de Relations développeurs de jeux et de Technologies graphiques de Microsoft Windows effectue une analyse des performances pour de nombreux jeux Windows chaque année. Pendant ces sessions, nous obtenons une expérience pratique pour associer les commentaires des développeurs et les requêtes que nous recevons quotidiennement. Parfois, nous pouvons vous aider à identifier un incident mystérieux ou tout autre problème dans un titre, ce qui nous permet d’approfondir vos connaissances sur les problèmes que les développeurs rencontrent.

Cet article présente un grand nombre des problèmes courants que nous avons rencontrés dans les jeux de PC actuels.

-   [Performances limitées du processeur](#cpu-limited-performance)
-   [Gestion des lots médiocre](#poor-batch-management)
-   [Copie excessive de la mémoire](#excessive-memory-copying)
-   [Utilisation excessive de l’envoi de dessin dynamique](#excessive-use-of-dynamic-draw-submission)
-   [Surcharge élevée dans le traitement des fichiers](#high-overhead-in-file-processing)
-   [Installation lente et frustrante](#slow-and-frustrating-installation)
-   [Manque de considérations sur la mémoire physique](#lack-of-consideration-of-physical-memory)
-   [Dépendance excessive sur Real-Time conversion du taux d’échantillonnage audio](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragmentation de la mémoire virtuelle](#fragmention-of-virtual-memory)
-   [Manipulation du mot de contrôle Floating-Point](#manipulation-of-the-floating-point-control-word)
-   [Installation facultative du runtime DirectX](#optional-installation-of-the-directx-runtime)
-   [Utilisation excessive de la synchronisation des threads](#excessive-use-of-thread-synchronization)
-   [Utilisation de RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>Performances de CPU-Limited

La grande majorité des jeux est limitée par les performances de l’UC sur les systèmes dotés d’unités de traitement graphique (GPU) hautes performances. Cela est parfois dû à une mauvaise utilisation du traitement par lot pour les envois de tirage, mais plus généralement, cela est dû au fait que d’autres systèmes de jeux consomment une grande partie des cycles d’UC disponibles. Dans les rares cas où nous avons vu la limitation du GPU, la cause est un taux de remplissage très élevé ou une demande de nuanceur de pixels, des paramètres haute résolution ou des performances de nuanceur de sommets réduites par une carte vidéo.

Étant donné que la plupart des titres sont limités au processeur, les performances les plus importantes gagnent de l’optimisation des systèmes de jeux gourmands en ressources processeur. En règle générale, les systèmes d’intelligence artificielle et physique, ainsi que la logique de détection des collisions associée, sont les principaux consommateurs de cycles de processeur dans le même temps que les applications Microsoft Direct3D. Tout travail d’amélioration de ces systèmes peut améliorer les performances globales du jeu.

## <a name="poor-batch-management"></a>Gestion des lots médiocre

L’obtention d’un bon parallélisme avec le GPU nécessite que les lots de dessin contiennent suffisamment de géométrie et que les nuanceurs aient la complexité appropriée, afin que la carte vidéo reste occupée, tout en n’utilisant pas autant de lots que le tampon de commande est submergé. Sur le matériel de la génération actuelle, nous vous recommandons d’environ 300 ou moins de tirages par lot de tirages par trame (moins de processeurs moins performants) pour empêcher le traitement du pilote du tampon de commande de devenir un goulot d’étranglement de performances. Certains autres appels d’état d’API et combinaisons de pilotes peuvent entraîner un traitement coûteux du processeur (compilation du pilote des nuanceurs, par exemple). nous vous recommandons donc vivement d’analyser les performances de routine.

## <a name="excessive-memory-copying"></a>Copie excessive de la mémoire

Lors du développement de la plupart des titres de PC, les développeurs utilisent des structures de données et des chaînes pratiques pour la gestion de contenu. Le travail du processeur requis pour la comparaison de chaînes, la copie et d’autres manipulations a souvent une surcharge mesurable, en particulier lors de la mise en compte des résultats de performance associés au cache et au sous-système de mémoire. Les plans doivent être établis lors du développement de ces systèmes pour supprimer ou réduire la dépendance au traitement des chaînes une fois que le produit entre dans les phases de test et de mise en production principales.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Utilisation excessive de l’envoi de dessin dynamique

Le matériel vidéo moderne fonctionne bien lorsque vous traitez des données statiques. Les adaptateurs haut de gamme disposent souvent d’une très grande quantité de mémoire vidéo, mais cette mémoire ne peut pas être utilisée efficacement par Dynamic Data.

Bien que les modèles d’utilisation raisonnablement efficaces des tampons de vertex/tampons d’index dynamiques puissent être implémentés pour le contenu dynamique, de nombreux titres surveillent cet idiome pour ce qui est du contenu statique. Nous le voyons le plus souvent avec des arbres de partitionnement d’espace binaire (BSP) et des systèmes basés sur le portail qui stockent la géométrie dans une structure de données qui ne mappe pas au matériel et qui doit être traitée dans des mémoires tampons pour chaque trame. Le fait de placer autant de contenu que possible dans les ressources statiques peut considérablement réduire la surcharge de bande passante liée au transfert de données vers la carte vidéo, améliorer l’utilisation de la mémoire VRAM intégrée et réduire la surcharge du processeur/cache impliquée dans le traitement de ce contenu.

## <a name="high-overhead-in-file-processing"></a>Surcharge élevée dans le traitement des fichiers

Les jeux de PC ont obtenu une réputation pour des temps de chargement longs, en particulier lorsqu’ils sont comparés aux titres de console avec des exigences de temps de chargement strictes. Notre analyse de la façon dont de nombreux titres utilisent le sous-système de fichiers révèle certains problèmes courants.

La surcharge liée à l’ouverture d’un fichier est généralement bien supérieure à celle que les développeurs attendent. Avec les scanneurs de virus à la demande dans un usage répandu et les fonctionnalités supplémentaires de NTFS, l’ouverture d’un fichier est une opération relativement coûteuse. L’ouverture de nombreux fichiers à la fois, ou l’ouverture et la fermeture du même fichier à plusieurs reprises, constituent donc une mauvaise méthode de gestion des fichiers. Certains jeux ont tenté de réduire ce coût de performance en testant l’existence d’un fichier avant de l’ouvrir. En réalité, le test de l’existence d’un fichier sur NTFS nécessite l’ouverture du fichier. ainsi, le test avant d’ouvrir entraîne le paiement de deux fois le coût.

Les jeux qui autorisent les modifications du module complémentaire, ou mods, ou qui incluent toujours la génération de modèles automatique de développement pour vérifier les fichiers de données de remplacement, peuvent entraîner des retards importants lors du chargement du jeu en raison de la vérification de ces fichiers, même si ces fichiers ne sont pas présents. Nous recommandons que les jeux vérifient uniquement ces fichiers lorsqu’ils sont exécutés avec un commutateur de ligne de commande spécial, ou à l’aide d’un autre indicateur de mode, afin que seuls les utilisateurs qui utilisent cette fonctionnalité paient en fait le coût des performances de ces contrôles (souvent étendus).

Des performances supplémentaires peuvent être obtenues à partir du système de fichiers de la façon suivante :

-   Utilisation appropriée de l’indicateur de fichier indicateurs de fichier d' \_ indicateur d' \_ accès aléatoire et d’indicateur de \_ fichier \_ \_ \_ analyse séquentielle
-   Dimensionnement des mémoires tampons pour éviter un grand nombre d’appels aux API de lecture/écriture du système d’exploitation
-   Accès asynchrone aux fichiers
-   Chargement des threads en arrière-plan

Nous vous recommandons également de convertir les données hors connexion (au moment de la génération ou de l’installation) au lieu de vous appuyer sur la conversion lorsque le jeu est exécuté pour la première fois, ce qui permet d’imposer des taxes de performances significatives pour chaque utilisateur.

## <a name="slow-and-frustrating-installation"></a>Installation lente et frustrante

Un autre problème courant que nous avons rencontré est le temps d’installation très long requis pour de nombreux jeux de PC modernes. Les programmes d’installation invitent l’utilisateur plusieurs fois, parfois simplement à indiquer à l’utilisateur, par exemple, « vous n’avez pas besoin d’installer DirectX ». En règle générale, ces programmes d’installation malveillants nécessitent que l’utilisateur sélectionne **suivant** ou **OK** à plusieurs moments avant que l’installation du jeu commence réellement. Une fois qu’il a commencé, nous avons vu certains titres prendre une heure ou plus avant que l’utilisateur ait l’opportunité de jouer le jeu. Nous pensons que la première heure de l’expérience de jeu ne doit pas être l’installation.

Nous vous recommandons d’utiliser un certain nombre d’approches pour traiter l’installation. Tout d’abord, laissez les invites simples et au minimum. Deuxièmement, concevez vos données de jeu de sorte que certains ou l’ensemble des fichiers de données puissent être utilisés directement à partir du disque de distribution, dans la mesure du possible. les lecteurs de DVD modernes ont une très grande bande passante. Troisièmement, envisagez d’implémenter Install-on-Demand dans vos titres pour réduire ou éliminer le processus d’installation et permettre aux utilisateurs d’accéder au jeu aussi rapidement que possible. (Pour plus d’informations sur l’installation à la demande, consultez [installation à la demande pour les jeux](/windows/desktop/DxTechArts/install-on-demand-for-games).)

Pour plus d’informations sur l’installation de jeux, consultez [simplification de l’installation de jeux](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Manque de considérations sur la mémoire physique

En raison de la grande variabilité du matériel PC sur le marché, les titres utilisent généralement des tests de configuration ad hoc pour sélectionner les paramètres par défaut pour le niveau de détail graphique. Certains des titres que nous avons vus utilisent la taille de la mémoire vidéo dans ces tests, mais ne parviennent pas à les mettre en corrélation avec la taille de la mémoire physique. Pour gérer les situations de périphériques perdus, la majeure partie de la mémoire vidéo (VRAM locale sur la carte et ouverture de mémoire AGP non locale) doit être sauvegardée par la mémoire physique, soit à l’aide de ressources managées, soit en utilisant des structures de données personnalisées. Certaines cartes vidéo haut de gamme ont des tailles VRAM qui rivalisent avec la taille des mémoires d’UC de bas de gamme. Dans les situations où le système dispose d’une mémoire physique limitée par rapport à la carte vidéo, la plupart de ces VRAMs ne peuvent pas être utilisés efficacement et des paramètres de détail inférieurs doivent être configurés.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance sur Real-Time conversion du taux d’échantillonnage audio

Une autre source courante de la gravure de cycle d’UC que nous avons constatée se produit lorsque le système audio est nécessaire pour convertir la vitesse de lecture pendant la combinaison dans le tampon matériel. avec les pilotes Windows Driver Model (WDM), le format de mémoire tampon matérielle n’est pas contrôlé par l’application directe, car il s’agit d’une ressource de niveau noyau. au lieu de cela, le format est sélectionné en fonction du format de qualité la plus élevée de toutes les sources et des capacités du matériel. par défaut, Windows XP utilise une conversion de taux d’échantillonnage de haute qualité pour ce processus, et si la majorité des exemples audio requièrent une conversion de taux, une partie importante des cycles de l’uc est consommée.

Nous vous recommandons de créer toutes vos mémoires tampons DirectSound avec le même taux d’échantillonnage. Si vous utilisez des fonctions Microsoft Win32 **WaveOut** , vous devez également utiliser un taux d’échantillonnage cohérent. Avec les pilotes WDM, les mémoires tampons sont toutes mélangées par le noyau, et si vous utilisez un taux d’échantillonnage plus élevé sur certains d’entre eux, les taux d’échantillonnage de tous les REST sont convertis en correspondance. Notez que cela implique l’utilisation du même taux de lecture pour tous vos échantillons audio, y compris les mémoires tampons de décompression audio en continu. la définition du taux de mémoire tampon principale n’a aucun effet, sauf si vous ciblez Windows 98 ou Windows Millennium Edition.

> [!Note]  
> sur Windows Vista et les versions ultérieures du système d’exploitation, DirectSound et **waveOut** utilisent l' [API de Session audio Windows (WASAPI)](/windows/desktop/CoreAudio/wasapi) pour toute la sortie audio.

 

## <a name="fragmention-of-virtual-memory"></a>Fragmentation de la mémoire virtuelle

Nous avons vu un certain nombre de problèmes récents liés à la limite de 32 bits sur l’espace mémoire du processus. Alors que 2 Go d’espace d’adressage virtuel pour les processus en mode utilisateur ont été plus qu’un historique suffisant, l’utilisation accrue de fichiers mappés en mémoire volumineux, d’allocateurs de mémoire personnalisés et de l’augmentation de la taille de VRAM (qui doit être mappée dans l’espace de processus) a commencé à provoquer des situations où les allocations d’espace mémoire virtuelle échouent Certaines dll non-Microsoft utilisent des emplacements à démarrage fixe au milieu de l’espace d’adressage virtuel, ce qui entraîne une fragmentation qui entraîne des échecs d’allocation.

Ces problèmes s’affichent le plus souvent lorsque le jeu utilise un schéma d’allocation de mémoire personnalisé qui tente d’allouer un grand segment continu d’espace de mémoire virtuelle. Nous vous recommandons d’écrire des allocateurs de sorte qu’ils demandent des parties de l’espace d’adressage virtuel plus raisonnablement, le cas échéant. Par exemple, en demandant 64 ou 256 Mo à la fois, mais pas 1 Go. Toutefois, il convient de veiller à ne pas provoquer une fragmentation supplémentaire. L’avènement des systèmes d’exploitation et du matériel 64 bits contribuera beaucoup à ces problèmes à l’avenir, mais vous devez veiller à ce que les systèmes 32 bits de génération actuelle soient pris en compte.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipulation du mot de contrôle Floating-Point

En guise d’aide au débogage, certains développeurs ont activé des exceptions sur l’unité de virgule flottante (FPU) via des manipulations du mot de contrôle à virgule flottante. Cette opération est très problématique et risque d’entraîner un blocage du processus. Tout comme la Convention d’appel exige que le registre ebx soit préservé, la majorité du système suppose que le FPU est dans un État par défaut, donne des résultats raisonnables et ne génère pas d’exceptions. Les pilotes et autres composants système calculent souvent des résultats en partant de l’hypothèse que les valeurs d’erreur standard apparaissent dans les registres pour des conditions erronées, mais si les exceptions sont activées, elles ne sont pas gérées et entraînent des blocages.

Direct3D définit l’unité à virgule flottante sur simple précision, en arrondissant à la valeur la plus proche dans le cadre de l’initialisation du thread appelant, sauf si l' \_ indicateur D3DCREATE FPU \_ Preserve est utilisé, auquel cas le mot de contrôle à virgule flottante est intact. Dans la mesure où le mot de contrôle est un paramètre par thread, garantir que tous les threads de votre application sont définis en mode de précision simple peut optimiser les performances. n’oubliez pas que l’appel de [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) n’est pas valide pour le codage natif x64, qui utilise exclusivement SSE à la place, et il est extrêmement onéreux sur l’architecture basée sur PowerPC de l’uc Xbox 360.

> [!Note]  
> Si vous modifiez le mot de contrôle, utilisez [**\_ controlfp \_**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) et sachez que pour les plateformes x64, vous ne pouvez pas modifier la précision à virgule flottante via le mot de contrôle.

 

Dans toutes les bibliothèques où nous avons besoin d’utiliser des règles d’arrondi ou d’autres comportements différents, par exemple pour gérer les nuanceurs de vertex logiciels ou la compilation, nous enregistrons et restaurons le mot de contrôle. Si un jeu doit utiliser des exceptions d’arrondi non standard ou FPU, il doit enregistrer et restaurer le mot de contrôle à virgule flottante, et vous devez vous assurer qu’il n’appelle pas de code externe qui n’a pas été prouvé comme étant à l’abri de ces problèmes, y compris les API système.

## <a name="optional-installation-of-the-directx-runtime"></a>Installation facultative du runtime DirectX

Un certain nombre de jeux demandent à l’utilisateur s’il faut installer DirectX. Cela peut entraîner des problèmes si l’utilisateur suppose que le package redistribuable DirectX le plus récent est installé et qu’il ignore l’installation et, par la suite, l’installation se poursuit correctement. Si le jeu requiert une version spécifique de D3DX ou d’autres fonctionnalités mises à jour qui n’ont pas été installées, le jeu ne fonctionnera pas et l’utilisateur sera très frustré.

Il est fortement recommandé que le programme d’installation du jeu installe en mode silencieux le package redistribuable DirectX sur lequel le jeu a été créé. Le processus d’installation de DirectX est conçu pour vérifier si quelque chose doit être mis à jour et retourne rapidement si ce n’est pas le cas. Par conséquent, il n’est pas nécessaire de demander à l’utilisateur l’installation de DirectX.

Une installation sans assistance de DirectX peut être effectuée en exécutant cette commande à partir de votre package d’installation : **dxsetup.exe/Silent**

En outre, la taille réelle du dossier redistribuable peut être configurée pour inclure uniquement les fichiers CAB (.cab) qui sont réellement nécessaires pour les plateformes et l’utilisation cibles du jeu.

> [!Note]  
> Avant d’utiliser **Dxsetup**, lisez- [le de façon indirecte](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Utilisation excessive de la synchronisation des threads

Lors du profilage des jeux, les zones réactives principales sont souvent liées à l’entrée et à la sortie des sections critiques. Avec la prévalence des UC multicœur, l’utilisation du multithreading dans les jeux a considérablement augmenté, et de nombreuses implémentations s’appuient sur une utilisation intensive de la synchronisation des threads. Le temps processeur nécessaire pour prendre une section critique même sans aucune contention est tout à fait significatif, et toutes les autres formes de synchronisation des threads sont encore plus coûteuses. Vous devez donc veiller à réduire l’utilisation de ces Primitives.

Une source courante de synchronisation excessive dans les jeux est l’utilisation de [D3DCREATE \_ multithread](/windows/desktop/direct3d9/d3dcreate). Cet indicateur, tout en rendant Direct3D thread-safe pour le rendu à partir de plusieurs threads, adopte une approche très prudente, ce qui entraîne une surcharge de synchronisation élevée. Les jeux doivent éviter cet indicateur. Au lieu de cela, concevez le moteur de sorte que toutes les communications avec Direct3D proviennent d’un thread unique et que toutes les communications entre les threads soient traitées directement. Pour plus d’informations sur la conception de jeux multithread, consultez l’article [codage de plusieurs cœurs sur Xbox 360 et Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores).

## <a name="use-of-rdtsc"></a>Utilisation de RDTSC

L’utilisation de l’instruction **RDTSC** x86 n’est pas recommandée. **RDTSC** ne parvient pas à calculer correctement le minutage sur certains schémas de gestion de l’alimentation qui modifient la fréquence de l’UC de manière dynamique et sur de nombreux processeurs multicœurs pour lesquels le compteur de cycle n’est pas synchronisé entre les cœurs. Les jeux doivent à la place utiliser l’API [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) . Pour plus d’informations sur les problèmes liés à **RDTSC** et l’implémentation du minutage haute résolution avec **QueryPerformanceCounter**, consultez l’article [synchronisation des jeux et processeurs multicœurs](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).

 

 
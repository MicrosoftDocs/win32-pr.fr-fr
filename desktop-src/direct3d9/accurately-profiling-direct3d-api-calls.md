---
description: Une fois que vous disposez d’une application Microsoft Direct3D fonctionnelle et que vous souhaitez améliorer ses performances, vous utilisez généralement un outil de profilage en dehors de la conservation ou une technique de mesure personnalisée pour mesurer le temps nécessaire à l’exécution d’un ou plusieurs appels de l’interface de programmation d’applications (API). Si vous avez effectué cette opération mais que vous obtenez des résultats de synchronisation qui varient d’une séquence de rendu à l’autre, ou que vous faites des calculs qui ne comportent pas de résultats d’expérimentation réels, les informations suivantes peuvent vous aider à comprendre pourquoi.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Profilage précis des appels d’API Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e47da58a3614270f89eefa1cfa33fbf30cf26544c1013d010696a68e4602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097467"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Profilage précis des appels d’API Direct3D (Direct3D 9)

-   [Il est difficile de Profiler avec précision Direct3D](#accurately-profiling-direct3d-is-difficult)
-   [Comment Profiler avec précision une séquence de rendu Direct3D](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Profilage des modifications de l’État Direct3D](#profiling-direct3d-state-changes)
-   [Résumé](#summary)
-   [A](#appendix)

Une fois que vous disposez d’une application Microsoft Direct3D fonctionnelle et que vous souhaitez améliorer ses performances, vous utilisez généralement un outil de profilage en dehors de la conservation ou une technique de mesure personnalisée pour mesurer le temps nécessaire à l’exécution d’un ou plusieurs appels de l’interface de programmation d’applications (API). Si vous avez effectué cette opération mais que vous obtenez des résultats de synchronisation qui varient d’une séquence de rendu à l’autre, ou que vous faites des calculs qui ne comportent pas de résultats d’expérimentation réels, les informations suivantes peuvent vous aider à comprendre pourquoi.

Les informations fournies ici sont basées sur l’hypothèse que vous connaissez et que vous avez besoin de connaître les éléments suivants :

-   Programmation C/C++
-   Programmation de l’API Direct3D
-   Mesure du temps de l’API
-   La carte vidéo et son pilote logiciel
-   Résultats inexpliqués possibles d’une expérience de profilage précédente

## <a name="accurately-profiling-direct3d-is-difficult"></a>Il est difficile de Profiler avec précision Direct3D

Un profileur signale le temps passé dans chaque appel d’API. Cela permet d’améliorer les performances en recherchant et en réglant les zones réactives. Il existe différents types de profileurs et de techniques de profilage.

-   Un profileur d’échantillonnage devient inactif une grande partie du temps, en se réexécutant à des intervalles spécifiques pour échantillonner les fonctions en cours d’exécution. Elle retourne le pourcentage de temps passé dans chaque appel. En règle générale, un profileur d’échantillonnage n’est pas très invasif pour l’application et a un impact minimal sur la surcharge de l’application.
-   Un profileur d’instrumentation mesure le temps réel nécessaire pour qu’un appel retourne. Elle nécessite la compilation des délimiteurs de démarrage et d’arrêt dans une application. Un profileur d’instrumentation est comparativement plus invasif pour une application qu’un générateur de profils d’échantillonnage.
-   Il est également possible d’utiliser une technique de profilage personnalisée avec un minuteur à hautes performances. Cela produit des résultats très similaires à ceux d’un profileur d’instrumentation.

Le type de profileur ou la technique de profilage utilisé n’est qu’une partie du défi qui consiste à générer des mesures précises.

Le profilage vous donne des réponses qui vous aident à budgétiser les performances. Supposons, par exemple, que vous sachiez qu’un appel d’API calcule la moyenne de 1000 cycles d’horloge à exécuter. Vous pouvez déclarer des conclusions sur les performances, telles que les suivantes :

-   Un processeur de 2 GHz (qui passe 50% de son temps de rendu) est limité à l’appel de cette API 1 million fois par seconde.
-   Pour atteindre 30 images par seconde, vous ne pouvez pas appeler cette API plus de 33 000 fois par frame.
-   Vous ne pouvez afficher que 3.3 Ko d’objets par trame (en supposant que 10 de ces appels d’API sont effectués pour chaque séquence de rendu de l’objet).

En d’autres termes, si vous aviez suffisamment de temps par appel d’API, vous pourriez répondre à une question de budgétisation, comme le nombre de primitives qui peuvent être rendues de manière interactive. Toutefois, les nombres bruts retournés par un profileur d’instrumentation ne répondront pas précisément aux questions de budget. Cela est dû au fait que le pipeline graphique présente des problèmes de conception complexes tels que le nombre de composants qui doivent effectuer le travail, le nombre de processeurs qui contrôlent le flux de travail entre les composants et les stratégies d’optimisation implémentées dans le runtime et dans un pilote qui sont conçues pour rendre le pipeline plus efficace.

### <a name="each-api-call-goes-through-several-components"></a>Chaque appel d’API passe par plusieurs composants

Chaque appel est traité par plusieurs composants en direction de l’application vers la carte vidéo. Par exemple, considérez la séquence de rendu suivante contenant deux appels pour dessiner un seul triangle :


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



Le diagramme conceptuel suivant montre les différents composants par le biais desquels les appels doivent réussir.

![diagramme des composants graphiques parcourant les appels d’API](images/microbenchmarkinstructionflow2.png)

L’application appelle Direct3D qui contrôle la scène, gère les interactions de l’utilisateur et détermine la façon dont le rendu est effectué. Tout ce travail est spécifié dans la séquence de rendu, qui est envoyée au runtime à l’aide d’appels d’API Direct3D. La séquence de rendu est pratiquement indépendante du matériel (autrement dit, les appels d’API sont indépendants du matériel, mais une application connaît les fonctionnalités prises en charge par une carte vidéo).

Le Runtime convertit ces appels dans un format indépendant du périphérique. Le Runtime gère toutes les communications entre l’application et le pilote, afin qu’une application s’exécute sur plusieurs éléments de matériel compatibles (selon les fonctionnalités requises). Lors de la mesure d’un appel de fonction, un profileur d’instrumentation mesure le temps qu’il a passé dans une fonction, ainsi que l’heure à laquelle la fonction doit être retournée. L’une des limitations d’un profileur d’instrumentation est qu’il peut ne pas inclure le temps nécessaire à un pilote pour envoyer le travail résultant à la carte vidéo, ni l’heure de la carte vidéo pour traiter le travail. En d’autres termes, un profileur d’instrumentation hors connexion ne parvient pas à attribuer un attribut à l’ensemble du travail associé à chaque appel de fonction.

Le pilote logiciel utilise une connaissance matérielle spécifique de la carte vidéo pour convertir les commandes indépendantes du périphérique en une séquence de commandes de carte vidéo. Les pilotes peuvent également optimiser la séquence de commandes qui sont envoyées à la carte vidéo, afin que le rendu sur la carte vidéo soit effectué efficacement. Ces optimisations peuvent entraîner des problèmes de profilage, car la quantité de travail effectuée n’est pas celle qu’elle semble être (vous devrez peut-être comprendre les optimisations pour les prendre en compte). Le pilote retourne généralement le contrôle à l’exécution avant que la carte vidéo ait terminé le traitement de toutes les commandes.

La carte vidéo effectue la majorité du rendu en combinant les données des mémoires tampons de vertex et d’index, des textures, des informations d’état de rendu et des commandes graphiques. Lorsque la carte vidéo termine le rendu, le travail créé à partir de la séquence de rendu est terminé.

Chaque appel d’API Direct3D doit être traité par chaque composant (le runtime, le pilote et la carte vidéo) pour restituer quoi que ce soit.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Plusieurs processeurs contrôlent les composants

La relation entre ces composants est encore plus complexe, car l’application, le runtime et le pilote sont contrôlés par un processeur et la carte vidéo est contrôlée par un processeur distinct. Le diagramme suivant illustre deux types de processeurs : une unité centrale (UC) et une unité de traitement graphique (GPU).

![diagramme d’une UC et d’un GPU et de leurs composants](images/microbenchmarkprocessors.png)

Les PC disposent d’au moins un processeur et d’un GPU, mais ils peuvent avoir plus d’un ou des deux. Les processeurs sont situés sur la carte mère et les GPU se trouvent soit sur la carte mère, soit sur la carte vidéo. La vitesse du processeur est déterminée par une puce de l’horloge sur la carte mère, et la vitesse du GPU est déterminée par une puce d’horloge distincte. L’horloge de l’UC contrôle la vitesse du travail effectué par l’application, le runtime et le pilote. L’application envoie un travail au GPU par le biais du runtime et du pilote.

L’UC et le GPU s’exécutent généralement à des vitesses différentes, indépendamment les unes des autres. Le GPU peut répondre au travail dès que le travail est disponible (en supposant que le GPU a fini de traiter le travail précédent). Le travail GPU est effectué en parallèle avec le travail du processeur mis en surbrillance par la ligne courbée dans la figure ci-dessus. Un profileur mesure généralement les performances de l’UC, et non le GPU. Cela complique le profilage, car les mesures effectuées par un profileur d’instrumentation incluent le temps processeur, mais peuvent ne pas inclure le temps GPU.

L’objectif du GPU est de décharger le traitement du processeur vers un processeur conçu spécifiquement pour le travail graphique. Sur les cartes vidéo modernes, le GPU remplace une grande partie des tâches de transformation et d’éclairage dans le pipeline du processeur au GPU. Cela réduit considérablement la charge de travail du processeur, ce qui laisse plus de cycles de processeur disponibles pour d’autres traitements. Pour paramétrer une application graphique pour des performances de pointe, vous devez mesurer les performances de l’UC et du GPU, et équilibrer le travail entre les deux types de processeurs.

Ce document ne couvre pas les sujets liés à la mesure des performances du GPU ou à l’équilibrage du travail entre l’UC et le GPU. Si vous souhaitez mieux comprendre les performances d’un GPU (ou d’une carte vidéo particulière), visitez le site Web du fournisseur pour obtenir plus d’informations sur les performances du GPU. Au lieu de cela, ce document met l’accent sur le travail effectué par le runtime et le pilote en réduisant le travail du GPU à une quantité négligeable. Cela est en partie basé sur l’expérience dans laquelle les applications qui rencontrent des problèmes de performances sont généralement limitées par le processeur.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Les optimisations du runtime et du pilote peuvent masquer les mesures de l’API

Le runtime intègre une optimisation des performances qui peut saturer la mesure d’un appel individuel. Voici un exemple de scénario illustrant ce problème. Considérez la séquence de rendu suivante :


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Exemple 1 : séquence de rendu simple

En examinant les résultats des deux appels dans la séquence de rendu, un profileur d’instrumentation peut retourner des résultats similaires à ceux-ci :


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



Le profileur retourne le nombre de cycles de processeur requis pour traiter le travail associé à chaque appel (n’oubliez pas que le GPU n’est pas inclus dans ces numéros, car le GPU n’a pas encore commencé à travailler sur ces commandes). Étant donné que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) nécessitait presque un million de cycles à traiter, vous pouvez conclure qu’il n’est pas très efficace. Toutefois, vous verrez bientôt pourquoi cette conclusion est incorrecte et comment vous pouvez générer des résultats qui peuvent être utilisés pour la budgétisation.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>La mesure des modifications d’état nécessite des séquences de rendu prudentes

Tous les appels autres que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)ou [**Clear**](/windows/desktop/api) (tels que [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api)et [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) produisent un changement d’État. Chaque modification d’État définit l’état du pipeline qui contrôle comment le rendu sera effectué.

Les optimisations dans le runtime et/ou le pilote sont conçues pour accélérer le rendu en réduisant la quantité de travail requise. Voici quelques-unes des optimisations de modification d’État qui peuvent polluer les moyennes de profil :

-   Un pilote (ou le Runtime) peut enregistrer une modification d’État comme un état local. Étant donné que le pilote peut fonctionner dans un algorithme « paresseux » (en différant le travail jusqu’à ce qu’il soit absolument nécessaire), le travail associé à certains changements d’État peut être retardé.
-   Le Runtime (ou un pilote) peut supprimer les modifications d’État en optimisant. Par exemple, vous pouvez supprimer un changement d’État redondant qui désactive l’éclairage, car l’éclairage a déjà été désactivé.

Il n’existe aucun moyen infaillible d’examiner une séquence de rendu et de conclure les modifications d’État qui définiront un bit d’intégrité et de différer le travail, ou sera simplement supprimée par l’optimisation. Même si vous pouviez identifier des modifications d’État optimisées dans le runtime ou le pilote d’aujourd’hui, le runtime ou le pilote de demain est susceptible d’être mis à jour. Vous ne connaissez pas non plus facilement l’état précédent et il est donc difficile d’identifier les changements d’État redondants. La seule façon de vérifier le coût d’un changement d’État est de mesurer la séquence de rendu qui comprend les modifications d’État.

Comme vous pouvez le voir, les complications causées par l’utilisation de plusieurs processeurs, les commandes traitées par plusieurs composants et les optimisations intégrées aux composants rendent le profilage difficile à prédire. Dans la section suivante, chacun de ces défis de profilage sera traité. Des exemples de séquences de rendu Direct3D s’affichent, avec les techniques de mesure associées. Grâce à ces connaissances, vous serez en mesure de générer des mesures précises et reproductibles sur des appels individuels.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Comment Profiler avec précision une séquence de rendu Direct3D

Maintenant que certains des défis de profilage ont été mis en évidence, cette section vous montrera des techniques qui vous aideront à générer des mesures de profil qui peuvent être utilisées pour la budgétisation. Des mesures de profilage précises et reproductibles sont possibles si vous comprenez la relation entre les composants contrôlés par l’UC et comment éviter les optimisations de performances implémentées par le runtime et le pilote.

Pour commencer, vous devez être en mesure de mesurer avec précision la durée d’exécution d’un appel d’API unique.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Choisissez un outil de mesure précis comme QueryPerformanceCounter

le système d’exploitation Microsoft Windows comprend un minuteur haute résolution qui peut être utilisé pour mesurer les temps écoulés à haute résolution. La valeur actuelle d’une telle minuterie peut être retournée à l’aide de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Après l’appel de **QueryPerformanceCounter** pour retourner les valeurs de début et de fin, la différence entre les deux valeurs peut être convertie en temps réel écoulé (en secondes) à l’aide de **QueryPerformanceCounter**.

les avantages de l’utilisation de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) sont qu’elle est disponible dans Windows et qu’elle est facile à utiliser. Entourez simplement les appels avec un appel **QueryPerformanceCounter** et enregistrez les valeurs de début et de fin. Par conséquent, ce document explique comment utiliser **QueryPerformanceCounter** pour profiler les durées d’exécution, de la même manière qu’un profileur d’instrumentation le mesure. Voici un exemple qui montre comment incorporer **QueryPerformanceCounter** dans votre code source :


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



Exemple 2 : implémentation personnalisée du profilage avec QPC

Start et stop sont deux entiers volumineux qui contiendront les valeurs Start et Stop retournées par le minuteur hautes performances. Notez que QueryPerformanceCounter (&Start) est appelé juste avant [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et QueryPerformanceCounter (&Stop) est appelé juste après [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Après avoir obtenu la valeur d’arrêt, QueryPerformanceFrequency est appelé pour retourner FREQ, qui est la fréquence de la minuterie haute résolution. Dans cet exemple hypothétique, supposons que vous obteniez les résultats suivants pour Start, stop et FREQ :



| Variable locale | Nombre de graduations |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| Fréq           | 3579545         |



 

Vous pouvez convertir ces valeurs en nombre de cycles nécessaires pour exécuter les appels d’API comme suit :


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



En d’autres termes, il faut environ 4568 cycles d’horloge pour traiter [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sur cet ordinateur de 2 GHz. Vous pouvez convertir ces valeurs en temps réel nécessaire pour exécuter tous les appels de la façon suivante :


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



L’utilisation de QueryPerformanceCounter requiert l’ajout de mesures de démarrage et d’arrêt à votre séquence de rendu et l’utilisation de QueryPerformanceFrequency pour convertir la différence (nombre de graduations) en nombre de cycles du processeur ou en temps réel. L’identification de la technique de mesure est un bon point de départ pour le développement d’une implémentation de profilage personnalisée. Mais avant de commencer à effectuer des mesures, vous devez savoir comment gérer la carte vidéo.

### <a name="focus-on-cpu-measurements"></a>Focus sur les mesures de l’UC

Comme indiqué précédemment, l’UC et le GPU fonctionnent en parallèle pour traiter le travail généré par les appels d’API. Une application réelle nécessite de profiler les deux types de processeurs pour déterminer si votre application est limitée par le processeur ou par GPU. Étant donné que les performances du GPU sont spécifiques au fournisseur, il serait très difficile de produire des résultats dans ce document qui couvre la variété des cartes vidéo disponibles.

Au lieu de cela, ce document se concentre uniquement sur le profilage du travail effectué par le processeur à l’aide d’une technique personnalisée pour mesurer le travail du runtime et du pilote. Le travail GPU est réduit à une quantité insignifiante, de sorte que les résultats de l’UC sont plus visibles. L’un des avantages de cette approche est que cette technique produit les résultats dans l’annexe que vous devez être en mesure de mettre en corrélation avec vos mesures. Pour réduire le travail requis par la carte vidéo à un niveau non significatif, réduisez simplement le travail de rendu le moins possible. Cela peut être accompli en limitant les appels de dessin pour afficher un triangle unique et peut être davantage limité afin que chaque triangle contienne uniquement un pixel.

L’unité de mesure utilisée dans ce document pour mesurer le travail de l’UC est le nombre de cycles d’horloge de l’UC plutôt que le temps réel. Les cycles d’horloge de l’UC ont l’avantage d’être plus portables (pour les applications limitées par le processeur) que le temps écoulé réel sur les ordinateurs avec des vitesses de processeur différentes. Cette valeur peut être facilement convertie en temps réel si vous le souhaitez.

Ce document ne couvre pas les sujets liés à l’équilibrage de la charge de travail entre l’UC et le GPU. N’oubliez pas que l’objectif de ce document est de ne pas mesurer les performances globales d’une application, mais de mesurer avec précision le temps nécessaire au runtime et au pilote pour traiter les appels d’API. Avec ces mesures précises, vous pouvez effectuer la tâche de budgétisation de l’UC pour comprendre certains scénarios de performances.

### <a name="controlling-runtime-and-driver-optimizations"></a>Contrôle des optimisations du runtime et du pilote

Avec une technique de mesure identifiée et une stratégie pour réduire le travail du GPU, l’étape suivante consiste à comprendre les optimisations du runtime et du pilote qui s’imposent lorsque vous profilez.

Le travail du processeur peut être divisé en trois compartiments : l’application, le travail d’exécution et le pilote fonctionnent. Ignorez le travail de l’application, car il est sous contrôle du programmeur. Du point de vue de l’application, le runtime et le pilote sont semblables aux zones noires, car l’application n’a aucun contrôle sur ce qui est implémenté dans ces zones. La clé consiste à comprendre les techniques d’optimisation qui peuvent être implémentées dans le runtime et le pilote. Si vous ne comprenez pas ces optimisations, il est très facile de passer à une mauvaise conclusion quant à la quantité de travail effectuée par le processeur en fonction des mesures du profil. En particulier, il existe deux rubriques relatives à un élément appelé mémoire tampon de commande et ce qu’il peut faire pour obscurcir le profilage. Ces rubriques sont les suivantes :

-   Optimisation du Runtime avec la mémoire tampon de commande. La mémoire tampon de commande est une optimisation du runtime qui réduit l’impact d’une transition de mode. Pour contrôler le minutage de la transition en mode, consultez [contrôle du tampon de commande](#controlling-the-command-buffer).
-   Négation des effets de minutage de la mémoire tampon de commande. Le temps écoulé d’une transition de mode peut avoir un impact important sur le profilage des mesures. La stratégie consiste à [rendre la séquence de rendu volumineuse par rapport à la transition en mode](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Contrôle de la mémoire tampon de commande

Lorsqu’une application effectue un appel d’API, le Runtime convertit l’appel d’API en un format indépendant du périphérique (que nous appelons une commande) et le stocke dans le tampon de commande. Le tampon de commande est ajouté au diagramme suivant.

![diagramme des composants de l’UC, y compris une mémoire tampon de commande](images/microbenchmarkcommandbuffer2.png)

Chaque fois que l’application effectue un autre appel d’API, le runtime répète cette séquence et ajoute une autre commande à la mémoire tampon de commande. À un moment donné, le runtime vide la mémoire tampon (en envoyant les commandes au pilote). dans Windows XP, le vidage du tampon de commande entraîne une transition du mode à mesure que le système d’exploitation bascule du runtime (exécuté en mode utilisateur) au pilote (exécuté en mode noyau), comme indiqué dans le diagramme suivant.

-   mode utilisateur : mode de processeur non privilégié qui exécute le code de l’application. Les applications en mode utilisateur ne peuvent pas accéder aux données système, sauf par le biais des services système.
-   mode noyau : mode processeur privilégié dans lequel s’exécute le code exécutif Windows. Un pilote ou un thread s’exécutant en mode noyau a accès à toute la mémoire système, à l’accès direct au matériel et aux instructions de l’UC pour effectuer des e/s avec le matériel.

![diagramme des transitions entre le mode utilisateur et le mode noyau](images/microbenchmarkcommandbuffer3.png)

La transition se produit chaque fois que l’UC passe du mode utilisateur au mode noyau (et inversement) et que le nombre de cycles nécessaires est élevé par rapport à un appel d’API individuel. Si le runtime a envoyé chaque appel d’API au pilote lorsqu’il a été appelé, chaque appel d’API entraînerait le coût d’une transition de mode.

Au lieu de cela, la mémoire tampon de commande est une optimisation du runtime conçue pour réduire le coût effectif de la transition du mode. La mémoire tampon de commande met en file d’attente de nombreuses commandes de pilote en vue d’une transition en mode unique. Quand le runtime ajoute une commande à la mémoire tampon de commande, le contrôle est retourné à l’application. Un profileur n’a aucun moyen de savoir que les commandes de pilote n’ont probablement pas encore été envoyées au pilote. Par conséquent, les nombres retournés par un profileur d’instrumentation hors service sont trompeurs puisqu’il mesure le travail du runtime, mais pas le fonctionnement du pilote associé.

### <a name="profile-results-without-a-mode-transition"></a>Résultats de profil sans transition de mode

À l’aide de la séquence de rendu de l’exemple 2, voici quelques mesures de minutage typiques qui illustrent la grandeur d’une transition de mode. En supposant que les appels [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) n’entraînent pas de transition en mode, un profileur d’instrumentation hors connexion peut retourner des résultats similaires à ceux-ci :


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Chacun de ces nombres est la durée nécessaire au runtime pour ajouter ces appels au tampon de commande. Étant donné qu’il n’y a aucune transition en mode, le pilote n’a pas encore effectué de travail. Les résultats du profileur sont exacts, mais ils ne mesurent pas tout le travail que la séquence de rendu finira par entraîner l’exécution du processeur.

### <a name="profile-results-with-a-mode-transition"></a>Résultats de profil avec une transition de mode

À présent, examinez ce qui se passe pour le même exemple quand une transition de mode se produit. Cette fois, supposons que [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) provoquent une transition de mode. Une fois encore, un profileur d’instrumentation à l’emploi peut retourner des résultats similaires à ceux-ci :


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



La durée mesurée pour [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est à peu de temps égale, mais l’augmentation spectaculaire du temps passé dans [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) est due à la transition en mode. Voici ce qui se passe :

1.  Supposons que le tampon de commande dispose de suffisamment d’espace pour une commande avant le démarrage de la séquence de rendu.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est converti en un format indépendant du périphérique et ajouté à la mémoire tampon de commande. Dans ce scénario, cet appel remplit la mémoire tampon de commande.
3.  Le runtime tente d’ajouter [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) à la mémoire tampon de commande, mais ne le peut pas, car il est plein. Au lieu de cela, le runtime vide la mémoire tampon de commande. Cela provoque la transition en mode noyau. Supposons que la transition dure environ 5000 cycles. Cette fois, participe au temps passé dans **DrawPrimitive**.
4.  Le pilote traite ensuite le travail associé à toutes les commandes qui ont été vidées de la mémoire tampon de commande. Supposons que le temps du pilote pour traiter les commandes qui ont presque rempli le tampon de commande est d’environ 935 000 cycles. Supposons que le fonctionnement du pilote associé à [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est d’environ 2750 cycles. Cette fois, participe au temps passé dans [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).
5.  Lorsque le pilote termine son travail, la transition en mode utilisateur retourne le contrôle au Runtime. Le tampon de commande est maintenant vide. Supposons que la transition dure environ 5000 cycles.
6.  La séquence de rendu se termine en convertissant [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) et en l’ajoutant à la mémoire tampon de commande. Supposons que cela prend environ 900 cycles. Cette fois, participe au temps passé dans **DrawPrimitive**.

En résumant les résultats, vous voyez :


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Tout comme la mesure pour [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sans la transition de mode (cycles 900), la mesure pour **DrawPrimitive** avec la transition de mode (947 950 cycles) est exacte, mais inutile en termes de budget du travail de l’UC. Le résultat contient le bon fonctionnement du runtime, le pilote fonctionne pour [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), le pilote fonctionne pour toutes les commandes qui précèdent **SetTexture** et les transitions en deux modes. Toutefois, il manque le travail du pilote **DrawPrimitive** dans la mesure.

Une transition en mode peut avoir lieu en réponse à un appel. Cela dépend de ce qui se trouvait précédemment dans le tampon de commande. Vous devez contrôler la transition du mode pour comprendre la quantité de travail de l’UC (Runtime et pilote) associée à chaque appel. Pour ce faire, vous avez besoin d’un mécanisme pour contrôler la mémoire tampon de commande et le minutage de la transition de mode.

### <a name="the-query-mechanism"></a>Mécanisme de requête

Le mécanisme de requête de Microsoft Direct3D 9 a été conçu pour permettre au runtime d’interroger le GPU à des fins de progression et de retourner certaines données à partir du GPU. Lors du profilage, si le travail du GPU est réduit afin d’avoir un impact négligeable sur les performances, vous pouvez retourner l’état du GPU pour aider à mesurer le fonctionnement du pilote. Après tout, le fonctionnement du pilote est terminé lorsque le GPU a vu les commandes du pilote. En outre, le mécanisme de requête peut être coaxiaux en contrôlant deux caractéristiques de mémoire tampon de commande qui sont importantes pour le profilage : lorsque le tampon de commande est vidé et la quantité de travail dans la mémoire tampon.

Voici la même séquence de rendu à l’aide du mécanisme de requête :


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



Exemple 3 : utilisation d’une requête pour contrôler la mémoire tampon de commande

Voici une explication plus détaillée de chacune de ces lignes de code :

1.  Créez une requête d’événement en créant un objet de requête avec l' \_ événement D3DQUERYTYPE.
2.  Ajoutez un marqueur d’événement de requête à la mémoire tampon de commande en appelant [**issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ end**](d3dissue-end.md)). Ce marqueur indique au pilote d’effectuer le suivi de la fin de l’exécution des commandes précédées du marqueur par le GPU.
3.  Le premier appel vide la mémoire tampon de commande, car l’appel de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) avec [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) force le vidage de la mémoire tampon de commande. Chaque appel suivant consiste à vérifier le GPU pour voir quand il termine le traitement de l’ensemble du travail de mémoire tampon de commande. Cette boucle ne retourne pas \_ la réponse OK tant que le GPU n’est pas inactif.
4.  Échantillonne l’heure de début.
5.  Appelez les appels d’API en cours de profilage.
6.  Ajoutez un deuxième marqueur d’événement de requête à la mémoire tampon de commande. Ce marqueur sera utilisé pour suivre l’achèvement des appels.
7.  Le premier appel vide la mémoire tampon de commande, car l’appel de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) avec [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) force le vidage de la mémoire tampon de commande. Lorsque le GPU termine le traitement de l’ensemble du travail de mémoire tampon de commande, **GetData** retourne \_ la valeur OK, et la boucle est abandonnée, car le GPU est inactif.
8.  Échantillonne l’heure d’arrêt.

Voici les résultats mesurés avec QueryPerformanceCounter et QueryPerformanceFrequency :



| Variable locale | Nombre de graduations |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| Fréq           | 3579545         |



 

Conversion des battements en cycles une nouvelle fois (sur une machine de 2 GHz) :


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Voici la répartition du nombre de cycles par appel :


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



Le mécanisme de requête nous a permis de contrôler le runtime et le travail du pilote mesuré. Pour comprendre chacun de ces nombres, voici ce qui se passe en réponse à chacun des appels d’API, ainsi que les minutages estimés :

1.  Le premier appel vide la mémoire tampon de commande en appelant [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) avec [**D3DGETDATA \_ flush**](d3dgetdata-flush.md). Lorsque le GPU termine le traitement de l’ensemble du travail de mémoire tampon de commande, **GetData** retourne \_ la valeur OK, et la boucle est abandonnée, car le GPU est inactif.
2.  La séquence de rendu commence par convertir [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) en un format indépendant du périphérique et en l’ajoutant à la mémoire tampon de commande. Supposons que cela prend environ 100 cycles.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) est converti et ajouté à la mémoire tampon de commande. Supposons que cela prend environ 900 cycles.
4.  Le [**problème**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) ajoute un marqueur de requête à la mémoire tampon de commande. Supposons que cela prend environ 200 cycles.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) provoque le vidage de la mémoire tampon de commande, ce qui force la transition en mode noyau. Supposons que cela prend environ 5000 cycles.
6.  Le pilote traite ensuite le travail associé aux quatre appels. Supposons que le temps du pilote pour traiter le [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est d’environ 2964 cycles, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) est d’environ 3600 cycles, le [**problème**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) est d’environ 200 cycles. Ainsi, le temps total du pilote pour les quatre commandes est d’environ 6450 cycles.
    > [!Note]  
    > Le pilote prend également un peu de temps pour voir l’état du GPU. Étant donné que le fonctionnement du GPU est trivial, le GPU doit déjà être fait. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne la réponse \_ OK en fonction de la probabilité que le GPU soit terminé.

     

7.  Lorsque le pilote termine son travail, la transition en mode utilisateur retourne le contrôle au Runtime. Le tampon de commande est maintenant vide. Supposons que cela prend environ 5000 cycles.

Les nombres pour [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) sont les suivants :


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



Le mécanisme de requête utilisé en association avec QueryPerformanceCounter mesure tout le travail du processeur. Cette opération s’effectue avec une combinaison de marqueurs de requête et des comparaisons d’état des requêtes. Les marqueurs de début et de fin de requête ajoutés au tampon de commande permettent de contrôler la quantité de travail dans la mémoire tampon. En attendant que le code de retour correct soit retourné, la mesure de début est effectuée juste avant le début d’une séquence de rendu propre, et la mesure d’arrêt est effectuée juste après que le pilote a terminé le travail associé au contenu de la mémoire tampon de commande. Cela permet de capturer efficacement le travail du processeur effectué par le runtime ainsi que le pilote.

Maintenant que vous connaissez la mémoire tampon de commande et l’effet qu’elle peut avoir sur le profilage, vous devez savoir qu’il existe quelques autres conditions qui peuvent entraîner le vidage du tampon de commande par le Runtime. Vous devez les surveiller dans vos séquences de rendu. Certaines de ces conditions sont en réponse à des appels d’API, d’autres sont en réponse à des modifications de ressources dans le Runtime. L’une des conditions suivantes entraîne une transition de mode :

-   Quand l’une des méthodes de verrouillage ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) est appelée sur une mémoire tampon de vertex, une mémoire tampon d’index ou une texture (sous certaines conditions avec certains indicateurs).
-   Lors de la création d’une mémoire tampon de l’appareil ou d’un vertex, d’un tampon d’index ou d’une texture.
-   Quand une mémoire tampon de périphérique ou de vertex, une mémoire tampon d’index ou une texture sont détruites par la dernière version.
-   Lorsque [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) est appelé.
-   Lorsqu’il est [**présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) , est appelé.
-   Lorsque la mémoire tampon de commande est remplie.
-   Lorsque [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) est appelé avec D3DGETDATA \_ Flush.

Veillez à surveiller ces conditions dans vos séquences de rendu. À chaque fois qu’une transition de mode est ajoutée, 10 000 cycles de travail du pilote sont ajoutés à vos mesures de profilage. En outre, la mémoire tampon de commande n’est pas dimensionnée statiquement. Le runtime peut modifier la taille de la mémoire tampon en réponse à la quantité de travail qui est générée par l’application. Il s’agit d’une autre optimisation qui est dépendante d’une séquence de rendu.

Veillez donc à contrôler les transitions de mode pendant le profilage. Le mécanisme de requête offre une méthode fiable pour vider le tampon de commande afin que vous puissiez contrôler le minutage de la transition du mode, ainsi que la quantité de travail que contient la mémoire tampon. Toutefois, même cette technique peut être améliorée en réduisant le temps de transition du mode pour qu’elle soit non significative en ce qui concerne le résultat mesuré.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Rendre la séquence de rendu plus grande comparée à la transition de mode

Dans l’exemple précédent, le commutateur en mode noyau et le commutateur en mode utilisateur consomment environ 10 000 cycles qui n’ont rien à faire avec le fonctionnement du runtime et du pilote. Étant donné que la transition de mode est intégrée au système d’exploitation, elle ne peut pas être réduite à zéro. Pour rendre le mode non significatif, la séquence de rendu doit être ajustée pour que le fonctionnement du pilote et du runtime soit un ordre de grandeur supérieur aux commutateurs de mode. Vous pouvez essayer d’effectuer une soustraction pour supprimer les transitions, mais l’amortissement du coût sur un coût de séquence de rendu bien plus élevé est plus fiable.

La stratégie de réduction du mode de transition jusqu’à ce qu’il devienne non significatif consiste à ajouter une boucle à la séquence de rendu. Par exemple, examinons les résultats de profilage si vous ajoutez une boucle qui répétera la séquence de rendu 1500 fois :


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



Exemple 4 : ajouter une boucle à la séquence de rendu

Voici les résultats mesurés avec QueryPerformanceCounter et QueryPerformanceFrequency :



| Variable locale | Nombre de tics |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| Fréq           | 3579545        |



 

L’utilisation des mesures QueryPerformanceCounter 2 840 est maintenant terminée. La conversion des battements en cycles est identique à celle que nous avons déjà indiquée :


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



En d’autres termes, il faut environ 6,9 millions cycles sur cet ordinateur de 2 GHz pour traiter les appels 1500 dans la boucle de rendu. Des cycles de 6,9 millions, la durée des transitions de mode est d’environ 10 Ko, donc les résultats du profil sont presque entièrement mesurant le travail associé à [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Notez que l’exemple de code requiert un tableau de deux textures. Pour éviter une optimisation du runtime qui supprime [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) si elle définit le même pointeur de texture chaque fois qu’elle est appelée, utilisez simplement un tableau de deux textures. De cette façon, chaque fois que la boucle est exécutée, le pointeur de texture change et le travail complet associé à **SetTexture** est effectué. Assurez-vous que les deux textures ont la même taille et le même format, afin qu’aucun autre État ne change en cas de texture.

Et maintenant, vous disposez d’une technique pour profiler Direct3D. Il s’appuie sur le compteur de performances élevé (QueryPerformanceCounter) pour enregistrer le nombre de graduations qu’il prend pour traiter le travail. Le travail est soigneusement contrôlé pour être le travail du runtime et du pilote associé aux appels d’API à l’aide du mécanisme de requête. Une requête fournit deux méthodes de contrôle : tout d’abord pour vider la mémoire tampon de commande avant le démarrage de la séquence de rendu, et ensuite pour retourner à la fin du travail GPU.

Jusqu’à présent, ce document explique comment profiler une séquence de rendu. Chaque séquence de rendu a été assez simple, contenant un appel [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) unique et un appel [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Cela a été fait pour se concentrer sur la mémoire tampon de commande et l’utilisation du mécanisme de requête pour la contrôler. Voici un bref résumé de la procédure de profilage d’une séquence de rendu arbitraire :

-   Utilisez un compteur de performances élevé comme QueryPerformanceCounter pour mesurer le temps nécessaire au traitement de chaque appel d’API. Utilisez QueryPerformanceFrequency et le taux d’horloge de l’UC pour convertir cela en nombre de cycles de processeur par appel d’API.
-   Réduisez le nombre d’opérations GPU en affichant des listes de triangles, où chaque triangle contient un pixel.
-   Utilisez le mécanisme de requête pour vider la mémoire tampon de commande avant la séquence de rendu. Cela permet de garantir que le profilage capturera la quantité correcte de travail de Runtime et de pilote associée à la séquence de rendu.
-   Contrôler la quantité de travail ajoutée à la mémoire tampon de commande à l’aide de marqueurs d’événements de requête. Cette même requête détecte à quel moment le travail du GPU est terminé. Étant donné que le fonctionnement du GPU est trivial, il est quasiment équivalent à la mesure de la fin du fonctionnement du pilote.

Toutes ces techniques sont utilisées pour profiler les changements d’État. En supposant que vous avez lu et compris comment contrôler le tampon de commande et que vous avez terminé avec succès les mesures de ligne de base sur [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), vous êtes prêt à ajouter des modifications d’État à vos séquences de rendu. Il existe quelques défis supplémentaires de profilage lors de l’ajout de modifications d’État à une séquence de rendu. Si vous envisagez d’ajouter des modifications d’État à vos séquences de rendu, veillez à passer à la section suivante.

## <a name="profiling-direct3d-state-changes"></a>Profilage des modifications de l’État Direct3D

Direct3D utilise de nombreux États de rendu pour contrôler presque tous les aspects du pipeline. Les API qui entraînent des changements d’État incluent toute fonction ou méthode autre que les \* appels de primitives de dessin.

Les changements d’État sont délicats, car il est possible que vous ne puissiez pas voir le coût d’un changement d’État sans rendu. Cela est dû à l’algorithme paresseux utilisé par le pilote et le GPU pour différer le travail jusqu’à ce qu’il soit absolument nécessaire. En général, vous devez suivre ces étapes pour mesurer un seul changement d’État :

1.  Commencez par Profiler [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .
2.  Ajoutez une modification d’État à la séquence de rendu et profilez la nouvelle séquence.
3.  Soustraire la différence entre les deux séquences pour connaître le coût du changement d’État.

Naturellement, tout ce que vous avez appris à utiliser le mécanisme de requête et à placer la séquence de rendu dans une boucle pour nier le coût de la transition en mode s’applique toujours.

### <a name="profiling-a-simple-state-change"></a>Profilage d’une modification d’état simple

À partir d’une séquence de rendu qui contient [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), voici la séquence de code pour mesurer le coût de l’ajout de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



Exemple 5 : mesure d’un appel d’API de modification d’État

Notez que la boucle contient deux appels, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). La séquence de rendu effectue une boucle de 1500 fois et génère des résultats similaires à ceux-ci :



| Variable locale | Nombre de tics |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| Fréq           | 3579545        |



 

La conversion des battements en cycles à nouveau donne :


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



La division par le nombre d’itérations dans la boucle génère :


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Chaque itération de la boucle contient un changement d’État et un appel de dessin. Le fait de soustraire le résultat de la séquence de rendu [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) laisse :


```
3850 - 1100 = 2750 cycles for SetTexture
```



Il s’agit du nombre moyen de cycles pour ajouter des [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) à cette séquence de rendu. Cette même technique peut être appliquée à d’autres modifications d’État.

Pourquoi la [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est-elle appelée simple changement d’État ? Étant donné que l’état défini est restreint afin que le pipeline effectue la même quantité de travail chaque fois que l’État est modifié. Contraindre les deux textures à la même taille et au même format garantit la même quantité de travail pour chaque appel **SetTexture** .

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Profilage d’une modification d’État qui doit être activée/désactivée

D’autres modifications d’État peuvent entraîner la modification de la quantité de travail effectuée par le pipeline Graphics pour chaque itération de la boucle de rendu. Par exemple, si le test z est activé, chaque couleur de pixel met à jour une cible de rendu uniquement après que la valeur z du nouveau pixel a été testée par rapport à la valeur z du pixel existant. Si le test z est désactivé, ce test par pixel n’est pas effectué et la sortie est écrite beaucoup plus rapidement. L’activation ou la désactivation de l’État z-test modifie considérablement la quantité de travail effectuée (par le processeur et le GPU) pendant le rendu.

[**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) requiert un état de rendu particulier et une valeur d’État pour activer ou désactiver le test z. La valeur d’État particulière est évaluée au moment de l’exécution pour déterminer la quantité de travail nécessaire. Il est difficile de mesurer ce changement d’État dans une boucle de rendu tout en préservant l’état du pipeline pour qu’il bascule. La seule solution consiste à basculer le changement d’État au cours de la séquence de rendu.

Par exemple, la technique de profilage doit être répétée deux fois, comme suit :

1.  Commencez par profiler la séquence de rendu [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) . Appelez cette ligne de base.
2.  Profiler une deuxième séquence de rendu qui bascule le changement d’État. La boucle de séquence de rendu contient les éléments suivants :
    -   Changement d’État pour définir l’État dans une condition « false ».
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) exactement comme la séquence d’origine.
    -   Changement d’État pour définir l’État dans une condition « true ».
    -   Deuxième [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pour forcer la réalisation de la deuxième modification d’État.
3.  Recherchez la différence entre les deux séquences de rendu. Pour ce faire :
    -   Multipliez la séquence de base [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) par 2, car il existe deux appels **DrawPrimitive** dans la nouvelle séquence.
    -   Soustrait le résultat de la nouvelle séquence de la séquence d’origine.
    -   Divisez le résultat par 2 pour obtenir le coût moyen du changement d’état « false » et « true ».

Avec la technique de bouclage utilisée dans la séquence de rendu, le coût de la modification de l’état du pipeline doit être mesuré en basculant l’état d’une « vraie » à une condition « false » et vice versa, pour chaque itération de la séquence de rendu. La signification de « true » et « false » ici ne sont pas des littéraux, ce qui signifie simplement que l’État doit être défini dans des conditions opposées. Cela entraîne la mesure des modifications d’État au cours du profilage. Bien entendu, tout ce que vous avez appris à utiliser le mécanisme de requête et à placer la séquence de rendu dans une boucle pour nier le coût de la transition en mode s’applique toujours.

Par exemple, voici la séquence de code pour mesurer le coût d’activation ou de désactivation du test z :


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



Exemple 5 : mesure d’un changement d’état de basculement

La boucle bascule l’État en exécutant deux appels [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . Le premier appel **SetRenderState** désactive z-testing et le second **SetRenderState** active les tests z. Chaque **SetRenderState** est suivi par [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , de sorte que le travail associé au changement d’État est traité par le pilote au lieu de définir uniquement un bit non intègre dans le pilote.

Ces nombres sont raisonnables pour cette séquence de rendu :



| Variable locale | Nombre de graduations |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| Fréq           | 3579545         |



 

La conversion des battements en cycles à nouveau donne :


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



La division par le nombre d’itérations dans la boucle génère :


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Chaque itération de la boucle contient deux modifications d’État et deux appels de dessin. La soustraction des appels de dessin (en supposant que 1100 cycles) laisse :


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Il s’agit du nombre moyen de cycles pour les deux changements d’État. la durée moyenne pour chaque changement d’État est donc :


```
4000 / 2  = 2000 cycles for each state change
```



Par conséquent, le nombre moyen de cycles pour activer ou désactiver les tests z est de 2000 cycles. Il est intéressant de noter que QueryPerformanceCounter mesure la demi-heure et le z-désactivent la moitié du temps. Cette technique mesure en fait la moyenne des deux modifications d’État. En d’autres termes, vous mesurez le temps de basculement d’un État. À l’aide de cette technique, vous n’avez aucun moyen de savoir si les heures d’activation et de désactivation sont équivalentes, car vous avez mesuré la moyenne des deux. Toutefois, il s’agit d’un nombre raisonnable à utiliser lors du budget d’un état de basculement en tant qu’application qui provoque cette modification d’état uniquement en basculant cet État.

Maintenant, vous pouvez appliquer ces techniques et Profiler toutes les modifications d’État que vous souhaitez, n’est-ce pas ? Pas tout à fait. Vous devez toujours faire attention aux optimisations conçues pour réduire la quantité de travail qui doit être effectuée. Il existe deux types d’optimisations que vous devez connaître lors de la conception de vos séquences de rendu.

### <a name="watch-out-for-state-change-optimizations"></a>Méfiez-vous des optimisations de changement d’État

La section précédente montre comment profiler les deux types de modifications d’État : un changement d’état simple qui est restreint pour générer la même quantité de travail pour chaque itération et une modification de l’état de basculement qui modifie radicalement la quantité de travail effectuée. Que se passe-t-il si vous prenez la séquence de rendu précédente et y ajoutez un autre changement d’État ? Par exemple, cet exemple prend la séquence de rendu z>-Enable et y ajoute une comparaison z-Func :


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



L’État z-Func définit le niveau de comparaison lors de l’écriture dans la mémoire tampon z (entre la valeur z d’un pixel actuel et la valeur z d’un pixel dans le tampon de profondeur). D3DCMP \_ ne désactive jamais la comparaison z-test, tandis que D3DCMP \_ définit toujours la comparaison à chaque fois que le test z est effectué.

Le profilage de l’un de ces changements d’État dans une séquence de rendu avec [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) génère des résultats similaires à ceux-ci :



| Changement d’État unique | Nombre moyen de cycles |
|---------------------|--------------------------|
| D3DRS \_ ZENABLE uniquement | 2000                     |



 

ou



| Changement d’État unique | Nombre moyen de cycles |
|---------------------|--------------------------|
| D3DRS \_ ZFUNC uniquement   | 600                      |



 

Toutefois, si vous profilez \_ à la fois D3DRS ZENABLE et D3DRS \_ ZFUNC dans la même séquence de rendu, vous pouvez voir des résultats comme ceux-ci :



| Les deux modifications d’État            | Nombre moyen de cycles |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

Vous pouvez vous attendre à ce que le résultat soit la somme des cycles 2000 et 600 (ou 2600), car le pilote effectue tout le travail associé à la définition des deux États de rendu. Au lieu de cela, la moyenne est de 2000 cycles.

Ce résultat reflète une optimisation de changement d’État implémentée dans le runtime, le pilote ou le GPU. Dans ce cas, le pilote peut voir le premier [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et définir un état de modification qui différerait le travail jusqu’à la version ultérieure. Lorsque le pilote voit le deuxième **SetRenderState**, le même état modifié peut être défini de manière redondante et le même travail est reporté une nouvelle fois. Quand [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) est appelé, le travail associé à l’état modifié est enfin traité. Le pilote exécute le travail une fois, ce qui signifie que les deux premières modifications d’État sont effectivement consolidées par le pilote. De même, le troisième et le quatrième État sont consolidés de manière efficace par le pilote en un seul changement d’État lorsque le second **DrawPrimitive** est appelé. Le résultat net est que le pilote et le GPU traitent une seule modification d’État pour chaque appel de dessin.

Il s’agit d’un bon exemple d’optimisation du pilote dépendant de la séquence. Le pilote a différé le travail à deux reprises en définissant un état modifié, puis il a effectué le travail une fois pour effacer l’état modifié. Il s’agit d’un bon exemple du type d’amélioration de l’efficacité qui peut se produire lorsque le travail est différé jusqu’à ce qu’il soit absolument nécessaire.

Comment savoir quels sont les changements d’État qui définissent un état de modification en interne et, par conséquent, retarder le travail jusqu’à la date ultérieure ? Uniquement en testant les séquences de rendu (ou en parlant aux Writers de pilote). Les pilotes sont mis à jour et améliorés régulièrement pour que la liste des optimisations ne soit pas statique. Il n’existe qu’une seule façon de savoir exactement ce qu’est un changement d’état des coûts dans une séquence de rendu donnée, sur un ensemble de matériel spécifique. et c’est pour cela qu’il faut le mesurer.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Méfiez-vous des optimisations de DrawPrimitive

En plus des optimisations de modification d’État, le runtime tente d’optimiser le nombre d’appels de dessin que le pilote doit traiter. Par exemple, considérez les appels de retour vers l’arrière-plan :


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Exemple 5A : deux appels de dessin

Cette séquence contient deux appels de dessin, que le runtime consolidera en un seul appel équivalent à :


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Exemple 5B : un appel de dessin concaténé unique

Le runtime concatène ces deux appels de dessin particuliers en un seul appel, ce qui réduit le travail du pilote de 50%, car le pilote n’a à présent qu’à traiter un appel de dessin.

En général, le runtime concatène deux ou plusieurs appels [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de secours dans les cas suivants :

1.  Le type primitif est une liste de triangles (D3DPT \_ TRIANGLELIST).
2.  Chaque appel [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) successif doit faire référence à des vertex consécutifs dans la mémoire tampon de vertex.

De même, les conditions appropriées pour la concaténation de deux ou plusieurs appels [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) de secours sont les suivantes :

1.  Le type primitif est une liste de triangles (D3DPT \_ TRIANGLELIST).
2.  Chaque appel [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successif doit faire référence à des index consécutifs dans la mémoire tampon d’index.
3.  Chaque appel [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successif doit utiliser la même valeur pour BaseVertexIndex.

Pour empêcher la concaténation pendant le profilage, modifiez la séquence de rendu afin que le type primitif ne soit pas une liste de triangles, ou modifiez la séquence de rendu afin qu’il n’y ait pas d’appels de dessin arrière à dos utilisant des vertex (ou des index) consécutifs. Plus précisément, le runtime concatène également les appels de dessin qui remplissent les deux conditions suivantes :

-   Lorsque l’appel précédent est [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), si l’appel de dessin suivant :
    -   utilise une liste de triangles, et
    -   Spécifie le StartVertex = précédent StartVertex + PrimitiveCount précédent \* 3
-   Lors de l’utilisation de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), si l’appel de dessin suivant est utilisé :
    -   utilise une liste de triangles, et
    -   spécifie StartIndex = précédent StartIndex + PrimitiveCount précédent \* 3, et
    -   Spécifie le BaseVertexIndex = précédent BaseVertexIndex

Voici un exemple plus subtil de dessin de la concaténation d’appel qui est facile à ignorer lorsque vous profilez. Supposons que la séquence de rendu ressemble à ceci :


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Exemple 5C : un changement d’État et un appel de dessin

La boucle itère jusqu’à 1500 triangles, en définissant une texture et en dessinant chaque triangle. Cette boucle de rendu prend environ 2750 cycles pour [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) et 1100 cycles pour [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , comme indiqué dans les sections précédentes. Vous vous attendez peut-être à ce que le déplacement de **SetTexture** en dehors de la boucle de rendu réduise la quantité de travail effectuée par le pilote de 1500 \* 2750 cycles, ce qui correspond à la quantité de travail associée à l’appel de **SetTexture** 1500 fois. L’extrait de code ressemble à ceci :


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Exemple 5D : exemple 5c avec le changement d’État en dehors de la boucle

Le déplacement de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) en dehors de la boucle de rendu réduit la quantité de travail associée à **SetTexture** , car elle est appelée une fois au lieu de 1500 fois. Un effet secondaire moins évident est que le travail pour [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) est également réduit de 1500 appels à 1 appel, car toutes les conditions de concaténation des appels de dessin sont satisfaites. Lorsque la séquence de rendu est traitée, le runtime traite les appels 1500 dans un appel de pilote unique. En déplaçant cette ligne de code, la quantité de travail de pilote a été considérablement réduite :


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Ces résultats sont entièrement corrects, mais sont très trompeurs dans le contexte de la question d’origine. L’optimisation de l’appel de dessin a entraîné une réduction considérable de la quantité de travail du pilote. Il s’agit d’un problème courant lors de la création d’un profilage personnalisé. Lors de l’élimination des appels d’une séquence de rendu, veillez à éviter la concaténation des appels de dessin. En fait, ce scénario est un exemple puissant de la quantité d’amélioration des performances du pilote possible grâce à cette optimisation du Runtime.

Vous savez maintenant comment mesurer les changements d’État. Commencez par Profiler [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Ajoutez ensuite chaque modification d’État supplémentaire à la séquence (dans certains cas, en ajoutant un appel et, dans d’autres cas, en ajoutant deux appels) et mesurez la différence entre les deux séquences. Vous pouvez convertir les résultats en cycles ou en cycles ou en temps. Tout comme la mesure des séquences de rendu avec QueryPerformanceCounter, la mesure des modifications d’État individuel s’appuie sur le mécanisme de requête pour contrôler la mémoire tampon de commande et sur la modification de l’État dans une boucle pour réduire l’impact des transitions de mode. Cette technique mesure le coût du basculement d’un État, puisque le profileur retourne la moyenne d’activation et de désactivation de l’État.

Avec cette fonctionnalité, vous pouvez commencer à générer des séquences de rendu arbitraires et mesurer précisément le travail du runtime et du pilote associé. Les numéros peuvent ensuite être utilisés pour répondre à des questions de budgétisation, telles que le « nombre de ces appels », peuvent être effectuées dans la séquence de rendu tout en maintenant une fréquence d’images raisonnable, en supposant des scénarios limités par le processeur.

## <a name="summary"></a>Résumé

Cet article montre comment contrôler le tampon de commande afin que les appels individuels puissent être profilés avec précision. Les nombres de profilage peuvent être générés en graduations, en cycles ou en temps absolu. Ils représentent la quantité de travail d’exécution et de pilote associée à chaque appel d’API.

Commencez par profiler un \* appel de la primitive de dessin dans une séquence de rendu. Veillez à effectuer les opérations suivantes :

1.  Utilisez QueryPerformanceCounter pour mesurer le nombre de graduations par appel d’API. Utilisez QueryPerformanceFrequency pour convertir les résultats en cycles ou en temps si vous le souhaitez.
2.  Utilisez le mécanisme de requête pour vider la mémoire tampon de commande avant de commencer.
3.  Incluez la séquence de rendu dans une boucle pour réduire l’impact de la transition du mode.
4.  Utilisez le mécanisme de requête pour mesurer le moment où le GPU a terminé son travail.
5.  Méfiez-vous de la concaténation du runtime qui aura un impact majeur sur la quantité de travail effectuée.

Vous bénéficiez ainsi d’une performance de base pour [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) qui peut être utilisée pour générer à partir de. Pour profiler un changement d’État, suivez ces conseils supplémentaires :

1.  Ajoutez la modification d’État à un profil de séquence de rendu connu la nouvelle séquence. Étant donné que le test est effectué dans une boucle, vous devez définir l’État à deux reprises comme valeurs opposées (par exemple, activer et désactiver par exemple).
2.  Comparez la différence entre les temps de cycle entre les deux séquences.
3.  Pour les changements d’État qui modifient de manière significative le pipeline (par exemple, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), soustraire la différence entre les deux séquences pour obtenir le temps nécessaire au changement d’État.
4.  Pour les changements d’État qui modifient de manière significative le pipeline (et, par conséquent, nécessitent des États de basculement tels que [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), soustraire la différence entre les séquences de rendu et la division par 2. Le nombre moyen de cycles pour chaque changement d’État est alors généré.

Mais méfiez-vous des optimisations qui provoquent des résultats inattendus lors du profilage. Les optimisations de changement d’État peuvent définir des États de modification qui entraînent le report du travail. Cela peut entraîner des résultats de profil qui ne sont pas aussi intuitifs que prévu. Les appels de dessin qui sont concaténés réduisent considérablement le travail du pilote, ce qui peut entraîner des conclusions trompeuses. Les séquences de rendu soigneusement planifiées sont utilisées pour empêcher la modification de l’État et les concaténations des appels de dessin. L’astuce consiste à empêcher les optimisations de se produire au cours du profilage afin que les nombres que vous génériez soient des chiffres de budgétisation raisonnables.

> [!Note]  
> La duplication de cette stratégie de profilage dans une application sans le mécanisme de requête est plus difficile. Avant Direct3D 9, le seul moyen prévisible de vider le tampon de commande consiste à verrouiller une surface active (telle qu’une cible de rendu) pour attendre que le GPU soit inactif. Cela est dû au fait que le verrouillage d’une surface force le runtime à vider le tampon de commande au cas où il y aurait des commandes de rendu dans la mémoire tampon qui doivent mettre à jour la surface avant qu’elle ne soit verrouillée, en plus d’attendre la fin du GPU. Cette technique est fonctionnelle, bien qu’il soit plus discret que d’utiliser le mécanisme de requête introduit dans Direct3D 9.

 

## <a name="appendix"></a>Annexe

Les nombres de ce tableau sont une plage de approximations pour la quantité de travail de Runtime et de pilote associée à chacun de ces changements d’État. Les approximations sont basées sur les mesures réelles effectuées sur les pilotes à l’aide des techniques présentées dans le document. Ces nombres ont été générés à l’aide du runtime Direct3D 9 et dépendent du pilote.

Les techniques décrites dans ce document sont conçues pour mesurer le travail du runtime et du pilote. En général, il est peu pratique de fournir des résultats qui correspondent aux performances du processeur et du GPU dans chaque application, car cela nécessiterait un tableau exhaustif de séquences de rendu. En outre, il est particulièrement difficile de tester les performances du GPU, car il dépend fortement de la configuration de l’État dans le pipeline avant la séquence de rendu. Par exemple, l’activation de la fusion alpha n’a que peu d’incidence sur la quantité de travail du processeur nécessaire, mais peut avoir un impact important sur la quantité de travail effectuée par le GPU. Par conséquent, les techniques décrites dans ce document limitent le travail du GPU au minimum possible en limitant la quantité de données qui doivent être rendues. Cela signifie que les nombres de la table correspondent plus précisément aux résultats obtenus à partir d’applications qui sont limitées par l’UC (par opposition à une application limitée par le GPU).

Il est recommandé d’utiliser les techniques présentées pour couvrir les scénarios et les configurations les plus importants pour vous. Les valeurs de la table peuvent être utilisées pour effectuer une comparaison avec les nombres que vous générez. Étant donné que chaque pilote varie, le seul moyen de générer les chiffres réels est de générer des résultats de profilage à l’aide de vos scénarios.



| Appel d’API                             | Nombre moyen de cycles |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500-11250             |
| SetFVF                               | 6400-11200             |
| SetVertexShader                      | 3000-12100             |
| SetPixelShader                       | 6300-7000              |
| SPECULARENABLE                       | 1900-11200             |
| SetRenderTarget                      | 6000-6250              |
| SetPixelShaderConstant (1 constante)  | 1500-9000              |
| NORMALIZENORMALS                     | 2200-8100              |
| Éclaircie                          | 1300-9000              |
| SetStreamSource                      | 3700-5800              |
| Unit                             | 1700-7500              |
| DIFFUSEMATERIALSOURCE                | 900-8300               |
| AMBIENTMATERIALSOURCE                | 900-8200               |
| COLORVERTEX                          | 800-7800               |
| SetLight                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| SetIndices                           | 900-5600               |
| AMBIANT                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SPECULARMATERIALSOURCE               | 900-4600               |
| EMISSIVEMATERIALSOURCE               | 900-4500               |
| SetMaterial                          | 1000-3700              |
| ZENABLE                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MINFILTER                            | 1700-2500              |
| MAGFILTER                            | 1700-2400              |
| SetVertexShaderConstant (1 constante) | 1000-2700              |
| COLOROP                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| CULLMODE                             | 500-2570               |
| PORTION                             | 500-2550               |
| DrawIndexedPrimitive                 | 1200-1400              |
| ADDRESSV                             | 1090-1500              |
| ADRESSE                             | 1070-1500              |
| DrawPrimitive                        | 1050-1150              |
| SRGBTEXTURE                          | 150-1500               |
| STENCILMASK                          | 570-700                |
| STENCILZFAIL                         | 500-800                |
| STENCILREF                           | 550-700                |
| ALPHABLENDENABLE                     | 550-700                |
| STENCILFUNC                          | 560-680                |
| STENCILWRITEMASK                     | 520-700                |
| STENCILFAIL                          | 500-750                |
| ZFUNC                                | 510-700                |
| ZWRITEENABLE                         | 520-680                |
| STENCILENABLE                        | 540-650                |
| STENCILPASS                          | 560-630                |
| SRCBLEND                             | 500-685                |
| \_StencilMODE deux côtés \_              | 450-590                |
| ALPHATESTENABLE                      | 470-525                |
| ALPHAREF                             | 460-530                |
| ALPHAFUNC                            | 450-540                |
| DESTBLEND                            | 475-510                |
| COLORWRITEENABLE                     | 465-515                |
| wrapper CCW \_ STENCILFAIL                     | 340-560                |
| wrapper CCW \_ STENCILPASS                     | 340-545                |
| wrapper CCW \_ STENCILZFAIL                    | 330-495                |
| SCISSORTESTENABLE                    | 375-440                |
| wrapper CCW \_ STENCILFUNC                     | 250-480                |
| SetScissorRect                       | 150-340                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 

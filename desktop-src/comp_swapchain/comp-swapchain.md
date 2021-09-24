---
title: Guide de programmation utilise permutation de la composition
description: L’API utilise permutation de la composition est un successeur sectaire du utilise permutation DXGI, qui permet aux applications d’afficher et de présenter du contenu à l’écran.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: cd87e1d47e3e44c922310937c0106348ebb4954f
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523835"
---
# <a name="composition-swapchain-programming-guide"></a>Guide de programmation utilise permutation de la composition

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

L’API utilise permutation de la composition est un successeur sectaire du utilise permutation DXGI, qui permet aux applications d’afficher et de présenter du contenu à l’écran. L’utilisation de cette API sur DXGI utilise permutation présente plusieurs avantages. Un contrôle plus précis est accordé à votre application en ce qui concerne l’état du utilise permutation, et une plus grande liberté est fournie lorsqu’il s’agit de la façon dont le utilise permutation est utilisé. En outre, l’API fournit une meilleure histoire pour un temps de présentation précis.

## <a name="what-is-presentation"></a>Qu’est-ce que la présentation ?

La *Présentation* est le concept d’affichage des résultats des opérations de dessin à l’écran. Un *présent* est une instance unique de la présentation d' &mdash; une demande d’affichage des résultats d’une opération de dessin sur une seule mémoire tampon, à l’écran. Un présent peut contenir des attributs supplémentaires qui décrivent comment s’afficher à l’écran. Dans cette API, un présent peut également avoir une *heure cible*, qui est un horodateur relatif au système (une interruption) qui décrit l’heure idéale à laquelle le présent doit être affiché. Votre application peut l’utiliser pour contrôler plus précisément la vitesse à laquelle le contenu s’affiche à l’écran, et synchroniser les cadeaux avec d’autres événements du système, tels qu’une piste audio.

La synchronisation est au cœur de la présentation. Autrement dit, les opérations de dessin sont généralement effectuées par un GPU, par opposition à l’UC et, par conséquent, elles s’exécutent sur une chronologie asynchrone à partir de celle du processeur qui a émis les opérations initialement. La présentation est une opération soumise au GPU qui garantit que les opérations de dessin qui ont été émises précédemment auront terminé avant l’affichage de la mémoire tampon à l’écran.

Votre application émet généralement un grand nombre de cadeaux dans le temps et a plusieurs textures à sélectionner lors de l’émission de cadeaux. Votre application doit utiliser les mécanismes de synchronisation fournis par cette API pour garantir qu’une fois que vous avez dessiné et présenté une mémoire tampon, vous ne faites pas de nouveau dessin à cette mémoire tampon tant que ce contenu n’a pas été affiché et remplacé par la suite par une nouvelle mémoire tampon à partir d’un présent présent. Dans le cas contraire, le contenu de la mémoire tampon que votre application signifiait présenter initialement peut être remplacé comme indiqué sur l’écran.

## <a name="presentation-modesmdashcomposition-multiplane-overlay-and-iflip"></a>Composition des modes &mdash; de présentation, superposition de superposition et iflip

Les mémoires tampons présentées par votre application peuvent être affichées par le système de différentes manières.

La méthode la plus simple, qui est la valeur par défaut, est que le présent sera envoyé à DWM et que le DWM affichera un frame basé sur la mémoire tampon présentée. Autrement dit, il existe une copie (ou plus précisément, un rendu 3D) de la mémoire tampon de présentation dans la mémoire tampon de mise en mémoire tampon que le DWM envoie à l’affichage. Cette méthode d’affichage d’un présent est appelée composition.

Un mode d’affichage plus performant consiste à analyser le tampon de présentation directement sur le matériel et à éliminer la copie qui a lieu. Cette méthode d’affichage d’un présent est appelée *scanout directe*. Lors du traitement des présentations, DWM peut décider de programmer le matériel pour effectuer une analyse directe d’une mémoire tampon de présentation, en affectant la mémoire tampon à un plan de *superposition* (ou plan MPO), ou en inversant directement le tampon sur le matériel ( *retournement direct*).

Une façon encore plus performante d’afficher un présent serait de faire en sorte que les cadeaux s’affichent directement par le noyau graphique et contourner le DWM entièrement. Cette méthode de présentation est appelée *retournement indépendant* (iflip). La superposition et les iflip Multiplans sont décrits dans [pour optimiser les performances, utilisez dxgi Flip Model](https://devblogs.microsoft.com/directx/dxgi-flip-model/).

La composition est la plus facile à être prise en charge, mais également la moins efficace. La surface doit être spécialement allouée pour être éligible pour le scanout direct ou iflip, et ce type d’allocation spéciale a des exigences système plus strictes que la composition utilise permutation. Elle est uniquement disponible sur le matériel WDDM 3,0 et supérieur. Par conséquent, votre application peut demander la prise en charge de l’API pour la présentation de la composition uniquement, ainsi qu’une présentation qui qualifie pour scanout ou iflip direct.

## <a name="presentation-factory-checking-capability-and-presentation-manager"></a>Présentation Factory, vérification des fonctionnalités et gestionnaire de présentation

Le premier objet que votre application va utiliser en dehors de l’API utilise permutation de la composition est la *fabrique de présentation*. La fabrique de présentation est créée par votre application et liée à un appareil Direct3D que votre application passe à l’appel de création, et, par conséquent, a une affinité avec la carte vidéo associée à cet appareil.

La fabrique de présentation expose des méthodes pour vérifier si le système actuel et le périphérique graphique peuvent utiliser l’API utilise permutation de composition. Vous pouvez utiliser des méthodes de fonctionnalité comme [**IPresentationFactory :: IsPresentationSupported**](/windows/win32/api/presentation/nf-presentation-ipresentationfactory-ispresentationsupported) pour vérifier la prise en charge du système. Si les méthodes de fonctionnalité indiquent la prise en charge du système pour l’API, vous pouvez utiliser la fabrique de présentation pour créer un *Gestionnaire de présentation*. Ce gestionnaire de présentation est l’objet que vous utilisez pour effectuer des fonctions de présentation et est lié aux mêmes appareil et carte vidéo Direct3D que cette fabrique de présentation qui a été utilisée pour le créer.

actuellement, la configuration système requise pour l’utilisation de l’API utilise permutation de composition est tout à la fois les pilotes GPU prenant en charge WDDM (Windows modèle de pilote de périphérique) 2,0. Pour utiliser l’API utilise permutation de la composition de la manière la plus performante (directe de scanout et de retournement indépendant, ou *iflip*), les systèmes ont besoin de pilotes GPU prenant en charge WDDM 3,0.

Si le système n’est pas en mesure d’utiliser l’API utilise permutation de composition, votre application doit avoir un codePath distinct pour gérer la présentation à l’aide de méthodes plus anciennes, telles qu’un utilise permutation DXGI.

## <a name="register-presentation-buffers-to-present"></a>Enregistrer les tampons de présentation à présenter

Le gestionnaire de présentation effectue le suivi des mémoires tampons qu’il peut présenter. Pour présenter une texture Direct3D, votre application doit d’abord créer cette texture avec Direct3D, puis l’inscrire auprès du gestionnaire de présentation. Lorsqu’une texture a été inscrite auprès du gestionnaire de présentation, elle est appelée *mémoire tampon de présentation* et peut à partir de ce point être présentée à l’écran par ce gestionnaire de présentation. Votre application peut ajouter et supprimer des tampons de présentation comme vous le souhaitez, bien qu’il existe un nombre maximal de mémoires tampons de présentation qui peuvent être ajoutées à un seul gestionnaire de présentation (actuellement 31). Ces mémoires tampons de présentation peuvent également être de tailles et de formats différents, qui prendront effet à la présentation d’une mémoire tampon de présentation individuelle.

Une texture peut être enregistrée avec un nombre quelconque de gestionnaires de présentation ; Toutefois, ce n’est pas considéré comme une utilisation normale dans la plupart des cas, et les scénarios de synchronisation compliqués s’imposent que votre application est responsable de la gestion.

## <a name="defining-the-content-to-be-presented"></a>Définition du contenu à présenter

En général, les mémoires tampons que nous présentons doivent être associées au contenu dans une arborescence d’éléments *visuels*. Par conséquent, nous devons définir une sorte de *liaison* . ainsi, lorsque votre application émet des problèmes, il est évident que dans l’arborescence d’éléments visuels, les mémoires tampons en cours de présentation sont censées se trouver. Nous appelons ce *contenu de présentation* de liaison.

Le contenu présenté peut prendre de nombreuses formes. Votre application peut souhaiter présenter une seule mémoire tampon à afficher, ou elle peut souhaiter présenter du contenu stéréo avec des tampons pour les yeux gauche et droit, et ainsi de suite. La version initiale de cette API prend en charge la présentation d’une seule mémoire tampon à l’écran.

Nous définissons une *surface de présentation* comme une forme de contenu de présentation dans laquelle une seule mémoire tampon est présentée à la fois. Une surface de présentation peut être définie en tant que contenu dans une arborescence d’éléments visuels et peut afficher une seule mémoire tampon de présentation à la fois à l’écran. Le gestionnaire de présentation met à jour la mémoire tampon affichée par une ou plusieurs surfaces de présentation de manière atomique.

Le gestionnaire de présentation peut être utilisé pour créer une ou plusieurs surfaces de présentation pour une *poignée de surface de composition* donnée. chaque descripteur de surface de composition peut être lié à un ou plusieurs visuels dans une arborescence d’éléments visuels (par le biais de stratégies décrites dans [**Windows. UI. composition**](/uwp/api/windows.ui.composition) et la documentation de l’API [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal) ) pour définir la relation entre la surface de présentation associée et l’emplacement où elle apparaît dans son arborescence d’éléments visuels. Votre application peut mettre à jour une ou plusieurs surfaces de présentation, qui sont envoyées au système et qui ont lieu lors de l’opération suivante.

Notez que le gestionnaire de présentation peut présenter n’importe quelle mémoire tampon de présentation à n’importe quel nombre de surfaces de présentation qu’il souhaite. Il n’existe aucune restriction. Toutefois, il revient à votre application d’effectuer le suivi des mémoires tampons que vous avez émises et de leur emplacement, afin de vous assurer que vous n’essayez pas d’émettre un nouveau dessin dans cette mémoire tampon alors qu’elle est toujours affichée par une surface de présentation.

## <a name="applying-properties-to-presentation-surface"></a>Application de propriétés à la surface de présentation

En plus de spécifier les mémoires tampons à afficher dans une surface de présentation, un présent peut également spécifier d’autres propriétés pour cette aire de présentation. Celles-ci incluent des propriétés qui définissent la manière dont la texture source est échantillonnée, y compris le mode Alpha et l’espace colorimétrique, la façon dont la texture source est transformée et disposée, ainsi que les restrictions affichées ou readback pour le contenu protégé. Toutes ces méthodes sont exposées en tant que méthodes d’accesseur Set de propriété sur une surface de présentation qui peut être modifiée par votre application et, tout comme les mises à jour de mémoire tampon, prend effet lorsque le présent de votre application a lieu.

## <a name="presenting-to-the-presenting-surface"></a>Présenter à la surface de présentation

Une fois que votre application a créé des surfaces de présentation, inscrit des tampons de présentation et spécifie des mises à jour à délivrer pendant un présent, vous pouvez appliquer ces propriétés en présentant. Votre application émet un présent par le biais du gestionnaire de présentation. Lorsque cette présentation est traitée par le système, toutes les mises à jour sont appliquées de manière atomique. En outre, votre application peut également spécifier d’autres propriétés du présent, telles que la durée idéale (le temps de l’heure *cible* ) et d’autres propriétés plus rares, telles que la vitesse de contenu prévue, qui peut être utilisée pour activer les modes d’actualisation personnalisés sur le système. Étant donné que les cadeaux peuvent être planifiés à un moment donné, votre application peut émettre plusieurs cadeaux à l’avance. Ces cadeaux sont traités un par un, car leur heure planifiée est atteinte. 

## <a name="synchronizing-presentation"></a>Synchronisation de la présentation

Votre application doit s’assurer qu’au moment de son affichage dans les mémoires tampons, et que les problèmes se présentent, elle sélectionne une mémoire tampon à afficher, qui n’est actuellement référencée par aucun autre présent précédent en suspens, ce qui peut entraîner le remplacement du contenu de la mémoire tampon prévu. En outre, si votre application émet un rendu sur une mémoire tampon actuellement affichée par une surface de présentation dans le matériel scanout, son rendu peut être bloqué indéfiniment, car Direct3D n’autorise pas le rendu de la *mémoire tampon d’avant*.

L’API utilise permutation de composition fournit quelques mécanismes différents pour permettre à votre application d’exercer une synchronisation correcte des mémoires tampons qu’elle a présentées.

Une mémoire tampon est considérée comme *disponible* s’il n’y a pas de présentation en suspens qui la référencent et qu’elle n’est pas actuellement affichée par le système. Dans le cas contraire, il n’est pas disponible. L’API fournit un événement pour chaque mémoire tampon de présentation qui indique si la mémoire tampon est disponible ou non. Il s’agit de la méthode de synchronisation la plus simple à utiliser pour votre application. Avant de dessiner dans une mémoire tampon et de la présenter, votre application peut s’assurer que son événement *disponible* est signalé. L’événement disponible pour une mémoire tampon particulière devient *non* signalé au moment où il a été lié à une surface de présentation dans l’API et reste insignalé jusqu’à ce que le présent soit mis hors service.

Deuxièmement, le gestionnaire de présentation effectue le suivi d’une limite de mise hors service *présente* pour communiquer avec votre application, qui s’affichent. La valeur de la clôture correspond à l’identificateur actuel du dernier présent qui a commencé *la phase de* mise hors service de son cycle de vie, comme indiqué dans la section du cycle de *vie* ci-dessous. Une fois qu’un présent s’est passé dans cette phase, il est possible de supposer que toutes les mémoires tampons qui ont été remplacées par des présentation ultérieures peuvent être réutilisées.

Cette méthode de synchronisation est plus avancée, mais permet un meilleur contrôle de la limitation du flux de travail, et est plus instructif quant à l’état du système en ce qui concerne la profondeur de la file d’attente actuelle actuelle. Pour obtenir une vue d’ensemble du cycle de vie d’un présent, consultez la section ci-dessous.

## <a name="lifecycle-of-a-present"></a>Cycle de vie d’un présent

Les présentation du gestionnaire de présentation sont mises en file d’attente dans le système dans le cadre de sa *file d’attente actuelle*. Les processus système sont présentés dans l’ordre de mise en file d’attente. En outre, chaque présent est associé à un *identificateur présent* associé unique (au gestionnaire de présentation), qui est une valeur d’incrémentation assignée à un présent, commençant à 1 pour le premier présent, et incrémentant de 1 pour chaque présent présent. Cet identificateur présent est utilisé dans différentes parties de l’API, telles que les primitives de synchronisation et les statistiques de présentation, pour faire référence à cette présence particulière.

Chaque fois que vos problèmes d’application suivent un cycle de vie spécifique, comme décrit ici.

Une fois que votre application a configuré les modifications à effectuer dans le cadre d’un présent, elle utilise le gestionnaire de présentation pour émettre le présent. À ce stade, on dit que le présent est *en attente*.

Une fois en attente, un présent sera placé dans la file d’attente présente du gestionnaire de présentation, où il sera conservé jusqu’à ce que l’un des deux événements se produise.

* Le présent est *annulé*. Le gestionnaire de présentation permet à votre application d’annuler des présentations émises précédemment. Dans ce cas, le présent est dit comme étant *annulé*, puis il est immédiatement mis *hors* service. Sur cette transition, les événements *disponibles* de la mémoire tampon associée pour le présent annulé seront mis à jour, mais la clôture de la période de mise hors service ne sera pas signalée, car le présent présent présent (avant les produits qui ont été annulés) restera affiché. Pour cette raison, votre application ne peut pas utiliser la clôture de mise hors service actuelle pour déterminer les cadeaux qui ont été annulés. Vous devez à la place en savoir plus sur les statistiques d’état actuelles qui sont renvoyées pour chaque annulation présente. Nous suggérons que votre application utilise des événements *disponibles* dans la mémoire tampon pour trouver une mémoire tampon disponible à présenter après une annulation. Une fois ce contenu affiché, le précédent présentera le processus de mise hors service et mettra à jour la clôture de mise hors service actuelle.
* S’il n’est pas annulé, le présent sera finalement *prêt* à être traité. Pour être prêt, deux conditions majeures doivent être remplies.
  * Tous les travaux de dessin émis dans le contexte Direct3D avant l’appel de la présente doivent être terminés. Cela permet de s’assurer que la mémoire tampon n’est pas affichée avant que le dessin de votre application ne soit terminé.
  * Si une heure de la cible actuelle a été spécifiée, alors l’heure relative au système actuelle qui devrait être en mesure d’afficher le présent correspond à l’heure cible demandée que votre application a appliquée au présent.

Lorsque le système décide de trouver un présent à afficher à l’écran, il choisit le dernier présent qui est *prêt* à être présent pour s’afficher. S’il existe plusieurs présentation *prêtes* , toutes les versions sauf la plus récente (autrement dit, la présente avec l’identificateur le plus élevé) seront *ignorées*, et passer immédiatement à l’État retiré, à partir duquel les événements de tampon *disponibles* seront signalés, mais la clôture de mise *hors* service actuelle ne sera pas signalée, car la ignore présente l’état *affiché* .

Lorsque l’affichage *prêt* est choisi, le système commence à faire le travail pour l’afficher à l’écran. Cela peut signifier le rendu de la mémoire tampon dans le cadre d’une trame DWM, puis la demande du matériel afficher ce frame à l’écran, ou l’envoi direct du tampon au matériel scanout dans le cas de iflip. Une fois cette opération effectuée, on dit que le présent est *mis en file d’attente*. À un niveau élevé, cela signifie qu’il est en train de s’afficher.

Lorsque le matériel est utilisé pour afficher le présent, il s’agit d’un *affichage*. À partir de là, il reste visible à l’écran jusqu’à ce qu’une figure suivante s’affiche et le remplace.

Quand un présent présent sera mis en file d’attente, nous savons que le matériel finit par cesser d’afficher le présent. À ce stade *, on dit* que le présent est en cours de mise hors service.

Quand ce présent présent sera affiché, alors le présent présent sera dit être mis *hors* service.

Le gestionnaire de présentation expose une *clôture* de mise hors service présente, qui est signalée à l’identificateur actuel de chaque présent lorsqu’il passe à *l’état de* mise hors service. Ce signal indique à votre application qu’elle est devenue sécurisée pour émettre un travail de rendu dans les mémoires tampons associées à cette présente sans altérer un présent précédent. Si votre application émet un travail de rendu pendant l' *État de mise* hors service du présent, le travail de rendu sera mis en file d’attente jusqu’à ce que le présent passe à l’état *retiré* , à partir duquel il sera exécuté. Si le travail de rendu est émis après que le présent a été mis *hors* service, il est exécuté immédiatement.

Voici un diagramme de ce changement d’État.

![Cycle de vie d’un présent](images/lifecycle-of-a-present.png)

## <a name="diagram-of-buffers-surfaces-and-presents"></a>Diagramme de mémoires tampons, de surfaces et de cadeaux

Voici un diagramme qui concerne le gestionnaire de présentation, les mémoires tampons de présentation, les surfaces de présentation, les présentations et les mises à jour.

![Diagramme de mémoires tampons, de surfaces et de cadeaux](images/buffers-surfaces-and-presents.png)

Ce diagramme illustre un gestionnaire de présentation, avec deux surfaces de présentation et trois mémoires tampons de présentation, avec deux émissions émises jusqu’à présent &mdash; dans la première mémoire tampon affichée 1 de la surface 1 et dans la mémoire tampon 2 de la surface 2. La deuxième surface mise à jour présente la surface 2 pour afficher la mémoire tampon de présentation 3 et n’a pas modifié la liaison de la surface 1. Une fois le présent 2 affiché, surface 1 affiche la mémoire tampon 1, et surface 2 affiche la mémoire tampon 3, qui peut être affichée dans l’état actuel des objets dans le gestionnaire de présentation. Chaque présent dans la file d’attente prend effet lors de son traitement dans le système.

> [!NOTE]
> Étant donné que le présent 2 n’a pas modifié la mémoire tampon pour surface 1, surface 1 était liée à la mémoire tampon 1 à partir du présent présent. Dans ce sens, il existe une référence « implicite » sur la mémoire tampon 1 dans le présent 2, car la surface 1 reste liée à la mémoire tampon 1 après l’affichage de la valeur 2.

## <a name="adding-presentation-surfaces-to-visual-tree"></a>Ajout de surfaces de présentation à l’arborescence d’éléments visuels

Les surfaces de présentation sont du contenu qui existe dans une arborescence d’éléments visuels de composition. Chaque surface de présentation est liée à une *poignée de surface de composition*. dans Windows. UI. Composition, un pinceau surface peut être créé pour un handle de surface de Composition préexistant et lié à un visuel sprite. Dans DirectComposition, une surface de composition peut être créée à partir d’une poignée de surface de composition préexistante et liée en tant que contenu à un visuel. Pour plus d’informations, consultez la documentation correspondante pour chaque API.

les api telles que Windows Media Foundation, conçues pour utiliser cette API, exposent les descripteurs de surface de composition qui seront pré-liés à une surface de présentation. Une application peut également créer sa propre poignée de surface de composition pour la lier par la suite à une surface de présentation et l’ajouter à une arborescence d’éléments visuels en appelant [DCompositionCreateSurfaceHandle](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle).

## <a name="reading-presentation-statistics"></a>Lecture des statistiques de présentation

L’API utilise permutation de la composition expose les *statistiques de présentation*, qui décrit diverses informations sur la façon dont un présent particulier a été traité. Les informations peuvent généralement décrire le mode d’utilisation d’une surface de présentation dans un frame DWM, le point dans le temps à partir duquel elle s’est affichée, si elle a été affichée, et ainsi de suite.

Il existe différents types de statistiques de présentation et ils sont conçus pour être développés dans les futures versions de l’API. Une application utilise le gestionnaire de présentation pour s’inscrire afin de recevoir les types de statistiques qui l’intéressent. Ces statistiques sont ensuite transmises à la *file d’attente des statistiques* du gestionnaire de présentation. Le gestionnaire de présentation expose un *événement Statistics available* aux applications, qui est un handle d’événement qui indique quand la file d’attente des statistiques a des éléments de statistiques disponibles pour la lecture. Dans ce cas, votre application peut défiler le premier élément de statistiques en dehors de la file d’attente, la lire et la traiter. Le gestionnaire de présentation réinitialise l’événement Statistics available lorsque votre application a lu toutes les statistiques qui se trouvent actuellement dans la file d’attente. Une application lit et traite généralement les statistiques dans une boucle jusqu’à ce que l’événement statistiques disponibles soit réinitialisé. Il est courant que votre application traite cette file d’attente de statistiques dans la même boucle de travail que celle utilisée pour émettre des cadeaux. Le modèle d’utilisation suggéré consiste à hiérarchiser les statistiques de traitement sur l’émission de nouvelles présentation, afin de garantir que la file d’attente ne déborde pas.

La file d’attente comporte un nombre maximal de statistiques qu’elle doit suivre, qui sera de l’ordre de 512-1024 statistiques. La profondeur maximale de file d’attente doit être suffisante pour stocker environ 5 secondes de statistiques dans des cas normaux. Si la file d’attente des statistiques est pleine et que davantage de statistiques sont signalées, la stratégie est que les statistiques les plus anciennes seront mises hors service pour faire de la place.

## <a name="related-topics"></a>Rubriques connexes

* [Utilise permutation de la composition](comp-swapchain-portal.md)
* [Pour des performances optimales, utilisez DXGI Flip Model](https://devblogs.microsoft.com/directx/dxgi-flip-model/)

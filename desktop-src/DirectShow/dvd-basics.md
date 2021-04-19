---
description: Notions de base sur les DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Notions de base sur les DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d0b2af8bc16fa0890c0103a063e750364cece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513896"
---
# <a name="dvd-basics"></a>Notions de base sur les DVD

Les fonctionnalités qui rendent les DVD attrayants pour les consommateurs (création de branche transparente, plusieurs langues, contrôle parental, prise en charge du karaoké et angles multiples) rendent également le travail du développeur un peu plus complexe. Un lecteur de DVD doit non seulement lire des flux audio, vidéo et sous-images, mais également effectuer le suivi des options de navigation que le disque autorise actuellement et gérer correctement de nombreux types de commandes utilisateur. Le navigateur DVD vous protège de la majeure partie de cette complexité tout en vous permettant de créer une application de DVD entièrement fonctionnelle. Vous n’avez pas besoin de vous référer à la spécification du DVD pour utiliser efficacement l’API du navigateur DVD, mais vous devez connaître les concepts de base de la navigation sur DVD.

**Données de contrôle de navigation**

Les données audio et vidéo sur un disque DVD-Video sont entrelacées à intervalles réguliers avec différents genres de données de contrôle de navigation. Ces données peuvent être une instruction qui indique au joueur de faire quelque chose, par exemple se déplacer vers un emplacement particulier sur le disque, ou il peut s’agir d’un marqueur d’information uniquement qui informe le joueur, par exemple que le contenu qui suit a un niveau de gestion parental supérieur au contenu précédent, ou que le chapitre ignorer l’opération est désactivé. Le lecteur relaie ces informations à une application, et il est de la responsabilité de l’application d’agir dessus. Ces marqueurs de navigation font partie de ce qui offre aux DVD son niveau d’interactivité d’utilisateur supérieur par rapport aux CD vidéo. Une application de lecteur de DVD doit gérer les événements qui proviennent du disque, ainsi que les événements qui proviennent de l’utilisateur.

**Données audio, vidéo et sous-image**

Un disque DVD-Video contient trois types principaux de flux : vidéo, audio et sous-image.

-   Le flux vidéo peut contenir jusqu’à neuf « angles », qui peuvent être considérés comme des sous-flux. Les auteurs de DVD peuvent inclure plusieurs angles partout où ils souhaitent offrir à la visionneuse un choix d’angles de caméra à partir desquels afficher la même scène. Un seul angle peut être actif à la fois. Le flux vidéo contient également des données de sous-titres de ligne 21, le cas échéant.
-   Il peut y avoir jusqu’à huit flux audio distincts, ou suivis, qui fournissent jusqu’à huit bandes-son multicanaux et permettent aux disques Karaoké DVD d’utiliser l’audio multicanal.
-   Un DVD peut contenir jusqu’à 32 flux de sous- *image* . Celles-ci se composent de bitmaps 16 couleurs compressées avec un canal alpha, qui sont superposés au-dessus de la vidéo. En règle générale, les flux de sous-image contiennent des sous-titres et des boutons de menu, même s’ils peuvent également contenir d’autres graphiques. Un flux de sous-image peut avoir une langue spécifiée. Le contenu de la sous-image est toujours affiché, et le contenu de la sous-image s’affiche uniquement si l’utilisateur l’active.

Notez que les légendes dans un flux de sous-image ne sont pas les mêmes que les sous-titres de ligne-21 fermés. Les sous-titres, qui sont destinés à des observateurs difficiles à entendre, sont incorporés dans le signal vidéo. Ils se composent entièrement de chaînes de caractères. Les légendes de sous-image, en revanche, sont des bitmaps graphiques. Sur un appareil grand public, les sous-titres sont affichés par l’ensemble de télévision, tandis que le flux de sous-image est rendu par le lecteur DVD. Un DVD peut contenir les deux types de légende.

**Titres et chapitres**

Le contenu vidéo d’un DVD est divisé en *titres* et *menus*. Les titres sont divisés en unités que la spécification de DVD appelle *des parties de titres* (PTTs). Plus souvent, il s’agit de *scènes* ou de *chapitres*. (La documentation DirectShow utilise le terme « chapitre ».) La visionneuse peut accéder à des titres ou chapitres spécifiques dans des titres.

L’auteur d’un DVD décide comment diviser le contenu en titres et chapitres. Lorsqu’un DVD contient un film de longueur de fonctionnalité, le film entier est souvent placé dans un titre, divisé en chapitres pour les scènes individuelles. Les fonctionnalités supplémentaires sur le DVD, telles que les codes de fin ou les scènes supprimées, sont placées dans des titres distincts. Toutefois, ces divisions sont arbitraires et de nombreux DVD sont organisés différemment.

Il peut y avoir jusqu’à 99 titres sur un disque et les auteurs de disques peuvent diviser le titre en autant de chapitres logiques que 999. Dans la plupart des films de fonctionnalités sur DVD, le contenu des films est mis en forme en tant que série de chapitres qui s’exécutent automatiquement l’un après l’autre. Sur ces disques, le marqueur de fin de chapitre contient une instruction de branchement qui indique au joueur de poursuivre la lecture du chapitre suivant de la séquence. Ces titres sont appelés des *titres de PGC séquentiels*. (PGC représente la chaîne de programme, un autre nom pour un groupe de chapitres qui appartiennent. Ce terme n’est pas utilisé dans la documentation du navigateur DVD.) Sur les disques avec d’autres types de contenu, tels que les disques de karaoké, un marqueur de fin de chapitre peut demander au lecteur d’afficher un menu, ou il peut simplement indiquer au joueur qu’il doit s’arrêter.

Les développeurs d’applications DVD utilisent des numéros de titres et de chapitres pour accéder à des points spécifiques sur un disque. Pour un accès plus fin, vous pouvez utiliser un numéro de titre et un code d’heure. Les codes de temps ne peuvent être utilisés qu’avec un seul titre de PGC séquentiels, car les autres types ne contiennent pas de cartes de code d’heure.

**Menus**

La spécification DVD définit six types de menu :

-   **Bonhomme.** Le menu titre est le premier menu à afficher. En général, il contient des boutons permettant de sélectionner des titres. Le menu du titre est également appelé *menu Gestionnaire vidéo*. Il n’y a qu’un seul menu de titre sur un DVD.
-   **Causes.** Un menu racine est le menu de niveau supérieur d’un titre. Chaque titre peut avoir un menu racine. Les quatre menus suivants sont des sous-menus du menu racine. Un menu racine est également appelé *menu jeu de titres vidéo*. Le menu racine contient généralement des boutons qui permettent d’accéder à l’un des titres de l’ensemble de titres. En outre, il peut avoir des sous-menus qui permettent à l’utilisateur de choisir des options pour le flux audio, l’angle de la caméra, le flux de sous-image ou le chapitre. Toutefois, ces sous-menus ne sont pas utilisés sur la plupart des DVD.
-   **Sous-titres.** Le menu sous-image sélectionne le flux de sous-image.
-   **HD.** Le menu audio sélectionne le flux audio. En général, ce menu permet à la visionneuse de sélectionner une piste de langue.
-   **Angle.** Le menu angle sélectionne l’angle de la caméra.
-   **Chapitre.** Le menu du chapitre, également appelé « menu PTT », sélectionne les chapitres d’un titre.

La plupart des menus ont des boutons, qui peuvent être *sélectionnés* et *activés*. La sélection d’un bouton modifie l’apparence du bouton. L’activation d’un bouton déclenche une commande de DVD, telle que l’émission d’un autre menu ou le démarrage de la lecture.

**Niveaux de gestion parental**

Tout ou partie d’un disque DVD peut être encodé avec un niveau de gestion parental (PML) numéroté de 1 à 8. Huit est le niveau le plus restrictif (adultes uniquement) et l’autre est le moins restrictif (tous âges). L’idée est d’empêcher les enfants de regarder du contenu pour adultes sans consentement parental, tout en permettant aux adultes d’observer du contenu enfant. Au États-Unis et au Canada, les niveaux correspondent au système d’évaluation de MPAA (G, PG, PG-13, NC-17), mais ce n’est pas le cas dans les autres pays ou régions.

Étant donné que les chapitres peuvent exister de manière logique dans un bloc parental, il peut y avoir deux versions du même chapitre dans un titre, chacune ayant un PML différent et dans un autre bloc parental. Par exemple, un enfant qui se connecte et lit le disque voit une version du chapitre 3 et un adulte qui se connecte voit une version différente, en supposant que l’application prend en charge PMLs.

Un titre ou un chapitre peut également contenir des PMLs temporaires, dont le contenu est évalué plus haut que le PML pour le titre ou le chapitre dans son ensemble. Cela signifie qu’un titre peut avoir plusieurs niveaux de contrôle parental. Les PMLs temporaires sont généralement créés en tant que blocs angulaires, de sorte qu’une scène dans un film peut avoir deux versions, une pour les plus jeunes et une pour les adultes.

L’application de lecteur est chargée d’appliquer les niveaux de contrôle parental.

**Domaines**

Le terme *domaine* fait référence à l’état interne d’un lecteur de DVD ; il ne s’agit pas d’un nom créé sur le disque. Les domaines sont importants, car certaines commandes de DVD ne sont valides que dans certains domaines. DirectShow offre un moyen d’interroger le domaine actuel et d’être averti lorsque le domaine change. Les domaines suivants sont définis :

-   **Première lecture.** Dans ce domaine, le lecteur DVD vient de démarrer la lecture du DVD. Après avoir entré le premier domaine Play, le lecteur passe à un autre domaine, soit un domaine de menu, soit le domaine title, en fonction du disque.
-   **Menu du gestionnaire vidéo.** Le lecteur présente le menu du gestionnaire vidéo, également appelé menu du titre.
-   **Menu STM.** Le lecteur présente un menu associé à un jeu de titres vidéo, soit le menu racine, soit un sous-menu (audio, sous-image, angle ou chapitre).
-   **Bonhomme.** Le joueur lit une vidéo dans un titre.
-   **Erreur.** Le lecteur n’affiche rien. (Strictement parlant, la spécification DVD n’appelle pas cet état de domaine, mais elle peut être traitée comme une seule.)

Le domaine peut être considéré comme une variable d’État qui est surveillée par un lecteur de DVD, afin d’assurer le suivi du type de contenu que le lecteur lit actuellement sur le disque. les lecteurs de DVD utilisent des domaines pour éviter d’émettre des commandes incompréhensibles sur le lecteur de DVD.

**Contrôles de l’opération de l’utilisateur**

Les contrôles d’opération de l’utilisateur (UOPs) sont des marqueurs sur un disque que les auteurs de DVD peuvent insérer partout pour limiter les options de navigation d’un utilisateur. La plupart des disques suivent des restrictions UOP standard. Par exemple, la plupart des disques ne permettent pas à la visionneuse d’avancer rapidement ou d’afficher un menu dans le premier domaine de lecture. En principe, chaque disque peut insérer une commande UOP à n’importe quel point du disque, même si la commande est valide dans le domaine actuel. Par exemple, un disque peut être créé pour interdire le transfert rapide dans un titre donné ou pour empêcher l’affichage d’un menu particulier une fois que l’utilisateur a entré le domaine du titre. Le navigateur DVD est conforme à toutes les commandes de ce disque et ne permet pas à une application de remplacer les contrôles UOP du disque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 




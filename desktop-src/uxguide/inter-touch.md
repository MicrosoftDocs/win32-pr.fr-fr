---
title: Toucher
description: toutes les applications Microsoft Windows doivent avoir une expérience tactile exceptionnelle. Et la création d’une telle expérience est plus facile que vous ne le pensez.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294491"
---
# <a name="touch"></a>Toucher

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

toutes les applications Microsoft Windows doivent avoir une expérience tactile exceptionnelle. Et la création d’une telle expérience est plus facile que vous ne le pensez.

Touch fait référence à l’utilisation d’un ou de plusieurs doigts pour fournir une entrée via un affichage de périphérique et interagir avec des Windows et des applications. Une application optimisée tactile dispose d’une interface utilisateur et d’un modèle d’interaction conçus pour prendre en charge les zones tactiles les plus grandes et les plus précises, les différents facteurs de forme des appareils tactiles et les nombreuses postures et poignées que les utilisateurs peuvent adopter lors de l’utilisation d’un appareil tactile.

![Utilisateur qui interagit avec Tablet PC à l’aide de Touch](images/inter_touch_image1.jpeg)

Chaque appareil d’entrée a ses atouts. Le clavier est le mieux adapté à la saisie de texte et donne des commandes avec un déplacement minimal. La souris est idéale pour un pointage efficace et précis. Touch est idéal pour la manipulation d’objets et pour donner des commandes simples. Un stylet est idéal pour une expression de forme libre, comme avec l’écriture manuscrite et le dessin.

Windows 8.1 est optimisé pour la réactivité, la précision et la facilité d’utilisation avec touch, tout en prenant en charge des méthodes d’entrée traditionnelles (telles que la souris, le stylet et le clavier). La vitesse, la précision et les commentaires tactiles fournis par les modes de saisie traditionnels sont familiers et attrayants pour de nombreux utilisateurs et peuvent être mieux adaptés à des scénarios d’interaction spécifiques.

Vous trouverez des instructions relatives à la souris, au stylet et à l’accessibilité dans des rubriques distinctes.

Lorsque vous réfléchissez à l’expérience d’interaction pour votre application :

Ne partez pas du principe que si une interface utilisateur fonctionne bien pour une souris, elle fonctionne également bien pour les fonctions tactiles. Bien que la prise en charge de la souris soit un bon point de départ, une bonne expérience tactile a quelques exigences supplémentaires.

Supposons que si une interface utilisateur fonctionne bien pour un doigt, elle fonctionne également bien pour un stylet. Faire de votre application touchable vous permet également de fournir une bonne prise en charge du stylet. La principale différence réside dans le fait que les doigts ont un Tip plus pointu, donc ils ont besoin de plus grandes cibles.

Avec Touch, vous pouvez manipuler directement des objets et de l’interface utilisateur, ce qui permet une expérience plus rapide, plus naturelle et plus attrayante.

## <a name="provide-a-great-touch-experience"></a>Fournir une expérience tactile exceptionnelle

Vous devez vous assurer que les utilisateurs peuvent effectuer efficacement des tâches critiques et importantes à l’aide d’une entrée tactile. Toutefois, certaines fonctionnalités spécifiques de l’application, telles que la manipulation de texte ou de pixels, peuvent ne pas être adaptées à la saisie tactile et peuvent être réservées pour l’appareil d’entrée le plus approprié.

Si vous n’avez pas d’expérience en matière de développement d’applications tactiles, il est préférable de les apprendre. Procurez-vous un ordinateur tactile, mettez la souris et le clavier de côté et utilisez uniquement vos doigts pour interagir avec votre application. Si vous avez une tablette, Expérimentez-la dans des positions différentes, par exemple sur votre genoux, sur une table ou sur vos bras lorsque vous êtes debout. Essayez de l’utiliser en orientation portrait et paysage.

Les applications tactiles optimisées qui fonctionnent le mieux avec Touch interaction sont généralement :

-   **Naturel et intuitif.** Les interactions sont conçues pour correspondre à la façon dont les utilisateurs interagissent avec les objets dans le monde réel.
-   **Moins intrusif.** L’utilisation de Touch est silencieuse et, par conséquent, bien moins gênante que la saisie ou le clic.
-   **Portatif.** Les appareils tactiles sont plus compacts, car de nombreuses tâches peuvent être effectuées sans clavier, souris, stylet ou pavé tactile. Ils sont également plus flexibles, car une surface de travail n’est pas nécessaire.
-   **Directe et attrayante.** Touch vous donne l’impression que vous manipulez directement des objets à l’écran.
-   **Moins précis.** Les utilisateurs ne peuvent pas cibler les objets avec précision avec Touch, par rapport à une souris ou un stylet.

Touch offre un aspect naturel et réaliste à l’interaction. La manipulation et l’animation directes réalisent cette impression, en donnant aux objets un mouvement et des commentaires réalistes et dynamiques. Prenons l’exemple d’un jeu de cartes. Non seulement il est pratique et facile de faire glisser des cartes à l’aide d’un doigt, mais l’expérience prend un sentiment réel lorsque vous pouvez lancer, déplacer et faire tourner les cartes comme s’il s’agissait d’un jeu physique. Et lorsque vous essayez de déplacer une carte qui ne peut pas être déplacée, il est préférable de faire en sorte que la carte résiste, mais n’empêche pas le mouvement, et de la rétablir lorsqu’elle est libérée, pour indiquer clairement que l’action a été reconnue, mais qu’elle ne peut pas être effectuée.

Heureusement, si votre application est déjà bien conçue, il est facile de faire une expérience tactile exceptionnelle. À cet effet, il s’agit d’un programme bien conçu :

-   **Garantit que la plupart des tâches importantes peuvent être effectuées efficacement à l’aide d’un doigt** (au moins les tâches qui n’impliquent pas beaucoup de saisie ou de manipulation de pixels détaillée).
-   **Utilise des contrôles de grande taille pour les fonctions tactiles.** Les contrôles communs ont une taille minimale de 23x23 pixels (13x13), et les contrôles les plus couramment utilisés sont au moins de 40 x 40 pixels (23x22). Pour éviter tout comportement qui ne répond pas, les éléments d’interface utilisateur doivent avoir au moins 5 pixels (3 unités de capacité) entre eux. Pour les autres contrôles, assurez-vous qu’ils ont au moins un 23x23 pixel (13x13 DLU), cliquez sur cible, même si leur apparence statique est bien plus petite. Consultez dimensionnement du contrôle standard.
-   **Prend en charge l’entrée de souris.** Les contrôles interactifs ont des intuitivité clairs et visibles. Les objets ont des comportements standard pour les interactions de souris standard (simple et double-clic, cliquer avec le bouton droit, faire glisser et pointer).
-   **Prend en charge l’entrée au clavier.** L’application fournit des affectations de touches de raccourci standard, en particulier pour les commandes de navigation et de modification qui peuvent également être générées par le biais de gestes tactiles.
-   **Garantit l’accessibilité.** Utilise UI Automation ou Microsoft Active Accessibility (MSAA) pour fournir un accès par programme à l’interface utilisateur pour les technologies d’assistance. L’application répond de manière appropriée aux modifications de l’orientation, du thème, des paramètres régionaux et du système.
-   **Élimine les interactions inutiles.** Pour éviter la perte de données ou l’accès au système, utilisez les valeurs par défaut les plus sûres et les plus sécurisées. Si la sécurité et la sécurité ne sont pas des facteurs, l’application sélectionne l’option la plus probable ou la plus pratique.
-   **Fournit un équivalent tactile pour le pointage.** Ne vous fiez pas au pointage comme une seule façon d’effectuer une action.
-   **Garantit que les gestes prennent effet immédiatement.** Gardez les points de contact sous les doigts de l’utilisateur en douceur tout au long du mouvement, ce qui permet d’effectuer le mappage du mouvement directement sur le mouvement de l’utilisateur.
-   **Utilise des mouvements standard dans la mesure du possible.** Mouvements personnalisés uniquement pour les interactions propres à votre application.
-   **Garantit que les commandes indésirables ou destructrices peuvent être inversées ou corrigées.** Les actions accidentelles sont plus probables quand vous utilisez Touch.

## <a name="guidelines-for-touch-input"></a>Instructions pour les entrées tactiles

avec touch, votre application Windows peut utiliser des mouvements physiques pour émuler la manipulation directe des éléments d’interface utilisateur.

Tenez compte des meilleures pratiques suivantes lors de la conception de votre application tactile :

**La réactivité est essentielle pour créer des expériences tactiles directes et attrayantes.** Pour faire en sorte que les gestes soient directs, les gestes doivent prendre effet immédiatement, et les points de contact d’un objet doivent rester correctement sous les doigts de l’utilisateur tout au long du mouvement. L’effet de l’entrée tactile doit être directement mappé sur le mouvement de l’utilisateur. par exemple, si l’utilisateur fait pivoter ses doigts de 90 degrés, l’objet doit également pivoter de 90 degrés. Tout décalage, réponse hachée, perte de contact ou résultats inexacts détruit la perception de la manipulation directe et de la qualité.

**La cohérence est essentielle pour créer des expériences tactiles qui semblent naturelles et intuitives.** Une fois que les utilisateurs apprennent un mouvement standard, ils s’attendent à ce que le mouvement ait le même effet sur toutes les applications. Pour éviter toute confusion et frustration, n’assignez jamais de significations non standard aux gestes standard. Utilisez plutôt des mouvements personnalisés pour les interactions propres à votre programme.

nous allons ensuite décrire le langage de Windows touch, mais avant de commencer, voici une brève liste de termes de saisie tactile de base.

-   **Mouvement**

    Un geste est l’acte ou le mouvement physique effectué sur le périphérique d’entrée (doigt, doigts, stylet/stylet, souris, etc.). Par exemple, pour lancer, activer ou appeler une commande, vous utilisez un appui sur le doigt pour un appareil tactile ou un pavé tactile (équivalent à un clic gauche avec une souris, un robinet avec un stylet ou une entrée sur un clavier).

-   **Manipulation**

    Une manipulation est la réaction immédiate, en temps réel, ou la réponse d’un objet ou d’une interface utilisateur à un geste. Par exemple, les gestes de diapositive et de balayage entraînent généralement un déplacement d’un élément ou d’une interface utilisateur.

    Le résultat final d’une manipulation, le manifeste par l’objet à l’écran et dans l’interface utilisateur, est l’interaction.

-   **Interaction**

    Les interactions dépendent de la façon dont une manipulation est interprétée et de la commande ou de l’action qui résulte de la manipulation. Par exemple, les objets peuvent être déplacés à l’aide des gestes de diapositive et de balayage, mais les résultats diffèrent selon qu’un seuil de distance est franchi ou non. Vous pouvez utiliser la diapositive pour faire glisser un objet ou un panoramique dans une vue, tandis que l’option balayer peut être utilisée pour sélectionner un élément ou afficher une barre d’application.

### <a name="the-windows-touch-language"></a>langage tactile Windows

Windows fournit un ensemble concis d’interactions tactiles utilisées dans le système. L’application de ce langage tactile rend votre application plus familière que les utilisateurs connaissent déjà. Cela augmente la confiance des utilisateurs en facilitant l’apprentissage et l’utilisation de votre application. Pour en savoir plus sur l’implémentation du langage tactile, consultez gestes, manipulations et interactions.

**Appuyez longuement pour en savoir plus**

Le geste appuyer et maintenir affiche des informations détaillées ou des visuels d’apprentissage (par exemple, une info-bulle ou un menu contextuel) sans valider une action ou une commande. Le panoramique est toujours possible si un mouvement coulissant est démarré alors que le visuel est affiché.

> [!IMPORTANT]
> Vous pouvez utiliser la fonctionnalité appuyer et maintenir pour la sélection dans les cas où les panoramiques horizontal et vertical sont activés.

 

État d’entrée : un ou deux doigts en contact avec l’écran.

Motion : pas de mouvement.

État de sortie : le dernier doigt vers le haut termine le mouvement.

Effet : afficher plus d’informations.

![Appuyez sur la touche \- \- pour \-learn.png](images/inter-touch-image2.png)

Mouvement d’appui et de maintien.

**Pointage**

Hover est une interaction utile, car elle permet aux utilisateurs d’obtenir des informations supplémentaires par le biais de conseils avant d’initier une action. L’affichage de ces conseils permet aux utilisateurs de se sentir plus confiants et réduit les erreurs.

Malheureusement, le survol n’est pas pris en charge par touch technologies, de sorte que les utilisateurs ne peuvent pas passer à l’utilisation d’un doigt. La solution la plus simple à ce problème consiste à tirer pleinement parti du pointage, mais uniquement de la manière dont il n’est pas nécessaire d’effectuer une action. En pratique, cela signifie généralement que l’action peut également être effectuée en cliquant, mais pas nécessairement exactement de la même façon.

![Capture d’écran montrant un exemple d’interaction de survol en regard d’un exemple de l’action de clic.](images/inter-touch-image13.png)

Dans cet exemple, les utilisateurs peuvent voir la date du jour en pointant ou en cliquant sur.

**Appuyer pour l’action principale**

Le recours à un élément appelle son action principale, par exemple le lancement d’une application ou l’exécution d’une commande.

État d’entrée : un doigt en contact avec l’écran ou le pavé tactile et levé avant le seuil de temps pour une interaction d’appui et de maintien.

Motion : pas de mouvement.

État de sortie : le doigt termine le mouvement.

Effet : lancez une application ou exécutez une commande.

![pression \- tactile \-primary.png](images/inter-touch-image3.png)

Mouvement TAP.

**Glisser-déplacer**

La diapositive est principalement utilisée pour les interactions panoramiques, mais elle peut également être utilisée pour le déplacement (où le panoramique est restreint à une direction), le dessin ou l’écriture. Vous pouvez également utiliser la diapositive pour cibler des éléments compacts compacts et compactés en les nettoyant (en glissant le doigt sur les objets connexes tels que les cases d’option).

État d’entrée : un ou deux doigts en contact avec l’écran.

Motion : faites glisser, tout autre doigt restant à la même position l’un par rapport à l’autre.

État de sortie : le dernier doigt vers le haut termine le mouvement.

Effet : déplacez l’objet sous-jacent directement et immédiatement lorsque les doigts se déplacent. Veillez à conserver le point de contact sous le doigt tout au long du mouvement.

![\-slide.png tactile](images/inter-touch-image4.png)

Mouvement de panoramique.

**Faire glisser pour sélectionner, commande et déplacer**

En glissant le doigt sur une petite distance, perpendiculaire à la direction de panoramique (où le panoramique est limité à une direction), sélectionne des objets dans une liste ou une grille. Affiche la barre d’application avec les commandes appropriées lorsque des objets sont sélectionnés.

État d’entrée : un ou plusieurs doigts touchent l’écran.

Motion : faites glisser une petite distance et soulevez avant que le seuil de distance pour une interaction de déplacement se produise.

État de sortie : le dernier doigt vers le haut termine le mouvement.

Effet : l’objet sous-jacent est sélectionné, ou déplacé, ou la barre de l’application est affichée. Veillez à conserver le point de contact sous le doigt tout au long du mouvement.

![d : \\ sdkenlistment \\ m \- UX \- Design \\ m \- UX \- images de conception \\ \\ tactile \-swipe.png](images/inter-touch-image5.png)

Mouvement de balayage.

**Pincer et étirer pour agrandir**

Les mouvements de pincement et d’étirement sont utilisés pour trois types d’interactions : zoom optique, redimensionnement et zoom sémantique.

Le zoom optique ajuste le niveau d’agrandissement de la zone de contenu entière pour obtenir une vue plus détaillée du contenu. En revanche, le redimensionnement est une technique permettant d’ajuster la taille relative d’un ou plusieurs objets dans une zone de contenu sans modifier la vue de la zone de contenu.

Le zoom sémantique est une technique tactile optimisée pour la présentation et la navigation dans les données structurées ou le contenu au sein d’une seule vue (par exemple, la structure de dossiers d’un ordinateur, d’une bibliothèque de documents ou d’un album photo) sans avoir besoin de parcourir, de faire défiler ou de contrôler l’arborescence. Le zoom sémantique fournit deux vues différentes du même contenu en vous permettant d’afficher plus de détails quand vous effectuez un zoom avant et moins de détails.

État d’entrée : deux doigts dans le contact avec l’écran en même temps.

Motion : les doigts s’éloignent (Stretch) ou ensemble (pincement) sur un axe.

État de sortie : tout doigt vers le haut termine le mouvement.

Effet : effectuez un zoom avant ou arrière sur l’objet sous-jacent, et immédiatement lorsque les doigts séparent ou approchent sur l’axe. Veillez à conserver les points de contact sous le doigt tout au long du mouvement.

![areazoom.png d’atterrissage \-](images/inter-touch-image6.png)

Mouvement de zoom.

**Activer la rotation**

La rotation avec deux ou plusieurs doigts provoque la rotation d’un objet. Faites pivoter l’appareil lui-même pour faire pivoter l’écran tout entier.

État d’entrée : deux doigts dans le contact avec l’écran en même temps.

Motion : l’un ou les deux doigts pivotent autour de l’autre, en se déplaçant perpendiculairement à la ligne qui les relie.

État de sortie : tout doigt vers le haut termine le mouvement.

Effet : faites pivoter l’objet sous-jacent de la même façon que les doigts. Veillez à conserver les points de contact sous le doigt tout au long du mouvement.

![\-turn.png tactile](images/inter-touch-image7.png)

Mouvement de rotation.

la Rotation n’est logique que pour certains types d’objets, donc elle n’est pas mappée à une interaction système Windows.

La rotation est souvent effectuée différemment par différentes personnes. Certaines personnes préfèrent faire pivoter un doigt autour d’un doigt pivot, tandis que d’autres préfèrent faire pivoter les deux doigts dans un mouvement circulaire. La plupart des gens utilisent une combinaison des deux, avec un doigt qui se déplace plus que l’autre. Bien que la rotation lisse sur un angle soit la meilleure interaction, dans de nombreux contextes, tels que l’affichage de photos, il est préférable de régler à la rotation de 90 degré le plus proche une fois que l’utilisateur a pu aller. Dans la modification de photos, vous pouvez utiliser une petite rotation pour redresser la photo.

**Faire glisser à partir de Edge pour les commandes d’application**

Le fait de faire glisser le doigt sur une petite distance à partir du bord inférieur ou supérieur de l’écran révèle les commandes de l’application dans une barre d’application.

État d’entrée : un ou plusieurs doigts touchent le cadre.

Motion : faites glisser une petite distance sur l’écran et soulevez.

État de sortie : le dernier doigt vers le haut termine le mouvement.

Effet : la barre de l’application s’affiche.

![\-edge.png en \- bas du balayage tactile \-](images/inter-touch-image8.png)

![\- \-edge.png côté balayage \- tactile](images/inter-touch-image9.png)

Mouvement de balayage à partir du bord.

Développeurs : pour plus d’informations, consultez énumération de la [**\_ configuration DIRECTMANIPULATION**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) .

### <a name="control-usage"></a>Utilisation du contrôle

Ici, nous fournissons des instructions pour l’optimisation des contrôles pour l’utilisation tactile.

-   **Utilisez des contrôles communs.** La plupart des contrôles courants sont conçus pour prendre en charge une bonne expérience tactile.
-   **Choisissez des contrôles personnalisés qui sont conçus pour prendre en charge Touch.** Vous pouvez avoir besoin de contrôles personnalisés pour prendre en charge les expériences spéciales de votre programme. Choisissez des contrôles personnalisés qui :
    -   La taille peut être suffisamment grande pour faciliter le ciblage et la manipulation.
    -   En cas de manipulation, déplacez et réagissez sur la manière dont les objets réels se déplacent et réagissent, par exemple en ayant un élan et un frottement.
    -   Sont indulgent avec en permettant aux utilisateurs de corriger facilement les erreurs.
    -   Indulgent avec d’inexactitude en cliquant et en faisant glisser. Les objets qui sont supprimés vers leur destination doivent se trouver à l’emplacement approprié.
    -   Obtenir des commentaires visuels clairs lorsque le doigt se trouve sur le contrôle.
-   **Utilisez des contrôles limités.** Les contrôles restreints, tels que les listes et les curseurs, lorsqu’ils sont conçus pour un ciblage simple tactile, peuvent être mieux que des contrôles non restreints comme des zones de texte, car ils réduisent le besoin d’entrée de texte.
-   **Fournissez les valeurs par défaut appropriées.** Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée par défaut. Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez l’option la plus probable ou la plus pratique, en éliminant ainsi toute interaction inutile.
-   **Indiquez la saisie semi-automatique du texte.** Fournit une liste des valeurs les plus probables, ou les valeurs d’entrée les plus récentes, pour faciliter grandement la saisie de texte.
-   **Pour les tâches importantes qui utilisent une sélection multiple**, si une liste de sélection multiple standard est normalement utilisée, fournissez une option pour utiliser une liste de cases à cocher à la place.

### <a name="control-sizes-and-touch-targeting"></a>Contrôler les tailles et le ciblage tactile

En raison de la grande surface d’ébauche, les petits contrôles trop proches peuvent être difficiles à cibler précisément.

En règle générale, une taille de contrôle de 23x23 pixels (13x13) est une taille de contrôle interactive minimale pour tous les périphériques d’entrée. En revanche, les contrôles spin à 15x11 pixels sont beaucoup trop petits pour être utilisés efficacement avec Touch.

![Capture d’écran montrant la largeur et la hauteur des boutons de sélection vers le haut et vers le haut, mesurant 9 dlu (15 pixels) en largeur de 5 unités de mesure (9 pixels).](images/inter-touch-image14.png)

N’oubliez pas que la taille minimale est véritablement basée sur la zone physique, et non sur les métriques de disposition telles que les pixels ou les unités de mémoire. La recherche indique que la zone cible minimale pour une interaction efficace et précise à l’aide d’un doigt est 6X6 millimètres (mm). Cette zone se traduit par des métriques de disposition comme suit :



| Police             | Millimètres | Pixels relatifs | Dlu  |
|------------------|-------------|-----------------|-------|
| Segoe UI de 9 points | 6x6         | 23x23           | 13x13 |
| Tahoma 8 points   | 6x6         | 23x23           | 15x14 |



 

En outre, les recherches montrent qu’une taille minimale de 10x10 mm (environ 40 x 40 pixels) permet une meilleure rapidité et une plus grande précision, et est également plus confortable pour les utilisateurs. Lorsque cela est possible, utilisez cette plus grande taille pour les boutons de commande utilisés pour les commandes les plus importantes ou les plus fréquemment utilisées.

L’objectif n’est pas d’avoir des contrôles géants, juste ceux qui sont facilement utilisés avec Touch.

![capture d’écran qui affiche la barre d’outils Microsoft Word avec le bouton « grammaire de l’orthographe de B C & » mis en surbrillance, avec une hauteur de 41 DLU et une largeur de 40 DLU.](images/inter-touch-image15.png)

dans cet exemple, Microsoft Word utilise des boutons supérieurs à 10x10 mm pour les commandes les plus importantes.

![capture d’écran montrant la calculatrice Windows.](images/inter-touch-image16.png)

Cette version de Calculator utilise des boutons supérieurs à 10x10 mm pour ses commandes les plus fréquemment utilisées.

Il n’existe pas de taille parfaite pour les cibles tactiles. Différentes tailles fonctionnent pour différentes situations. Les actions ayant des conséquences graves (par exemple, supprimer et fermer) ou les actions fréquemment utilisées doivent utiliser des cibles tactiles de grande taille. Les actions peu utilisées avec des conséquences mineures peuvent utiliser de petites cibles.

**Instructions relatives à la taille cible pour les contrôles personnalisés**



| Orientation de la taille                                                                                 | Description                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![taille minimale recommandée pour 7X7](images/inter_touch_image10.jpeg)<br/>      | **7X7 mm : taille minimale recommandée**<br/> 7X7 mm est une taille minimale correcte si la mauvaise cible peut être corrigée dans un ou deux mouvements ou dans un délai de cinq secondes. Le remplissage entre les cibles est tout aussi important que la taille cible.<br/>                               |
| ![9 x 9 taille recommandée pour la précision](images/inter_touch_image11.jpeg)<br/> | **En cas de précision**<br/> Les actions fermer, supprimer et autres avec des conséquences graves ne peuvent pas permettre des pressions accidentelles. Utilisez des cibles 9 x 9 mm si le fait de toucher la mauvaise cible nécessite plus de deux gestes, cinq secondes ou une modification de contexte majeure pour corriger le problème.<br/>     |
| ![taille minimale de 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Quand il ne s’intègre pas**<br/> Si vous entassez des choses, il est possible d’utiliser des cibles de 5 à 5 x 5 tant que le fait de toucher la mauvaise cible peut être corrigé avec un seul geste. L’utilisation de 2 mm de remplissage entre les cibles est extrêmement importante dans ce cas.<br/> |



 

**Recommandations relatives à la taille cible pour les contrôles communs**

-   **Pour les contrôles communs, utilisez les tailles de contrôle recommandées.** Le dimensionnement de contrôle recommandé est conforme à la taille minimale de 23x23 pixel (13x13 DLU), à l’exception des cases à cocher et des cases d’option (la largeur du texte compense un peu), des contrôles spin (qui ne sont pas utilisables avec Touch, mais qui sont redondants) et des séparateurs.

    ![Capture d’écran montrant un exemple de contrôles courants, y compris des contrôles audio, un bouton « Parcourir Internet maintenant » et une fenêtre de l’Explorateur de fichiers.](images/inter-touch-image17.png)

    Les tailles de contrôle recommandées sont facilement touchable.

-   **Pour les boutons de commande utilisés pour les commandes les plus importantes ou les plus fréquemment utilisées, utilisez une taille minimale de 40 x 40 pixels (23x22) chaque fois que cela est possible.** Cela offre une meilleure rapidité et une plus grande précision, et est également plus confortable pour les utilisateurs.

    ![Capture d’écran montrant plusieurs tailles d’un bouton Envoyer un message électronique, avec les tailles les plus petites aux plus grandes, de gauche à droite.](images/inter-touch-image18.png)

    Lorsque cela est possible, utilisez des boutons de commande plus grands pour les commandes importantes ou fréquemment utilisées.

-   **Pour les autres contrôles :**

    -   **Utilisez des cibles de clic plus larges.** Pour les petits contrôles, augmentez la taille de la cible par rapport à l’élément d’interface graphique visible statiquement. Par exemple, les boutons d’icône de 16x16 pixels peuvent avoir un 23x23 pixel clic sur les boutons cible et les éléments de texte peuvent avoir des rectangles de sélection de 8 pixels de plus que le texte et de 23 pixels de haut.

        Utilisation correcte :

        ![Capture d’écran montrant une barre d’outils avec la taille cible correcte.](images/inter-touch-image19.png)

        Incorrect :

        ![Capture d’écran montrant une arborescence U I avec une zone cible incorrecte.](images/inter-touch-image20.png)

        Utilisation correcte :

        ![Capture d’écran montrant une arborescence U I avec la taille correcte pour la zone cible.](images/inter-touch-image21.png)

        Dans les exemples appropriés, les cibles de clic sont plus volumineuses que les éléments d’interface utilisateur visibles statiquement.

    -   **Utiliser des cibles de clic redondantes.** Il est acceptable que les cibles de clic soient inférieures à la taille minimale si ce contrôle a des fonctionnalités redondantes.

        Par exemple, les triangles de divulgation progressive utilisés par le contrôle Tree View sont uniquement des pixels 6x9, mais leurs fonctionnalités sont redondantes avec leurs étiquettes d’élément associées.

        ![Capture d’écran montrant une arborescence U I avec des cibles de clic redondantes.](images/inter-touch-image22.png)

        Les triangles de la vue d’arborescence sont trop petits pour être facilement touchable, mais ils sont redondants dans les fonctionnalités avec leurs étiquettes associées plus grandes.

        Respectez les mesures système. Ne pas coder en dur. Si nécessaire, les utilisateurs peuvent modifier les métriques du système ou les PPP en fonction de leurs besoins. Toutefois, considérez ceci comme un dernier recours, car les utilisateurs ne doivent pas normalement ajuster les paramètres système pour rendre l’interface utilisateur utilisable.

        ![Capture d’écran montrant une hauteur de menu standard à gauche et une plus grande hauteur de menu à droite.](images/inter-touch-image23.png)

        Dans cet exemple, la métrique système pour la hauteur de menu a été modifiée.

Modification de texte

La modification du texte est l’une des interactions les plus délicates lors de l’utilisation d’un doigt. L’utilisation de contrôles limités, de valeurs par défaut appropriées et de la saisie semi-automatique, élimine ou réduit la nécessité d’entrer du texte. Toutefois, si votre application implique la modification de texte, vous pouvez rendre les utilisateurs plus productifs en zoomant automatiquement l’interface utilisateur d’entrée jusqu’à 150% par défaut quand Touch est utilisé.

Par exemple, un programme de messagerie peut afficher l’interface utilisateur à la taille normale touchable, mais zoomer l’interface utilisateur d’entrée sur 150% pour composer des messages.

![Capture d’écran montrant un message électronique U I.](images/inter-touch-image24.png)

Dans cet exemple, l’interface utilisateur d’entrée est zoomée sur 150 pour cent.

### <a name="control-layout-and-spacing"></a>Contrôler la disposition et l’espacement

L’espacement entre les contrôles est un facteur important pour faciliter la touchable des contrôles. Le ciblage est plus rapide mais moins précis en cas d’utilisation d’un doigt comme périphérique de pointage, ce qui se traduit par des utilisateurs plus souvent en dehors de la cible prévue. Lorsque les contrôles interactifs sont placés très proches les uns des autres, mais ne se touchent pas réellement, les utilisateurs peuvent cliquer sur l’espace inactif entre les contrôles. Étant donné que le fait de cliquer sur l’espace inactif n’a pas de résultat ou de rétroaction visuelle, les utilisateurs sont souvent incertains mal.

**Ajustez dynamiquement l’espacement en fonction de l’appareil d’entrée utilisé.** Cela s’avère particulièrement utile avec l’interface utilisateur temporaire, comme les menus et les lanceurs.

**Fournissez un minimum de 5 pixels (3 dlu) d’espace entre les régions cibles des contrôles interactifs.** Si les petits contrôles sont trop espacés, l’utilisateur doit appuyer avec précision pour éviter de cliquer sur l’objet incorrect.

**Facilitez la différenciation des contrôles dans les groupes en utilisant plus que l’espacement vertical recommandé entre les contrôles.** Par exemple, les cases d’option à hauteur de 19 pixels sont plus courtes que la taille minimale recommandée de 23 pixels. Une fois l’espace vertical disponible, vous pouvez obtenir approximativement le même effet que le dimensionnement recommandé en ajoutant 4 pixels supplémentaires à la norme 7 pixels.

Utilisation correcte :

![Capture d’écran montrant un exemple standard d’espacement vertical entre les contrôles.](images/inter-touch-image25.png)

Mieux :

![Capture d’écran montrant un exemple de contrôles avec davantage d’espacement vertical.](images/inter-touch-image26.png)

Dans un meilleur exemple, l’espacement supplémentaire entre les cases d’option les rend plus faciles à distinguer.

Il peut arriver que l’espacement supplémentaire soit souhaitable quand vous utilisez Touch, mais pas quand vous utilisez la souris ou le clavier. Dans ce cas, utilisez uniquement une conception plus spacieux quand une action est initiée à l’aide de Touch.

**Choisissez une disposition qui place les contrôles à proximité de l’endroit où ils vont probablement être utilisés.** Dans la mesure du possible, conservez les interactions entre les tâches dans une petite zone et recherchez les contrôles proches de l’endroit où ils vont probablement être utilisés. Évitez les déplacements à distance longue, en particulier pour les tâches courantes et les opérations de glisser-déplacer.

Supposons que l’emplacement actuel du pointeur est le plus proche possible d’une cible, ce qui la rend facile à acquérir. Ainsi, les menus contextuels tirent pleinement parti de la Loi de Fitts, tout comme les mini-barres d’outils utilisées par Microsoft Office.

![capture d’écran montrant un exemple de menu contextuel et une mini-barre d’outils de Microsoft Office côte à côte.](images/inter-touch-image27.png)

**Évitez de placer de petits contrôles près du bord de l’application ou de l’affichage.** Les petites cibles proches des bords peuvent être difficiles à toucher (les panneaux d’affichage peuvent interférer avec les gestes de périphérie). Pour vous assurer que les contrôles sont faciles à cibler quand une fenêtre est agrandie, faites-en au moins 23x23 pixels (13x13) ou placez-les en dehors du bord de la fenêtre.

**Utilisez l’espacement recommandé.** L’espacement recommandé est convivial. Toutefois, si votre application peut tirer parti d’un grand dimensionnement et d’un espacement plus important, envisagez le dimensionnement et l’espacement recommandés au minimum lorsque cela est approprié.

**Fournissez au moins 5 pixels (3 unités de commande) d’espace entre les contrôles interactifs.** Cela évite toute confusion lorsque les utilisateurs appuient en dehors de la cible prévue.

Envisagez d’ajouter plus que l’espacement vertical recommandé dans des groupes de contrôles, tels que des liens de commande, des cases à cocher et des cases d’option, ainsi qu’entre les groupes. Cela les rend plus faciles à distinguer.

**Envisagez d’ajouter dynamiquement plus que l’espace vertical recommandé lorsqu’une action est initiée à l’aide de Touch.** Cela rend les objets plus faciles à distinguer, mais sans occuper plus d’espace lors de l’utilisation d’un clavier ou d’une souris. Augmentez l’espacement d’un tiers de sa taille normale ou d’au moins 8 pixels.

![image](images/inter-touch-image28.png)

dans cet exemple, les listes de raccourcis de la barre des tâches Windows 7 sont plus spacieux quand elles sont affichées avec touch.

### <a name="interaction"></a>Interaction

L’utilisation des contrôles appropriés vous permet d’obtenir uniquement une partie de la façon dont vous avez besoin d’une application optimisée tactile. vous devez également prendre en compte le modèle d’interaction global que ces contrôles prennent en charge. Voici quelques recommandations pour vous aider à le faire.

-   **Rendez le point de suspension redondant.** Le survol n’est pas pris en charge par la plupart des technologies tactiles, de sorte que les utilisateurs avec des écrans tactiles ne peuvent effectuer aucune tâche nécessitant un pointage.
-   **Pour les applications qui ont besoin d’une entrée de texte, intégrez entièrement la fonctionnalité de clavier tactile** en :
    -   Fournir les valeurs par défaut appropriées pour les entrées utilisateur.
    -   Fournir des suggestions de saisie semi-automatique le cas échéant.

    > [!Note]  
    > Développeurs : pour plus d’informations sur l’intégration du clavier tactile, consultez [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Autoriser les utilisateurs à effectuer un zoom sur l’interface utilisateur du contenu si votre programme a des tâches qui requièrent la modification de texte.** Envisagez le zoom automatique sur 150 pour cent quand Touch est utilisé.
-   **Fournissez un panoramique et un zoom en douceur et réactifs, quel que soit le cas.** Redessinez rapidement après un panoramique ou un zoom pour rester réactif. Cela est nécessaire pour que la manipulation directe soit véritablement directe.
-   **Pendant un panoramique ou un zoom, assurez-vous que les points de contact restent sous le doigt tout au long du mouvement.** Dans le cas contraire, il est difficile de contrôler le panoramique ou le zoom.
-   **Étant donné que les gestes sont mémorisés, attribuez-leur des significations cohérentes entre les applications.** N’attribuez pas des significations différentes aux gestes avec une sémantique fixe. Utilisez plutôt un geste approprié spécifique à l’application.

### <a name="forgiveness"></a>Effacement

La manipulation directe rend le toucher naturel, expressif, efficace et attrayant. Toutefois, en cas de manipulation directe, il peut y avoir une manipulation accidentelle et, par conséquent, la nécessité de le faire.

L’effacement est la possibilité d’inverser ou de corriger facilement une action indésirable. Vous faites une expérience tactile indulgent avec en fournissant une annulation, en donnant de bons commentaires visuels, en ayant une séparation physique claire entre les commandes fréquemment utilisées et les commandes destructrices, et en permettant aux utilisateurs de corriger facilement les erreurs. L’Association d’une annulation permet d’éviter que des actions indésirables ne se produisent en premier lieu, ce que vous pouvez faire en utilisant des contrôles et des confirmations restreints pour des actions ou des commandes risquées qui ont des conséquences inattendues.

-   **Fournissez une commande Annuler.** Il est préférable de fournir un moyen simple d’annuler toutes les commandes, mais votre application peut avoir des commandes dont l’effet ne peut pas être annulé.
-   **Chaque fois que cela est possible, fournissez de bons commentaires sur le doigt, mais n’effectuez pas d’actions jusqu’au moment.** Cela permet aux utilisateurs de corriger les erreurs avant de les créer.
-   **Chaque fois que cela est possible, autorisez les utilisateurs à corriger facilement les erreurs.** Si une action prend effet sur le doigt, autorisez les utilisateurs à corriger les erreurs en glissant alors que le doigt est toujours en cours d’exécution.
-   **Dans la mesure du possible, indiquez qu’une manipulation directe ne peut pas être effectuée en résistant au mouvement.** Autoriser le déplacement, mais faire en sorte que l’objet soit rétabli en place lorsqu’il est relâché pour indiquer clairement que l’action a été reconnue mais ne peut pas être effectuée.
-   **Avoir une séparation physique claire entre les commandes fréquemment utilisées et les commandes destructrices.** Dans le cas contraire, les utilisateurs peuvent toucher accidentellement des commandes destructrices. Une commande est considérée comme destructrice si son effet est répandu et qu’elle ne peut pas être facilement annulée, ou bien l’effet n’est pas immédiatement visible.
-   **Confirmez les commandes pour les actions risquées ou les commandes qui ont des conséquences inattendues.** Utilisez une boîte de dialogue de confirmation à cet effet.
-   **Pensez à confirmer toute autre action que les utilisateurs ont tendance à faire accidentellement lors de l’utilisation de Touch, et qui passent inaperçus ou sont difficiles à annuler.** En règle générale, elles sont appelées « confirmations de routine » et sont déconseillées en fonction de l’hypothèse que les utilisateurs n’émettent pas souvent ces commandes par accident avec la souris ou le clavier. Pour empêcher les confirmations inutiles, présentez ces confirmations uniquement si la commande a été lancée à l’aide de Touch.

    Les confirmations de routine sont acceptables pour les interactions que les utilisateurs effectuent souvent accidentellement en utilisant Touch.

    Développeurs : vous pouvez faire la distinction entre les événements de souris et les événements tactiles à l’aide de l’API [**\_ \_ source du message d’entrée**](/windows/win32/api/winuser/ns-winuser-input_message_source) .


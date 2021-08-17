---
title: Liste de contrôle d’expérience utilisateur pour les applications de bureau
description: Voici un ensemble d’instructions importantes dans le Guide de l’expérience utilisateur. Vous pouvez l’utiliser comme liste de vérification pour vous assurer que l’interface utilisateur de votre programme obtient ces éléments importants.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 712b31a7a5166e41e590470aea48f60a1f159850da3ea6917b36ece9ada80fa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332469"
---
# <a name="ux-checklist-for-desktop-applications"></a>Liste de contrôle d’expérience utilisateur pour les applications de bureau

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Voici un ensemble d’instructions importantes dans le Guide de l’expérience utilisateur. Vous pouvez l’utiliser comme liste de vérification pour vous assurer que l’interface utilisateur de votre programme obtient ces éléments importants.

## <a name="windows"></a>Windows

-   **prendre en charge la résolution minimale Windows de 800 x 600 pixels.** Pour les interfaces utilisateur (IU) critiques qui doivent fonctionner en mode sans échec, prennent en charge une [résolution efficace](glossary.md) de 640 x 480 pixels. Veillez à tenir compte de l’espace utilisé par la barre des tâches en réservant 48 [pixels relatifs](glossary.md) verticaux pour les fenêtres affichées avec la barre des tâches.
-   **Optimisez les dispositions de fenêtres redimensionnables pour une résolution efficace de 1024 x 768 pixels.** Redimensionnez automatiquement ces fenêtres pour réduire la résolution de l’écran d’une manière qui reste fonctionnelle.
-   **Veillez à tester votre Windows en mode 96 points par pouce (dpi) (à 800x600 pixels), 120 ppp (à 1024 x 768 pixels) et 144 dpi (en 1200x900 pixels).** Vérifiez les problèmes de disposition, tels que le découpage des contrôles, du texte et des fenêtres, et l’étirement des icônes et des bitmaps.
-   **Pour les programmes qui utilisent des scénarios tactiles et mobiles, optimisez pour 120 ppp.** Les écrans haute résolution sont actuellement répandus sur les PC tactiles et les ordinateurs portables.
-   **Si une fenêtre est une fenêtre enfant, affiche initialement « centré » en haut de la fenêtre propriétaire.** Jamais en-dessous. Pour l’affichage suivant, envisagez de l’afficher à son dernier emplacement (par rapport à la fenêtre propriétaire) si cela est susceptible d’être plus pratique.
-   **Si une fenêtre est contextuelle, affichez-la toujours près de l’objet à partir duquel elle a été lancée.** Toutefois, placez-le en dehors de la méthode (en décalant de préférence vers la droite et vers la droite) pour que l’objet ne soit pas couvert par la fenêtre.

## <a name="layout"></a>Layout

-   **Dimensionnez les contrôles et les volets dans une fenêtre pour qu’ils correspondent à leur contenu standard.** Évitez le texte tronqué et les ellipses qui lui sont associées. Les utilisateurs ne doivent jamais avoir à interagir avec une fenêtre pour afficher son contenu standard : réserver le redimensionnement et le défilement pour du contenu anormalement volumineux. Vérification spécifique :
    -   **Tailles de contrôle.** Dimensionnez les contrôles sur leur contenu standard, en rendant les contrôles plus larges, plus hauts ou en plusieurs lignes, si nécessaire. Dimensionnez les contrôles pour éliminer ou réduire le défilement dans les fenêtres qui disposent de beaucoup d’espace disponible. En outre, il ne doit jamais y avoir d’étiquettes tronquées, ni de texte tronqué dans les fenêtres qui disposent de beaucoup d’espace disponible. Toutefois, pour faciliter la lecture du texte, envisagez de limiter les largeurs de ligne à 65 caractères.
    -   **Largeurs de colonne.** Assurez-vous que les colonnes d’affichage de liste ont un dimensionnement par défaut, minimal et maximal. Choisissez affichages liste largeurs de colonne par défaut qui ne génèrent pas de texte tronqué, en particulier si de l’espace est disponible dans l’affichage de liste.
    -   **Équilibre de la disposition.** La disposition d’une fenêtre doit avoir un sens à peu près équilibrée. Si la disposition semble lourde, envisagez de rendre les contrôles plus larges et de déplacer certains contrôles vers la droite.
    -   **Redimensionnement de la disposition.** Quand une fenêtre est redimensionnable et que les données sont tronquées, vérifiez que les tailles de fenêtres supérieures affichent plus de données. Lorsque les données sont tronquées, les utilisateurs attendent des fenêtres de redimensionnement pour afficher plus d’informations.
-   **Définissez une taille de fenêtre minimale s’il y a une taille au-dessous de laquelle le contenu n’est plus utilisable.** Pour les contrôles redimensionnables, définissez la taille minimale des éléments redimensionnables sur leur plus petite taille fonctionnelle, telle que la largeur minimale des colonnes fonctionnelles dans les affichages de liste.

## <a name="text"></a>Texte

-   **Utilisez des termes ordinaires et conversationnels lorsque vous le pouvez.** Concentrez-vous sur les objectifs de l’utilisateur, et non sur la technologie. Cela est particulièrement efficace si vous décrivez un concept ou une action technique complexe. Imagine vous intéressent à l’épaule de l’utilisateur et expliquent comment accomplir cette tâche.
-   **Soyez poli, pris en charge et encourageant.** L’utilisateur ne doit jamais se sentir à l’aise avec, à tort ou à intimidant.
-   **Supprimez le texte redondant.** Recherchez du texte redondant dans les titres de la fenêtre, les instructions principales, les instructions supplémentaires, les zones de contenu, les liens de commande et les boutons de validation. En règle générale, laissez le texte intégral dans les instructions principales et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
-   **Utilisez la mise en majuscules de style titre pour les titres et les majuscules de style des phrases pour tous les autres éléments de l’interface utilisateur.** cela est plus approprié pour le ton Windows.
    -   **Exception :** Pour les applications héritées, vous pouvez utiliser la mise en majuscules de style titre pour les boutons de commande, les menus et les en-têtes de colonnes si nécessaire pour éviter de mélanger les styles de mise en majuscules.
-   **Pour les noms de fonctionnalités et de technologies, soyez prudent en majuscules.** En règle générale, seuls les principaux composants doivent être en majuscules (à l’aide de la mise en majuscules du style titre).
-   **Pour les noms de fonctionnalités et de technologies, soyez cohérent en majuscules.** Si le nom apparaît plusieurs fois sur un écran de l’interface utilisateur, il doit toujours apparaître de la même façon. De même, dans tous les écrans de l’interface utilisateur du programme, le nom doit être présenté de manière cohérente.
-   **Ne mettez pas en majuscules les noms des éléments génériques de l’interface utilisateur,** tels que la barre d’outils, le menu, la barre de défilement, le bouton et l’icône.
    -   **Exceptions :** Barre d’adresses, barre de liens, ruban.
-   **N’utilisez pas toutes les lettres majuscules pour les touches du clavier.** Au lieu de cela, suivez la casse utilisée par les claviers standard ou en minuscules si la touche n’est pas étiquetée sur le clavier.
-   **Les ellipses signifient incomplète.** Utilisez des ellipses dans le texte de l’interface utilisateur comme suit :
    -   **Commandes.** Indique qu’une commande a besoin d’informations supplémentaires. N’utilisez pas de points de suspension quand une action affiche une autre fenêtre, uniquement lorsque des informations supplémentaires sont requises. les commandes dont le verbe implicite est d’afficher une autre fenêtre n’acceptent pas les points de suspension, tels que avancé, aide, Options, propriétés ou Paramètres.
    -   **Métadonnée.** Indique que le texte est tronqué.
    -   **Celles.** Indique qu’une tâche est en cours (par exemple, « recherche en cours... »).

**Conseil :** Le texte tronqué dans une fenêtre ou une page avec un espace inutilisé indique une mauvaise disposition ou une taille de fenêtre par défaut trop petite. S’efforcer des dispositions et des tailles de fenêtre par défaut qui éliminent ou réduisent la quantité de texte tronqué. Pour plus d’informations, consultez [Disposition](vis-layout.md).

-   **N’utilisez pas de texte en bleu qui n’est pas un lien, car les utilisateurs peuvent supposer qu’il s’agit d’un lien.** Utilisez le gras ou une nuance de gris à l’endroit où vous utiliseriez sinon du texte en couleur.
-   **Utilisez l’attribut gras avec modération pour attirer l’attention sur le texte que les utilisateurs doivent lire.**
-   **Utilisez l’instruction principale pour décrire de façon concise ce que les utilisateurs doivent faire dans une fenêtre ou une page donnée.** Les bonnes instructions principales communiquent l’objectif de l’utilisateur au lieu de se concentrer uniquement sur la manipulation de l’interface utilisateur.
-   **Exprimez l’instruction principale sous la forme d’une direction impérative ou d’une question spécifique.**
-   **Ne placez pas de points à la fin des étiquettes de contrôle ou des instructions principales.**
-   **Utilisez un espace entre les phrases.** Non deux.

## <a name="controls"></a>Contrôles

-   **Général**
    -   **Étiquetez chaque contrôle ou groupe de contrôles. Exceptions**
        -   Les zones de texte et les listes déroulantes peuvent être étiquetées à l’aide d’invites.
        -   Les contrôles subordonnés utilisent l’étiquette du contrôle associé. Les contrôles spin sont toujours des contrôles subordonnés.
    -   **Pour tous les contrôles, sélectionnez le plus sûr (pour éviter la perte de données ou l’accès au système), la valeur la plus sécurisée par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la valeur la plus probable ou la plus pratique.
    -   **Préférer les contrôles restreints.** Utilisez des contrôles restreints comme les listes et les curseurs dans la mesure du possible, au lieu de contrôles non restreints comme des zones de texte, afin de réduire le besoin d’entrée de texte.
    -   **Reconsidérez les contrôles désactivés.** Les contrôles désactivés peuvent être difficiles à utiliser, car les utilisateurs doivent littéralement déduire la raison pour laquelle ils sont désactivés. Désactivez un contrôle lorsque les utilisateurs s’attendent à ce qu’il s’applique et qu’ils peuvent facilement déduire la raison pour laquelle le contrôle est désactivé. Supprimez le contrôle lorsqu’il n’existe aucun moyen pour les utilisateurs de l’activer ou qu’ils ne s’attendent pas à l’appliquer, ou laissez-le activé, mais fournissez un message d’erreur lorsqu’il est utilisé de manière incorrecte.
        -   **Conseil :** Si vous ne savez pas si vous devez désactiver un contrôle ou fournir un message d’erreur, commencez par composer le message d’erreur que vous pouvez fournir. Si le message d’erreur contient des informations utiles que les utilisateurs cibles ne peuvent pas déduire rapidement, laissez le contrôle activé et fournissez l’erreur. Sinon, désactivez le contrôle.
-   **Boutons de commande**
    -   **Préférer des étiquettes spécifiques à des étiquettes génériques.** Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette. Les utilisateurs sont beaucoup plus susceptibles de lire des étiquettes de bouton de commande que du texte statique.
        -   **Exception :** Ne renommez pas le bouton Annuler si la signification de l’annulation n’est pas ambiguë. Les utilisateurs ne doivent pas avoir à lire tous les boutons pour déterminer le bouton qui annule une action. Toutefois, renommez annuler s’il n’est pas clair que l’action est annulée, par exemple lorsqu’il y a plusieurs actions en attente.
    -   **Lorsque vous posez une question, utilisez des étiquettes qui correspondent à la question.** Par exemple, fournissez Oui et aucune réponse à une question oui ou non.
    -   **N’utilisez pas de boutons appliquer dans les boîtes de dialogue qui ne sont pas des feuilles de propriétés ou des éléments du panneau de configuration.** Le bouton appliquer signifie appliquer les modifications en attente, mais laissez la fenêtre ouverte. Cela permet aux utilisateurs d’évaluer les modifications avant de fermer la fenêtre. Toutefois, seules les feuilles de propriétés et les éléments du panneau de configuration en ont besoin.
    -   Étiquette d’un bouton Annuler si l’annulation retourne l’environnement à son état précédent (sans effet secondaire); Sinon, étiquetez le bouton Fermer (si l’opération est terminée) ou arrêtez (si l’opération est en cours) pour indiquer qu’il laisse l’état modifié actuel intact.
-   **Liens de commande**
    -   **Toujours présenter des liens de commande dans un ensemble de deux ou plus.** Logiquement, il n’y a aucune raison de poser une question qui n’a qu’une seule réponse.
    -   **Fournissez un bouton Annuler explicite.** N’utilisez pas de lien de commande à cet effet. Très souvent, les utilisateurs se rendent compte qu’ils ne souhaitent pas exécuter une tâche. L’utilisation d’un lien de commande pour annuler obligerait les utilisateurs à lire tous les liens de commande avec soin pour déterminer celui que vous voulez annuler. Le fait d’avoir un bouton Annuler explicite permet aux utilisateurs d’annuler une tâche de manière efficace.
    -   **Si le fait de fournir un bouton Annuler explicite laisse un lien de commande unique, fournissez un lien de commande pour annuler et un bouton Annuler.** Ce faisant, il est clair que les utilisateurs ont le choix. Phrase ce lien de commande explique en quoi il diffère de la première réponse, au lieu de simplement « annuler » ou une variante.
-   **Cases à cocher ne plus afficher ce message \<item\>**
    -   **Envisagez d’utiliser une option « ne plus afficher ce message \<item\> » pour permettre aux utilisateurs de supprimer une boîte de dialogue périodique, uniquement s’il n’existe pas de meilleure solution.** Il est préférable de toujours afficher la boîte de dialogue si les utilisateurs en ont vraiment besoin, ou simplement l’éliminer si ce n’est pas le cas.
    -   **Remplacez \<item\> par l’élément spécifique.** Par exemple, ne plus afficher ce rappel. Quand vous faites référence à une boîte de dialogue en général, utilisez ne plus afficher ce message.
    -   **Indiquez clairement quand l’entrée utilisateur sera utilisée pour les futures valeurs par défaut** en ajoutant la phrase suivante sous l’option : vos sélections seront utilisées par défaut à l’avenir.
    -   **Ne sélectionnez pas l’option par défaut. Si la boîte de dialogue ne doit être affichée qu’une seule fois, faites-le sans demander.** N’utilisez pas cette option comme excuse pour importuner les utilisateurs ; Assurez-vous que le comportement par défaut n’est pas ennuyeux.
    -   **Si les utilisateurs sélectionnent l’option et cliquent sur Annuler, cette option n’est pas prise en compte.** Ce paramètre est une méta-option, donc il ne suit pas le comportement d’annulation standard qui ne laisse aucun effet secondaire. Notez que si les utilisateurs ne souhaitent pas voir la boîte de dialogue à l’avenir, ils veulent également l’annuler.
-   **Liens**
    -   **N’attribuez pas** de [clé d’accès](glossary.md). Les liens sont accessibles à l’aide de la touche Tab.
    -   **N’ajoutez pas « Click » ou « cliquez ici » au texte du lien.** Cela n’est pas nécessaire, car un lien implique un clic.
-   **Info-bulles**
    -   **Utilisez des info-bulles pour fournir des étiquettes pour les contrôles sans étiquette.** Vous n’avez pas besoin de fournir des info-bulles de contrôles étiquetés simplement pour des raisons de cohérence.
    -   **Les info-bulles peuvent également fournir des détails supplémentaires sur les boutons de la barre d’outils étiquetés si cela s’avère utile.** Ne vous contentez pas de répéter ou de repasser un mot de ce qui figure déjà dans l’étiquette.
    -   **Évitez de couvrir l’objet avec lequel l’utilisateur est sur le ou l’utilisateur d’interagir.** Placez toujours le Conseil sur le côté de l’objet, même si cela nécessite une séparation entre le pointeur et l’info-bulle. Une séparation n’est pas un problème tant que la relation entre l’objet et son info-bulle est claire.
        -   **Exception :** Info-bulles de nom complet utilisés dans les listes et les arborescences.
    -   **Pour les collections d’éléments, évitez de couvrir l’objet suivant que l’utilisateur est susceptible d’afficher ou d’interagir avec.** Pour les éléments disposés horizontalement, évitez de placer des conseils à droite ; pour les éléments organisés verticalement, évitez de placer des conseils ci-dessous.
-   **Affichage progressif**
    -   **Utilisez plus ou moins de boutons de divulgation progressive pour masquer les options avancées ou rarement utilisées, les commandes et les détails dont les utilisateurs n’ont généralement pas besoin.** Ne masquez pas les éléments couramment utilisés, car les utilisateurs ne les trouveront peut-être pas. Mais vérifiez que ce qui est masqué a une valeur.
    -   Si la surface affiche toujours des options, des commandes ou des détails, utilisez les paires d’étiquettes suivantes :
        -   **Plus ou moins d’options.** Utilisez pour les options ou un mélange d’options, de commandes et de détails.
        -   **Plus ou moins de commandes.** Utilisez uniquement pour les commandes.
        -   **Plus ou moins de détails.** À utiliser pour plus d’informations uniquement.
        -   **Plus ou moins \<object name\> .** Utilisez pour d’autres types d’objets, tels que les dossiers.
    -   Sinon :
        -   **Options d’affichage/de masquage.** Utilisez pour les options ou un mélange d’options, de commandes et de détails.
        -   **Afficher/masquer les commandes.** Utilisez uniquement pour les commandes.
        -   **Afficher/masquer les détails.** À utiliser pour plus d’informations uniquement.
        -   **Afficher/masquer \<object name\> .** Utilisez pour d’autres types d’objets, tels que les dossiers.
-   **Barres de progression**
    -   **Utilisez les barres de progression de la désachèvement pour les opérations qui requièrent un laps de temps limité,** même si cette durée ne peut pas être prédite avec précision. Les barres de progression indéterminées indiquent que la progression est effectuée, mais ne fournit aucune autre information. Ne choisissez pas une barre de progression indéterminée uniquement en fonction du manque de précision possible uniquement.
    -   **Indiquez une estimation du temps restant si vous pouvez le faire correctement.** Les estimations de temps restantes qui sont exactes sont utiles, mais les estimations qui sont en dehors de la marque ou du rebond autour ne sont pas utiles. Vous devrez peut-être effectuer un traitement avant de pouvoir fournir des estimations précises. Dans ce cas, n’affichez pas d’estimations potentiellement inexactes au cours de cette période initiale.
    -   **Ne pas redémarrer la progression.** Une barre de progression perd sa valeur si elle redémarre (peut-être parce qu’une étape de l’opération se termine), car les utilisateurs n’ont aucun moyen de savoir à quel moment l’opération se termine. Au lieu de cela, vous devez faire en sorte que toutes les étapes de l’opération partagent une partie de la progression et que la barre de progression passe à l’achèvement une fois.
    -   **Fournissez des détails de progression utiles.** Fournissez des informations de progression supplémentaires, mais uniquement si les utilisateurs peuvent en faire une autre. Assurez-vous que le texte s’affiche suffisamment longtemps pour permettre aux utilisateurs de le lire.
    -   **Ne combinez pas une barre de progression à un pointeur occupé.** Utilisez l’un ou l’autre, mais pas les deux à la fois.
-   **Invites**
    -   **Utilisez une invite lorsque l’espace à l’écran est d’une qualité telle que l’utilisation d’une étiquette ou d’une instruction n’est pas souhaitable,** par exemple dans une barre d’outils.
    -   **L’invite est principalement destinée à identifier l’objectif de la zone de texte ou de la zone de liste déroulante de manière compacte.** Il ne doit pas s’agir d’informations essentielles que l’utilisateur doit voir lors de l’utilisation du contrôle.
    -   **Le texte de l’invite ne doit pas être confondu avec du texte réel.** Pour ce faire :
        -   Dessinez le texte de l’invite en italique gris et le texte d’entrée réel en noir latin.
        -   Le texte de l’invite ne doit pas être modifiable et doit disparaître une fois que les utilisateurs cliquent dans ou sur l’onglet dans la zone de texte.
            -   **Exception :** Si la zone de texte a le focus d’entrée par défaut, l’invite s’affiche et disparaît lorsque l’utilisateur commence à taper.
    -   N’utilisez pas de ponctuation de fin ni de points de suspension.
-   **Notifications**
    -   **Utilisez les notifications pour les événements qui ne sont pas liés à l’activité de l’utilisateur actuel, ne nécessitent pas d’action immédiate de l’utilisateur, et les utilisateurs peuvent librement ignorer.**
    -   **Ne pas abuser des notifications :**
        -   **Utilisez les notifications uniquement si vous en avez besoin.** Lorsque vous affichez une notification, vous pouvez potentiellement interrompre les utilisateurs ou même les ennuyeux. Assurez-vous que l’interruption est justifiée.
        -   **Utilisez des notifications pour les événements non critiques ou les situations qui ne nécessitent pas d’action immédiate de l’utilisateur.** Pour les événements critiques ou les situations qui nécessitent une action immédiate de l’utilisateur, utilisez un autre élément d’interface utilisateur (par exemple, une boîte de dialogue modale).
        -   **N’utilisez pas de notifications pour les publications de fonctionnalités !**

## <a name="keyboard"></a>Clavier

-   **Affectez le focus d’entrée initial au contrôle que les utilisateurs sont le plus susceptibles d’interagir avec en premier,** ce qui est souvent le premier contrôle interactif. Si le premier contrôle interactif n’est pas un bon choix, envisagez de modifier la disposition de la fenêtre.
-   **Affectez des taquets de tabulation à tous les contrôles interactifs, y compris les zones d’édition en lecture seule. Exceptions**
    -   Groupes de contrôles connexes qui se comportent comme un seul contrôle, tel que les cases d’option. De tels groupes comportent un seul taquet de tabulation.
    -   Contiennent correctement des groupes afin que les touches de direction recyclent vers l’avant et vers l’arrière dans le groupe et restent dans le groupe.
-   **L’ordre de tabulation doit s’écouler de gauche à droite, de haut en bas.** En général, l’ordre de tabulation doit suivre l’ordre de lecture. Envisagez de faire des exceptions pour les contrôles couramment utilisés en les plaçant plus tôt dans l’ordre de tabulation. L’onglet doit parcourir tous les taquets de tabulation dans les deux directions sans s’arrêter. Dans un groupe, l’ordre de tabulation doit être dans l’ordre séquentiel, sans exceptions.
-   **Dans un taquet de tabulation, l’ordre des touches de direction doit s’écouler de gauche à droite, de haut en bas,** sans exceptions. Les touches de direction doivent parcourir tous les éléments dans les deux directions sans s’arrêter.
-   **Présentez les boutons de validation dans l’ordre suivant :**
    -   OK/ \[ do it \] /Yes
    -   \[Ne le faites pas \] /non
    -   Annuler
    -   Appliquer (le cas échéant)

\[le cas échéant \] , \[ il \] s’agit de réponses spécifiques à l’instruction principale.

-   **Ne confondez pas les touches d’accès rapide avec les touches de raccourci.** Bien que les touches d’accès rapide et les touches de raccourci fournissent un accès clavier à l’interface utilisateur, elles ont des objectifs et des instructions différents.
-   **Dans la mesure du possible, assignez des clés d’accès uniques à tous les contrôles interactifs ou à leurs étiquettes.** Les [zones de texte en lecture seule](ctrl-text-boxes.md) sont des contrôles interactifs (dans la mesure où les utilisateurs peuvent les faire défiler et copier du texte). ils bénéficient donc des clés d’accès. **N’affectez pas de clés d’accès à :**
    -   Boutons OK, annuler et fermer. Enter et ESC sont utilisés pour leurs clés d’accès. Toutefois, attribuez toujours une clé d’accès à un contrôle qui signifie OK ou annuler, mais qui a une étiquette différente.
-   **Assignez des touches de raccourci aux commandes les plus couramment utilisées.** Les programmes et fonctionnalités rarement utilisés n’ont pas besoin de touches de raccourci, car les utilisateurs peuvent utiliser des clés d’accès à la place.
-   **Ne définissez pas une touche de raccourci comme seule façon d’effectuer une tâche.** Les utilisateurs doivent également être en mesure d’utiliser la souris ou le clavier avec la touche de tabulation, la flèche et les touches d’accès.
-   **N’affectez pas des significations différentes à des touches de raccourci connues.** Étant donné qu’elles sont mémorisées, les significations incohérentes des raccourcis bien connus sont frustrantes et sujettes aux erreurs.
-   **N’essayez pas d’affecter des touches de raccourci de programme à l’ensemble du système.** Les touches de raccourci de votre programme ne seront effectives que si votre programme a le focus d’entrée.

## <a name="mouse"></a>Souris

-   **Ne demandez jamais aux utilisateurs de cliquer sur un objet pour déterminer s’il est cliquable.** Les utilisateurs doivent être en mesure de déterminer la possibilité de clic par le biais de l’inspection visuelle seule.
    -   L’interface utilisateur principale (comme les boutons de validation) doit avoir une offre de clic statique. Les utilisateurs ne doivent pas avoir à POINTER pour découvrir l’interface utilisateur principale.
    -   L’interface utilisateur secondaire (par exemple, les commandes secondaires ou les contrôles de divulgation progressive) peut afficher sa possibilité de clic au pointage.
    -   Les liens de texte doivent suggérer statiquement du texte de lien, puis afficher leur caractère de clic (souligné ou autre changement de présentation, à l’aide d’un pointeur en forme de main) au pointage.
    -   Les liens graphiques affichent uniquement un pointeur vers la main au pointage.
-   **Utilisez le pointeur main (ou « Link Select ») uniquement pour les liens textuels et de texte.** Dans le cas contraire, les utilisateurs doivent cliquer sur les objets pour déterminer s’ils sont des liens.

## <a name="dialog-boxes"></a>Boîtes de dialogue

-   **Les boîtes de dialogue modales nécessitant une interaction, utilisez-les pour les éléments auxquels les utilisateurs doivent répondre avant de poursuivre leur tâche.** Assurez-vous que l’interruption est justifiée, par exemple pour des tâches uniques critiques ou peu fréquentes qui requièrent l’achèvement. Sinon, envisagez des alternatives non modales.
-   **Les boîtes de dialogue non modales ne nécessitent pas d’interaction. vous devez donc les utiliser lorsque les utilisateurs doivent basculer entre une boîte de dialogue et la fenêtre propriétaire.** Elles sont préférables pour les tâches fréquentes, répétitives ou en cours. Toutefois, les rubans, les barres d’outils et les fenêtres de palette sont souvent de meilleures solutions.

## <a name="property-sheets"></a>Feuilles de propriétés

-   **Vérifiez que les propriétés sont nécessaires.** N’encombrez pas vos pages de propriétés avec des propriétés inutiles simplement pour éviter de prendre des décisions de conception matérielle.
-   **Présenter les propriétés en termes d’objectifs d’utilisateur plutôt que de technologie.** La seule raison pour laquelle une propriété configure une technologie spécifique ne signifie pas que vous devez présenter la propriété en ce qui concerne cette technologie.
    -   Si vous devez présenter des paramètres en termes de technologie (peut-être parce que vos utilisateurs reconnaissent le nom de la technologie), incluez une brève description de l’avantage de l’utilisateur.
-   **Utilisez des étiquettes d’onglet explicites et explicites.** évitez les étiquettes d’onglet génériques qui peuvent s’appliquer à n’importe quel onglet, tel que général, avancé ou Paramètres.
-   **Évitez les pages générales.** Vous n’êtes pas obligé de disposer d’une page générale. Utilisez une page générale uniquement si :
    -   Les propriétés s’appliquent à plusieurs tâches et sont significatives pour la plupart des utilisateurs. Ne placez pas de propriétés spécialisées ou avancées sur une page général, mais vous pouvez les rendre accessibles via un bouton de commande sur la page général.
    -   Les propriétés ne correspondent pas à une catégorie plus spécifique. Si c’est le cas, utilisez plutôt ce nom pour la page.
-   **Évitez les pages avancées.** Utilisez une page avancée uniquement si :
    -   Les propriétés s’appliquent aux tâches rares et sont particulièrement explicites pour les utilisateurs expérimentés.
    -   Les propriétés ne correspondent pas à une catégorie plus spécifique. Si c’est le cas, utilisez plutôt ce nom pour la page.
-   **N’utilisez pas d’onglets si une fenêtre de propriétés n’a qu’un seul onglet et n’est pas extensible.** Utilisez une boîte de dialogue standard avec OK, annuler et un bouton appliquer facultatif à la place. Toutefois, les fenêtres de propriétés extensibles (qui peuvent être étendues par des tiers) doivent utiliser des onglets.

## <a name="wizards"></a>Assistants

-   **Envisagez d’abord les alternatives légères, telles que les boîtes de dialogue, les volets de tâches ou les pages uniques.** Les assistants sont une interface utilisateur lourde, mieux utilisée pour les tâches à plusieurs étapes, peu fréquentes. Vous n’avez pas besoin d’utiliser les assistants. vous pouvez fournir des informations et de l’aide utiles dans toutes les interfaces utilisateur.
-   **Utilisez Next uniquement lorsque vous avancez jusqu’à la page suivante sans engagement.** L’avancement jusqu’à la page suivante est considéré comme un engagement quand son effet ne peut pas être annulé en cliquant sur précédent ou annuler.
-   **Utilisez l’arrière-plan uniquement pour corriger les erreurs.** Hormis les erreurs de correction, les utilisateurs ne doivent pas cliquer sur précédent pour progresser dans une tâche.
-   **lorsque les utilisateurs s’engagent sur une tâche, utilisez un bouton de validation qui est une réponse spécifique à l’instruction principale (par exemple, imprimer, Connecter ou démarrer).** N’utilisez pas d’étiquettes génériques comme Next (qui n’implique pas engagement) ou terminer (qui n’est pas spécifique) pour la validation d’une tâche. Les étiquettes sur ces boutons de validation doivent être logiques. Démarrez toujours les étiquettes de bouton de validation avec un verbe. **Exceptions :**
    -   Utilisez terminer lorsque les réponses spécifiques sont toujours génériques, telles que enregistrer, sélectionner, choisir ou récupérer.
    -   Utilisez terminer pour modifier un paramètre spécifique ou une collection de paramètres.
-   **Utilisez des liens de commande uniquement pour les choix, pas pour les engagements.** Les boutons de validation spécifiques indiquent un engagement bien supérieur à celui des liens de commande dans un Assistant.
-   **Quand vous utilisez des liens de commande, masquez le bouton suivant, mais laissez le bouton Annuler.**
-   **Utilisez la touche Fermer pour Follow-Up et les pages de saisie semi-automatique.** N’utilisez pas annuler, car la fermeture de la fenêtre n’abandonne pas les modifications ou les actions effectuées à ce stade. N’utilisez pas Done, car il ne s’agit pas d’un verbe impératif.
-   **N’utilisez pas « Wizard » dans les noms d’Assistant.** par exemple, utilisez « Connecter à un réseau » au lieu de « assistant installation réseau ». Toutefois, il est acceptable de faire référence aux assistants en tant qu’assistants. par exemple : « si vous configurez un réseau pour la première fois, vous pouvez obtenir de l’aide à l’aide de l’Connecter à un assistant réseau ».
-   **Conserver les sélections de l’utilisateur via la navigation.** Par exemple, si l’utilisateur apporte des modifications, clique sur précédent, puis sur suivant, ces modifications doivent être conservées. Les utilisateurs ne sont pas censés devoir réentrer les modifications, sauf s’ils ont explicitement choisi de les effacer.

## <a name="wizard-pages"></a>Pages de l’assistant

-   **Concentrez-vous sur la prise de décision efficace.** Réduisez le nombre de pages pour vous concentrer sur Essentials. Consolidez les pages associées et prenez les pages facultatives du circuit principal. Le fait de faire en sorte que les utilisateurs cliquent sur suivant dans votre Assistant peut paraître une bonne expérience dans un premier temps, mais si les utilisateurs n’ont jamais besoin de modifier les paramètres par défaut, les pages sont probablement inutiles.
-   **N’utilisez pas les pages d’accueil. rendez la première page fonctionnelle chaque fois que possible.** Utilisez une page Prise en main facultative uniquement lorsque :
    -   L’Assistant a des conditions préalables nécessaires pour terminer correctement l’Assistant.
    -   Les utilisateurs ne comprennent peut-être pas l’objectif de l’Assistant en fonction de sa première page de choix, et il n’y a pas d’espace pour obtenir une explication supplémentaire.
    -   L’instruction principale pour Prise en main pages est « avant de commencer : ».
-   **Sur les pages dans lesquelles les utilisateurs sont invités à faire des choix, optimisez les cas les plus probables.** Ces types de pages doivent présenter des choix réels, pas seulement des instructions.
    -   Si vous n’utilisez pas de page Prise en main, Expliquez l’objectif de l’Assistant en haut de la première page de choix.
-   **Utilisez les pages de validation pour clarifier la tâche lorsque les utilisateurs effectuent la validation.** En règle générale, la page de validation est la dernière page de choix et le bouton suivant est à nouveau labellisé pour indiquer la tâche en cours de validation.
    -   N’utilisez pas les pages de résumé qui résument simplement les sélections précédentes de l’utilisateur, à moins que la tâche soit risquée (impliquant la sécurité ou la perte de temps ou de l’argent), ou qu’il y a de bonnes chances que les utilisateurs ne comprennent pas leurs sélections et qu’ils aient besoin de les passer en revue.
-   **N’utilisez pas les pages de félicitations qui ne font rien, mais qui terminent l’Assistant.** Si les résultats de l’Assistant sont clairement évidents pour les utilisateurs, fermez simplement l’Assistant sur le bouton validation finale.
    -   Utilisez Follow-Up pages lorsqu’il existe des tâches associées que les utilisateurs sont susceptibles de faire comme suivi. Évitez les tâches de suivi familières, telles que « envoyer un message électronique ».
    -   Utilisez les pages de saisie semi-automatique uniquement lorsque les résultats ne sont pas visibles et qu’il n’existe pas de meilleure façon de fournir des commentaires pour l’achèvement des tâches.
    -   Les assistants qui contiennent des pages de progression doivent utiliser une page de fin ou une page de Follow-Up pour indiquer l’achèvement des tâches. Pour les tâches de longue durée, fermez l’Assistant sur la page valider et utilisez les notifications pour envoyer vos commentaires.

## <a name="error-messages"></a>Messages d’erreur

-   **N’attribuez pas de messages d’erreur lorsque les utilisateurs ne sont pas susceptibles d’effectuer une action ou de modifier leur comportement** en tant que résultat du message. S’il n’y a aucune action que les utilisateurs peuvent effectuer, ou si le problème n’est pas significatif, supprimez le message d’erreur.
-   **Dans la mesure du possible, proposez une solution afin que les utilisateurs puissent résoudre le problème.** Toutefois, assurez-vous que la solution proposée est susceptible de résoudre le problème. Ne gaspillez pas le temps des utilisateurs en suggérant des solutions possibles, mais improbables.
-   **Être spécifiques.** Évitez les formulations vagues, telles que l’erreur de syntaxe et l’opération illégale. Fournissez des noms, des emplacements et des valeurs spécifiques des objets concernés.
-   **N’utilisez pas de formulation qui est responsable de l’utilisateur ou qui implique une erreur de l’utilisateur.** Évitez d’utiliser vous et votre dans la formulation. Alors que la voix active est généralement préférée, utilisez la voix passive lorsque l’utilisateur est l’objet et peut-être être responsable de l’erreur si la voix active a été utilisée.
-   **N’utilisez pas OK pour les messages d’erreur.** Les utilisateurs n’affichent pas les erreurs comme OK. Si le message d’erreur n’a pas d’action directe, utilisez plutôt fermer.
-   **N’utilisez pas les mots suivants :**
    -   Erreur, échec (utilisez à la place le problème)
    -   Échec de (utilisation impossible à la place)
    -   Non conforme, non valide, incorrect (utilisation incorrecte ou non valide à la place)
    -   Abandonner, arrêter, terminer (utilisez plutôt Stop)
    -   Catastrophique, fatale (utilisation grave à la place)

Ces termes sont inutiles et contraires au ton encourageant de Windows. Au lieu de cela, une icône d’erreur, lorsqu’elle est [utilisée correctement](vis-std-icons.md), communique suffisamment pour signaler un problème.

-   **Ne pas accompagner les messages d’erreur avec des effets sonores.** Cela est transférerez et inutile.

## <a name="warning-messages"></a>Messages d’avertissement

-   **Les avertissements décrivent une condition susceptible de provoquer un problème à l’avenir.** Les avertissements ne sont pas des erreurs ou des questions. par conséquent, n’utilisez pas les questions de routine comme avertissements.
-   **Ne fournissez pas de messages d’avertissement lorsque les utilisateurs ne sont pas susceptibles d’effectuer une action ou de modifier leur comportement en tant que résultat du message.** S’il n’y a aucune action que les utilisateurs peuvent effectuer, ou si la condition n’est pas significative, supprimez le message d’avertissement.

## <a name="confirmations"></a>Confirmations

-   **N’utilisez pas de confirmations inutiles.** Utilisez les confirmations uniquement lorsque :
    -   Il y a une bonne raison de ne pas continuer et un risque raisonnable, parfois pour les utilisateurs.
    -   L’action a des conséquences importantes ou ne peut pas être facilement annulée.
    -   L’action a des conséquences que les utilisateurs n’ont peut-être pas conscience.
    -   La poursuite de l’action oblige les utilisateurs à effectuer un choix qui n’a pas de valeur par défaut appropriée.
    -   Compte tenu du contexte actuel, les utilisateurs sont susceptibles d’avoir effectué une action erronée.
-   **La phrase est validée comme une question oui ou non, et vous fournissez oui ou aucune réponse.** Contrairement à d’autres types de boîtes de dialogue, les confirmations sont conçues pour empêcher les utilisateurs de prendre des décisions rapides. Si les utilisateurs n’ont pas pensé à leur réponse, une confirmation n’a pas de valeur.

## <a name="icons"></a>Icônes

-   **Toutes les icônes doivent respecter les règles d’icône de** [style Aero](vis-icons.md). remplacez tous les Windows les icônes de style XP.
-   **Choisissez les icônes standard en fonction de leur type de message, et non pas de la gravité du problème sous-jacent :**
    -   **Erreurs.** Une erreur ou un problème qui s’est produit.
    -   **Tres.** Condition susceptible de provoquer un problème à l’avenir.
    -   **Informations.** Informations utiles.

Si un problème combine différents types de messages, concentrez-vous sur l’aspect le plus important sur lequel les utilisateurs doivent agir.

-   **Les icônes doivent toujours correspondre à l’instruction principale ou à un autre texte correspondant.**
-   **Les icônes d’erreur ne sont pas nécessaires pour les problèmes d’entrée d’utilisateur non critiques.** Toutefois, les icônes sont nécessaires pour les erreurs sur place, car dans le cas contraire, ces commentaires contextuels seraient trop faciles à oublier.
-   **N’utilisez pas les icônes d’avertissement pour « atténuer » les erreurs non critiques.** Les erreurs ne sont pas des avertissements ; Appliquez les règles de l’icône d’erreur à la place.
-   **Pour les boîtes de dialogue de question, utilisez des icônes d’avertissement uniquement pour les questions ayant des conséquences importantes.** N’utilisez pas d’icônes d’avertissement pour les questions de routine.

## <a name="help"></a>Aide

-   **Lien vers des rubriques d’aide spécifiques pertinentes.** N’êtes pas lié à la page d’aide, à la table des matières, à une liste de résultats de recherche ou à une page qui se contente de créer des liens vers d’autres pages. Évitez d’établir une liaison avec les pages structurées sous la forme d’une grande liste de questions fréquemment posées, car elle oblige les utilisateurs à rechercher celle qui correspond au lien sur lequel ils ont cliqué. N’hésitez pas à créer des liens vers des rubriques d’aide spécifiques qui ne sont pas pertinentes et utiles pour la tâche en cours. Ne liez jamais des pages vides.
-   **Ne placez pas de liens d’aide sur chaque fenêtre ou page pour des raisons de cohérence.** Le fait de fournir un lien d’aide dans un même emplacement ne signifie pas que vous devez les fournir partout.
-   **Dans la mesure du possible, l’aide sur les expressions lie le texte en termes de question principale à la réponse du contenu de l’aide.** N’utilisez pas la formulation « en savoir plus sur » ou « obtenir de l’aide pour cela ».
-   **Utilisez le lien d’aide complet pour le texte du lien,** pas seulement les mots clés.
-   **Utilisez des phrases complètes.**
-   **N’utilisez pas de ponctuation ou d’ellipses de fin, sauf pour les points d’interrogation.**
-   **Si le contenu de l’aide est en ligne, désactivez-le dans le texte du lien.** Cela permet de prédire le résultat des liens.


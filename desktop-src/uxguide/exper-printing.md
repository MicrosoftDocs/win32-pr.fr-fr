---
title: Impression (notions de base de la conception)
description: L’impression est l’expérience utilisateur sur papier. C’est facile à ignorer, mais il s’agit d’une partie importante de l’expérience utilisateur globale.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104549976"
---
# <a name="printing-design-basics"></a>Impression (notions de base de la conception)

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

L’impression est l’expérience utilisateur sur papier. C’est facile à ignorer, mais il s’agit d’une partie importante de l’expérience utilisateur globale.

Dans cet article, l' *impression* fait référence à l’expérience utilisateur sur papier, où la sortie est dirigée vers le papier au lieu de l’affichage à l’écran. Le *format convivial* de l’imprimante fait référence aux modifications que le programme peut apporter à l’écran de sortie, ce qui le rend plus adapté à la sortie papier.

Malgré la prédiction que le calcul aurait abouti à un « bureau sans papier », étonnamment assez, nous imprimons maintenant autant que jamais. Nous distribuons des copies papier des jeux de présentation Microsoft PowerPoint, nous imprimons des articles que nous détectons en ligne, mais souhaitons effectuer des recherches plus attentivement ultérieurement, nous imprimons des messages électroniques importants ou des CV que nous avons reçus sous forme électronique, etc. Bien qu’il soit facile de négliger l’impression lors de la conception d’une interface utilisateur, n’oubliez pas que l’impression est une partie importante de l’expérience utilisateur globale.

**Remarque :** Les instructions relatives aux [boîtes de dialogue courantes](win-common-dlg.md) sont présentées dans un article distinct.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour déterminer si votre programme doit prendre en charge l’impression, posez-vous les questions suivantes :

-   **Quel est le type de programme que vous concevez ?** Le type de programme est un bon indicateur du niveau approprié de prise en charge de l’impression. La création, l’affichage et la navigation de documents et d’images nécessitent une excellente prise en charge de l’impression, tandis que d’autres types de programmes peuvent uniquement nécessiter une prise en charge de l’impression à un degré moindre. (Pour obtenir la liste des types de programmes, consultez la section [modèles d’impression](#printing-patterns) de cet article.)
-   **Le programme est-il utilisé dans les scénarios qui tirent parti de la sortie papier directe ?** Dans ce cas, il est plus pratique d’ajouter la prise en charge de l’impression à votre programme que d’exiger que les utilisateurs copient les données vers un autre programme à imprimer.

## <a name="design-concepts"></a>Principes de conception

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Concevoir votre programme pour éliminer toute impression inutile

Il existe de nombreuses raisons pour lesquelles les utilisateurs doivent imprimer d’autres, dont certains sont moins nombreux. Les utilisateurs doivent imprimer parce qu’ils le souhaitent, pas parce qu’ils le doivent. Demander aux utilisateurs d’imprimer peut être un signe de fonctionnalités manquantes. Par exemple, dans les anciens utilisateurs devaient imprimer des documents pour formuler des commentaires et suggérer des révisions, mais les utilisateurs peuvent désormais effectuer ces tâches directement dans les documents Microsoft Word. **Passez en revue les scénarios de votre programme qui impliquent l’impression et, dans la mesure du possible, assurez-vous que l’impression est facultative et non le résultat des fonctionnalités manquantes.**

Il est également intéressant de vous prévaloir que la conservation des ressources, comme le papier et l’encre, est utile et permet aux organisations de gagner de l’argent à long terme.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Comprendre les différences entre l’affichage et l’impression de l’écran

Bien qu’il existe de nombreuses similitudes entre la sortie d’affichage et l’impression, il existe de nombreuses différences. Sortie d’impression :

-   **A une résolution élevée.** L’affichage de la sortie est généralement à 96 ou 120 points par pouce (dpi), alors que la sortie de l’imprimante est généralement à 600 dpi ou plus.
-   **A des polices optimales différentes.** Bien que les polices bien conçues fonctionnent bien pour l’affichage et l’impression, les polices Serif sont plus lisibles avec des résolutions élevées pour de grandes quantités de texte que les polices sans serif. Ainsi, de grandes quantités de texte destinées principalement à l’impression doivent utiliser une police serif, tandis que le texte principalement destiné à l’affichage doit utiliser une police sans serif. Pour plus d’informations, consultez [polices](vis-fonts.md) (Segoe UI).
-   **A des proportions.** L’affichage présente généralement un [rapport hauteur](glossary.md) /largeur faible (4:3 ou 5:4), tandis que l’impression utilise un rapport hauteur/largeur élevé (8,5:11 ou 1:1.4142 en fonction des tailles de page standard). Cela est dû au fait que l’impression [en mode portrait](glossary.md) est plus courante que le [mode paysage](glossary.md).
-   **A des pages.** Par conséquent, la sortie d’impression :
    -   A des tailles de page standard. La norme dans le États-Unis et le Canada est le livre blanc de 8.5 « x11 ». la norme partout ailleurs est le papier A4.
    -   Contient des sauts de page.
    -   A des marges de page.
    -   Contient des en-têtes et des pieds de page.
    -   A une sortie simple ou recto-verso.
    -   Peut avoir plusieurs copies.
    -   Peuvent être imprimées dans le désordre ou de manière sélective.
-   **Offre de nombreuses options.** Les utilisateurs peuvent choisir une imprimante et un format de papier, des options d’imprimante (telles que la qualité d’impression, l’impression recto-verso et l’agrafage), le nombre de copies, les plages de pages, le classement et le format d’impression.
-   **Prend du temps et de l’argent.** L’impression d’un document volumineux ou d’une photo de haute qualité peut prendre beaucoup de temps, et le coût du papier et de l’encre augmente au fil du temps. En revanche, l’affichage de la sortie est instantané et essentiellement gratuit.
-   **Peut être noir et blanc.** Aujourd’hui, de nombreuses imprimantes sont noires et blanches, tandis que peu d’écrans sont monochromes.
-   **N’est pas interactif.** Les utilisateurs ne peuvent pas faire défiler des pages ou des contrôles pour afficher davantage de contenu. Ils ne peuvent pas cliquer sur les liens ou les boutons, ni pointer sur des contrôles. Le contenu interactif n’a pas de valeur à l’impression.
-   **Peut manquer de papier, d’encre ou de toner, ou être hors ligne.** Par conséquent, la sortie papier nécessite davantage de gestion des erreurs et de dépannage.

Ces différences peuvent affecter la conception de votre impression. La création d’une bonne expérience d’impression nécessite plus que de diriger la sortie de votre programme vers l’imprimante.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG et les exigences en constante évolution de l’affichage de l’écran

Historiquement, le principe le plus fondamental pour l’expérience utilisateur d’impression est connu sous le nom de WYSIWYG (« ce que vous voyez c’est ce que vous obtenez »). Ce principe suggère qu’il doit y avoir une relation forte entre ce qui apparaît sur l’écran et ce qui est imprimé. Avant que le WYSIWYG ne devienne une pratique standard, il n’existait souvent aucune relation entre les versions d’affichage et d’impression d’un document. Les utilisateurs devaient imprimer pour voir ce que le document a vraiment regardé sur papier. L’utilisation de WYSIWYG était une excellente amélioration de la productivité, car la plupart des programmes à ce moment étaient principalement conçus pour la création et l’impression de documents.

Aujourd’hui, il est courant que les sites Web optimisent l’affichage et que leur format convivial puisse paraître très différent. En outre, nous disposons de divers périphériques informatiques (par exemple, des téléphones intelligents et des assistants numériques personnels) qui nécessitent souvent une sortie optimisée pour des écrans de petite taille. Bien que l’approche WYSIWYG soit toujours la meilleure approche pour les programmes de création de documents, il est souvent plus judicieux de l’optimiser pour un large éventail d’appareils cibles. Pour ces programmes, ce que vous voyez sur un PC peut être différent de ce que vous voyez sur les autres appareils, ce qui peut être différent de ce que vous obtenez sur la page imprimée.

### <a name="optimize-for-printing"></a>Optimiser pour l’impression

Les programmes qui n’utilisent pas une expérience d’impression WYSIWYG stricte peuvent toujours s’optimiser pour l’impression des manières suivantes :

-   Reformater la disposition pour la taille de la page cible.
-   Fournissez un aperçu avant impression, avec des options de personnalisation simples permettant aux utilisateurs d’effectuer des expérimentations directement dans la boîte de dialogue d’impression (par exemple, en faisant glisser des marges).
-   Le cas échéant, fournissez une option de format compatible avec l’imprimante.
    -   Consolidez des documents partiels distincts en un seul document.
    -   Retirez les arrière-plans et les autres éléments de conception tels que les publicités, surtout s’ils ne sont pas adaptés pour une imprimante noir et blanc.
    -   Supprimer les éléments interactifs, tels que les contrôles de navigation et les boutons de commande.
    -   Assurez-vous que toutes les données sont visibles sans barre de défilement ou pointage.

        **Version d’affichage :**

        ![capture d’écran d’un rapport optimisé pour l’écran ](images/exper-printing-image1.png)

        **Version conviviale de l’imprimante :**

        ![capture d’écran du même rapport optimisé pour l’impression ](images/exper-printing-image2.png)

        Dans la version conviviale de l’imprimante, toutes les données sont visibles sur la page imprimée et les éléments interactifs sont supprimés.

    -   Remplacez les liens par leur équivalent textuel.

        **Acceptable:**

        Pour plus d’informations, consultez le Guide de l’expérience utilisateur.

        **Optimisé pour l’impression :**

        Pour plus d’informations, consultez le Guide de l’expérience utilisateur ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Convertit le texte clair sur un arrière-plan foncé en texte foncé sur un arrière-plan blanc.

### <a name="include-the-right-print-options"></a>Inclure les options d’impression appropriées

La boîte de dialogue Options d’impression courante fournit des options permettant d’effectuer les opérations suivantes :

-   Sélectionnez l’imprimante et le format du papier.
-   Définissez les propriétés de l’imprimante.
-   Sélectionnez la plage de pages, le nombre de copies et le classement.
-   Utilisez les deux côtés du papier.

Votre programme peut nécessiter des options supplémentaires, telles que les options de contenu du document (le contenu à imprimer), les options de mise en forme (comment imprimer, y compris la qualité d’impression, les tailles d’image, l’ajustement au frame) et les options de couleur. Si vous avez besoin de fournir des options supplémentaires, faites-le en étendant la boîte de dialogue commune options d’impression. Ne créez pas une boîte de dialogue d’impression personnalisée.

Lorsque vous concevez les options d’impression, tenez compte de l’expérience de l’impression de plusieurs documents. Il est probable que le travail d’impression suivant soit très similaire au dernier travail d’impression. Optimisez les paramètres par défaut pour les réimpressions et les travaux d’impression similaires. n’effectuez pas de redémarrage complet des utilisateurs à chaque fois.

### <a name="design-print-preview-for-performance-and-usability"></a>Conception de l’aperçu avant impression pour les performances et la convivialité

**Un travail d’impression incorrect gaspille du temps et de l’argent. Pour les programmes de création de document, les utilisateurs doivent être en mesure d’évaluer les résultats avant d’effectuer l’impression réelle.** Un aperçu avant impression doit permettre aux utilisateurs d’effectuer les opérations suivantes :

-   Évaluez les marges, les sauts de page, l’orientation des pages, les en-têtes et les pieds de page.
-   Parcourez toutes les pages.
-   Imprimer directement à partir de l’aperçu avant impression.

Certains documents complexes (tels que les dessins de conception assistée par ordinateur \[ \] ) peuvent prendre beaucoup de temps pour s’afficher. Les performances de la préversion sont importantes. un aperçu avant impression peut devenir assez fastidieux s’il faut un certain temps pour afficher chaque page. **Par conséquent, il est préférable de disposer d’un aperçu avant impression qui s’affiche rapidement et qui est suffisamment précis pour permettre aux utilisateurs d’évaluer les résultats d’impression plutôt que de disposer d’une préversion entièrement précise qui s’affiche lentement.**

Lors de la conception de l’aperçu avant impression, envisagez l’ensemble de la tâche de préparation à l’impression. Que les utilisateurs vont chercher ? Qu’est-ce qui va changer ? Les programmes de création de documents doivent fournir un aperçu interactif pour que les utilisateurs puissent ajuster les paramètres fréquemment modifiés tels que les marges et les sauts de ligne dans la version préliminaire.

Toutefois, dans la mesure du possible, votre programme doit faire la bonne chose par défaut. Quand cela est nécessaire, avertissez-vous des situations d’impression peu susceptibles d’être destinées à l’utilisateur. Ne vous fiez pas aux utilisateurs qui rencontrent des problèmes à l’aide de l’aperçu avant impression. Par exemple, supposons qu’une feuille de calcul comporte trop de colonnes à imprimer sur une seule page en mode portrait. Alors que le programme peut présenter une boîte de dialogue de confirmation, une meilleure solution consiste à imprimer automatiquement en mode paysage.

**Si vous ne faites que cinq choses...**

1.  Concevez une expérience d’impression adaptée à votre type de programme.
2.  Passez en revue les scénarios de votre programme qui impliquent l’impression et, dans la mesure du possible, rendez-vous obligatoire pour l’impression.
3.  Fournissez des extensions d’impression utiles en personnalisant la boîte de dialogue d’impression courante. Ne créez pas une boîte de dialogue d’impression personnalisée à cet effet.
4.  Optimisez les options d’impression pour les réimpressions et les travaux d’impression similaires.
5.  Fournissez une fonctionnalité en version préliminaire chaque fois que nécessaire.

## <a name="printing-patterns"></a>Modèles d’impression

Le type de programme est l’indicateur principal de l’expérience d’impression appropriée :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Création de documents avancée</strong><br/> Utilisé pour créer, afficher et imprimer des documents haut de gamme. La possibilité de créer des impressions de haute qualité est l’une des principales raisons pour lesquelles le programme existe. Destiné aux utilisateurs expérimentés. <br/></td>
<td><strong>Objectifs de l’utilisateur :</strong> Résultats parfait contrôle détaillé de la sortie de l’impression.<br/> <strong>Exemple :</strong> Microsoft Word<br/> <strong>Expérience d’impression recommandée :</strong><br/>
<ul>
<li>Sortie optimisée pour l’impression (WYSIWYG).</li>
<li>Fonctionnalités avancées de mise en forme des documents, avec des options pour imprimer des objets volumineux.</li>
<li>Options d’impression avancées, y compris les en-têtes et les pieds de page. Les options d’impression liées aux documents sont enregistrées dans le document lui-même.</li>
<li>Aperçus d’impression rapides, précis et puissants.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Création de documents intermédiaires</strong><br/> Utilisé pour créer et afficher des documents plus complexes. La possibilité de créer des impressions de bonne qualité est importante, mais pas nécessairement l’une des principales raisons pour lesquelles le programme existe. Destiné aux utilisateurs intermédiaires. <br/></td>
<td><strong>Objectifs de l’utilisateur :</strong> Bons résultats avec un minimum d’effort. Contrôle sur la sortie de l’impression.<br/> <strong>Exemples :</strong> La plupart des Microsoft Office programmes, tels qu’Outlook et Excel.<br/> <strong>Expérience d’impression recommandée :</strong><br/>
<ul>
<li>Sortie optimisée pour l’impression (WYSIWYG).</li>
<li>Certaines fonctionnalités de mise en forme du document, avec la possibilité d’imprimer des objets volumineux sans troncation.</li>
<li>Certaines options d’impression personnalisées, y compris les en-têtes et les pieds de page.</li>
<li>Aperçus d’impression précis et faciles à utiliser.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Création de documents simples</strong><br/> Utilisé pour créer et afficher des documents simples. Ciblé pour tous les utilisateurs. <br/></td>
<td><strong>Objectifs de l’utilisateur :</strong> Prise en charge de l’impression de base avec les options d’impression standard. Les utilisateurs s’attendent à obtenir de bons résultats sans peaufinage.<br/> <strong>Exemples :</strong> WordPad, Paint.<br/> <strong>Expérience d’impression recommandée :</strong><br/>
<ul>
<li>La sortie peut être optimisée pour l’impression (WYSIWYG), mais cela n’est pas obligatoire.</li>
<li>Certaines fonctionnalités de mise en forme du document, avec la possibilité d’imprimer des objets volumineux sans troncation.</li>
<li>Options d’impression standard ; les options d’impression personnalisées sont facultatives.</li>
<li>Aperçus d’impression simples ou inexistants.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Visionneuses de documents</strong><br/> Utilisé pour afficher des documents. Les utilisateurs ne peuvent pas modifier le contenu ou le format du document. <br/></td>
<td><strong>Objectifs de l’utilisateur :</strong> Prise en charge de l’impression de base avec les options d’impression standard. Les utilisateurs s’attendent à obtenir de bons résultats sans peaufinage. Les problèmes d’impression sont gérés automatiquement, car les utilisateurs ne peuvent pas modifier le document.<br/> <strong>Exemple :</strong> Windows Internet Explorer<br/> <strong>Expérience d’impression recommandée :</strong><br/>
<ul>
<li>La sortie peut être optimisée pour l’impression (WYSIWYG), mais cela n’est pas obligatoire.</li>
<li>Le programme gère automatiquement les sauts de page, élimine les pages vides, gère les objets volumineux et supprime les arrière-plans et d’autres éléments de conception.</li>
<li>Options d’impression standard ; les options d’impression personnalisées sont facultatives.</li>
<li>Aperçus d’impression simples ou inexistants.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Utilitaires ou applications métier</strong><br/> Utilisé pour effectuer des tâches simples et spécifiques. Ciblé pour tous les utilisateurs. <br/></td>
<td><strong>Objectifs de l’utilisateur :</strong> Possibilité d’exporter efficacement les données sélectionnées. Les utilisateurs s’attendent à obtenir de bons résultats sans peaufinage. Souvent, pour ces programmes, les utilisateurs sont agréablement surpris de trouver un support pour l’impression.<br/> <strong>Expérience d’impression recommandée :</strong><br/>
<ul>
<li>La prise en charge de l’impression est facultative selon les scénarios pris en charge.</li>
<li>La sortie peut être optimisée pour l’impression (WYSIWYG), mais cela n’est pas obligatoire.</li>
<li>Certaines fonctionnalités de mise en forme de document. Peut être acceptable si des objets volumineux sont tronqués.</li>
<li>Options d’impression standard.</li>
<li>Les aperçus d’impression sont facultatifs.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **N’imprimez pas les pages ou pages vierges avec des en-têtes et des pieds de page.** Toutefois, imprimez des pages vierges si les en-têtes ou les pieds de page contiennent des numéros de page et que ces numéros de page peuvent être référencés ailleurs.
-   **Met entièrement en file d’attente les travaux d’impression en attente avant l’arrêt d’un programme.**

### <a name="formatting-pages"></a>Mise en forme des pages

-   **Reformater la disposition du texte pour l’ajuster à la taille de la page cible.** Ne pas tronquer le texte.
-   Si les utilisateurs ne contrôlent pas le format du document :
    -   **Gérer automatiquement les objets volumineux en mettant à l’échelle, en faisant pivoter ou en fractionnant les pages.** Pour plus d’instructions sur l’impression d’objets volumineux, consultez [objets surdimensionnés](#oversized-objects).
    -   **Optimisez les sauts de page pour éliminer les pages vides et presque vides.**
    -   **Convertit le texte clair sur un arrière-plan foncé en texte foncé sur un arrière-plan blanc.**
    -   **Retirez les arrière-plans et les autres éléments de conception,** surtout s’ils ne sont pas adaptés pour une imprimante noir et blanc.
-   **Si votre programme présente des documents partiels distincts, fournissez une option de format compatible avec l’impression pour les consolider dans un document unique pour l’impression.**
-   **Supprimer les éléments interactifs :**
    -   Supprimer les contrôles de navigation et les boutons de commande.
    -   Assurez-vous que toutes les données sont visibles sans barre de défilement.
    -   Remplacez les liens par leur équivalent textuel.

        **Acceptable:**

        Pour plus d’informations, consultez le Guide de l’expérience utilisateur.

        **Optimisé pour l’impression :**

        Pour plus d’informations, consultez le Guide de l’expérience utilisateur ( https://msdn.microsoft.com/windowsvista/uxguide) .

        Dans cet exemple, le lien est remplacé par son équivalent texte entre parenthèses.

    -   Déplacez les informations utiles affichées au pointage sur Inline.

### <a name="oversized-objects"></a>Objets surdimensionnés

La gestion d’objets volumineux, tels que des feuilles de calcul, des graphiques et des photos, est un problème propre à l’impression. Choisissez l’une des approches suivantes :

-   **Mettez l’objet à l’échelle pour l’ajuster à la page.** Cette approche fonctionne bien si l’objet n’est que légèrement trop volumineux pour être imprimé, il est important de maintenir l’objet sur une seule page et l’objet est toujours lisible en cas de réduction de la taille des objets.

    ![capture d’écran de la photo mise à l’échelle jusqu’à la moitié d’une page ](images/exper-printing-image3.png)

    Dans cet exemple, la grande image est mise à l’échelle pour s’ajuster à la page.

-   **Faites pivoter la page.** Cette approche fonctionne bien lorsque quelques pages s’impriment mieux en mode paysage en mode Portrait (et vice versa).

    ![capture d’écran d’une photo paysage en mode portrait ](images/exper-printing-image4.png)

    Dans cet exemple, la grande image est pivotée pour s’adapter mieux à la page.

-   **Imprimez l’objet sur plusieurs pages.** L’approche fonctionne bien lorsque l’objet ne peut pas être mis à l’échelle, ou ne doit pas être mis à l’échelle, et la rotation de la page n’a pas d’aide ou n’est pas souhaitée. Si l’objet a des limites internes (telles que les séparateurs de colonne et de ligne dans une feuille de calcul), Rompez les pages sur ces limites plutôt que dans le contenu. De même, répétez tous les éléments requis pour comprendre la page, tels que les légendes ou les en-têtes de colonne. Lors du fractionnement d’un objet sur plusieurs pages, assignez les numéros de page dans l’ordre de lecture (de gauche à droite, de haut en bas).

    ![capture d’écran des têtes de colonne répétées sur la page suivante ](images/exper-printing-image5.png)

    Dans cet exemple, la table volumineuse est imprimée sur deux pages. Les en-têtes de colonnes sont conservés d’une page à l’autres pour faciliter la compréhension rapide.

-   **Tronque l’objet** (en imprimant uniquement la partie de l’objet toujours visible après troncation). Cette approche est la solution la plus simple à implémenter, mais probablement la moins acceptable. Notez également que la troncation n’est jamais acceptable pour le texte.

    ![capture d’écran de la moitié de la photo sur la page portrait ](images/exper-printing-image6.png)

    Dans cet exemple, la grande image est tronquée.

### <a name="headers-and-footers"></a>En-têtes et pieds de page

-   **Fournissez des en-têtes et des pieds de page pour les programmes de création de documents avancés et intermédiaires.** Envisagez de fournir des en-têtes et des pieds de page pour d’autres types de programmes s’ils sont utilisés pour les documents multipages.
-   **Personnalisez les en-têtes et les pieds de page.** Autorisez les utilisateurs à définir les parties gauche, centrale et droite.
    -   Pour les en-têtes, placez le nom du document sur le côté gauche par défaut.
    -   Pour les pieds de page, placez le copyright ou la source du document sur le côté gauche, et le numéro de la page sur le côté droit, par défaut.
-   **Utilisez le chemin d’accès convivial et les URL.** Affichez les espaces sous la forme d’espaces, et non pas « %20 ».

### <a name="print-commands"></a>Commandes d’impression

-   **Pour les menus contextuels et les barres de menus, utilisez la commande Imprimer qui affiche la boîte de dialogue commune options d’impression.** Utilisez des points de suspension pour indiquer que des informations supplémentaires sont requises.

    ![capture d’écran du menu fichier, commande Imprimer sélectionnée ](images/exper-printing-image7.png)

    Dans cet exemple, la commande Imprimer contient des points de suspension pour indiquer qu’elle affichera la boîte de dialogue Options d’impression commune pour obtenir plus d’informations.

-   **Pour les barres d’outils utilisées avec une barre de menus, utilisez une commande Imprimer immédiate.** En cliquant sur le bouton, vous imprimez une seule copie du document sur l’imprimante par défaut. Ces commandes de barre d’outils doivent être immédiates. Pour indiquer que la commande est immédiate, placez l’imprimante par défaut dans l’info-bulle. Les utilisateurs peuvent accéder à la commande impression complète à partir de la barre de menus.

    ![capture d’écran de l’icône d’imprimante et de son info-bulle ](images/exper-printing-image8.png)

    Dans cet exemple, la commande Imprimer dans une barre d’outils s’imprime immédiatement au lieu d’afficher la boîte de dialogue commune options d’impression. Le fait de placer l’imprimante par défaut dans l’info-bulle fournit un renforcement textuel que l’utilisateur ignore la boîte de dialogue.

-   **Pour les barres d’outils utilisées sans barre de menus, utilisez un bouton imprimer le fractionnement.** En cliquant sur le bouton, vous imprimez une seule copie du document sur l’imprimante par défaut. En cliquant sur la flèche du bouton, vous affichez un menu avec les commandes d’impression complète, d’aperçu avant impression et de mise en page.

    ![capture d’écran de l’icône d’imprimante sur le bouton partagé ](images/exper-printing-image9.png)

    Dans cet exemple, la barre d’outils Windows Internet Explorer utilise un contrôle bouton partagé pour fournir toutes les commandes d’impression.

-   **Pour l’interface utilisateur de commande du ruban, placez la commande Imprimer dans le menu de l’application.**

    ![capture d’écran des commandes placées verticalement à gauche ](images/exper-printing-image10.png)

    Pour les rubans, la commande Imprimer est accessible à l’aide du menu de l’application.

### <a name="print-options"></a>Options d’impression

-   **Ne créez pas une boîte de dialogue Options d’impression personnalisées.** Si vous devez fournir des options supplémentaires, étendez la boîte de dialogue commune options d’impression. N’utilisez pas de boîte de dialogue distincte pour les options d’impression supplémentaires.

**Incorrect :**

![capture d’écran de la boîte de dialogue Options d’impression personnalisées ](images/exper-printing-image11.png)

Dans cet exemple, Fabrikam utilise incorrectement un dialogue distinct pour les options d’impression supplémentaires.

**Développeurs :** Pour plus d’informations sur la façon d’étendre la boîte de dialogue d’impression commune, consultez [PRINTDLGEX structure](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Lors de l’extension de la boîte de dialogue commune options d’impression, ne dupliquez aucune des fonctionnalités déjà fournies.**
-   **Si les utilisateurs sont susceptibles de gérer les paramètres d’un travail d’impression à la suivante, définissez ces paramètres par défaut.** Pour le premier travail d’impression après le lancement du programme, utilisez les valeurs par défaut standard, y compris l’imprimante par défaut. Pour les travaux d’impression suivants dans l' [instance](glossary.md)de programme, conservez la dernière imprimante et le format de papier sélectionnés. Ne conservez pas le nombre de copies ou de plages de pages, car celles-ci sont beaucoup moins susceptibles d’être resélectionnées ultérieurement.
-   **Optimisez les paramètres en supprimant les options qui ne s’appliquent pas actuellement.** Supprimer les options qui ne sont pas cohérentes avec les fonctionnalités de l’imprimante sélectionnée ou les caractéristiques du document actif. Par exemple, une application d’impression photo peut limiter les combinaisons de format de papier, de type de papier et de qualité d’impression qui donnent les meilleurs résultats. par conséquent, le choix d’une option de papier glacé peut supprimer les enveloppes des formats papier. Si, pour une raison quelconque, les utilisateurs souhaitent voir toutes les options, vous pouvez fournir cette possibilité par le biais d’un contrôle tel qu’une case à cocher.

**Développeurs :** Pour savoir comment déterminer les fonctionnalités de l’imprimante sélectionnée, consultez [schéma d’impression](../printdocs/print-schema.md).

-   **Pour les programmes de création de documents avancés, enregistrez les options d’impression relatives aux documents dans le document lui-même.** Pour ces programmes, les options d’impression font partie intégrante du document.
-   **Pour les autres types de programmes, enregistrez les paramètres pour chaque utilisateur.**
-   **Envisagez de sélectionner une imprimante autre que celle par défaut pour l’impression spécialisée.** Par exemple, une application d’impression photo peut toujours sélectionner l’imprimante utilisée en dernier par le programme, quelle que soit l’imprimante système par défaut. Cela suppose que l’imprimante par défaut du système n’est probablement pas une imprimante photo. Ces programmes doivent enregistrer le paramètre de la dernière imprimante sélectionnée.
-   **Ne verrouillez pas votre programme lors de la détection des fonctionnalités de l’imprimante.** Cela présente une expérience utilisateur médiocre. Au lieu de cela, vous pouvez :
    -   Procédez à la détection des fonctionnalités de l’imprimante dans un thread séparé.
    -   Expiration après 10 secondes.
    -   Fournissez une boîte de dialogue pour permettre aux utilisateurs d’annuler.

![capture d’écran de la boîte de dialogue « Connexion à » ](images/exper-printing-image12.png)

Dans cet exemple, la boîte de dialogue permet d’annuler facilement la détection des fonctionnalités de l’imprimante si l’utilisateur décide que la tâche prend trop de temps.

### <a name="print-previews"></a>Imprimer les aperçus

-   **Fournissez une fonctionnalité d’aperçu avant impression chaque fois que nécessaire.** Tous les programmes de création de documents bénéficient des aperçus avant impression, mais les utilisateurs ne les attendent pas dans des programmes simples de création de documents. Pour les programmes de création de documents avancés, pensez à utiliser la prise en charge de l’aperçu avant impression directement dans la fenêtre principale du programme.

![capture d’écran de la page affichée en mode aperçu avant impression ](images/exper-printing-image13.png)

Dans cet exemple, Word prend en charge l’aperçu avant impression dans la fenêtre principale du programme.

-   Fournit des fonctionnalités d’aperçu avant impression qui permettent aux utilisateurs d’effectuer les opérations suivantes :
    -   Évaluez les marges, les sauts de page, l’orientation des pages, les en-têtes et les pieds de page.
    -   Parcourez toutes les pages.
    -   Imprimer directement à partir de l’aperçu avant impression.

Envisagez de fournir un aperçu interactif interactif afin que les utilisateurs puissent ajuster les paramètres fréquemment modifiés, tels que les marges et les sauts de ligne, directement dans la version préliminaire.

-   **Afficher les pages d’aperçu avant impression en une seconde.** Il est préférable de disposer d’un aperçu avant impression qui s’affiche rapidement et qui est suffisamment précis pour permettre aux utilisateurs d’évaluer les résultats de l’impression plutôt que de disposer d’une préversion entièrement précise qui s’affiche lentement.
-   **Pour les programmes de création de documents avancés, envisagez d’étendre la boîte de dialogue d’impression standard en incorporant la fonctionnalité en préversion directement dans celle-ci,** au lieu de créer une boîte de dialogue distincte pour celle-ci.
-   **Fournissez un bouton évident pour fermer le mode aperçu.**

![capture d’écran de l’icône et de l’étiquette de fermeture de l’aperçu avant impression ](images/exper-printing-image14.png)

Le mode aperçu avant impression dans Word a une commande fermer l’aperçu évidente.

### <a name="printing-errors"></a>Erreurs d’impression

**Remarque :** Une fois le travail d’impression mis en attente sur l’imprimante, Windows est responsable des erreurs suivantes. Votre programme doit uniquement gérer les erreurs qui se produisent avant que le travail d’impression ne soit mis en attente.

-   **Avant de spouler un travail d’impression, vérifiez les problèmes d’impression potentiels que l’utilisateur peut résoudre.** Une confirmation claire et concise avant de poursuivre l’impression. Dans la mesure du possible, offrez la possibilité de résoudre le problème automatiquement. Cela peut vous empêcher de perdre du temps et de l’argent.

## <a name="text"></a>Texte

-   Pour l’option d’impression sur les deux côtés du papier, étiquetez l’option imprimer recto-verso. N’utilisez pas l’expression duplex manuel.

## <a name="documentation"></a>Documentation

-   Utilisez l’impression, et non l’impression, en tant que verbe.
-   Il est acceptable d’utiliser PrintOut pour faire référence au résultat d’un travail d’impression.
-   Utilisez la file d’attente à l’impression et non l’imprimante.


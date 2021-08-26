---
title: Aide
description: Utilisez l’aide comme mécanisme secondaire pour aider les utilisateurs à se terminer et à mieux comprendre les tâches \ 8212 ; le mécanisme principal est l’interface utilisateur proprement dite. Appliquez ces instructions pour rendre le contenu véritablement utile et facile à trouver.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2a71abf4b90aeaf19f43997c5d8e98ad42f56d5daa86699ff8504ca5a3080bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935790"
---
# <a name="help"></a>Aide

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Utilisez l’aide comme mécanisme secondaire pour aider les utilisateurs à se terminer et mieux comprendre les tâches que le mécanisme principal est l’interface utilisateur. Appliquez ces instructions pour rendre le contenu véritablement utile et facile à trouver.

Un système d’aide est constitué de différents types de contenu conçus pour aider les utilisateurs lorsqu’ils ne parviennent pas à effectuer une tâche, à comprendre un concept plus en détail, ou à avoir besoin de plus de détails techniques que ceux disponibles dans l’interface utilisateur.

Dans cet article, nous faisons référence à l’aide comme secondaire de l’interface utilisateur. L’interface utilisateur est principale parce que c’est là que les utilisateurs essaient d’abord de résoudre leurs problèmes. Ils consultent le système d’aide uniquement s’ils ne peuvent pas accomplir leur tâche avec l’interface utilisateur.

![capture d’écran de la page aide et support Windows ](images/winenv-help-image1.png)

la page d’informations d’aide et de Support Windows, disponible dans le menu Démarrer.

**Remarque :** Les instructions relatives au [style et au ton](text-style-tone.md) sont présentées dans un article distinct.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **Quel est le degré de motivation de vos utilisateurs cibles ?** Plus ils sont particulièrement motivés pour découvrir les fonctionnalités de votre programme et devenir des utilisateurs intermédiaires ou même avancés de l’informatique, plus ils sont disposés à rechercher les réponses à leurs questions en consultant les rubriques d’aide.
-   **Utilisez-vous l’aide pour corriger une mauvaise interface utilisateur ?** Plus votre interface utilisateur est performante, moins les utilisateurs rechercheront de l’aide supplémentaire. Si votre programme a une interface utilisateur principale très claire et utile (par exemple, des messages d’erreur sans jargon, des assistants bien écrits et des boîtes de dialogue non ambiguës), vous n’aurez peut-être pas besoin d’un système d’aide secondaire.
-   **Votre programme est-il relativement simple ?** Dans ce cas, envisagez d’incorporer tout le contenu d’assistance nécessaire dans vos surfaces d’interface utilisateur principales. Les utilisateurs sont plus susceptibles de rechercher de l’aide supplémentaire dans les programmes qui effectuent des tâches complexes.
-   **Votre application est-elle destinée aux développeurs, aux professionnels de l’informatique ou à d’autres experts en logiciels ?** Ces utilisateurs ont tendance à s’attendre à une aide de référence pour les conventions de langage de programmation et une aide conceptuelle détaillée pour la maîtrise des fonctionnalités.

## <a name="design-concepts"></a>Principes de conception

Si vous décidez d’inclure l’aide dans votre programme, intégrez-la dans votre conception globale. L’interface d’aide doit être simple, efficace et pertinente. il doit permettre aux utilisateurs d’obtenir facilement de l’aide, puis de revenir à leur tâche. Pensez à votre système d’aide en termes de temps des utilisateurs : minimisez les interruptions en anticipant les endroits où ils rencontreront des problèmes dans votre programme, puis résolvez ces problèmes en incorporant l’assistance fondamentale directement dans votre interface utilisateur et en créant des points d’entrée clairs et cohérents dans votre aide plus détaillée.

Windows assistance a été conçue conformément à ces principes. voici quelques-unes des modifications apportées à la conception de l’expérience utilisateur d’aide Windows :

-   Plus de points d’entrée détectables pour l’aide de l’interface utilisateur principale (en particulier les nouveaux liens d’aide des surfaces de l’interface utilisateur, telles que les boîtes de dialogue, les messages d’erreur et les assistants). Les liens d’aide vous permettent d’accéder directement à la rubrique correspondante dans l’aide de.
-   Une icône de bouton d’aide est disponible dans le coin supérieur droit de la plupart des pages Hub du panneau de contrôle, ainsi que des dossiers Shell.
-   les utilisateurs peuvent choisir d’obtenir le contenu d’aide le plus à jour auprès de Windows aide et de Support en ligne lorsqu’ils sont en ligne.
-   Les rubriques d’aide sont maintenant basées sur les tâches plutôt que sur les fonctionnalités, afin que les utilisateurs puissent accomplir leurs tâches rapidement et efficacement.
-   Les rubriques d’aide sont à présent principalement basées sur des scénarios utilisateur connus.
-   Les rubriques d’aide sont plus souples [et informelles](text-style-tone.md), à l’aide d’un langage réaliste.
-   Les rubriques d’aide sont conçues pour une analyse efficace, car les utilisateurs lisent rarement le mot de contenu pour Word.

### <a name="an-analogy-for-help"></a>Une analogie pour l’aide

Pour en savoir plus sur la conception de votre système d’aide, pensez à une analogie de la vie quotidienne. Vous êtes perdu dans une ville inconnue. Que faire dans cette situation ? Un grand nombre réagirait comme suit :

-   Soyez orienté ; Recherchez des points de repère, des signes de rue (noms et pointeurs à des endroits).
-   Recherchez Maps.
-   Enfin, en dernier recours, demandez des instructions ou appelez un ami.

La conception de l' « interface » de la ville affecte le besoin d’assistance. Les rues bien étiquetées, les directions explicites (les pointeurs vers les hôpitaux, les aéroports, les musées et le Bureau de poste) et des points de vue clairs, tels que des caractéristiques géographiques importantes ou des bâtiments, vous aident à trouver votre chemin.

Vous demandez de l’aide en dernier recours. C’est une indication que la « interface » de la ville a échoué en étant mal conçue et confuse. Vous êtes plus susceptible de demander de l’aide sur un emplacement qui a une étiquette spécifique qui suggère une utilité. Par exemple, il est plus probable que vous souhaitiez demander de l’aide à un emplacement intitulé « directions » ou « informations » plutôt qu’un lieu général comme la salle de ville, bien que tout le monde puisse vous fournir des instructions.

Lorsque vous demandez de l’aide, il est probable que vous soyez frustré et que vous souhaitiez simplement accéder à la destination prévue. Vous n’êtes probablement pas à l’esprit pour passer du temps à effectuer une visite guidée de la ville ou à en apprendre davantage sur son histoire. En outre, votre motivation dépend de l’importance de la tâche. Si vous essayez de trouver votre chambre d’hôtel, vous allez faire tout ce qu’elle nécessite. Toutefois, si votre objectif est de trouver un lieu d’importance mineure, il vous suffira probablement d’abandonner au bout d’un petit effort.

Tous ces aspects de la recherche dans l’espace réel correspondent à la manière dont les utilisateurs se trouvent en général dans l’espace virtuel de votre programme. La recherche d’aide au-delà de l’interface utilisateur principale est le fait que sa nature est désorientée. faites de votre mieux pour atténuer une telle expérience grâce à une interface utilisateur bien conçue et des « signes de rue » intelligents pour diriger les utilisateurs vers les réponses dont ils ont besoin.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Conception de l’interface utilisateur pour que l’aide soit inutile

Essayez d’apporter de l’aide en premier lieu, en procédant comme suit :

-   Simplification de la découverte et de l’exécution des tâches courantes.
-   En fournissant [des instructions principales](text-ui.md)claires.
-   Fournir des étiquettes de contrôle claires et concises qui sont orientées objectif et orientées tâche.
-   Fournir des instructions supplémentaires et des explications si nécessaire.
-   Anticiper les problèmes évitables en utilisant des contrôles limités à des choix valides, en fournissant des valeurs par défaut appropriées, en gérant tous les formats d’entrée et en empêchant les erreurs.
-   Écriture de messages d’erreur qui fournissent une solution ou une action claire pour l’utilisateur.
-   Éviter les confusions de conceptions d’interface utilisateur, telles que les tâches avec un mauvais Workflow ou l’utilisation de contrôles qui sont désactivés sans raison apparente.
-   Travailler avec des rédacteurs et des éditeurs tôt dans le cycle de développement pour créer un texte de haute qualité et cohérent avec l' [interface utilisateur](text-ui.md) dans votre programme.

Les utilisateurs n’ont pas besoin d’aller ailleurs pour déterminer comment utiliser votre interface utilisateur. Ajoutez des informations essentielles directement dans l’interface utilisateur principale, plutôt que de forcer les utilisateurs à sortir de leur contexte immédiat et dans le volet d’aide. Si des informations importantes existent uniquement dans une rubrique d’aide, il est probable que les utilisateurs ne le voient pas. Pour obtenir des informations facultatives et plus explicatives, utilisez les liens d’aide de l’interface utilisateur principale vers la rubrique d’aide correspondante pour obtenir une assistance supplémentaire.

### <a name="considering-user-motivation"></a>Motivation de l’utilisateur

Pour la plupart des utilisateurs, la vitesse et l’efficacité font partie des principaux programmes. Les utilisateurs veulent faire leur travail. En règle générale, ils ne souhaitent pas en savoir plus sur le programme et la technologie pour ses propres besoins. leur patience s’étend uniquement dans la mesure où ce programme répond à leurs propres intérêts et résout les problèmes en cours.

Concevez votre système d’aide pour qu’il corresponde à la motivation de vos utilisateurs. Prenons l’exemple d’un utilisateur qui a été reporté sur un kiosque d’un musée. Si elle ne peut pas déterminer comment effectuer rapidement la tâche, elle est probablement simplement en déplacement. Il est peu probable que vous passiez du temps à utiliser l’aide. En guise d’alternative, un utilisateur fortement motivé a une tolérance supérieure pour le temps passé à rechercher des réponses dans votre système d’aide. Un utilisateur professionnel qui doit équilibrer les livres, par exemple, est probablement disposé à consulter le contenu de l’aide pour tirer le meilleur parti de cette nouvelle application comptable.

### <a name="writing-content-for-scanning"></a>Écriture de contenu pour l’analyse

Écrire des rubriques d’aide en sachant qu’elles seront analysées à la recherche d’informations spécifiques, et non de mots pour Word. Écrivez de façon concise, obtenez rapidement le point et fournissez des informations sur lesquelles les utilisateurs peuvent agir.

-   Écrivez des rubriques « Comment » en utilisant des étapes numérotées dans un format cohérent afin que les utilisateurs reconnaissent qu’ils obtiennent de l’aide procédurale.
-   Écrivez des rubriques de référence avec la facilité d’analyse à l’esprit, en utilisant des tables, par exemple, pour présenter les options d’interface utilisateur ou la syntaxe de langage.
-   Écrivez des rubriques conceptuelles qui sont organisées logiquement par sous-titres, afin que l’utilisateur puisse ignorer des sections entières de moindre intérêt.

Dans tout le contenu d’aide, il est plus facile d’analyser des listes à puces que des blocs de texte de paragraphe standard. Utilisez des listes à puces judicieusement, mais pas en tant que Crutch pour les documents non organisés.

### <a name="creating-content-that-matters"></a>Création de contenu important

Étant donné qu’aucun système d’aide ne peut anticiper chaque question que chaque utilisateur peut avoir, concentrez-vous sur la majeure partie du contenu pour répondre aux questions principales dans les principaux scénarios pour vos utilisateurs cibles. Par exemple, les recherches efficaces et l’établissement d’une connectivité réseau (entre autres) peuvent être des rubriques très sollicitées. En outre, concentrez-vous sur les tâches dans les principaux scénarios utilisateur, plutôt que de documenter une fonctionnalité ou une technologie de manière exhaustive.

**Conseil :** Le support technique est une bonne source de contenu d’aide. Les support technique conservent souvent des enregistrements de questions fréquemment posées sur des programmes ou des tâches que les utilisateurs tentent d’effectuer (et échouent).

Il n’est pas nécessaire de fournir de l’aide pour toutes les fonctionnalités de l’interface utilisateur. **Très souvent, il n’est pas utile d’obtenir de l’aide pour tenter de créer de l’aide pour tout.** Si l’interface utilisateur est bien conçue, la plupart de ces rubriques d’aide ne seront pas très utiles. ils restatent simplement ce qui est évident.

S’il existe plusieurs façons d’effectuer une tâche, dans la plupart des cas, vous pouvez simplement documenter la méthode la plus courante utilisée par les utilisateurs inexpérimentés. Les exceptions à cela incluent les considérations d’accessibilité (documentant les équivalents clavier des actions de la souris, par exemple) et les considérations relatives à la plateforme (documentation pour le facteur de forme de la tablette, par exemple, ou pour les environnements de serveur où la ligne de commande peut remplacer l’interface utilisateur graphique).

N’oubliez pas que les utilisateurs ne pensent souvent pas aux problèmes qu’ils rencontrent exactement comme vous le feriez. Par exemple, il peut être étrange de considérer qu’il s’agit d’un « compte ». Veillez à concevoir vos fonctionnalités de recherche et d’indexation, puis à prendre en compte les variations de terminologie et les synonymes.

Toutefois, entre l’interface utilisateur principale et le système d’aide, les termes doivent être très similaires s’ils ne sont pas identiques. Les utilisateurs peuvent être confondus lorsque la langue du système d’aide n’est pas très proche de ce qu’elles voient sur l’écran.

### <a name="writing-compelling-help-link-text"></a>Écriture d’un texte de lien d’aide attrayant

Lorsque vous créez un lien vers une rubrique d’aide à partir de votre interface utilisateur principale, veillez à écrire un texte de lien d’aide attrayant. Un langage clair et spécifique inspire confiance. Les utilisateurs ont tendance à croire que des liens d’aide génériques (un bouton avec le mot « aide » ou « en savoir plus » sur celui-ci) ne mènent pas aux informations appropriées sans investissement significatif.

**Si vous ne faites que cinq choses...**

1.  Concevez votre interface utilisateur afin que les utilisateurs n’aient pas besoin d’aide.
2.  Rendez votre aide utile en mettant en avant le contenu sur les questions principales dans les principaux scénarios pour vos utilisateurs cibles.
3.  Présentez le contenu de l’aide afin qu’il soit facile à analyser.
4.  Sachez que vous n’avez pas besoin de fournir de l’aide pour toutes les fonctionnalités de l’interface utilisateur.
5.  Rendez les points d’entrée de l’aide détectables et attrayants.

## <a name="usage-patterns"></a>Modèles d’usage

Différents types de contenu sont utilisés à des fins différentes.



|    Type de contenu                                                                                                        |   Exemple                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aide procédurale**<br/> fournit les étapes d’exécution d’une tâche. <br/>                       | L’aide procédurale doit se concentrer sur les informations « comment » plutôt que sur « quoi » ou « pourquoi ». <br/> ![capture d’écran de la page d’aide « supprimer les fichiers temporaires » ](images/winenv-help-image2.png)<br/> Dans cet exemple, la rubrique d’aide explique comment utiliser une fonctionnalité de l’utilitaire de nettoyage de disque, en fournissant les étapes à suivre dans l’ordre.<br/>                                              |
| **Aide conceptuelle**<br/> fournit des informations générales, des vues d’ensemble des fonctionnalités ou des processus. <br/> | L’aide conceptuelle doit fournir des informations « quoi » ou « pourquoi » au-delà de ce qui est nécessaire pour effectuer une tâche. <br/> ![capture d’écran de la page d’aide du Bureau (vue d’ensemble) ](images/winenv-help-image3.png)<br/> Dans cet exemple, la rubrique d’aide définit ce qu’est le bureau et fournit des détails supplémentaires sur ce qu’il contient et la raison pour laquelle les utilisateurs interagissent avec lui.<br/>           |
| **Aide de référence**<br/> sert de livre de référence en ligne. <br/>                                | Vous pouvez utiliser l’aide de référence pour documenter un langage de programmation ou des interfaces de programmation. <br/> ![capture d’écran de la page d’aide « conventions typographiques » ](images/winenv-help-image4.png)<br/> Dans cet exemple, la rubrique d’aide répertorie les conventions typographiques utilisées pour cette langue ou application particulière, en fournissant les informations dans une table facile à analyser.<br/> |



 

## <a name="guidelines"></a>Consignes

### <a name="entry-points"></a>Points d’entrée

-   **Lien vers des rubriques d’aide spécifiques pertinentes.** N’êtes pas lié à la page d’aide, à la table des matières, à une liste de résultats de recherche ou à une page qui se contente de créer des liens vers d’autres pages. Évitez d’établir une liaison avec les pages structurées sous la forme d’une grande liste de questions fréquemment posées, car elle oblige les utilisateurs à rechercher celle qui correspond au lien sur lequel ils ont cliqué. N’hésitez pas à créer des liens vers des rubriques d’aide spécifiques qui ne sont pas pertinentes et utiles pour la tâche en cours. Ne liez jamais des pages vides.
-   **Ne placez pas de liens d’aide sur chaque fenêtre ou page pour des raisons de cohérence.** Le fait de fournir un lien d’aide dans un même emplacement ne signifie pas que vous devez les fournir partout.
-   **Utilisez les liens d’aide pour les boîtes de dialogue, les messages d’erreur, les assistants et les feuilles de propriétés.** Si le lien d’aide s’applique à des contrôles spécifiques, placez-le sous-dessous, aligné à gauche. Si le lien d’aide s’applique à la totalité de la fenêtre, placez-le dans le coin inférieur gauche de la zone de contenu de la fenêtre.

    ![capture d’écran de la feuille de propriétés avec la zone de groupe ](images/winenv-help-image5.png)

    Dans cet exemple, le deuxième lien d’aide s’applique à un groupe de contrôles.

    ![capture d’écran de la feuille de propriétés et du lien d’aide ](images/winenv-help-image6.png)

    Dans cet exemple, le lien d’aide s’applique à la fenêtre entière.

-   **Utilisez des liens d’aide au lieu de références textuelles génériques pour faciliter chaque fois que cela est possible.**

    **Correct :**

    Comment réparer les erreurs de disque ?

    **Incorrect :**

    Pour plus d’informations sur la réparation des erreurs de disque, consultez aide et support.

-   **Utilisez un bouton d’aide avec l’icône d’aide pour les pages Hub des éléments du panneau de configuration.** Placez-le dans le coin supérieur droit. Ces boutons n’ont pas d’étiquette, mais ont une info-bulle qui lit l’aide.

    ![capture d’écran de l’élément du panneau de configuration avec le bouton aide ](images/winenv-help-image7.png)

    Élément du panneau de configuration avec un bouton aide.

-   **L’aide F1 est facultative.** Les utilisateurs se sont habitués à trouver des informations d’aide relatives au contexte immédiat de l’interface utilisateur à l’écran en appuyant sur la touche F1, qui est intitulée aide sur les claviers standard. Vous pouvez inclure l’aide F1 si, par exemple, les études de convivialité montrent que vos utilisateurs s’attendent à les trouver, ou que l’interface utilisateur de votre programme est suffisamment complexe pour bénéficier d’une assistance contextuelle.
-   **Les programmes avec barres de menus peuvent avoir une catégorie de menu aide.** Pour obtenir des instructions sur le menu d’aide, consultez [menus](cmd-menus.md).

    ![capture d’écran de l’aide accessible à partir de la barre de menus ](images/winenv-help-image8.png)

    dans cet exemple, le Windows Paint accessoire a une catégorie de menu aide.

-   **Pour l’accessibilité du clavier, fournissez des taquets de tabulation pour les boutons d’aide et les liens.**
-   Le bouton aide et le comportement du lien doivent être les suivants : le volet aide s’ouvre et une rubrique d’aide dédiée s’affiche. l’interface utilisateur qui a appelé le volet d’aide doit rester ouverte pour préserver l’expérience contextuelle.
-   **N’utilisez pas les styles de point d’entrée d’aide obsolètes suivants : « en savoir plus » ou « en savoir plus sur... » liens, boutons d’aide génériques et boutons d’aide contextuelle sur la barre de titre.** Bien qu’ils aient été utilisés par le passé, les études de convivialité ont déterminé que les utilisateurs ont tendance à les ignorer. Utilisez plutôt des liens vers des rubriques d’aide spécifiques. Pour obtenir des instructions sur l’écriture de bons liens d’aide, consultez [liens d’aide](#text).

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec un lien « en savoir plus » ](images/winenv-help-image9.png)

    N’utilisez pas « en savoir plus » ou « en savoir plus sur... » liées.

    **Incorrect :**

    ![capture d’écran du bouton d’aide en regard des boutons valider ](images/winenv-help-image10.png)

    N’utilisez pas les boutons d’aide génériques.

    **Incorrect :**

    ![capture d’écran de l’icône de point d’interrogation sur la barre de titre ](images/winenv-help-image11.png)

    N’utilisez pas de boutons d’aide contextuelle sur la barre de titre.

### <a name="content"></a>Content

-   **Ne créez pas de contenu évident.** Les rubriques d’aide qui répètent ce qui se trouve dans l’interface utilisateur principale n’ajoutent pas de valeur.
-   **Ne créez pas de contenu sur lequel l’utilisateur ne peut agir d’une certaine manière.**
    -   **Exception :** Certains contenus conceptuels fournissent des informations d’arrière-plan importantes sans nécessairement diriger les actions de l’utilisateur.
-   **Évitez les résolutions vagues aux problèmes.** Par exemple, « contactez votre administrateur système » ou « réinstaller l’application » tend à nuire aux utilisateurs.
    -   **Exception :** Il est recommandé de contacter l’administrateur système s’il s’agit de la seule solution pratique, et les administrateurs système s’attendent à être contactés pour le problème.
-   **Évitez le contenu qui traite les scénarios utilisateur très peu probables.** Développez votre contenu d’aide principal pour ce que vous prévoyez d’utiliser normalement ; Notez les exceptions importantes à l’utilisation prévue, mais traitez ce contenu comme une priorité plus faible.
-   **Recueillez des commentaires de la part de vos utilisateurs sur l’utilité de vos rubriques d’aide.** Autorisez les utilisateurs à évaluer des rubriques individuelles. Organisez des [études de convivialité](glossary.md) sur votre documentation pour déterminer les problèmes liés à la qualité et à la détectabilité du contenu.
    -   **Conseil :** Les commentaires des utilisateurs sont également un excellent moyen de générer davantage de contenu basé sur les tâches, concentré sur ce que les utilisateurs font réellement avec votre programme, par opposition au contenu basé sur les fonctionnalités, qui se concentre simplement sur une description de la technologie.
-   **Offrez plusieurs moyens d’accéder à votre contenu.** Une table des matières, un index et un mécanisme de [recherche](ctrl-search-boxes.md) sont trois des méthodes les plus courantes pour améliorer la détectabilité.
-   **S’il existe plusieurs façons d’effectuer une tâche, dans la plupart des cas, vous pouvez simplement documenter la méthode la plus courante utilisée par les utilisateurs inexpérimentés.**

### <a name="icons"></a>Icônes

-   Utilisez l’icône d’aide uniquement pour les fenêtres Explorateur et les pages Hub des éléments du panneau de configuration. N’utilisez pas l’icône d’aide avec les liens d’aide.

**Correct :**

![capture d’écran avec icône de point d’interrogation ](images/winenv-help-image12.png)

dans cet exemple, une fenêtre d’explorateur de Windows utilise une icône d’aide pour fournir l’accès à l’aide.

**Incorrect :**

![capture d’écran de la fenêtre avec l’icône d’aide dans le volet gauche ](images/winenv-help-image13.png)

Dans cet exemple, l’icône d’aide dans la partie inférieure gauche est utilisée de manière incorrecte avec un lien d’aide.

## <a name="text"></a>Texte

**Liens d’aide**

-   Fournissez des informations spécifiques sur le contenu de la rubrique d’aide, en utilisant le plus de texte concis approprié, le cas échéant. Les utilisateurs ignorent souvent les liens d’aide génériques. Assurez-vous que les résultats du lien sont des utilisateurs prévisibles ne doivent pas être surpris par les résultats.

    -   **Exception :** Vous pouvez utiliser « plus d’informations » pour compléter les instructions qui sont directement dans l’interface utilisateur, en particulier si la fourniture d’informations spécifiques dans le lien d’aide entraîne une répétition inutile ou rend le lien moins attrayant.

    **Incorrect :**

    Un mot de passe fort contient au moins six lettres, chiffres et symboles en casse mixte. Qu’est-ce qu’un mot de passe fort ?

    **Correct :**

    Un mot de passe fort contient au moins six lettres, chiffres et symboles en casse mixte. Plus d’informations

    Dans l’exemple incorrect, le lien d’aide est répétitif. Il pose une question qui a déjà répondu.

-   Chaque fois que cela est possible, le texte de l’aide d’expression est lié à la question principale ayant obtenu une réponse par le contenu de l’aide. N’utilisez pas « en savoir plus sur », « en savoir plus sur » ou « obtenir de l’aide pour cette formulation ».

    **Incorrect :**

    En savoir plus sur l’ajout d’exceptions

    **Correct :**

    Quels sont les risques liés à l’autorisation des exceptions ?

    Comment faire ajouter des exceptions ?

    Dans les exemples corrects, le lien est formulées en termes de question principale ayant obtenu une réponse de la rubrique d’aide.

-   Si les informations les plus pertinentes peuvent être résumées succinctement, placez le résumé directement dans l’interface utilisateur au lieu d’utiliser un lien d’aide. Toutefois, vous pouvez utiliser un lien d’aide pour fournir des informations supplémentaires.

    **Incorrect :**

    ![capture d’écran du lien vers qu’est-ce qu’un mot de passe fort ? ](images/winenv-help-image14.png)

    **Correct :**

    ![capture d’écran d’un texte supplémentaire sur les mots de passe ](images/winenv-help-image15.png)

    **Conseillé**

    ![capture d’écran du texte avec un lien vers des informations supplémentaires ](images/winenv-help-image16.png)

    L’exemple correct résume les informations d’aide de façon succincte, ce qui permet d’améliorer de façon considérable la probabilité que les utilisateurs la lisent. Le meilleur exemple fournit un lien d’aide pour plus d’informations sur ce sujet complexe.

-   Expression aide Liens pour indiquer clairement l’assistance. Les liens d’aide ne doivent jamais être lus comme des liens d’action.
-   Utilisez le lien d’aide complet pour le texte du lien, pas seulement les mots clés.

    **Correct :**

    Quels sont les risques liés à l’autorisation des exceptions ?

    **Incorrect :**

    Quels sont les risques liés à l’autorisation des exceptions ?

    Dans l’exemple correct, l’ensemble de la phrase de lien d’aide est utilisé pour le texte du lien.

    -   **Exception :** Les liens d’aide vers des sites Web externes doivent simplement utiliser le nom du site ou de la page comme lien. Tout texte introduisant le nom du site n’a pas besoin d’être inclus dans le lien lui-même.

-   Les liens d’aide ne doivent pas nécessairement correspondre exactement aux en-têtes de rubrique d’aide, mais il doit y avoir une connexion forte et évidente entre les deux. Créez des liens et des en-têtes par paires pour cette raison.

    **Correct :**

    Comment améliorer les performances de cette fonctionnalité ? (texte de lien)

    Configuration de cette fonctionnalité pour des performances optimales (titre de rubrique)

    **Incorrect :**

    Comment améliorer les performances de cette fonctionnalité ? (texte de lien)

    Obtenir une vue d’ensemble de cette fonctionnalité (titre de rubrique)

    Dans l’exemple incorrect, l’en-tête de la rubrique d’aide diffère sensiblement de l’étendue du texte du lien d’aide et peut être en cours de désorientation.

-   Si le contenu de l’aide est en ligne, désactivez-le dans le texte du lien. Cela permet de prédire le résultat des liens.

    **Correct :**

    Pour obtenir des formats et des outils supplémentaires, accédez au site Web de Microsoft.

    **Incorrect :**

    Où puis-je trouver des formats et des outils supplémentaires ?

-   Utilisez des phrases complètes.
-   N’utilisez pas de ponctuation de fin, sauf pour les points d’interrogation.
-   N’utilisez pas de ellipses pour les liens d’aide ou les commandes.

**Contenu de l’aide**

-   Mettez en forme les éléments d’interface utilisateur en gras pour faciliter leur identification. Cela s’avère particulièrement utile pour les rubriques d’aide procédurales, permettant aux utilisateurs de parcourir les procédures et de voir rapidement les éléments pertinents de l’interface utilisateur.
-   Mettre en forme les légendes en italique. Cela s’applique aux tableaux, illustrations, captures d’écran et autres éléments graphiques qui tirent parti d’une brève explication textuelle.
-   Reportez-vous à l’aide tout simplement. En règle générale, n’utilisez pas l’aide en ligne de l’expression, sauf si vous faites référence au contenu sur votre site Web.

 


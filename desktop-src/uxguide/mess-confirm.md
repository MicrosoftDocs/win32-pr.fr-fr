---
title: Confirmations
description: Une confirmation est une boîte de dialogue modale qui demande si l’utilisateur souhaite effectuer une action.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b979987daa4cf2c40308a0cda9c23b08b73f4795
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556091"
---
# <a name="confirmations"></a>Confirmations

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une confirmation est une boîte de dialogue modale qui demande si l’utilisateur souhaite effectuer une action.

![Capture d’écran montrant un bloc-notes « voulez-vous enregistrer les modifications ? » de l'application de partage.](images/mess-confirm-image1.png)

Confirmation standard.

Les confirmations présentent les caractéristiques essentielles suivantes :

-   Ils sont affichés en tant que résultat direct d’une action lancée par l’utilisateur.
-   Ils vérifient que l’utilisateur souhaite poursuivre l’action.
-   Ils se composent d’une question simple et de deux réponses ou plus.

Les confirmations sont particulièrement utiles quand l’action oblige l’utilisateur à faire un choix pertinent et distinct qui ne peut pas être effectué ultérieurement. Ce choix implique souvent un élément de risque qui n’est pas évident pour l’utilisateur, mais les risques ne sont pas essentiels pour les confirmations. Ces éléments sont nécessaires pour justifier l’interruption de la réponse à une boîte de dialogue modale.

En revanche, les [messages d’avertissement](mess-warn.md) présentent une condition susceptible de provoquer un problème à l’avenir. Leurs caractéristiques fondamentales sont qu’elles impliquent des risques :

-   Elles impliquent la perte potentielle d’un ou plusieurs des éléments suivants :
    -   Une ressource précieuse, telle qu’une perte de données ou une perte financière.
    -   Accès ou intégrité du système.
    -   Confidentialité ou contrôle des informations confidentielles.
    -   Temps de l’utilisateur (quantité significative, par exemple, 30 secondes ou plus).
-   Ils ont des conséquences inattendues ou indésirables.
-   Ils requièrent maintenant une gestion correcte, car les erreurs ne peuvent pas être facilement corrigées et peuvent même être irréversibles.

Si une confirmation implique un risque, elle peut également être considérée comme un avertissement. Par conséquent, les instructions relatives aux messages d’avertissement s’appliquent également.

**Remarque :** Les instructions relatives [aux boîtes de dialogue](win-dialog-box.md), aux messages d' [erreur](mess-error.md), à la [mise en page](vis-layout.md)et aux [messages d’avertissement](mess-warn.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’utilisateur est-il invité à poser une question pour effectuer une action qui a au moins deux réponses ?** Si ce n’est pas le cas, le message n’est pas une confirmation.
-   **L’interface utilisateur présente-t-elle une erreur ou un problème qui s’est produit ?** Dans ce cas, utilisez un [message d’erreur](mess-error.md) à la place.
-   **La poursuite de l’action oblige-t-elle l’utilisateur à choisir un choix qui n’a pas de valeur par défaut appropriée ?** Dans ce cas, une confirmation peut être appropriée.
-   **Existe-t-il une autre conception qui élimine la nécessité de la confirmation ?** La nécessité d’une confirmation indique parfois un défaut de conception. Il existe souvent une meilleure solution de conception qui n’a pas besoin de confirmation.
-   **L’utilisateur est-il sur le sujet d’effectuer une action risquée ?** Dans ce cas, une confirmation est appropriée si l’action a des conséquences importantes ou si elle ne peut pas être facilement annulée.
-   **L’utilisateur est-il sur le sujet d’abandonner une tâche ?** Si c’est le cas, ne confirmez pas. Supposons que les utilisateurs comprennent les conséquences de la non-exécution d’une tâche.
-   **L’action a-t-elle des conséquences sur les utilisateurs ?** Dans ce cas, une confirmation peut être appropriée.
-   **Étant donné le contexte actuel, les utilisateurs sont susceptibles d’effectuer une action erronée ?** Dans ce cas, une confirmation peut être appropriée.
-   **Les utilisateurs effectuent-ils fréquemment l’action ?** Si c’est le cas, envisagez une autre conception. Les confirmations fréquentes sont ennuyeuses et ont peu de valeur, car les utilisateurs apprennent à répondre sans penser.
-   **L’action a-t-elle des implications en matière de sécurité ?** Si c’est le cas, une confirmation peut être requise même si les tests précédents l’indiquent autrement.

## <a name="design-concepts"></a>Principes de conception

### <a name="unnecessary-confirmations-are-annoying"></a>Les confirmations inutiles sont ennuyeuses

La première confirmation de Windows que vous avez créée a sans aucun doute été similaire à ce qui suit :

![capture d’écran de « voulez-vous vraiment ? » confirmation ](images/mess-confirm-image2.png)

Confirmation d’origine du ennuyeux.

Il s’agissait d’un démarrage très incorrect. Si vous souhaitez que les utilisateurs détestent votre programme, il vous suffit d’arroser les confirmations comme celles-ci. Pour comprendre pourquoi, considérez le point de vue de l’utilisateur. L’utilisateur a simplement demandé d’effectuer une action par la définition d’une confirmation de sorte que, à moins que quelque chose n’ait été cliqué ou appuyé accidentellement, l’utilisateur souhaite continuer.

Non seulement les confirmations inutiles sont gênantes, mais elles ne sont pas efficaces pour la protection de l’utilisateur contre les erreurs. Les utilisateurs découvrent rapidement le moment où un programme a des confirmations inutiles et leur réponse naturelle consiste à les faire disparaître le plus rapidement possible, souvent sans lecture. Par conséquent, ces confirmations n’ajoutent pas une étape supplémentaire à ces tâches.

N’utilisez pas de confirmations uniquement parce qu’il est possible que les utilisateurs fassent une erreur. **Au lieu de cela, les confirmations sont plus efficaces lorsqu’elles sont utilisées pour confirmer des actions qui ont des conséquences significatives ou inattendues.** Les bonnes confirmations ne sont jamais évidentes. ils doivent communiquer aux utilisateurs qu’ils doivent être conscients de la bonne raison de ne pas continuer. Ils sont utilisés uniquement lorsqu’ils sont véritablement nécessaires à une action, par exemple demander aux utilisateurs d’enregistrer les modifications uniquement lorsque des modifications méritent d’être enregistrées. Cela nécessite l’attention de l’utilisateur uniquement lorsqu’il est véritablement justifié.

Pour les autres types de confirmations, il existe souvent une meilleure solution de conception que le fait de forcer les utilisateurs à répondre à une question.

### <a name="consider-the-design-alternatives"></a>Prendre en compte les alternatives de conception

Voici quelques alternatives de conception qui éliminent le besoin de confirmations de routine :

-   **Éviter les erreurs.** Concevez des tâches afin que les erreurs significatives soient difficiles à faire accidentellement. Par exemple, séparez physiquement les commandes destructrices d’autres commandes et demandez l’exécution de plusieurs actions.
-   **Fournissez une annulation.** Offre la possibilité de restaurer des actions. Par exemple, la suppression d’un fichier dans Microsoft Windows ne nécessite généralement pas de confirmation, car les fichiers supprimés peuvent être récupérés à partir de la corbeille. Notez que si une action est très facile à effectuer, il suffit aux utilisateurs de rétablir l’action.
-   **Fournir des commentaires.** Rendez les résultats indésirables évidents. L’annulation seule n’est pas suffisante si les utilisateurs ne se rendent pas compte lorsqu’ils font une erreur. Par exemple, l’effet de la manipulation directe (par exemple, une opération de glisser-déplacer) doit toujours être évident.
-   **Supposons le résultat probable, mais facilitez la modification.** Si vous n’êtes pas sûr de ce que les utilisateurs veulent, mais qu’il existe un choix possible, sécurisé et sécurisé, supposez que vous avez choisi, de clarifier ce qui s’est passé et de le modifier facilement à l’aide d’un menu contextuel. Par exemple, Microsoft Word suppose que les utilisateurs veulent épeler correctement les mots. S’il reconnaît un mot mal orthographié et qu’il connaît l’orthographe correcte, Word effectue automatiquement la correction, mais permet aux utilisateurs de les restaurer.
-   **Éliminez complètement le choix.** Si le choix n’est pas important, les utilisateurs ne se soucient pas. Mieux pour [simplifier](/previous-versions//dn742474(v=vs.85)) votre programme et éliminer le choix.

### <a name="make-confirmations-require-thought"></a>Les confirmations doivent être pensées

Pour qu’une confirmation ait une valeur, les utilisateurs doivent comprendre la raison de ne pas continuer. Parfois, la raison est évidente, comme lorsque les utilisateurs ferment un document avec des modifications qui n’ont pas été enregistrées :

![Capture d’écran montrant une peinture « voulez-vous enregistrer les modifications ? » « Hello World ! ».](images/mess-confirm-image3.png)

Dans cet exemple, la raison de la confirmation est évidente.

Dans d’autres situations, la raison peut ne pas être si évidente.

Lorsque vous choisissez des étiquettes de bouton de validation pour les boîtes de dialogue, les [recommandations générales](win-dialog-box.md) permettent de choisir des étiquettes qui sont des réponses spécifiques à l’instruction principale. Cela débouche sur une prise de décision efficace, car les utilisateurs doivent lire une quantité minimale de texte pour continuer. Toutefois, cet objectif d’efficacité peut être contre-productive pour les confirmations. Prenons l’exemple suivant :

**Incorrect :**

![capture d’écran de la confirmation avec le bouton désinstaller ](images/mess-confirm-image4.png)

Dans cet exemple, la réponse correcte doit être pensée.

Si vous présentez cette confirmation immédiatement après que l’utilisateur a donné la commande de désinstallation, la réponse de l’utilisateur est probablement « bien sûr que je souhaite désinstaller ! ». L’utilisateur clique sur désinstaller sans en donner une autre.

Pour les confirmations, nous ne voulons pas que les utilisateurs fassent des Hasty, des décisions émotionnelles. Pour encourager les utilisateurs à réfléchir à leur réponse, nous devons fournir une petite vitesse de prise de décision. Dans la pratique, il est généralement préférable d’effectuer cette opération en précisant soigneusement les boutons de validation. Par exemple, nous pouvons utiliser une langue supplémentaire pour indiquer qu’il existe une raison pour ne pas continuer.

**Conseillé**

![capture d’écran du bouton « désinstaller quand même » ](images/mess-confirm-image5.png)

Dans cet exemple, « tout de même » est ajouté à l’étiquette du bouton de validation pour indiquer que la confirmation donne une raison de ne pas continuer.

Si cette approche n’est pas pratique, nous pouvons utiliser des boutons de validation oui/non.

**En outre, mieux :**

![capture d’écran de la confirmation avec les boutons Oui/non ](images/mess-confirm-image6.png)

Dans cet exemple, l’utilisation de boutons de validation oui/non force les utilisateurs à lire au moins l’instruction principale.

### <a name="provide-all-the-information"></a>Fournir toutes les informations

Si vous envisagez de poser une question, vous devez fournir suffisamment d’informations pour que les utilisateurs puissent répondre intelligemment à cette question. Examinez la boîte de dialogue confirmer le remplacement de fichier de Windows XP :

![capture d’écran de la boîte de dialogue « confirmer le remplacement du fichier » ](images/mess-confirm-image7.png)

Boîte de dialogue confirmer le remplacement du fichier de Windows XP.

Cette confirmation fournit-elle toutes les informations dont les utilisateurs peuvent avoir besoin pour répondre à la question ? Avant de répondre, prenez en compte les scénarios utilisateur les plus courants :

-   Copiez (ou déplacez) l’autre fichier en remplaçant celui qui existe déjà.
-   Conservez le fichier existant, sans copier ou déplacer l’autre fichier.
-   Conservez ou copiez le fichier le plus récent (scénario principal).
-   Conservez le fichier existant ou copiez l’autre fichier, en fonction de critères tels que le contenu et la taille du fichier.
-   Conservez le fichier existant et copiez l’autre fichier à l’aide d’un nom différent.
-   Annulez l’opération en cas de problème ou d’inattendue.

Les utilisateurs peuvent obtenir le scénario 1 en cliquant sur Oui et sur scénario 2 en cliquant sur non. Ils peuvent obtenir le scénario 3 en comparant les dates des fichiers et en cliquant sur le bouton approprié, mais notez l’importance qu’il faut pour déterminer le fichier plus récent, puis déterminez le bouton approprié, en particulier pour ce qui est probablement le scénario le plus courant.

Les scénarios 4, 5 et 6 sont également étonnamment difficiles. Les tailles de fichier étant arrondies, par exemple, il est impossible de déterminer si ces fichiers ont la même taille ou même s’ils sont le même fichier. Les icônes sont destinées à l’application utilisée pour ouvrir le fichier, de sorte que les utilisateurs doivent ouvrir les fichiers pour inspecter et comparer leur contenu. Le fait de disposer de miniatures du contenu du fichier serait beaucoup plus utile pour répondre à la question.

La confirmation de copie du fichier de Windows Vista permet de gérer ces scénarios de manière bien meilleure en fournissant des informations supplémentaires et en ajoutant l’option permettant de conserver les deux fichiers :

![capture d’écran de la boîte de dialogue’copier le fichier' ](images/mess-confirm-image8.png)

Confirmation du fichier de copie de Windows Vista.

### <a name="provide-specific-useful-information"></a>Fournir des informations utiles spécifiques

Si vous envisagez de poser une question, assurez-vous que les utilisateurs comprennent la question et les implications des autres réponses. Prenons l’exemple de confirmation de sécurité de Windows Internet Explorer :

![capture d’écran de confirmation avec une question vague ](images/mess-confirm-image9.png)

Une confirmation de sécurité vague.

Cette confirmation demande à une question que les utilisateurs ne peuvent pas répondre intelligemment. L’utilisateur a demandé que Windows Internet Explorer affiche une page et ce message le conseille implicitement par le biais de la formulation du texte et en mettant en surbrillance non comme choix par défaut.

Le problème de sécurité spécifique que pose la page n’est pas suffisamment expliqué, donc le risque de continuer n’est pas évident. Les informations de la confirmation entraîneraient l’utilisateur à cliquer sur non ? En raison de l’imprécision du message, la confirmation n’est pas susceptible de décourager les utilisateurs de continuer, mais les empêchera de le faire.

Pour que cette confirmation soit utile, elle doit fournir des informations spécifiques qui peuvent amener l’utilisateur à décider de ne pas continuer. En général, pour chaque réponse dans une confirmation, examinez les scénarios qui l’exigent et assurez-vous que les informations fournies sont suffisantes pour que les utilisateurs puissent le choisir. Fournissez des choix, et non des dilemmes.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Comment déterminer si une confirmation est nécessaire

Le fait de réfléchir aux scénarios et à la probabilité de choisir chaque réponse suggère une méthode systématique pour déterminer si une confirmation est nécessaire. Si les utilisateurs sont susceptibles de sélectionner toutes les réponses, la confirmation est nécessaire et utile. Toutefois, si une seule réponse est probable (par exemple, 98% du temps), la confirmation est clairement inutile et doit être supprimée. Notez que les confirmations relatives aux problèmes de sécurité, juridiques et de sécurité sont des exceptions possibles.

![capture d’écran de « voulez-vous modifier les paramètres ? » ](images/mess-confirm-image10.png)

Cette confirmation est-elle nécessaire ? Les utilisateurs pourront-ils sélectionner non ? C’est possible, mais très peu probable. Cette confirmation doit être supprimée.

**Si vous ne faites que trois choses...**

1. Assurez-vous que votre confirmation est vraiment nécessaire. Il doit y avoir une raison légitime et claire de ne pas continuer, et une chance que les utilisateurs ne le soient pas.

2. Si la raison de la confirmation n’est pas immédiatement évidente, choisissez des boutons de validation qui encouragent les utilisateurs à réfléchir à leur réponse. En règle générale, cette opération est effectuée en apportant la confirmation sous la forme d’une question oui ou non et en fournissant des réponses entièrement explicites ou oui/non.

3. Tenez compte de tous les scénarios et fournissez les informations requises pour répondre intelligemment à la question.

## <a name="usage-patterns"></a>Modèles d’usage

Les confirmations ont plusieurs modèles d’utilisation :



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmations de routine**<br/> Confirmez que l’utilisateur souhaite effectuer une action de routine à risque faible. <br/>                                              | Ces confirmations sont généralement formulées « voulez-vous vraiment... ? » et ont souvent une case à cocher ne plus afficher ce message pour réduire leur nuisance. <br/> ![capture d’écran de « déplacer le dossier vers la corbeille » ](images/mess-confirm-image11.png)<br/> ![capture d’écran de « ne plus afficher le message » ](images/mess-confirm-image12.png)<br/> Exemples de confirmations de routine.<br/> **Remarque :** Ce modèle est généralement inutile et doit être évité.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmations d’action risquées**<br/> Confirmez que l’utilisateur souhaite effectuer une action qui présente un risque et ne peut pas être facilement annulée. <br/>            | Étant donné qu’ils présentent un risque, ces confirmations ont généralement une icône d’avertissement. <br/> ![Capture d’écran montrant un exemple de confirmation de mise en forme du volume.](images/mess-confirm-image13.png)<br/> ![Capture d’écran montrant un exemple de confirmation de suppression permanente.](images/mess-confirm-image14.png)<br/> Exemples de confirmations d’action risquées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmations de conséquence imprévues**<br/> Confirmez que l’utilisateur souhaite effectuer une action qui a des conséquences inattendues ou involontaires. <br/> | En plus de poser une question, ces confirmations signalent les conséquences inattendues. étant donné qu’ils ont des conséquences inattendues, ces confirmations ont généralement une icône d’avertissement. <br/> ![capture d’écran de « fermer tous les onglets ? » confirmé ](images/mess-confirm-image15.png)<br/> ![capture d’écran de l’annulation de l’installation confirmé ](images/mess-confirm-image16.png)<br/> exemples de confirmations de conséquence involontaires.<br/> Toutefois, ce modèle nécessite que les conséquences soient vraiment involontaires. <br/> **correcte**<br/> ![capture d’écran de l’option « désactiver le journal des clés ? » confirmé ](images/mess-confirm-image17.png)<br/> Les conséquences sont prévues ici. il s’agit donc d’une confirmation de routine.<br/> |
| **Précisions**<br/> Clarifiez la manière dont l’utilisateur souhaite effectuer une action qui a des conséquences potentiellement ambiguës ou inattendues. <br/>             | Les opérations de glisser-déplacer peuvent entraîner des clarifications si l’effet de l’opération peut être mal interprété. <br/> ![capture d’écran de « modifier uniquement cette occurrence ? »](images/mess-confirm-image18.png)<br/> ![capture d’écran de « toujours enregistrer à la sortie ? » confirmé ](images/mess-confirm-image19.png)<br/> Exemples de clarifications.<br/> **Remarque :** Ce modèle doit être évité, car il est préférable de concevoir des actions sans conséquences ambiguës et de supposer le résultat escompté le plus probable. <br/>                                                                                                                                                                                                                                     |
| **Confirmations de sécurité**<br/> Confirmez que l’utilisateur souhaite effectuer une action avec des conséquences sur la sécurité. <br/>                                   | ![capture d’écran de « voulez-vous exécuter ce logiciel ? » ](images/mess-confirm-image20.png)<br/> ![capture d’écran de « mémoriser le mot de passe ? » confirmation ](images/mess-confirm-image21.png)<br/> Exemples de confirmations de sécurité.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Ulterior des confirmations de motivation**<br/> fournissez des informations sur une action, mais présentez-la comme confirmation. <br/>                                       | Si ces boîtes de dialogue sont présentées comme des confirmations, leur objectif réel est l’éducation des utilisateurs ou la publication de fonctionnalités. <br/> ![capture d’écran voulez-vous utiliser cette barre d’outils dans votre barre des tâches ? ](images/mess-confirm-image22.png)<br/> Exemple de confirmation de Ulterior.<br/> **Remarque :** Ce modèle n’est pas recommandé, car il existe généralement une alternative plus directe. Par exemple, les [animations](vis-animations.md) sont une meilleure manière d’afficher la relation entre la cause et l’effet. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Utilisez les confirmations « enregistrer les modifications » uniquement en cas de modifications significatives.** Ne confirmez pas les modifications qui n’ont pas été apportées directement par l’utilisateur, telles que le reformatage automatique de document.

**Incorrect :**

![Capture d’écran montrant une Microsoft Office Outlook’voulez-vous enregistrer les modifications ? ' de l'application de partage.](images/mess-confirm-image23.png)

Cet exemple est incorrect lorsqu’il est utilisé pour un message électronique ou un document vide qui n’a pas été modifié par l’utilisateur.

### <a name="icons"></a>Icônes

-   Les confirmations n’utilisent pas d’icônes de barre de titre.
-   **L’icône de la zone de contenu pour une confirmation est basée sur son modèle de conception :**



    | Modèle                                                | Icône                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmations de routine <br/>                | Pas d'icône. <br/>                                                                                                                         |
    | Confirmations d’action risquées <br/>           | Icône d’avertissement. <br/>                                                                                                                    |
    | Confirmations de conséquence imprévues <br/> | Utilisez une icône d’avertissement en cas de risque, l’icône de fonctionnalité si elle est disponible ; Sinon, aucune icône. <br/>                                          |
    | Précisions <br/>                       | Si la confirmation concerne un document, utilisez la miniature du document ; dans le cas contraire, utilisez l’icône de fonctionnalité si elle est disponible ou aucune icône. <br/> |
    | Confirmations de sécurité <br/>               | Icône d’avertissement. <br/>                                                                                                                    |
    | Ulterior des confirmations de motivation <br/>        | Pas d'icône. <br/>                                                                                                                         |



 

-   **N’utilisez pas d’icônes d’avertissement pour les questions de routine.** Cela revient à la [sonnerie de Windows](text-style-tone.md) et à l’utilisation de votre programme comme une activité dangereuse. Supposons que les utilisateurs comprennent les conséquences de l’annulation d’une tâche avant qu’elle ne soit terminée.

**Incorrect :**

![capture d’écran de « voulez-vous mettre fin au didacticiel ? » ](images/mess-confirm-image24.png)

Dans cet exemple, une icône d’avertissement est utilisée pour poser une question de routine.

### <a name="commit-buttons"></a>Boutons de validation

-   **Utilisez des réponses spécifiques à l’instruction principale si la raison de la confirmation est évidente ou peut être rendue explicite.**

![capture d’écran de’voulez-vous enregistrer les modifications ? ' ](images/mess-confirm-image25.png)

Dans cet exemple, la raison de la confirmation est évidente. par conséquent, l’enregistrement et l’absence d’enregistrement fonctionnent bien.

-   **Dans le cas contraire, utilisez les boutons Oui et non pour les réponses de confirmation.** Cela fait que les utilisateurs donnent la confirmation avant de répondre. N’utilisez jamais OK et annuler pour les confirmations.

**Correct :**

![capture d’écran de’voulez-vous désinstaller les fichiers de support ? ' ](images/mess-confirm-image26.png)

Dans cet exemple, l’utilisation de boutons de validation oui/non force les utilisateurs à lire au moins l’instruction principale.

**Incorrect :**

![capture d’écran de l’annulation de votre réservation ? ](images/mess-confirm-image27.png)

Dans cet exemple, l’utilisation de OK/Cancel est confuse.

-   **Pour fermer un programme ou redémarrer Windows, utilisez des réponses spécifiques à l’instruction principale.** Pour éviter tout malentendu, n’utilisez pas la fonction Close ou yes/no à cet effet.

**Correct :**

![capture d’écran du bouton redémarrer maintenant Windows](images/mess-confirm-image28.png)

**Incorrect :**

![capture d’écran du bouton Oui](images/mess-confirm-image29.png)

Dans l’exemple incorrect, oui est utilisé pour redémarrer Windows.

### <a name="command-links"></a>Liens de commande

-   **Pour le modèle de clarifications, envisagez d’utiliser des liens de commande pour rendre les alternatives claires.**

**Acceptable:**

![capture d’écran de « modification d’une ou de toutes les occurrences » ](images/mess-confirm-image30.png)

**Conseillé**

![capture d’écran de la même question à l’aide des liens de commande ](images/mess-confirm-image31.png)

Dans un meilleur exemple, les liens de commande rendent les alternatives claires.

-   **Commencez par présenter les liens de commande les plus couramment utilisés.** L’ordre qui en résulte doit suivre à peu près la probabilité d’utilisation, mais également avoir un Flow logique.
-   Si un lien de commande requiert une explication supplémentaire, **fournissez une explication supplémentaire.** Les explications supplémentaires décrivent la raison pour laquelle les utilisateurs peuvent choisir l’option ou ce qui se passe si l’option est sélectionnée.

Pour obtenir des instructions et des exemples supplémentaires, consultez [liens de commande](ctrl-command-links.md).

### <a name="default-values"></a>Valeurs par défaut

-   **La réponse par défaut pour une confirmation est basée sur son modèle de conception :**



    | Modèle                                                 | Réponse par défaut                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Confirmations de routine <br/>                | Poursuit. <br/>                                                            |
    | Confirmations d’action risquées <br/>           | Ne continuez pas (ou le choix sécurisé). <br/>                                 |
    | Confirmations de conséquence imprévues <br/> | Si les conséquences sont significatives, ne continuez pas ; Sinon, continuez. <br/> |
    | Précisions <br/>                       | Réponse la plus probable. <br/>                                           |
    | Confirmations de sécurité <br/>               | Ne pas continuer. <br/>                                                      |
    | Ulterior des confirmations de motivation <br/>        | Poursuit. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Ne plus afficher ce message

-   **Utilisez cette option uniquement pour les modèles de confirmation de la routine et Ulterior.** Pour les autres modèles, si les informations sont nécessaires, elles doivent toujours être affichées.
-   **Ne fournissez pas cette option pour justifier l’affichage d’une confirmation inutile.** Il vous suffit de supprimer la confirmation.

**Incorrect :**

![capture d’écran de « faire disparaître ces rappels ? » ](images/mess-confirm-image32.png)

**Toujours incorrect :**

![capture d’écran de « ne plus afficher le message »](images/mess-confirm-image33.png)

Dans ces exemples, l’ajout de l’option ne plus afficher ce message ne permet pas de corriger une confirmation inutile.

Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).

### <a name="bulk-operations"></a>Opérations en bloc

-   Pour les confirmations qui s’appliquent aux opérations en bloc, fournissez une option pour appliquer la confirmation à la totalité de l’opération.

![capture d’écran de’voulez-vous faire pour tous les éléments ? ' case à cocher ](images/mess-confirm-image34.png)

Cet exemple a une option pour les opérations en bloc.

-   Éliminer ou reporter les confirmations dans une opération en bloc.

**Incorrect :**

![capture d’écran de la boîte de dialogue « confirmer la suppression du fichier » ](images/mess-confirm-image35.png)

Dans cet exemple, l’Explorateur Windows dans Windows XP confirme chaque fichier en lecture seule lors d’un déplacement de fichiers en bloc. Il est préférable de copier les fichiers en lecture seule sans demander ou différer la gestion de ces fichiers et de présenter la confirmation à la fin de la tâche.

### <a name="progressive-disclosure"></a>Affichage progressif

-   **Si vous devez inclure des informations avancées dans un message de confirmation, révélez-les à l’aide de boutons de divulgation progressive (par exemple, « afficher les détails »).** Cela simplifie la confirmation pour une utilisation classique. Ne masquez pas les informations nécessaires, car les utilisateurs ne le trouvent peut-être pas.
-   **N’utilisez pas « afficher les détails » à moins qu’il y ait vraiment plus de détails.** Ne restatez pas uniquement les informations existantes dans un format différent.

Pour obtenir des instructions sur l’étiquetage, consultez [Divulgation progressive](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Contrôle de compte d'utilisateur

-   **N’utilisez pas l’interface utilisateur d’élévation du contrôle de compte d’utilisateur (UAC) comme substitut pour une confirmation.** Si une action nécessite une confirmation, utilisez une boîte de dialogue distincte. Au cours de l' [interface utilisateur d’élévation](winenv-uac.md), les utilisateurs doivent se concentrer sur s’ils ont démarré la tâche et si le programme est digne de confiance.
-   **Affichez la confirmation avant l’interface utilisateur d’élévation.** Cela élimine les élévations inutiles.

## <a name="text"></a>Texte

### <a name="general"></a>Général

-   **Supprimez le texte redondant.** Recherchez du texte redondant dans les titres, des instructions principales, des instructions supplémentaires, des zones de contenu, des liens de commande et des boutons de validation. En règle générale, laissez le texte intégral dans les instructions et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
-   **N’utilisez pas « avertissement » ou « attention » dans le texte.** Si les utilisateurs doivent procéder à la prudence, indiquez-le à l’aide d’une icône d’avertissement.

**Incorrect :**

![capture d’écran de la confirmation de la mise en forme du volume ](images/mess-confirm-image36.png)

Dans cet exemple, le terme « avertissement » n’est pas nécessaire.

### <a name="titles"></a>Titres

-   **Utilisez le titre pour identifier la commande ou la fonctionnalité à l’origine de la confirmation. Exceptions**
    -   Si une confirmation est affichée par de nombreuses commandes différentes, envisagez d’utiliser le nom du programme à la place.
    -   Si ce titre est redondant ou confus avec l’instruction principale, utilisez le nom du programme à la place.

Toutefois, si la confirmation provient d’une tâche de longue durée et peut s’afficher correctement après le début de la tâche, utilisez toujours la commande ou la fonctionnalité pour identifier clairement le contexte.

-   **N’utilisez pas le titre pour expliquer ce que vous devez faire dans la boîte de dialogue** qui est l’objectif de l’instruction principale.
-   S’il ajoute de la clarté, commencez le titre par le mot confirmer.
-   **Pour les confirmations d’action risquées, vous pouvez ajouter le nom de l’objet impliqué pour une mise en évidence supplémentaire.**

![capture d’écran du titre de la boîte de dialogue « formater le lecteur f » ](images/mess-confirm-image13.png)

Dans cet exemple, le lecteur à mettre en forme est inclus dans le titre.

-   Utilisez la mise [en majuscules de style titre](glossary.md), sans ponctuation finale.

### <a name="main-instructions"></a>Instructions principales

-   **L’instruction principale pour une confirmation est basée sur son modèle de conception :**



    | Modèle                                                 | Instruction principale                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmations de conséquence imprévues <br/> | Indiquez la conséquence inattendue.<br/> **exception :** si une question demandant à l’utilisateur de continuer à s’exécuter clairement implique la conséquence imprévue, posez-la plutôt la question. <br/> ![capture d’écran de « fermer tous les onglets ? » confirmé ](images/mess-confirm-image15.png)<br/> Dans cet exemple, demander à l’utilisateur de s’exécuter suffisamment pour communiquer les conséquences de l’action.<br/> |
    | Tous les autres <br/>                           | Posez une question unique pour déterminer si l’utilisateur souhaite continuer. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **N’utilisez qu’une seule phrase complète.** Supprimez l’instruction principale jusqu’aux informations essentielles. Si vous devez apporter des explications supplémentaires, utilisez une instruction supplémentaire.
-   **Être spécifique s’il existe des objets impliqués, donnez-leur un nom complet.**
-   **Utilisez une formulation positive.** Une formulation positive est plus facile à comprendre pour les utilisateurs.

**Correct :**

Voulez-vous activer le partage de fichiers et d’imprimantes ?

**Incorrect :**

Voulez-vous désactiver le partage de fichiers et d’imprimantes ?

Toutefois, la formulation doit correspondre à la commande associée, même si la commande est négativement formulées ; par exemple, utilisez Disable pour confirmer une commande Disable.

-   Bien qu’il n’existe pas de règles strictes pour les formulations, **ces phrases de confirmation courantes comportent le connotation indiqué :**



    | Expression                                                            | Connotation                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Voulez-vous vraiment \[ effectuer une action \] ? <br/> | Confirmation du résultat direct d’une demande de l’utilisateur. <br/> |
    | Voulez-vous \[ effectuer une action \] ? <br/>           | Confirmation d’un effet secondaire d’une demande de l’utilisateur. <br/>     |
    | Voulez-vous \[ Sélectionner un résultat \] ? <br/>          | Vous avez besoin d’une clarification. <br/>                           |
    | \[Effectuer une action \] ? <br/>                          | Aucun connotation. <br/>                                 |



 

-   Pour les confirmations d’action risquées, utilisez le terme de manière permanente pour indiquer qu’une action ne peut pas être annulée.

![capture d’écran de confirmation de suppression permanente ](images/mess-confirm-image37.png)

Dans cet exemple, « définitivement » indique que l’action ne peut pas être annulée.

-   Utilisez la mise [en majuscules de style phrase](glossary.md).

### <a name="supplemental-instructions"></a>Instructions supplémentaires

-   **L’instruction supplémentaire pour une confirmation est basée sur son modèle de conception :**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Modèle</strong><br/></td>
    <td><strong>Instruction supplémentaire</strong><br/></td>
    </tr>
    <tr class="even">
    <td>Confirmations de conséquence imprévues <br/></td>
    <td>Posez une question unique pour déterminer si l’utilisateur souhaite continuer. <br/></td>
    </tr>
    <tr class="odd">
    <td>Tous les autres <br/></td>
    <td>Expliquez les raisons les plus évidentes pour lesquelles l’utilisateur peut ne pas vouloir continuer. Ces raisons sont les suivantes : <br/>
    <ul>
    <li>Perte potentielle d’un ou plusieurs des éléments suivants : <ul>
    <li>Une ressource précieuse, telle qu’une perte de données ou une perte financière.</li>
    <li>Accès ou intégrité du système.</li>
    <li>Confidentialité ou contrôle des informations confidentielles.</li>
    </ul></li>
    <li>Actions irréversibles.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Ne répétez pas l’instruction principale avec un libellé légèrement différent.** Au lieu de cela, omettez l’instruction supplémentaire s’il n’y a pas d’autres à ajouter.
-   **Pour les confirmations de conséquence imprévues, envisagez d’utiliser le terme quand même pour indiquer de façon concise qu’il y a une raison de ne pas continuer** au cas où l’utilisateur aurait négligé l’instruction principale. Pour plus d’informations, consultez concepts de conception.
-   Utilisez des phrases complètes, des majuscules de style phrase et des signes de ponctuation de fin.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des confirmations :

-   Reportez-vous à une confirmation par son titre si le titre est spécifique à la confirmation (autrement dit, pas le nom du programme). Sinon, reportez-vous-y par son instruction principale.
-   Si nécessaire, vous pouvez faire référence à une boîte de dialogue de confirmation sous la forme d’un message.
-   Utilisez le texte exact, y compris la mise en majuscules.
-   Dans la mesure du possible, mettez en forme le texte en gras. Sinon, placez le texte entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans le message **copier le fichier** , cliquez sur le fichier le plus récent.


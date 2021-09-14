---
title: Messages d'avertissement
description: Un message d’avertissement est une boîte de dialogue modale, un message sur place, une notification ou une bulle qui avertit l’utilisateur d’une condition susceptible de provoquer un problème à l’avenir.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d12962cb8e984ffcb9f7f91875be7c6a724cea95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231120"
---
# <a name="warning-messages"></a>Messages d'avertissement

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Un message d’avertissement est une boîte de dialogue modale, un message sur place, une notification ou une bulle qui avertit l’utilisateur d’une condition susceptible de provoquer un problème à l’avenir.

![capture d’écran d’un message d’avertissement standard](images/mess-warn-image1.png)

Message d’avertissement modal standard.

La caractéristique fondamentale des avertissements est qu’ils impliquent le risque de perdre un ou plusieurs des éléments suivants :

-   Une ressource précieuse, telle que des données financières ou autres données importantes.
-   Accès ou intégrité du système.
-   Confidentialité ou contrôle des informations confidentielles.
-   Temps de l’utilisateur (quantité significative, par exemple, 30 secondes ou plus).

En revanche, une confirmation est une boîte de dialogue modale qui demande si l’utilisateur souhaite effectuer une action. Certains types d’avertissements sont présentés comme des confirmations et, dans ce cas, les instructions de confirmation s’appliquent également.

**Remarque :** Les instructions relatives aux [boîtes de dialogue](win-dialog-box.md), aux [confirmations](mess-confirm.md) [, aux](mess-error.md)[icônes standard](vis-std-icons.md), aux [notifications](mess-notif.md)et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’utilisateur est-il alerté d’une condition susceptible de provoquer un problème à l’avenir ?** Si ce n’est pas le cas, le message n’est pas un avertissement.
-   **L’interface utilisateur présente-t-elle une erreur ou un problème qui s’est déjà produit ?** Dans ce cas, utilisez un message d’erreur à la place.
-   **Les utilisateurs sont susceptibles d’effectuer une action ou de modifier leur comportement en tant que résultat du message ?** Si ce n’est pas le cas, la condition ne justifie pas l’interruption de l’utilisateur. il est donc préférable de supprimer l’avertissement.
-   **La condition correspond-elle au résultat direct d’une action lancée par l’utilisateur ?** Si ce n’est pas le cas, envisagez d’utiliser [des notifications d’événements non critiques](mess-notif.md).
-   **La condition est-elle une condition spéciale dans un contrôle ?** Si c’est le cas, utilisez plutôt une [bulle](ctrl-balloons.md) .
-   **Pour les confirmations, l’utilisateur est-il sur le sujet d’effectuer une action risquée ?** Dans ce cas, un avertissement est approprié si l’action a des conséquences importantes ou si elle ne peut pas être facilement annulée.
-   **Pour les autres types d’avertissements, l’utilisateur doit-il agir maintenant ou dans le futur ?** N’affiche pas les avertissements si les utilisateurs peuvent continuer à travailler de manière productive sans problèmes immédiats. Différez l’avertissement jusqu’à ce que la condition soit plus immédiate et pertinente.

## <a name="design-concepts"></a>Principes de conception

### <a name="avoid-overwarning"></a>Éviter le suravertissement

nous prévoyons un avertissement dans les programmes Microsoft Windows. le programme de Windows classique présente des avertissements apparemment partout, en vous avertissant des choses qui ont une importance minime. Dans certains programmes, presque toutes les questions sont présentées sous la forme d’un avertissement. Le suravertissement permet d’utiliser un programme comme une activité dangereuse et de délivrer des problèmes réellement significatifs.

**Incorrect :**

![capture d’écran d’un message d’avertissement inutile ](images/mess-warn-image2.png)

Un suravertissement rend votre programme dangereux et similaire à celui qui a été conçu par les juristes.

Le seul risque de perte de données ou un problème à l’avenir est insuffisant pour appeler un avertissement. En outre, les résultats indésirables doivent être inattendus ou involontaires, et ne peuvent pas être facilement corrigés. Dans le cas contraire, une erreur de l’utilisateur peut être interprétée pour entraîner une perte de données ou un problème potentiel et mériter un avertissement.

### <a name="characteristics-of-good-warnings"></a>Caractéristiques des avertissements corrects

Bons avertissements :

-   **Impliquent un risque.** Des avertissements bien avertisent les utilisateurs d’un événement important.

**Incorrect :**

![capture d’écran de’voulez-vous quitter ? ' warning ](images/mess-warn-image3.png)

Et alors? Cette confirmation suppose que les utilisateurs quittent souvent les programmes par accident.

-   **Avoir une pertinence immédiate.** Non seulement les utilisateurs doivent se soucier, mais ils doivent s’en soucier maintenant. Les utilisateurs ne sont généralement pas intéressés par les problèmes qu’ils peuvent rencontrer plus tard tant qu’ils peuvent effectuer leur travail maintenant.

**Incorrect :**

![capture d’écran de la batterie-avertissement de faible-entrée à trois heures ](images/mess-warn-image4.png)

Dans ce cas, il est préférable d’avertir l’utilisateur en trois heures.

-   **Mène à l’action.** Il y a un nom que les utilisateurs doivent faire ou connaître en tant que résultat de l’avertissement. Ils doivent peut-être prendre une mesure à l’avenir immédiatement ou ultérieurement. Peut-être qu’ils exécutent une tâche différemment. La conséquence de l’ignorance de l’avertissement doit être Clear. Les avertissements sans action font simplement des utilisateurs le sentiment paranoïaques.

**Incorrect :**

![capture d’écran de l’avertissement « Live Messenger est en cours d’exécution » ](images/mess-warn-image5.png)

Pourquoi cette notification a-t-elle un avertissement ? Que sont les utilisateurs censés faire (en plus de la préoccupation) ?

-   **Ne sont pas évidents.** N’affiche pas d’avertissement pour indiquer la conséquence évidente d’une action. Par exemple, supposons que les utilisateurs comprennent les conséquences de la non-exécution d’une tâche.

**Incorrect :**

![capture d’écran de voulez-vous quitter l’Assistant ? tres ](images/mess-warn-image6.png)

L’annulation d’un Assistant incomplet signifie que la tâche n’est pas terminée... qui savait ?

-   **Se produisent rarement.** Les avertissements de constante deviennent rapidement inefficaces et ennuyeux. Les utilisateurs sont souvent plus concentrés pour se débarrasser de l’avertissement que pour résoudre le problème.

**Incorrect :**

![capture d’écran de l’avertissement « mettre à jour les signatures de virus » ](images/mess-warn-image7.png)

Les utilisateurs sont plus susceptibles de se concentrer sur l’avertissement que de résoudre le problème sous-jacent.

Un message qui n’a pas ces caractéristiques peut toujours être un bon message, ce qui n’est pas un bon avertissement.

### <a name="determine-the-appropriate-message-type"></a>Déterminer le type de message approprié

Certains problèmes peuvent être présentés sous la forme d’une erreur, d’un avertissement ou d’informations, en fonction de l’importance et de la formulation. par exemple, supposons qu’une page Web ne peut pas charger un contrôle de ActiveX non signé basé sur la configuration actuelle de Windows Internet Explorer :

-   **Erreurs.** « cette page ne peut pas charger un contrôle de ActiveX non signé ». (Formulées en tant que problème existant.)
-   **Tres.** « cette page peut ne pas se comporter comme prévu, car Windows Internet Explorer n’est pas configuré pour charger les contrôles de ActiveX non signés ». ou «autoriser cette page à installer un contrôle de ActiveX non signé ? Cette opération à partir de sources non approuvées peut endommager votre ordinateur.» (Les deux formulées comme des conditions qui peuvent entraîner des problèmes futurs.)
-   **Informations.** « vous avez configuré Windows Internet Explorer pour bloquer les contrôles de ActiveX non signés ». (Formulées en tant que déclaration de faits.)

**Pour déterminer le type de message approprié, concentrez-vous sur l’aspect le plus important du problème que les utilisateurs doivent connaître ou agir.** En règle générale, si un problème empêche l’utilisateur de continuer, vous devez le présenter comme une erreur. Si l’utilisateur peut continuer, présentez-le en tant qu’avertissement. Élaborez l' [instruction principale](text-ui.md) ou un autre texte correspondant en fonction de ce Focus, puis choisissez une icône ([standard](vis-std-icons.md) ou autre) qui correspond au texte. Le texte d’instruction principal et les icônes doivent toujours correspondre.

### <a name="be-specific"></a>Être spécifique

Les avertissements sont plus intéressants lorsque les informations suivantes sont spécifiques et claires :

-   Source de l’avertissement.
-   La condition et le problème potentiels spécifiques.
-   Ce que l’utilisateur doit faire à son sujet.
-   Que se passe-t-il si l’utilisateur ne fait rien.

**Incorrect :**

![capture d’écran d’un avertissement vague de risque significatif ](images/mess-warn-image8.png)

Dans cet exemple, quel est le problème potentiel ? Qu’est-ce que l’utilisateur est censé faire, hormis le fait de ne pas utiliser le projecteur sur le réseau ? Sans aucune information spécifique, l’utilisateur peut se sentir mal à faire.

**Correct :**

![capture d’écran de l’avertissement de problème et des conséquences ](images/mess-warn-image9.png)

Dans cet exemple, le problème et les conséquences sont clairs.

Parfois, il y a un problème potentiel légitime, digne d’informant les utilisateurs, mais la solution et les conséquences ne sont pas connues. Au lieu de donner un avertissement vague, soyez précis en donnant les informations les plus probables ou l’exemple le plus courant.

**Correct :**

![capture d’écran des avertissements et des solutions d’erreur réseau ](images/mess-warn-image10.png)

Dans cet exemple, l’avertissement est rendu spécifique en fournissant la solution la plus probable.

Toutefois, dans ces cas-là, utilisez une formulation qui indique qu’il existe d’autres possibilités. Dans le cas contraire, les utilisateurs peuvent être trompeurs.

**Incorrect :**

![capture d’écran de l’avertissement de déconnexion du câble réseau ](images/mess-warn-image11.png)

**Correct :**

![la capture d’écran du câble est peut-être débranchée ](images/mess-warn-image12.png)

Dans l’exemple incorrect, les utilisateurs sont confondus si le câble est bien branché.

**Si vous ne faites que deux choses...**

1. Ne pas avertir. Limitez les avertissements aux conditions qui impliquent un risque et qui sont immédiatement pertinentes, exploitables, non évidentes et peu fréquentes. Sinon, supprimez ou reformulez le message.

2. Fournir des informations utiles spécifiques.

## <a name="usage-patterns"></a>Modèles d’usage

Les avertissements ont plusieurs modèles d’utilisation :




| Étiquette | Valeur |
|--------|-------|
| <strong>Prise de conscience</strong><br /> Rendre l’utilisateur conscient d’une condition ou d’un problème potentiel, mais l’utilisateur n’a peut-être pas à faire quoi que ce soit. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Exemples d’avertissements de sensibilisation.<br /> Les avertissements de sensibilisation présentent la présentation suivante : <br /><ul><li><strong>Instruction principale :</strong> Décrivez la condition ou le problème potentiel.</li><li><strong>Instructions supplémentaires :</strong> Expliquez l’implication et pourquoi elle est importante.</li><li><strong>Boutons de validation :</strong> Plus.</li></ul> | 
| <strong>Prévention des erreurs</strong><br /> N’oubliez pas que l’utilisateur a des informations qui peuvent empêcher un problème, en particulier quand vous faites des choix. <br /> | Les avertissements de prévention des erreurs sont mieux présentés à l’aide d’une icône d’avertissement sur place et du texte explicatif. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Exemples d’avertissements de prévention d’erreur.<br /> | 
| <strong>Problème imminent</strong><br /> L’utilisateur doit effectuer une opération pour éviter un problème imminent. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Exemple d’avertissement de problème imminent.<br /> Les avertissements de problèmes imminents présentent la présentation suivante : <br /><ul><li><strong>Instruction principale :</strong> Décrivez ce que l’utilisateur doit faire maintenant.</li><li><strong>Instructions supplémentaires :</strong> Expliquez la condition et pourquoi elle est importante.</li><li><strong>Boutons de validation :</strong> Un bouton de commande ou un lien de commande pour chaque option, ou OK si l’action se produit en dehors de la boîte de dialogue.</li></ul> | 
| <strong>Confirmation de l’action risquée</strong><br /> Confirmez que l’utilisateur souhaite effectuer une action qui présente un risque et ne peut pas être facilement annulée. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Exemple de confirmation d’action risquée.<br /> Les confirmations d’action risquées ont la présentation suivante : <br /><ul><li><strong>Instruction principale :</strong> Posez une question pour déterminer si l’utilisateur souhaite continuer.</li><li><strong>Instructions supplémentaires :</strong> Expliquez les raisons les plus évidentes pour lesquelles l’utilisateur peut ne pas vouloir continuer.</li><li><strong>Boutons de validation :</strong> Oui, non.</li></ul>Pour obtenir des instructions sur ce modèle, consultez <a href="mess-confirm.md">confirmations</a>. <br /> | 




 

## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

-   **Choisissez l’interface utilisateur de la présentation en fonction du type d’informations :**



| Interface utilisateur  | Idéal pour |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Boîtes de dialogue modales<br/> | Avertissements critiques (y compris les confirmations) auxquels les utilisateurs doivent répondre maintenant.<br/>                                                 |
| Sur place<br/>           | Informations susceptibles d’empêcher un problème, en particulier lorsque les utilisateurs effectuent des choix.<br/>                                         |
| Bande<br/>            | Informations susceptibles d’empêcher un problème, en particulier lorsqu’elles sont liées à la réalisation d’une tâche.<br/>                                     |
| Notifications<br/>      | Événements ou États significatifs qui peuvent être ignorés en toute sécurité, au moins temporairement.<br/>                                              |
| Bulles<br/>           | Un contrôle est dans un État qui affecte l’entrée. Cet État est probablement involontaire et l’utilisateur peut ne pas se rendre compte qu’une entrée est affectée.<br/> |



 

-   **Pour les boîtes de dialogue modales :**
    -   **Utilisez les boîtes de dialogue de tâches chaque fois que nécessaire pour obtenir une apparence et une disposition cohérentes.** les boîtes de dialogue de tâches requièrent Windows Vista ou version ultérieure. elles ne conviennent donc pas aux versions antérieures de Windows.
    -   **Affichez un seul message d’avertissement par condition.** Par exemple, affichez un avertissement unique qui explique complètement une condition au lieu de la décrire un détail à la fois par message. L’affichage d’une séquence de boîtes de dialogue d’avertissement pour une seule condition est confus et ennuyeux.
    -   **N’affichez pas un avertissement plus d’une fois par condition.** Les avertissements de constante deviennent rapidement inefficaces et ennuyeux. Les utilisateurs sont souvent plus concentrés pour se débarrasser de l’avertissement que pour résoudre le problème. Si vous devez avertir à plusieurs reprises pour une seule condition, utilisez la [remontée progressive](mess-notif.md).
-   **Ne pas accompagner les avertissements avec un effet sonore ou un bip.** Cela est transférerez et inutile.
    -   **Exception :** Si l’utilisateur doit répondre immédiatement, vous pouvez utiliser un effet sonore.

### <a name="icons"></a>Icônes

-   Ne placez pas d’icône d’avertissement dans la barre de titre d’une boîte de dialogue.
-   **Utilisez une icône d’avertissement.** Exceptions :
    -   Si l’avertissement concerne une fonctionnalité qui a une icône, vous pouvez utiliser l’icône de fonctionnalité avec une superposition d’avertissement.

        **Correct :**

        ![capture d’écran de l’icône de verrou avec icône d’avertissement superposition ](images/mess-warn-image21.png)

        Dans cet exemple, l’icône de fonctionnalité a une superposition d’avertissement.

-   Pour les boîtes de dialogue modales avec un avertissement de note de bas de page, placez l’icône d’avertissement dans la note de bas de page au lieu de la zone de contenu.

    **Correct :**

    ![capture d’écran de l’icône d’avertissement dans la note de bas de boîte de dialogue ](images/mess-warn-image22.png)

    Dans cet exemple, la note de bas de page contient l’icône d’avertissement.

Pour obtenir des instructions et des exemples supplémentaires, consultez [icônes standard](vis-std-icons.md).

### <a name="dont-show-this-message-again"></a>Ne plus afficher ce message

-   **Si une boîte de dialogue d’avertissement a besoin de cette option, réexaminez l’avertissement et sa fréquence.** S’il possède toutes les caractéristiques d’un bon avertissement (implique un risque, et qu’il est immédiatement pertinent, actionnable, pas évident et peu fréquent), il ne devrait pas être logique pour les utilisateurs de le supprimer.

Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Affichage progressif

-   **Si vous devez inclure des informations avancées dans un message d’avertissement, révélez-les à l’aide de boutons de divulgation progressive** (par exemple, « afficher les détails »). Cela simplifie l’avertissement pour une utilisation classique. Ne masquez pas les informations nécessaires, car les utilisateurs ne le trouvent peut-être pas.
-   **N’utilisez pas « afficher les détails » à moins qu’il y ait vraiment plus de détails.** Ne restatez pas uniquement les informations existantes dans un format différent.

Pour obtenir des instructions sur l’étiquetage, consultez [Divulgation progressive](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Valeurs par défaut

-   **Sélectionnez le niveau de réponse le plus sûr, le moins destructif ou le plus sécurisé par défaut.**

## <a name="text"></a>Texte

### <a name="general"></a>Général

-   **Supprimez le texte redondant.** Recherchez-en les titres, les instructions principales, les instructions supplémentaires, les zones de contenu, les liens de commande et les boutons de validation. En règle générale, laissez le texte intégral dans les instructions et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
-   **N’utilisez pas les termes « avertissement » ou « attention » dans le texte.** Lorsqu’il est [utilisé correctement](vis-std-icons.md), l’icône d’avertissement indique que les utilisateurs doivent procéder avec précaution.

**Incorrect :**

![capture d’écran de l’utilisation inutile de l’avertissement dans le texte ](images/mess-warn-image23.png)

Dans cet exemple, le terme « avertissement » n’est pas nécessaire.

### <a name="titles"></a>Titres

-   **Utilisez le titre pour identifier la commande ou la fonctionnalité à partir de laquelle l’avertissement provient.** Exceptions :
    -   Si un avertissement est affiché par de nombreuses commandes différentes, envisagez d’utiliser le nom du programme à la place.
    -   Si ce titre est redondant ou confus avec l’instruction principale, utilisez le nom du programme à la place.

**Incorrect :**

![capture d’écran du titre de la boîte de dialogue d’avertissement de sécurité ](images/mess-warn-image24.png)

Dans cet exemple, « avertissement de sécurité » n’identifie pas la commande ou la fonctionnalité à partir de laquelle l’avertissement provient.

-   **N’utilisez pas le titre pour expliquer ce que vous devez faire dans la boîte de dialogue** qui est l’objectif de l’instruction principale.
-   Utilisez la mise [en majuscules de style titre](glossary.md), sans ponctuation finale.

### <a name="main-instructions"></a>Instructions principales

-   L’instruction principale d’un avertissement est basée sur son modèle de conception :



| Modèle                        | Instruction principale                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Sensibilisation<br/>                 | Décrivez la condition ou le problème potentiel.<br/>              |
| Problème imminent<br/>          | Décrivez ce que l’utilisateur doit faire maintenant.<br/>                   |
| Confirmation de l’action risquée<br/> | Posez une question pour déterminer si l’utilisateur souhaite continuer.<br/> |



 

-   ![capture d’écran d’une notification de batterie faible ](images/mess-warn-image25.png)
-   Dans cet exemple, la notification de batterie faible est un avertissement de sensibilisation, donc l’instruction principale décrit la condition.
-   ![capture d’écran de l’avertissement modifier immédiatement la batterie ](images/mess-warn-image1.png)
-   Dans cet exemple, la boîte de dialogue batterie faible est un problème imminent, donc l’instruction principale décrit ce que l’utilisateur doit faire maintenant.
-   **N’utilisez qu’une seule phrase complète.** Supprimez l’instruction principale jusqu’aux informations essentielles. Si vous devez apporter des explications supplémentaires, utilisez une instruction supplémentaire.
-   **Utilisez des mots tels que « Now » et « immédiatement » si l’utilisateur doit agir immédiatement.** N’utilisez pas ces mots s’il n’y a pas d’urgence.
-   **Être spécifique s’il existe des objets impliqués, donnez-leur un nom complet.**
-   Utilisez la mise [en majuscules de style phrase](glossary.md).

### <a name="supplemental-instructions"></a>Instructions supplémentaires

-   L’instruction supplémentaire pour un avertissement est basée sur son modèle de conception :



| Modèle            | Instruction supplémentaire                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Sensibilisation<br/>                 | Expliquez l’implication et pourquoi elle est importante.<br/>                        |
| Problème imminent<br/>          | Expliquez la condition et pourquoi elle est importante.<br/>                          |
| Confirmation de l’action risquée<br/> | Expliquez les raisons les plus évidentes pour lesquelles l’utilisateur peut ne pas vouloir continuer.<br/> |



 

-   **Ne répétez pas l’instruction principale avec un libellé légèrement différent.** Au lieu de cela, omettez l’instruction supplémentaire s’il n’y a pas d’autres à ajouter.
-   Utilisez des phrases complètes, des majuscules de style phrase et des signes de ponctuation de fin.

### <a name="commit-buttons"></a>Boutons de validation

-   Pour les boîtes de dialogue d’avertissement, les boutons de validation sont basés sur le modèle de conception :



| Modèle               | Boutons de validation        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Sensibilisation<br/>                 | C’est presque ça. N’utilisez pas OK, car cela suggère que des problèmes potentiels sont possibles.<br/>                              |
| Problème imminent<br/>          | Un bouton de commande ou un lien de commande pour chaque option, ou OK si l’action se produit en dehors de la boîte de dialogue.<br/> |
| Confirmation de l’action risquée<br/> | Oui, non.<br/>                                                                                             |



 

-   **Incorrect :**
-   ![capture d’écran de la boîte de dialogue d’avertissement avec le bouton OK ](images/mess-warn-image26.png)
-   Les problèmes ne sont pas OK. Utilisez plutôt Close.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence aux avertissements :

-   Si l’avertissement pose une question, reportez-vous à un avertissement par sa question ; dans le cas contraire, utilisez l’instruction principale. Si la question ou l’instruction principale est longue ou détaillée, résumez-la.
-   Si nécessaire, vous pouvez faire référence à une boîte de dialogue d’avertissement en tant que message.
-   Dans la mesure du possible, mettez en forme le texte en gras. Sinon, placez le texte entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans le message voulez **-vous afficher les éléments non sécurisés ?** , cliquez sur Oui.

 


---
title: Icônes standard
description: Les icônes standard sont les icônes d’erreur, d’avertissement, d’informations et de point d’interrogation qui font partie de Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74f5b70fb218606eb5f87cbad247c1c75a100f9c5e0f675bb6c075e559fd1a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936385"
---
# <a name="standard-icons"></a>Icônes standard

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les icônes standard sont les icônes d’erreur, d’avertissement, d’informations et de point d’interrogation qui font partie de Windows.

![capture d’écran de quatre icônes standard ](images/vis-std-icons-image1.png)

Les icônes d’erreur, d’avertissement, d’informations et de point d’interrogation standard.

Les icônes standard ont les significations suivantes :

-   **Icône d’erreur.** L’interface utilisateur présente une erreur ou un problème qui s’est produit.
-   **Icône d’avertissement.** L’interface utilisateur présente une condition susceptible de provoquer un problème à l’avenir.
-   **Icône d’informations.** L’interface utilisateur présente des informations utiles.
-   **Icône de point d’interrogation.** L’interface utilisateur indique un point d’entrée d’aide.

les icônes standard sont notables, car elles sont intégrées à de nombreux Windows les interfaces de programmation d’applications (api), telles que les boîtes de [dialogue de tâches](win-dialog-box.md), les [boîtes de message](glossary.md), les [bulles](ctrl-balloons.md)et les [notifications](mess-notif.md). Ils sont également couramment utilisés sur des [messages sur place](glossary.md) et des barres d' [État](ctrl-status-bars.md).

**Remarque :** Les instructions relatives aux [icônes](vis-icons.md) sont présentées dans un article distinct.

## <a name="design-concepts"></a>Principes de conception

Il existe plusieurs facteurs dans le choix de l’icône standard appropriée qui, en partie, explique pourquoi ils sont souvent utilisés de manière incorrecte. Les erreurs les plus courantes sont les suivantes :

-   Utilisation d’une icône d’avertissement pour les erreurs mineures. Les avertissements ne sont pas des erreurs « adoucies ».
-   Utilisation d’une icône standard quand il est préférable d’utiliser aucune icône. Tous les messages n’ont pas besoin d’une icône.
-   Alarme des utilisateurs en donnant des avertissements pour des problèmes mineurs ou en présentant des questions de routine sous forme d’avertissements. Cela rend les programmes plus sujets aux dangers et perturbe les problèmes réellement importants.

Le reste de cette section explique comment réfléchir aux icônes standard afin d’éviter ces erreurs courantes.

### <a name="message-type-vs-severity"></a>Type de message et gravité

Choisissez les icônes standard en fonction du type de message, et non la gravité du problème sous-jacent. Les types de messages sont les suivants :

-   **Erreurs.** Une erreur ou un problème qui s’est produit.
-   **Tres.** Condition susceptible de provoquer un problème à l’avenir.
-   **Informations.** Informations utiles.

Par conséquent, un message d’erreur peut prendre une icône d’erreur mais jamais une icône d’avertissement. N’utilisez pas d’icônes d’avertissement pour « atténuer » les erreurs mineures. Par conséquent, en dépit de leur différence de gravité, la « taille de police incorrecte » est une erreur, tandis que « la poursuite de cette opération va définir votre maison en cas d’incendie » est un avertissement.

### <a name="determining-the-appropriate-message-type"></a>Détermination du type de message approprié

Certains problèmes peuvent être présentés sous la forme d’une erreur, d’un avertissement ou d’informations, en fonction de l’importance et de la formulation. par exemple, supposons qu’une page Web ne peut pas charger un contrôle de ActiveX non signé basé sur la configuration actuelle de Windows Internet Explorer :

-   **Erreurs.** « cette page ne peut pas charger un contrôle de ActiveX non signé ». (Formulées en tant que problème existant.)
-   **Tres.** « cette page peut ne pas se comporter comme prévu, car Windows Internet Explorer n’est pas configuré pour charger les contrôles de ActiveX non signés ». ou «autoriser cette page à installer un contrôle de ActiveX non signé ? Cette opération à partir de sources non approuvées peut endommager votre ordinateur.» (Les deux formulées comme des conditions qui peuvent entraîner des problèmes futurs.)
-   **Informations.** « vous avez configuré Windows Internet Explorer pour bloquer les contrôles de ActiveX non signés ». (Formulées en tant que déclaration de faits.)

**Pour déterminer le type de message approprié, concentrez-vous sur l’aspect le plus important du problème que les utilisateurs doivent connaître ou agir.** En règle générale, si un problème empêche l’utilisateur de continuer, il est présenté comme une erreur. Si l’utilisateur peut continuer, il s’agit d’un avertissement. Élaborez l' [instruction principale](text-ui.md) ou un autre texte correspondant en fonction de ce Focus, puis choisissez une icône (standard ou autre) qui correspond au texte. Le texte d’instruction principal et les icônes doivent toujours correspondre.

### <a name="severity"></a>Gravité

Si la gravité n’est pas prise en compte lorsque vous choisissez parmi les icônes d’erreur, d’avertissement et d’information, **la gravité est un facteur déterminant si une icône standard doit être utilisée du tout.**

Les icônes fonctionnent mieux quand elles sont utilisées pour communiquer visuellement. (Notez que pour des raisons d’accessibilité, cette communication visuelle doit toujours être redondante avec une autre forme, telle que du texte ou du son.) Les utilisateurs doivent être en mesure de déterminer en un clin d’œil la nature des informations et les conséquences de leur réponse. nous devons donc différencier les erreurs critiques et les avertissements de leurs équivalents ordinaires. Les erreurs critiques et les avertissements présentent les caractéristiques suivantes :

-   Elles impliquent la perte potentielle d’un ou plusieurs des éléments suivants :
    -   Une ressource précieuse, telle qu’une perte de données ou une perte financière.
    -   Accès ou intégrité du système.
    -   Confidentialité ou contrôle des informations confidentielles.
    -   Temps de l’utilisateur (quantité significative, par exemple, 30 secondes ou plus).
-   Ils ont des conséquences inattendues ou indésirables.
-   Ils requièrent désormais une gestion correcte, car les erreurs ne peuvent pas être facilement corrigées et peuvent même être irréversibles.

Pour distinguer les erreurs et les avertissements non critiques de ceux critiques, les messages non critiques sont généralement affichés sans icône. cela attire l’attention sur les messages critiques, rend les messages critiques et non critiques visuellement distincts et est cohérent avec le [ton Windows](text-style-tone.md).

Tous les messages n’ont pas besoin d’une icône. Les icônes ne sont pas un moyen de décorer des messages.

Voici un bon exemple d’avertissement critique, car il répond aux caractéristiques définies précédemment.

![capture d’écran d’un avertissement pour sauvegarder des données ](images/vis-std-icons-image2.png)

Dans cet exemple, un avertissement critique avertit les utilisateurs de la perte potentielle de données irréversibles.

Toutefois, l’exemple suivant n’est pas critique parce qu’il est susceptible d’être intentionnel et que ses résultats sont facilement annulés.

**Incorrect :**

![capture d’écran d’une utilisation trompeuse d’une icône d’avertissement ](images/vis-std-icons-image3.png)

Dans cet exemple, cette [confirmation](mess-confirm.md) n’est pas critique, car elle est susceptible d’être intentionnelle et facilement annulée.

Dans une interface utilisateur classique, la plupart des erreurs sont liées à des erreurs d’entrée d’utilisateur. La plupart des erreurs d’entrée utilisateur ne sont pas critiques, car elles sont facilement corrigées et les utilisateurs doivent les corriger avant de continuer. en outre, le fait d’attirer trop attention sur des erreurs mineures de l’utilisateur est contraire au ton Windows. Par conséquent, les erreurs d’entrée utilisateur mineures sont généralement affichées sans icône d’erreur. Pour renforcer leur nature non critique, nous faisons référence à ceux-ci en tant que problèmes d’entrée d’utilisateur.

![capture d’écran informant les utilisateurs de l’entrée correcte ](images/vis-std-icons-image4.png)

Dans cet exemple, ce problème mineur d’entrée utilisateur n’est pas critique, donc il n’a pas besoin d’une icône quand elle est présentée dans une boîte de dialogue.

### <a name="avoid-overwarning"></a>Éviter le suravertissement

nous prévoyons dans Windows programmes. le programme de Windows classique possède des icônes d’avertissement apparemment partout, ce qui vous avertit des choses qui ont une importance minime. Dans certains programmes, presque toutes les questions sont présentées sous la forme d’un avertissement. Le suravertissement permet d’utiliser un programme comme une activité dangereuse et de délivrer des problèmes réellement significatifs.

Le seul risque de perte de données est insuffisant pour appeler une icône d’avertissement. En outre, les résultats indésirables doivent être inattendus ou involontaires, et ne peuvent pas être facilement corrigés. Dans le cas contraire, une question incorrecte peut être interprétée pour entraîner la perte de données d’un certain type et mériter une icône d’avertissement.

Pour concentrer les icônes d’avertissement sur les problèmes réellement critiques :

-   Assurez-vous que le problème justifie l’attention de l’utilisateur. Les [confirmations de routine](mess-confirm.md) et les questions ne doivent pas avoir d’icônes d’avertissement.
-   Les utilisateurs risquent-ils de se comporter différemment en raison de l’icône d’avertissement ? Les utilisateurs sont-ils susceptibles de prendre en compte la décision plus soigneusement ?

**Incorrect :**

![capture d’écran de l’icône d’avertissement utilisée inutilement ](images/vis-std-icons-image5.png)

Dans cet exemple, les utilisateurs sont susceptibles de répondre différemment à cette question en raison de l’icône d’avertissement.

-   Y a-t-il une action importante à effectuer ou à prendre une décision ? Les avertissements sans action font simplement des utilisateurs le sentiment paranoïaques.

**Incorrect :**

![capture d’écran de l’icône d’avertissement utilisée avec le rappel ](images/vis-std-icons-image6.png)

Pourquoi cette notification a-t-elle un avertissement ? Que sont les utilisateurs censés faire (en plus de la préoccupation) ?

### <a name="context"></a>Contexte

Le contexte est également un facteur à prendre en compte lors de l’utilisation d’icônes standard, car le contexte communique des informations. En particulier :

-   Si les boîtes de dialogue (y compris les boîtes de dialogue de tâches et les boîtes de message) et les notifications n’ont pas besoin d’icônes pour les erreurs non critiques, les erreurs sur place nécessitent toujours des icônes d’erreur. Dans le cas contraire, ces commentaires non modaux seraient trop faciles à ignorer.
-   Les avertissements sur place ont toujours besoin d’icônes d’avertissement pour les distinguer du texte normal.
-   Les boîtes de dialogue, les notifications et les bulles n’ont pas besoin d’icônes d’informations car elles présentent clairement des informations. En revanche, les bannières requièrent des informations de 16 x 16 pixels ou d’autres icônes, car ces commentaires non modaux seraient trop faciles à oublier.

Étant donné que le contexte est un facteur important de l’utilisation des icônes, les règles d’icône standard de cet article sont fournies en termes de contexte.

### <a name="evaluating-standard-icon-appropriateness"></a>Évaluation de l’adéquation des icônes standard

Lors de l’évaluation du texte de l’interface utilisateur, lisez également les icônes standard. Lisez les icônes d’erreur comme « erreur ! », les icônes d’avertissement comme « avertissement, soyez très prudent ici ! » et les icônes d’informations « attention ! ». Continuez ensuite à lire le contexte restant, comme les boutons instruction principale, zone de contenu et valider. Assurez-vous que la signification et la tonalité de chaque icône standard correspondent à la signification et au ton de son contexte. Si ce n’est pas le cas, vous avez rencontré un problème.

**Si vous n’avez qu’une seule chose...**

Assurez-vous que la signification et la tonalité de chaque icône standard correspondent à la signification et au ton de son contexte. Si elles ne correspondent pas, modifiez ou supprimez l’icône.

## <a name="guidelines"></a>Consignes

**Remarque :** Pour les recommandations suivantes, « sur place » signifie sur toute surface de fenêtre normale, par exemple dans la zone de contenu d’un Assistant, une feuille de propriétés ou une page d’élément du panneau de configuration.

### <a name="general"></a>Général

-   Choisissez les icônes standard en fonction de leur type de message, et non pas de la gravité du problème sous-jacent :
    -   **Erreurs.** Une erreur ou un problème qui s’est produit.
    -   **Tres.** Condition susceptible de provoquer un problème à l’avenir.
    -   **Informations.** Informations utiles.
-   Si un problème chevauche différents types de messages, concentrez-vous sur l’aspect le plus important sur lequel les utilisateurs doivent agir.
-   Les icônes doivent toujours correspondre à l’instruction principale ou à un autre texte correspondant.

**Correct :**

![capture d’écran de l’icône d’erreur utilisée avec le texte d’erreur ](images/vis-std-icons-image7.png)

**Incorrect :**

![capture d’écran de l’icône d’avertissement utilisée avec le texte d’erreur ](images/vis-std-icons-image8.png)

Dans l’exemple incorrect, l’icône d’avertissement standard ne correspond pas à l’instruction principale (qui génère une erreur).

### <a name="icon-size"></a>Taille d'icône

-   **Choisissez la taille d’icône standard en fonction du contexte :**
  



    | Contexte                         | Quand l’utiliser                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Boîtes de dialogue<br/>  | Utiliser des pixels 32 x 32 pour les icônes de la zone de contenu ; 16x16 pixels pour les icônes de la zone de note de bas de page.<br/> |
    | Sur place<br/>      | Utilisez 32 x 32 pixels pour les pages d’erreur ; icônes de 16x16 pixels pour toutes les autres.<br/>           |
    | Notifications<br/> | Utilisez des icônes de 16 x 16 pixels.<br/>                                                       |
    | Bulles<br/>      | Utilisez des icônes de 16 x 16 pixels.<br/>                                                       |
    | Bande<br/>       | Utilisez des icônes de 16 x 16 pixels.<br/>                                                       |



 

### <a name="error-icons"></a>Icônes d’erreur

-   **Utilisez les icônes d’erreur uniquement lorsqu’une erreur ou un problème s’est produit :**



    | Contexte                           | Quand l’utiliser                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Boîtes de dialogue<br/>    | À utiliser pour les erreurs critiques uniquement. (n’utilisez pas les icônes standard pour les erreurs non critiques.) <br/> ![Capture d’écran montrant l’icône d’erreur utilisée avec un message d’erreur ](images/vis-std-icons-image9.png)<br/>                                              |
    | Erreurs sur place<br/> | Utilisez pour toutes les erreurs. <br/> ![capture d’écran de l’icône d’erreur utilisée avec un message d’erreur.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notifications<br/>   | À utiliser pour les erreurs critiques uniquement. (pour les [échecs d’action](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx).) <br/> ![Capture d’écran montrant une icône d’erreur utilisée avec un message d’erreur de notification.](images/vis-std-icons-image11.png)<br/> |
    | Bulles<br/>        | Ne pas utiliser. Les bulles ne doivent pas être utilisées pour les erreurs critiques et elles n’ont pas besoin d’icônes d’erreur pour les erreurs non critiques.<br/>                                                                                                               |
    | Bande<br/>         | Ne pas utiliser. Les bannières ne doivent pas être utilisées pour les erreurs.<br/>                                                                                                                                                                                  |



 

-   En règle générale, les icônes d’erreur ne sont pas nécessaires pour les problèmes d’entrée d’utilisateur non critiques. Toutefois, les icônes sont nécessaires pour les erreurs sur place, car dans le cas contraire, ces commentaires contextuels seraient trop faciles à oublier.
-   **Pour les boîtes de dialogue de tâche, n’utilisez pas d’icône d’erreur de note de bas de page.** Les icônes d’erreur doivent être présentées uniquement dans la zone de contenu.

### <a name="warning-icons"></a>Icônes d’avertissement

-   **Utilisez les icônes d’avertissement uniquement lorsqu’une condition peut entraîner un problème à l’avenir :**



    | Contexte                             |  Quand l’utiliser                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Boîtes de dialogue<br/>      | Utilisez pour tous les avertissements. <br/> ![capture d’écran de l’avertissement de modification d’extension de nom de fichier ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Avertissements sur place<br/> | Utilisez pour identifier le texte comme un avertissement. <br/> ![capture d’écran de l’avertissement indiquant que l’espace libre est insuffisant ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notifications<br/>     | Utilisez pour tous les avertissements. (pour les [événements système non critiques](glossary.md).) <br/> ![capture d’écran de la notification d’avertissement de batterie faible ](images/vis-std-icons-image14.png)<br/> |
    | Bulles<br/>          | À utiliser pour les [conditions spéciales](ctrl-balloons.md). <br/> ![capture d’écran de l’avertissement de la bulle de Verr. Maj ](images/vis-std-icons-image15.png)<br/>                           |
    | Bande<br/>           | Utilisez pour attirer l’attention sur la bannière. <br/> ![capture d’écran de la bannière avec avertissement de module de plateforme sécurisée manquant ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **N’utilisez pas les icônes d’avertissement pour « atténuer » les erreurs non critiques.** Les erreurs ne sont pas des avertissements appliquez les règles d’icône d’erreur à la place.
-   **Pour les boîtes de dialogue de question, utilisez des icônes d’avertissement uniquement pour les questions ayant des conséquences importantes.** N’utilisez pas d’icônes d’avertissement pour les questions de routine.

**Correct :**

![capture d’écran Avertissement pour ne pas arrêter la restauration du système ](images/vis-std-icons-image17.png)

**Incorrect :**

![capture d’écran d’avertissement concernant le rejet des rappels ](images/vis-std-icons-image18.png)

Dans l’exemple incorrect, une icône d’avertissement est utilisée de manière incorrecte pour une question de routine.

-   **Pour les boîtes de dialogue de tâches, vous pouvez utiliser une icône d’avertissement de note de bas de page pour avertir les utilisateurs des conséquences risquées.** Toutefois, utilisez une icône d’avertissement dans la zone de contenu ou la zone de note de bas de page, mais pas les deux.

![capture d’écran de l’avertissement d’un fichier potentiellement dangereux ](images/vis-std-icons-image19.png)

Dans cet exemple, un bouclier de sécurité jaune est utilisé dans une note de bas de page.

### <a name="information-icons"></a>Icônes d’informations

-   **Utilisez les icônes d’informations uniquement lorsque le contexte ne présente manifestement pas d’informations :**



    | Contexte                         | Quand l’utiliser                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Boîtes de dialogue<br/>  | Ne pas utiliser.<br/>                                                                                                                             |
    | Sur place<br/>      | Ne pas utiliser. Utilisez plutôt un texte brut statique ou une bannière.<br/>                                                                           |
    | Notifications<br/> | Ne pas utiliser.<br/>                                                                                                                             |
    | Bulles<br/>      | Ne pas utiliser.<br/>                                                                                                                             |
    | Bande<br/>       | Utilisez pour attirer l’attention sur la bannière. <br/> ![capture d’écran de la bannière avec les informations de paramètres ](images/vis-std-icons-image20.png)<br/> |



 

-   Les icônes d’informations ne sont pas nécessaires dans les boîtes de dialogue, les notifications et les bulles, car leur contexte communique suffisamment pour fournir des informations aux utilisateurs.
-   **Pour les boîtes de dialogue de tâche, n’utilisez pas d’icônes de note de bas de page.** Les notes de bas de page sont suffisamment visibles et ne disent pas qu’il s’agit d’informations.

### <a name="question-mark-icons"></a>Icônes de point d’interrogation

-   **Utilisez l’icône point d’interrogation uniquement pour les points d’entrée de l’aide.** Pour plus d’informations, consultez les instructions relatives aux [points d’entrée](winenv-help.md) de l’aide.
-   **N’utilisez pas l’icône de point d’interrogation pour poser des questions.** Là encore, utilisez l’icône de point d’interrogation uniquement pour les points d’entrée de l’aide. Il n’est pas nécessaire de poser des questions à l’aide de l’icône de point d’interrogation. il suffit de présenter une instruction principale comme question.
-   **Ne remplacez pas régulièrement les icônes de point d’interrogation par des icônes d’avertissement.** Remplacez l’icône du point d’interrogation par une icône d’avertissement uniquement si la question a des conséquences significatives. Sinon, n’utilisez aucune icône.

 


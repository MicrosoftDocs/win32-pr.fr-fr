---
title: Première expérience
description: Dans la première expérience idéale, les utilisateurs installent votre programme et l’utilisent immédiatement de manière productive, sans avoir à répondre à une série de questions ou à apprendre un ensemble de choses.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 04610b75e8ca4ea7602d00b840bbbd9002397d9e
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524453"
---
# <a name="first-experience"></a>Première expérience

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Dans la première expérience idéale, les utilisateurs installent votre programme et l’utilisent immédiatement de manière productive, sans avoir à répondre à une série de questions ou à apprendre un ensemble de choses.

Une interface utilisateur de première expérience aide les utilisateurs à passer de leur première exposition à un nouveau programme ou une nouvelle fonctionnalité à l’utilisation quotidienne.

Pour les programmes Windows, la première expérience initiale se produit lorsque les utilisateurs exécutent le programme d’installation. Les programmes d’installation sont généralement :

-   Oblige l’utilisateur à accepter un contrat de licence utilisateur final (CLUF).
-   Demandez une clé de produit.
-   Présente les options requises liées à la configuration, y compris l’installation de logiciels facultatifs.
-   Copiez le logiciel sur le disque dur de l’utilisateur.
-   Présente les options de programme qui s’appliquent à tous les utilisateurs.

![capture d’écran de la boîte de dialogue « tapez votre clé de produit » ](images/exper-first-exper-image1.png)

Une partie de l’expérience d’installation de Windows classique.

La première expérience continue ensuite à la première utilisation du programme ou de la fonctionnalité. Cette première utilisation peut :

-   Présente les options de programme qui s’appliquent uniquement à l’utilisateur actuel.
-   Proposez des didacticiels sur les produits ou les fonctionnalités.

![capture d’écran de la boîte de dialogue « Centre d’accueil » ](images/exper-first-exper-image2.png)

Première expérience d’utilisation.

**Remarque :** Les instructions relatives aux [options de programme](win-property-win.md) sont présentées dans un article distinct.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour décider, posez-vous les questions suivantes.

### <a name="setup-experience"></a>Expérience d’installation

Les conditions suivantes s’appliquent-elles ?

-   Les paramètres corrects sont requis pour utiliser le programme et s’appliquent à tous les utilisateurs.
-   Les paramètres personnalisent une expérience de base ou un essentiel à l’identification personnelle de l’utilisateur avec le programme.
-   Il n’y a pas de valeur par défaut sécurisée, l’utilisateur est susceptible de choisir des paramètres qui ne sont pas la valeur par défaut, ou les paramètres par défaut nécessitent le consentement de l’utilisateur.
-   Il est peu probable que l’utilisateur modifie les paramètres après l’installation.
-   La modification des paramètres nécessite une élévation.

Dans ce cas, envisagez de présenter les paramètres lors de l’installation.

### <a name="first-use-experience"></a>Expérience de première utilisation

Les conditions suivantes s’appliquent-elles ?

-   Les paramètres ou tâches appropriés sont requis pour utiliser le programme ou la fonctionnalité, et ils s’appliquent à des utilisateurs individuels.
-   Les paramètres personnalisent une expérience de base ou un essentiel à l’identification personnelle de l’utilisateur avec le programme.
-   Il n’y a pas de valeur par défaut sécurisée, l’utilisateur est susceptible de choisir des paramètres qui ne sont pas la valeur par défaut, ou les paramètres par défaut nécessitent le consentement de l’utilisateur.
-   Les utilisateurs sont susceptibles de faire de meilleurs choix dans le contexte du programme que dans le programme d’installation.
-   Il est peu probable que l’utilisateur modifie les paramètres à l’aide des options.

Dans ce cas, envisagez de présenter les tâches et les paramètres lors de la première utilisation du programme ou de la fonctionnalité.

## <a name="design-concepts"></a>Principes de conception

Dans la première expérience idéale, les utilisateurs installent votre programme (ou même le démarrent s’ils ne nécessitent pas d’installation) et l’utilisent de manière productive immédiatement sans répondre à une série de questions ou apprendre une série de choses.

Cette solution idéale peut être obtenue pour la plupart des programmes. vous devez donc vous efforcer de cette expérience idéale chaque fois que vous le pouvez. Toutefois, cet objectif n’est souvent pas disponible pour les programmes qui nécessitent une intégration système importante, disposent de nombreuses fonctionnalités facultatives ou ont des implications en matière de confidentialité. Par exemple, si votre programme possède des fonctionnalités susceptibles de révéler des informations personnelles à des tiers non fiables, les principes de l' [informatique fiable](https://www.microsoft.com/mscorp/twc/default.mspx) nécessitent que vous obteniez le consentement de l’utilisateur avant d’activer ces fonctionnalités.

### <a name="questions-arent-choices"></a>Les questions ne sont pas des choix

Les questions requièrent des réponses pour que les utilisateurs puissent continuer. Les questions au cours de la première expérience sont les obstacles que les utilisateurs doivent sauter avant de pouvoir utiliser votre programme de manière productive. En revanche, les choix sont facultatifs. Les utilisateurs n’ont pas à y répondre ou peuvent choisir de les afficher uniquement lorsqu’ils le souhaitent.

Ainsi, les paramètres présentés dans le processus principal d’un assistant d’installation sont des questions, alors que les paramètres en dehors du déroulement de l’installation principale ou dans une boîte de dialogue Options du programme sont des choix. Des questions inutiles rendent la première expérience de votre programme plus lourde et fastidieuse, en éliminant efficacement l’anticipation positive et l’excitation des utilisateurs sur la prise en main de votre programme.

### <a name="use-the-first-experience-when-you-must"></a>Utilisez la première expérience lorsque vous devez

Présentez les paramètres et les tâches aux utilisateurs lors des premières expériences lorsque vous devez, mais il existe généralement de meilleures alternatives :



| Première expérience  | Autres solutions       |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Questions sur l’installation<br/>                  | Sélectionnez les valeurs par défaut appropriées.<br/> Autorisez les utilisateurs à modifier les options du programme.<br/> Fournissez des chemins d’installation par défaut et personnalisés. <br/> |
| Questions relatives à la première utilisation<br/>              | Sélectionnez les valeurs par défaut appropriées et autorisez les utilisateurs à modifier les options du programme.<br/>                                                            |
| Tâches de première utilisation<br/>                  | Présenter à la place en contexte.<br/>                                                                                                           |
| Première utilisation des publications de fonctionnalités<br/> | Rendez les tâches les plus courantes et les plus importantes détectables et contextuelles.<br/>                                                                   |
| Didacticiels de première utilisation<br/>              | Rendez les fonctionnalités du programme explicites.<br/>                                                                                                 |
| Inscription du produit<br/>             | Commande fournir dans le menu aide et la zone à propos de.<br/>                                                                                             |



 

**Si vous n’avez qu’une seule chose...**

Gardez votre première expérience aussi simple que possible. Faites fonctionner votre programme immédiatement. Choisissez les valeurs par défaut sécurisées, sécurisées et pratiques, et posez des questions lors de l’installation et utilisez d’abord uniquement lorsque vous en avez besoin.

Vous n’avez qu’une seule chance de faire une bonne première impression et la première impression est durable.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Généralités

-   **Limitez les premières expériences aux tâches et aux paramètres nécessaires à l’utilisation d’un programme ou d’une fonctionnalité, et incluez-les uniquement lorsqu’il n’existe aucune meilleure solution.** Pour plus d’options, consultez le tableau précédent.
    -   **Exception :** Ajoutez des paramètres de personnalisation de personnalisation ou de programme à la première expérience si leur personnalisation fait partie de l’expérience de base ou cruciale pour l’identification personnelle de l’utilisateur avec le programme.

![capture d’écran de la boîte de dialogue’taper un nom d’ordinateur' ](images/exper-first-exper-image3.png)

Windows demande aux utilisateurs le nom de l’ordinateur et le choix de l’arrière-plan lors de l’installation, car ces paramètres aident à former une connexion émotionnelle au produit.

-   **Utilisez l’expérience d’installation** pour les tâches et les paramètres s’ils s’appliquent à tous les utilisateurs ou si la modification des paramètres nécessite une élévation.
-   **Utilisez la première expérience d’utilisation** pour les tâches et les paramètres s’ils s’appliquent à des utilisateurs individuels.

### <a name="presentation"></a>Présentation

-   **Préférez des tâches et des paramètres facultatifs aux tâches et paramètres requis.** Évitez de forcer les utilisateurs à configurer votre programme.

    ![capture d’écran de la boîte de dialogue « détection d’un nouveau matériel » ](images/exper-first-exper-image4.png)

    La boîte de dialogue Nouveau matériel détecté permet d’installer le logiciel du pilote au lieu d’effectuer une tâche obligatoire.

-   **Effectuez des tâches et des paramètres facultatifs à partir du déroulement principal des tâches chaque fois que cela est possible.** Par exemple, de nombreux programmes d’installation fournissent un chemin d’installation personnalisé pour supprimer les paramètres rarement modifiés du principal déroulement des tâches.

    ![capture d’écran des cases d’option complètes et personnalisées ](images/exper-first-exper-image5.png)

    Une expérience d’installation qui facilite le processus principal des tâches si l’utilisateur n’envisage pas de personnaliser l’installation.

-   **N’encombrez pas les utilisateurs avec des tâches et des paramètres :**
    -   **Commencez doucement.** Commencez avec des paramètres de personnalisation simples et progressez vers des tâches et des paramètres plus complexes et techniques. Par exemple, le programme d’installation de Windows démarre avec les informations personnelles et se termine par la configuration du réseau.
    -   **Utilisez une première expérience contextuelle** pour les tâches et les paramètres s’ils s’appliquent uniquement aux fonctionnalités qui ne sont pas fondamentales pour le programme principal.

        ![capture d’écran de la boîte de dialogue « Configuration audio et vidéo » ](images/exper-first-exper-image6.png)

        Windows Live Messenger dispose d’une configuration contextuelle pour l’audio et la vidéo, car elles sont utilisées par des fonctionnalités secondaires.

-   **Ne présentez pas tous les éléments en même temps.** Consolidez pour utiliser une seule interface utilisateur au lieu de plusieurs surfaces d’interface utilisateur, ou affichez les tâches à des moments différents et non en une seule fois.

    **Incorrect :**

    ![capture d’écran de cinq boîtes de dialogue superposées ](images/exper-first-exper-image7.png)

    Dans cet exemple, la première expérience d’utilisation est insurmontable.

-   **Posez des questions et des options en termes de objectifs et de tâches des utilisateurs, et non en termes de technologie.** Fournissez des options que les utilisateurs comprennent et distinguent clairement. Veillez à fournir suffisamment d’informations pour que les utilisateurs prennent des décisions avisées.
-   **Si le besoin d’informations personnelles n’est pas évident, expliquez pourquoi votre programme a besoin des informations et de la façon dont il sera utilisé.**

    ![capture d’écran du texte indiquant l’utilisation de l’adresse de messagerie ](images/exper-first-exper-image8.png)

    Dans cet exemple, une application de commerce électronique explique comment utiliser les informations personnelles.

-   **Présentez les premières expériences en mode plein écran uniquement si les utilisateurs ne peuvent pas effectuer d’autres tâches de manière productive.** Par exemple, le programme d’installation de Windows s’affiche en mode plein écran pour dissuader les utilisateurs d’effectuer d’autres tâches pendant l’installation de Windows. La plupart des premières expériences ne doivent pas être en plein écran.

### <a name="settings"></a>Paramètres

-   **Pour tous les paramètres, sélectionnez le plus sûr (pour éviter la perte de données ou l’accès au système), la valeur la plus sûre et la valeur privée par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la valeur la plus probable ou la plus pratique. Choisir les valeurs par défaut appropriées est un moyen efficace de simplifier la première expérience.
-   **Demander aux utilisateurs de s’abonner à :**

    -   Paramètres avec implications juridiques, tels que les contrats de licence utilisateur final (CLUF). Ces paramètres ne peuvent pas avoir de sélections par défaut.
    -   Fonctionnalités qui effectuent des modifications automatiques de la configuration du système, telles que les mises à jour automatiques de Windows.
    -   Fonctionnalités qui révèlent des informations d’identification personnelle (PII) ou des informations système.
    -   Les modifications apportées au bureau de l’utilisateur au-delà de l’ajout d’entrées au menu Démarrer, telles que l’ajout d’icônes au bureau ou à la barre de lancement rapide.
    -   Logiciels facultatifs, tels que les améliorations du produit, les abonnements et les produits tiers.

    ![capture d’écran de la boîte de dialogue Choisir les fonctionnalités souhaitées ](images/exper-first-exper-image9.png)

    Dans cet exemple, les utilisateurs choisissent les améliorations du produit, les abonnements et les produits tiers.

-   **Si un paramètre est fortement recommandé, ajoutez « (recommandé) » à l’étiquette.** Pour les cases d’option et les cases à cocher, veillez à ajouter à l’étiquette de contrôle, et non aux notes supplémentaires.
-   **Si un paramètre est destiné uniquement aux utilisateurs expérimentés, ajoutez « (avancé) » à l’étiquette.** Pour les cases d’option et les cases à cocher, veillez à ajouter à l’étiquette de contrôle, et non aux notes supplémentaires.

### <a name="tasks"></a>Tâches

-   **Aidez les utilisateurs à passer le temps d’attente de manière productive.**
    -   Si la durée d’attente est généralement comprise entre une et deux minutes, pensez à fournir des informations utiles pendant l’attente des utilisateurs, par exemple une présentation des nouveautés au cours de l’installation.
    -   Si la durée d’attente est généralement supérieure à deux minutes, faciliter l’exécution d’autres tâches pour les utilisateurs. Affichez le temps d’attente estimé, et recommandez-vous que les utilisateurs effectuent une autre tâche en attendant et rendent l’achèvement des tâches évident en modifiant l’écran de manière significative.
-   **Reconsidérez les didacticiels de présentation pendant la première expérience.** Les utilisateurs les plus susceptibles de vouloir utiliser votre programme immédiatement et sont intéressés par les didacticiels ultérieurement.
-   **N’utilisez pas de notifications de publication de fonctionnalités dans la première expérience.** Au lieu d’utiliser une [notification de publication de fonctionnalités](mess-notif.md), vous pouvez concevoir la fonctionnalité de manière à ce qu’elle soit plus facile à découvrir dans les contextes là où elle est nécessaire, ou à ne rien faire d’autre et permettre aux utilisateurs de découvrir la fonctionnalité de manière autonome.
-   **N’utilisez pas de notifications au cours de l’expérience Windows initiale.** Pour améliorer sa première expérience, Windows 7 supprime toutes les notifications affichées au cours des premières heures d’utilisation. Concevez votre programme en supposant que les utilisateurs ne verront pas ces notifications.

 


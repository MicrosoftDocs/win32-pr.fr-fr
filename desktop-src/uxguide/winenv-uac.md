---
title: Contrôle de compte d’utilisateur (concepts de base de conception)
description: Une expérience de contrôle de compte utilisateur bien conçue permet d’éviter les modifications indésirables à l’ensemble du système d’une manière prévisible et nécessitant un minimum d’effort.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b346e5cb581ac83ad2ebffabe73c5fbed636d814
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554595"
---
# <a name="user-account-control"></a>Contrôle de compte d'utilisateur

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une expérience de contrôle de compte utilisateur bien conçue permet d’éviter les modifications indésirables à l’ensemble du système d’une manière prévisible et nécessitant un minimum d’effort.

Avec le contrôle de compte d’utilisateur (UAC) entièrement activé, les administrateurs interactifs s’exécutent normalement avec le moins de privilèges utilisateur, mais ils peuvent s’élever automatiquement pour effectuer des tâches d’administration en donnant un consentement explicite avec l’interface utilisateur de consentement. Ces tâches d’administration incluent l’installation de logiciels et de pilotes, la modification des paramètres au niveau du système, l’affichage ou la modification d’autres comptes d’utilisateur et l’exécution d’outils d’administration.

Dans leur état le moins privilégié, les administrateurs sont appelés administrateurs protégés. Dans leur état élevé, elles sont appelées administrateurs élevés. En revanche, les utilisateurs standard ne peuvent pas s’élever eux-mêmes, mais ils peuvent demander à un administrateur de les élever à l’aide de l’interface utilisateur des informations d’identification. Le compte administrateur intégré ne nécessite pas d’élévation.

![capture d’écran du message de sécurité « autoriser le programme » ](images/winenv-uac-image1.png)

L’interface utilisateur de consentement, utilisée pour élever les administrateurs protégés à avoir des privilèges d’administrateur.

![capture d’écran du message demandant le mot de passe ](images/winenv-uac-image2.png)

Interface utilisateur d’informations d’identification, utilisée pour élever les utilisateurs standard.

Le contrôle de compte d’utilisateur offre les avantages suivants :

-   Cela réduit le nombre de programmes qui s’exécutent avec des privilèges élevés, ce qui contribue à empêcher les utilisateurs de modifier accidentellement leurs paramètres système et à empêcher les « programmes malveillants » d’obtenir un accès à l’ensemble du système. Lorsque l’élévation est refusée, le programme malveillant est uniquement en mesure d’affecter les données de l’utilisateur actuel. Sans élévation, les logiciels malveillants ne peuvent pas apporter de modifications au niveau du système ou affecter d’autres utilisateurs.
-   Pour les [environnements gérés](glossary.md), les expériences UAC bien conçues permettent aux utilisateurs d’être plus productifs lorsqu’ils s’exécutent en tant qu’utilisateurs standard en supprimant les restrictions inutiles.
-   Il permet aux utilisateurs standard de demander aux administrateurs de leur donner l’autorisation d’effectuer des tâches administratives au sein de leur session actuelle.
-   Pour les environnements familiaux, il offre un meilleur contrôle parental sur les modifications à l’ensemble du système, notamment sur les logiciels installés.

**Développeurs :** Pour plus d’informations sur l’implémentation, consultez [reconception de l’interface utilisateur pour la compatibilité UAC](/previous-versions/bb756990(v=msdn.10)).

Dans Windows Vista, les administrateurs protégés peuvent choisir d’être avertis de toutes les modifications système, ou aucun. Le paramètre UAC par défaut permet de notifier toutes les modifications, quelle que soit leur origine. Lorsque vous êtes informé, votre bureau est grisé et vous devez approuver ou refuser la demande dans la boîte de dialogue contrôle de compte d’utilisateur avant de pouvoir faire quoi que ce soit d’autre sur votre ordinateur. La gradation de votre bureau est appelée [Bureau sécurisé](glossary.md) , car d’autres programmes ne peuvent pas s’exécuter pendant qu’elle est grisée.

Windows 7 introduit deux paramètres intermédiaires de contrôle de compte d’utilisateur pour les administrateurs protégés, en plus des deux de Windows Vista. La première consiste à avertir les utilisateurs uniquement lorsqu’un programme effectue la modification, de sorte que les administrateurs sont automatiquement élevés lorsqu’ils effectuent eux-mêmes une modification. Il s’agit du paramètre UAC par défaut dans Windows 7, qui utilise également le Bureau sécurisé.

Le deuxième paramètre intermédiaire de Windows 7 est le même que le premier, sauf qu’il n’utilise pas le Bureau sécurisé.

![capture d’écran de quatre paramètres de contrôle de compte d’utilisateur dans Windows 7 ](images/winenv-uac-image3.png)

Windows 7 introduit deux paramètres intermédiaires de contrôle de compte d’utilisateur.

**Remarque :** Les instructions relatives à l’écriture de [code pour prendre en charge le contrôle de compte d’utilisateur](/previous-versions/aa905330(v=msdn.10)) sont présentées dans un article distinct.

## <a name="design-concepts"></a>Principes de conception

**Objectifs**

Une expérience de contrôle de compte d’utilisateur bien conçue a les objectifs suivants :

-   **Éliminez l’élévation inutile.** Les utilisateurs doivent avoir à élever uniquement pour effectuer des tâches qui requièrent des privilèges d’administrateur. Toutes les autres tâches doivent être conçues pour éliminer le besoin d’élévation. Souvent, les logiciels hérités nécessitent des privilèges d’administrateur inutilement en écrivant dans les sections de Registre HKLM ou HKCR, ou les fichiers programme ou les dossiers système Windows.
-   **Soyez prévisible.** Les utilisateurs standard doivent savoir quelles tâches requièrent un administrateur pour effectuer ou ne peuvent pas être exécutées du tout dans les environnements gérés. Les administrateurs doivent savoir quelles tâches requièrent une élévation. S’ils ne peuvent pas prédire la nécessité d’une élévation précise, ils sont plus enclins à donner leur consentement pour les tâches administratives lorsqu’ils ne le devraient pas.
-   **Nécessite un minimum d’effort.** Les tâches qui requièrent des privilèges d’administrateur doivent être conçues pour exiger une seule élévation. Les tâches qui requièrent plusieurs élévations deviennent rapidement fastidieuses.
-   **Rétablissez les privilèges minimum.** Une fois qu’une tâche nécessitant des privilèges d’administration est terminée, le programme doit revenir à l’état du privilège le moins important.

**Déroulement de la tâche d’élévation**

Quand une tâche requiert une élévation, elle présente les étapes suivantes :

1.  **Point d’entrée.** Les tâches qui nécessitent une élévation immédiate Lorsque UAC est entièrement activé ont des points d’entrée marqués avec la protection UAC. Dans ce cas, les utilisateurs doivent s’attendre à voir une interface utilisateur d’élévation immédiatement après avoir cliqué sur ces commandes. elles doivent être très prudentes quand elles voient l’interface utilisateur d’élévation à partir de tâches qui n’ont pas de protection.

    ![capture d’écran des icônes de blindage UAC et de leurs étiquettes ](images/winenv-uac-image4.png)

    Dans cet exemple, les éléments du panneau de configuration contrôle parental et comptes d’utilisateur requièrent une élévation.

    Lorsque le contrôle de compte d’utilisateur est partiellement activé ou complètement désactivé, la protection UAC est toujours affichée pour indiquer que la tâche implique des modifications au niveau du système et nécessite donc une élévation, même si l’utilisateur ne voit pas l’interface utilisateur d’élévation. Toujours afficher le contrôle de compte d’utilisateur pour les tâches qui requièrent une élévation permet de conserver l’interface utilisateur simple et prévisible.

2.  **Altitude.** Pour les administrateurs protégés, la tâche demande le consentement à l’aide de l’interface utilisateur de consentement. Pour les utilisateurs standard, la tâche demande des informations d’identification d’administrateur à l’aide de l’interface utilisateur des informations d’identification.

    ![capture d’écran de deux types d’élévation ](images/winenv-uac-image5.png)

    Ces exemples illustrent l’interface utilisateur des informations d’identification et l’interface utilisateur de consentement.

3.  **Séparer les processus élevés.** En interne, un nouveau processus élevé est créé pour effectuer la tâche.
4.  **Rétablir les privilèges minimum.** Si nécessaire, rétablissez le moindre privilège pour effectuer toutes les étapes qui ne nécessitent pas d’élévation.

Notez que les tâches ne mémorisent pas les États élevés. Par exemple, si l’utilisateur navigue vers l’avant et vers l’arrière sur un point d’entrée d’élévation dans un Assistant, l’utilisateur doit s’élever à chaque fois.

## <a name="usage-patterns"></a>Modèles d’usage

Le contrôle de compte d’utilisateur a plusieurs modèles d’utilisation (par ordre de préférence) :

1.  **Travaillez pour les utilisateurs standard.** Concevez la fonctionnalité pour tous les utilisateurs en limitant son étendue à l’utilisateur actuel. En limitant les paramètres à l’utilisateur actuel (par opposition à l’ensemble du système), vous éliminez le besoin d’une interface utilisateur d’élévation entièrement et permettez aux utilisateurs d’effectuer la tâche.

    **Incorrect :**

    ![capture d’écran du message : vous n’avez pas de privilège ](images/winenv-uac-image6.png)

    Dans cet exemple, les utilisateurs de Windows XP devaient disposer de privilèges d’administrateur pour afficher ou modifier le fuseau horaire actuel.

    **Correct :**

    ![capture d’écran de la boîte de dialogue date et heure ](images/winenv-uac-image7.png)

    Dans cet exemple, la fonctionnalité de fuseau horaire a été repensée dans Windows 7 et Windows Vista pour fonctionner pour tous les utilisateurs.

2.  **Avoir des éléments d’interface utilisateur distincts pour les utilisateurs standard et les administrateurs.** Séparez clairement les tâches utilisateur standard des tâches administratives. Donnez à tous les utilisateurs l’accès à des informations utiles en lecture seule. Identifiez clairement les tâches d’administration avec la protection UAC.

    ![graphique de la protection UAC présentant une élévation requise ](images/winenv-uac-image8.png)

    Dans cet exemple, l’élément du panneau de configuration système affiche son état pour tous les utilisateurs, mais la modification des paramètres au niveau du système nécessite une élévation.

3.  **Autoriser les utilisateurs standard à essayer une tâche et à élever en cas d’échec.** Si les utilisateurs standard peuvent afficher les informations et sont en mesure d’apporter des modifications sans élévation, autorisez-les à accéder à l’interface utilisateur et à les élever uniquement en cas d’échec de la tâche. Cette approche est appropriée lorsque les utilisateurs standard disposent d’un accès limité, par exemple avec les propriétés de leurs propres fichiers dans l’Explorateur Windows. Il est également approprié pour les paramètres sur les pages du concentrateur hybride du panneau de configuration.

    ![la capture d’écran de l’accès est un message refusé ](images/winenv-uac-image9.png)

    Dans cet exemple, l’utilisateur a tenté de modifier les propriétés du fichier programme, mais ne dispose pas de privilèges suffisants. L’utilisateur peut élever et réessayer.

4.  **Travaillez uniquement pour les administrateurs.** Utilisez cette approche uniquement pour les fonctionnalités et les programmes de l’administrateur ! Si une fonctionnalité est destinée uniquement aux administrateurs (et n’a pas de chemins de navigation ou d’informations en lecture seule utiles pour les utilisateurs standard), vous pouvez demander les informations d’identification d’administrateur au point d’entrée avant d’afficher l’interface utilisateur. Utilisez cette approche pour les longs assistants et [flux de pages](glossary.md) lorsque tous les chemins d’accès requièrent des privilèges d’administrateur.

    Si le programme entier est destiné uniquement aux administrateurs, marquez-le pour demander les informations d’identification d’administrateur afin de lancer. Windows affiche ces icônes de programme avec la superposition de protection UAC.

    ![capture d’écran du logo Windows et de la superposition de blindage UAC ](images/winenv-uac-image10.png)

    Dans cet exemple, le programme requiert des privilèges d’administrateur pour lancer.

## <a name="guidelines"></a>Consignes

### <a name="uac-shield-icon"></a>Icône de bouclier UAC

-   **Affichez les contrôles avec la protection UAC pour indiquer que la tâche nécessite une élévation immédiate Lorsque le contrôle de compte d’utilisateur est entièrement activé,** même si le contrôle de compte d’utilisateur n’est pas entièrement activé. Si tous les chemins d’accès d’un Assistant et d’un [Flow de page](glossary.md) requièrent une élévation, affichez la protection UAC au point d’entrée de la tâche. L’utilisation correcte de la protection UAC aide les utilisateurs à prédire quand une élévation est requise.
-   **Si votre programme prend en charge plusieurs versions de Windows, affichez la protection UAC si au moins une version requiert une élévation.** Étant donné que Windows XP ne nécessite jamais d’élévation, envisagez de supprimer les blindages UAC pour Windows XP si vous pouvez le faire de manière cohérente et sans nuire aux performances.
-   **N’affichez pas la protection UAC pour les tâches qui ne nécessitent pas d’élévation dans la plupart des contextes.** Étant donné que cette approche sera parfois trompeuse, l’approche recommandée consiste à utiliser une commande contextuelle correctement protégée à la place.

    ![capture d’écran des fichiers de photos dans l’Explorateur Windows ](images/winenv-uac-image11.png)

    Étant donné que la commande nouveau dossier requiert une élévation uniquement lorsqu’elle est utilisée dans les dossiers système, elle est affichée sans bouclier UAC.

-   La protection UAC peut être affichée sur les contrôles suivants :

    **Boutons de commande :**

    ![capture d’écran du bouton de commande avec l’icône de bouclier UAC ](images/winenv-uac-image12.png)

    Bouton de commande qui requiert une élévation immédiate.

    **Liens de commande :**

    ![capture d’écran du lien de commande avec l’icône de bouclier UAC ](images/winenv-uac-image13.png)

    Un lien de commande qui requiert une élévation immédiate.

    **Liées**

    ![capture d’écran du lien de modification du compte avec la protection UAC ](images/winenv-uac-image14.png)

    Un lien qui requiert une élévation immédiate.

    **Menus**

    ![capture d’écran du menu avec la protection UAC ](images/winenv-uac-image15.png)

    Menu déroulant qui requiert une élévation immédiate.

-   Étant donné que les tâches ne mémorisent pas les États élevés, **ne modifiez pas la protection UAC pour refléter l’État.**
-   **Affichez la protection UAC même si le contrôle de compte d’utilisateur a été désactivé ou si l’utilisateur utilise le compte administrateur intégré.** L’affichage cohérent de la protection UAC est plus facile à programmer et fournit aux utilisateurs des informations sur la nature de la tâche.

### <a name="elevation"></a>Elevation

-   **Dans la mesure du possible, concevez les tâches à effectuer par les utilisateurs standard sans élévation.** Donnez à tous les utilisateurs l’accès à des informations utiles en lecture seule.
-   **Élever sur une base par tâche, et non sur une base par paramètre.** Ne mélangez pas les paramètres utilisateur standard avec les paramètres d’administration dans une page ou une boîte de dialogue unique. Par exemple, si les utilisateurs standard peuvent modifier certains paramètres, mais pas tous, fractionnez-les en tant que surface d’interface utilisateur distincte.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue Paramètres de date et d’heure ](images/winenv-uac-image16.png)

    Dans cet exemple, les paramètres utilisateur standard sont mélangés de manière incorrecte avec les paramètres d’administration.

    **Correct :**

    ![capture d’écran de la même boîte de dialogue sans protection UAC ](images/winenv-uac-image17.png)

    Dans cet exemple, les paramètres de modification de la date et de l’heure se trouvent dans une boîte de dialogue distincte, accessible uniquement aux administrateurs. Les paramètres de fuseau horaire sont disponibles pour les utilisateurs standard et ne sont pas mélangés aux paramètres d’administration.

-   **Ne tenez pas compte de la nécessité d’élever les privilèges lorsque vous déterminez si un contrôle doit être affiché ou désactivé.** La raison est la suivante :
    -   Dans les environnements non gérés, partez du principe que les utilisateurs standard pourraient s’élever en demandant à un administrateur. La désactivation des contrôles qui nécessitent une élévation empêchera les utilisateurs d’élever les privilèges des administrateurs.
    -   Dans les environnements gérés, supposez que les utilisateurs standard ne peuvent pas s’élever du tout. La suppression des contrôles qui nécessitent une élévation empêchera les utilisateurs de savoir quand arrêter la recherche.
-   **Pour éliminer l’élévation inutile :**
    -   **Si une tâche peut nécessiter une élévation, élever le plus tard possible.** Si une tâche a besoin d’une [confirmation](mess-confirm.md), affichez l’interface utilisateur d’élévation uniquement une fois que l’utilisateur a confirmé. Si une tâche requiert toujours une élévation, élever à son point d’entrée.
    -   **Une fois élevé, restez élevé jusqu’à ce que les privilèges élevés ne soient plus nécessaires.** Les utilisateurs ne doivent pas avoir à élever plusieurs fois pour effectuer une seule tâche.
    -   **Si les utilisateurs doivent s’élever pour apporter une modification, mais choisissent de ne pas apporter de modifications, laissez les boutons validation positifs activés, mais gérez la validation comme une annulation.** Cela évite aux utilisateurs d’élever simplement pour fermer une fenêtre.
    -   **Incorrect :**
    -   ![capture d’écran de la fenêtre avec un seul bouton actif ](images/winenv-uac-image18.png)
    -   Dans cet exemple, le bouton enregistrer les modifications est désactivé pour éviter une élévation inutile, mais il est activé lorsque les utilisateurs modifient la sélection. Toutefois, le bouton de validation désactivé donne l’apparence que les utilisateurs n’ont pas vraiment de choix.
-   **N’affiche pas de message d’erreur lorsque les tâches échouent parce que les utilisateurs choisissent de ne pas s’élever.** Supposons que les utilisateurs choisissent intentionnellement de ne pas continuer, donc ils ne considèrent pas cette situation comme une erreur.

    **Incorrect :**

    ![capture d’écran du message : la restauration de Fabrikam ne peut pas être exécutée ](images/winenv-uac-image19.png)

    Dans cet exemple, la restauration de Fabrikam génère incorrectement un message d’erreur lorsque l’utilisateur décide de ne pas s’élever.

-   **N’affichez pas d’avertissements pour expliquer que les utilisateurs peuvent avoir besoin d’élever leurs privilèges pour effectuer des tâches.** Permettez aux utilisateurs de découvrir ce fait par eux-mêmes.
-   **Affichez la protection UAC et l’interface utilisateur d’élévation en fonction du tableau suivant :**

    |                       |                                                                                                                                                                  |                                                                                                                                                                                                                       |                                                                                                      |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Object**      | **Circonstance**                                                                                                                                                | **Où placer la protection UAC**                                                                                                                                                                               | **Quand élever**                                                                            |
    | Programme<br/>    | Le programme entier est destiné uniquement aux administrateurs.<br/>                                                                                                            | ![capture d’écran du logo Windows et de la superposition de blindage UAC ](images/winenv-uac-image10.png)<br/> Superposition de blindage UAC sur l’icône de programme.<br/>                                                                       | Affichez l’interface utilisateur d’élévation au lancement.<br/>                                                           |
    | Commande<br/>    | La commande entière est destinée aux administrateurs uniquement.<br/>                                                                                                            | ![capture d’écran du lien de modification du compte et de la protection UAC ](images/winenv-uac-image14.png)<br/> Bouclier UAC sur le bouton ou le lien de commande.<br/>                                                                      | Afficher l’interface utilisateur d’élévation lorsque l’utilisateur clique sur un bouton ou un lien de commande, mais après toute confirmation.<br/> |
    | Commande<br/>    | La commande affiche des informations en lecture seule utiles appropriées pour tous les utilisateurs, mais les modifications requièrent des privilèges d’administrateur.<br/>                               | ![capture d’écran du lien des paramètres de modification et de la protection UAC ](images/winenv-uac-image8.png)<br/> Bouclier UAC sur un bouton de commande ou un lien pour apporter des modifications.<br/>                                                      | Afficher l’interface utilisateur d’élévation lorsque l’utilisateur clique sur le bouton de commande, mais après toutes les confirmations.<br/>         |
    | Commande<br/>    | Les utilisateurs standard peuvent afficher les informations et éventuellement apporter des modifications sans élévation. autorisez les utilisateurs standard à essayer et à élever en cas d’échec.<br/> | ![capture d’écran d’erreur avec l’icône UAC sur le bouton Réessayer ](images/winenv-uac-image9.png)<br/> N’affiche pas la protection UAC pour la commande, mais l’affiche pour le point d’entrée d’élévation si la commande échoue.<br/> | Affichez l’interface utilisateur d’élévation quand l’utilisateur tente à nouveau la commande.<br/>                                       |
    | Étape de tâche<br/>  | Toutes les étapes suivantes requièrent une élévation.<br/>                                                                                                               | ![capture d’écran du bouton de commande suivant avec la protection UAC ](images/winenv-uac-image20.png)<br/> Bouclier UAC sur le bouton suivant (ou équivalent).<br/>                                                                | Afficher l’interface utilisateur d’élévation lorsque vous cliquez sur suivant ou sur un autre bouton valider.<br/>                         |
    | Étape de tâche<br/>  | Certaines branches requièrent une élévation.<br/>                                                                                                                      | ![capture d’écran du lien de commande avec la protection UAC ](images/winenv-uac-image21.png)<br/> Bouclier UAC sur les liens de commande qui requièrent une élévation.<br/>                                                              | Affichez l’interface utilisateur d’élévation lorsque l’utilisateur clique sur les liens de commande avec la protection UAC.<br/>                      |

    

     

### <a name="elevation-ui"></a>Interface utilisateur d’élévation

-   **Si l’utilisateur fournit un compte qui n’est pas valide (nom ou mot de passe) ou ne dispose pas de privilèges d’administrateur, il vous suffit de réafficher l’interface utilisateur des informations d’identification.** N’affiche pas de message d’erreur.
-   **Si l’utilisateur annule l’interface utilisateur d’informations d’identification, renvoyez l’utilisateur à l’interface utilisateur d’origine.** N’affiche pas de message d’erreur.
-   Si le contrôle de compte d’utilisateur a été désactivé et qu’un utilisateur standard tente d’effectuer une tâche qui nécessite une élévation, fournissez un message d’erreur indiquant «cette tâche nécessite des privilèges d’administrateur. Pour effectuer cette tâche, vous devez ouvrir une session à l’aide d’un compte d’administrateur.»

![la capture d’écran de la tâche nécessite un message de privilèges ](images/winenv-uac-image22.png)

Dans cet exemple, le contrôle de compte d’utilisateur a été désactivé, ce qui signifie qu’un message d’erreur indique que l’utilisateur doit utiliser un compte d’administrateur.

### <a name="wizards"></a>Assistants

-   **Ne pas élever plusieurs fois.** Une fois qu’un Assistant est élevé, il doit rester élevé.
-   Si la tâche est exécutée dans l’Assistant, placez un bouclier UAC sur le bouton « suivant » de la page de validation (qui doit recevoir une [étiquette plus spécifique](win-wizards.md)). Lorsque l’utilisateur valide :
    -   Si la page suivante est une page de progression, passez à cette page et affichez l’interface utilisateur d’élévation de façon modale. Après une élévation réussie, effectuez la tâche.
    -   Si la page suivante est une page de fin, passez à cette page (mais remplacez temporairement son contenu par « en attente d’autorisation... ») et affichez l’interface utilisateur d’élévation de manière modale. Après une élévation réussie, effectuez la tâche, puis affichez le contenu de la page de saisie semi-automatique.
    -   Si l’utilisateur annule l’interface utilisateur d’élévation, revenez à la page valider. Cela permet à l’utilisateur de réessayer.
-   Si la tâche est exécutée à la fin de l’Assistant, placez un bouclier de contrôle de compte d’utilisateur sur le bouton « terminer » de la page de validation (qui doit recevoir une [étiquette plus spécifique](win-wizards.md)). Lorsque l’utilisateur valide :
    -   Rester sur la page de validation et afficher l’interface utilisateur d’élévation de façon modale. Après une élévation réussie, fermez l’Assistant.
    -   Si l’utilisateur annule l’interface utilisateur d’élévation, revenez à la page valider. Cela permet à l’utilisateur de réessayer.
-   Pour les assistants de longue durée destinés uniquement aux administrateurs, vous pouvez demander les informations d’identification de l’administrateur au point d’entrée avant d’afficher l’interface utilisateur.

## <a name="text"></a>Texte

-   **N’utilisez pas de points de suspension juste parce qu’une commande requiert une élévation.** La nécessité d’élever est indiquée par la protection UAC.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence au contrôle de compte d’utilisateur :

-   Reportez-vous à la fonctionnalité contrôle de compte d’utilisateur (sur la première mention) ou UAC (à la mention suivante), pas de compte d’utilisateur ou LUA avec privilèges minimum.
-   Reportez-vous à non-administrateurs en tant qu’utilisateurs standard.
-   Reportez-vous aux administrateurs d’ordinateurs intégrés en tant qu’administrateurs intégrés.

Dans la documentation de l’utilisateur :

-   Reportez-vous à l’action consistant à donner son consentement pour effectuer une tâche administrative en donnant l’autorisation.

En programmation et dans d’autres documentations techniques :

-   Reportez-vous à l’action consistant à donner son consentement pour effectuer une tâche administrative en tant qu’élévation.
-   Dans le contexte du contrôle de compte d’utilisateur, reportez-vous aux administrateurs protégés lorsqu’ils ne sont pas élevés et aux administrateurs élevés après élévation.
-   Reportez-vous à la boîte de dialogue utilisée pour entrer les mots de passe en tant qu’interface utilisateur des informations d’identification. Reportez-vous à la boîte de dialogue utilisée pour donner votre consentement en tant qu’interface utilisateur de consentement. Reportez-vous à la fois en tant qu’interface utilisateur d’élévation.


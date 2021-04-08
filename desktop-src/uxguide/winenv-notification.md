---
title: Zone de notification
description: La zone de notification fournit des notifications et l’État. Les programmes bien conçus utilisent la zone de notification de manière appropriée, sans être gênants ou gênants.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0293038dd155f12b96b22dd1c273a50f1c030ffa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953330"
---
# <a name="notification-area"></a>Zone de notification

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La zone de notification fournit des notifications et l’État. Les programmes bien conçus utilisent la zone de notification de manière appropriée, sans être gênants ou gênants.

La zone de notification est une partie de la barre des tâches qui fournit une source temporaire pour les notifications et l’État. Elle peut également être utilisée pour afficher des icônes pour les fonctionnalités système et de programme qui n’ont aucune présence sur le bureau.

Les éléments de la zone de notification sont appelés icônes de la zone de notification, ou simplement des icônes si le contexte de la zone de notification est déjà clairement établi.

![capture d’écran de la zone de notification, de l’heure et de la date ](images/winenv-notification-image1.png)

Zone de notification.

Pour permettre aux utilisateurs de contrôler leur bureau dans Windows 7, toutes les icônes de la zone de notification ne sont pas affichées par défaut. Au lieu de cela, les icônes sont affichées dans le débordement de la zone de notification, sauf si l’utilisateur les a promues à la zone de notification.

![Capture d’écran montrant une zone de notification et un dépassement de capacité.](images/winenv-notification-image2.png)

Dépassement de capacité de la zone de notification.

**Remarque :** Les instructions relatives à la [barre des tâches](winenv-taskbar.md), aux [notifications](mess-notif.md) et aux [bulles](ctrl-balloons.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **Votre programme doit-il afficher une notification ?** Si c’est le cas, vous devez utiliser une icône de zone de notification.
-   **L’icône s’affiche-t-elle temporairement pour afficher un changement d’État ?** Dans ce cas, une icône de zone de notification peut être appropriée, en fonction des facteurs suivants :

    -   **L’État est-il utile et pertinent ?** Autrement dit, les utilisateurs risquent-ils de surveiller l’icône et de modifier leur comportement en raison de ces informations ? Si ce n’est pas le cas, n’affichez pas l’État ou placez-le dans un fichier journal.

        **Incorrect :**

        ![capture d’écran de la zone de notification avec l’icône de lecteur ](images/winenv-notification-image3.png)

        Dans cet exemple, l’icône d’activité du lecteur de disque n’est pas appropriée, car il est peu probable que les utilisateurs modifient leur comportement en fonction de celui-ci.

    -   **L’État est-il critique ? L’action immédiate est-elle nécessaire ?** Dans ce cas, affichez les informations d’une manière qui exige une attention et qui ne peuvent pas être ignorées facilement, par exemple une [boîte de dialogue](win-dialog-box.md).

    Les programmes conçus pour Windows 7 peuvent utiliser des icônes de superposition dans le bouton de la barre des tâches du programme pour afficher la modification de l’État, ainsi que les barres de progression du bouton de la barre des tâches pour afficher la progression des tâches de longue durée.

-   **La fonctionnalité a-t-elle déjà une « présence du Bureau » ?** Autrement dit, lors de l’exécution, la fonctionnalité s’affiche-t-elle dans une fenêtre du Bureau (éventuellement réduite) ? Dans ce cas, affichez l’État dans la [barre d’État](ctrl-status-bars.md)du programme, autre zone d’État ou, pour Windows 7, directement dans le bouton de la barre des tâches. Si la fonctionnalité n’a pas de présence pour le bureau, vous pouvez utiliser une icône d’accès aux programmes et pour afficher l’État.
-   **L’icône est-elle principalement utilisée pour lancer un programme ou accéder rapidement à ses fonctionnalités ou à ses paramètres ?** Dans ce cas, utilisez le menu Démarrer pour lancer des programmes à la place. La zone de notification n’est pas destinée à un programme rapide ou un accès aux commandes.

    ![capture d’écran de la barre d’outils Lancement rapide ](images/winenv-notification-image4.png)

    Dans cet exemple de Windows Vista, le lancement rapide est utilisé pour lancer rapidement l’Explorateur Windows et Windows Internet Explorer.

    Pour les programmes conçus pour Windows 7, les utilisateurs peuvent épingler les boutons de la barre des tâches pour un accès rapide aux programmes. Les programmes peuvent utiliser une liste de raccourcis ou une barre d’outils miniatures pour accéder aux commandes fréquemment utilisées directement à partir du bouton de barre d’outils d’un programme. La zone lancement rapide n’est pas affichée par défaut dans Windows 7.

    ![capture d’écran de la barre des tâches et de la liste de raccourcis avec des icônes ](images/winenv-notification-image5.png)

    Dans cet exemple, une liste de raccourcis est utilisée pour un accès rapide aux commandes.

## <a name="design-concepts"></a>Principes de conception

### <a name="the-windows-desktop"></a>Le bureau Windows

Le bureau Windows dispose des points d’accès aux programmes suivants :

-   **Zone de travail.** Zone à l’écran où les utilisateurs peuvent effectuer leur travail, ainsi que pour stocker des programmes, des documents et leurs raccourcis. Techniquement, le bureau comprend la barre des tâches. dans la plupart des contextes, il fait uniquement référence à la zone de travail.
-   **Bouton Démarrer.** Point d’accès pour tous les programmes et emplacements Windows spéciaux (documents, images, musique, jeux, ordinateur, panneau de configuration), avec les listes « les plus récemment utilisées » pour accéder rapidement aux programmes et documents récemment utilisés.
-   **Lancement rapide.** Point d’accès direct pour les programmes sélectionnés par l’utilisateur. Lancement rapide a été supprimé de Windows 7.
-   **Tâches.** Point d’accès pour l’exécution des programmes qui ont une présence sur le bureau. Bien que techniquement, la barre des tâches couvre l’ensemble de la barre du bouton Démarrer vers la zone de notification. dans la plupart des contextes, la barre des tâches fait référence à la zone comprise entre, contenant les boutons de la barre des tâches. Cette zone est parfois appelée TaskBand.
-   **Deskbands. Non recommandé.**
-   **Zone de notification.** Source à bref terme des notifications et de l’État, ainsi qu’un point d’accès pour les fonctionnalités système et de programme qui n’ont aucune présence sur le bureau.

![capture d’écran identifiant les points d’accès au bureau ](images/winenv-notification-image6.png)

Les points d’accès au bureau Windows incluent le bouton Démarrer, la barre des tâches et la zone de notification. Notez la fonctionnalité miniature du bouton de la barre des tâches.

**Le bureau est une ressource partagée limitée qui est le point d’entrée de l’utilisateur sur Windows.** Laissez les utilisateurs dans le contrôle. Vous devez utiliser les zones du bureau comme prévu pour toute autre utilisation. Par exemple, n’affichez jamais les zones de bureau comme des moyens de promouvoir votre programme ou sa [personnalisation](exper-branding.md).

### <a name="using-the-notification-area-appropriately"></a>Utilisation correcte de la zone de notification

La zone de notification était initialement conçue comme source temporaire pour les notifications et l’État. Son efficacité et sa commodité ont encouragé les développeurs à lui permettre d’autres tâches, telles que le lancement de programmes et l’exécution de commandes. Malheureusement, dans le temps, ces ajouts ont rendu la zone de notification trop grande et bruyante, et ont confondu avec les autres points d’accès au bureau.

Windows XP a résolu le problème de mise à l’échelle en rendant la zone réductible et en masquant les icônes inutilisées. Windows Vista a résolu le bruit en supprimant les notifications inutiles et ennuyeuses. Windows 7 a encore été plus loin en mettant l’accent sur son objectif initial de être une source de notification. **La plupart des icônes sont masquées par défaut dans Windows 7, mais elles peuvent être promues manuellement par l’utilisateur dans la zone de notification. Pour permettre aux utilisateurs de contrôler leurs postes de travail, votre programme n’a aucun moyen d’effectuer cette promotion automatiquement.** Windows affiche toujours les notifications pour les icônes masquées en les promouvant temporairement.

![capture d’écran de la zone de notification et du dépassement de capacité ](images/winenv-notification-image7.png)

Dans Windows 7, la plupart des icônes de la zone de notification sont masquées par défaut.

En outre, Windows 7 prend en charge de nombreuses fonctionnalités directement dans les boutons de la barre des tâches. Plus précisément, vous pouvez utiliser :

-   Les listes de raccourcis et les barres d’outils miniatures pour accéder rapidement aux commandes fréquemment utilisées.
-   Les icônes de superposition pour afficher l’état des programmes en cours d’exécution.
-   Barres de progression du bouton de la barre des tâches pour afficher la progression des tâches de longue durée.

En bref, si votre programme a une présence sur le bureau, tirez pleinement parti des fonctionnalités du bouton de la barre des tâches de Windows 7 à ces fins. **Gardez les icônes de la zone de notification axées sur l’affichage des notifications et de l’État.**

### <a name="keeping-users-in-control"></a>Maintien des utilisateurs dans le contrôle

Le maintien des utilisateurs dans le contrôle s’étend au-delà de la zone de notification. Selon la nature de votre icône, vous souhaiterez peut-être permettre aux utilisateurs d’effectuer les opérations suivantes :

-   **Supprimez l’icône.** Votre icône peut fournir un État utile et utile, mais même par conséquent, il se peut que les utilisateurs ne puissent pas le voir. Windows permet aux utilisateurs de masquer les icônes, mais cette fonctionnalité n’est pas facilement détectable. Pour conserver le contrôle des utilisateurs, indiquez une **icône d’affichage dans la zone de notification** de l’option dans le menu contextuel de l’icône. Notez que la suppression d’une icône n’a pas besoin d’affecter le programme, la fonctionnalité ou le processus sous-jacent.
-   **Sélectionnez les types de notifications à afficher.** Votre notification doit être utile et pertinente, mais il peut y avoir des notifications que les utilisateurs ne souhaitent pas voir. Ceci est particulièrement vrai pour les [notifications](mess-notif.md)de Money. Laissez les utilisateurs choisir d’activer les moins importants.
-   **Interrompez les fonctionnalités facultatives.** Les icônes sont utilisées pour afficher l’état des fonctionnalités sans présence sur le bureau. Ces fonctionnalités ont tendance à être des tâches en arrière-plan facultatives, telles que l’impression, l’indexation, l’analyse ou la synchronisation. Les utilisateurs peuvent souhaiter suspendre ces fonctionnalités pour augmenter les performances du système, réduire la consommation d’énergie ou les mettre hors connexion.
-   **Quittez le programme.** Fournissez les options les plus appropriées :
    -   **Quitter temporairement le programme.** Le programme est arrêté et redémarré lorsque Windows est redémarré. Cette approche convient aux utilitaires système importants tels que les programmes de sécurité.
    -   **Quitter définitivement le programme.** Le programme est arrêté et n’est pas redémarré lorsque Windows est redémarré (sauf si l’utilisateur choisit de redémarrer ultérieurement). Soit l’utilisateur ne souhaite plus exécuter le programme, soit il souhaite exécuter le programme à la demande peut-être pour améliorer les performances du système.

Bien qu’il soit judicieux de fournir la plupart de ces paramètres dans le menu contextuel de l’icône, l’expérience par défaut du programme doit être adaptée à la plupart des utilisateurs. N’activez pas toutes les options par défaut et attendez que les utilisateurs activent les fonctionnalités. Au lieu de cela, activez les fonctionnalités importantes par défaut et laissez les utilisateurs activer des fonctionnalités supplémentaires selon vos besoins.

**Si vous ne faites que quatre choses...**

1.  N’abusez pas de la zone de notification. Utilisez-le uniquement comme source pour les notifications et l’État, et pour les fonctionnalités sans présence sur le bureau.
2.  Gardez le contrôle des utilisateurs. Fournissez les options appropriées pour contrôler l’icône, ses notifications et les fonctionnalités sous-jacentes.
3.  Présente une expérience par défaut adaptée à la plupart des utilisateurs. Permettez aux utilisateurs d’activer les fonctionnalités souhaitées, plutôt que de les attendre à désactiver celles qui ne sont pas souhaitées.
4.  Tirez pleinement parti des fonctionnalités du bouton de la barre des tâches de Windows 7 pour afficher l’État et faire en sorte que les tâches les plus fréquemment exécutées par votre programme soient efficaces.

## <a name="usage-patterns"></a>Modèles d’usage

Les icônes de la zone de notification ont plusieurs modèles d’utilisation :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>État du système et accès</strong><br/> Affiché en continu pour afficher l’état du système important mais non critique et pour fournir l’accès aux fonctionnalités et paramètres appropriés. <br/></td>
<td>Les fonctionnalités système qui requièrent des icônes de zone de notification n’ont pas de présence Bureau permanente. Peut également être utilisé comme source de notification. <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> Dans cet exemple, les icônes de batterie, de réseau et de volume s’affichent en continu le cas échéant.<br/></td>
</tr>
<tr class="even">
<td><strong>État et accès aux tâches en arrière-plan</strong><br/> Affiché pendant qu’une tâche en arrière-plan est en cours d’exécution pour afficher l’État et fournir l’accès aux fonctionnalités et aux paramètres. <br/></td>
<td>Les processus en arrière-plan requièrent des icônes de zone de notification lorsqu’ils n’ont aucune présence bureau. Peut également être utilisé comme source de notification. <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> Dans cet exemple, l’icône du centre de maintenance permet aux utilisateurs de vérifier leur état même lorsqu’il n’a aucune présence sur le bureau.<br/></td>
</tr>
<tr class="odd">
<td><strong>État de l’événement temporaire</strong><br/> Les programmes avec présence sur le bureau peuvent afficher temporairement des icônes pour afficher les événements importants ou les modifications de l’État. <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> Dans cet exemple, les icônes pour l’impression et l’installation des mises à jour sont affichées temporairement pour afficher les événements importants ou les modifications de l’État.<br/></td>
</tr>
<tr class="even">
<td><strong>Source de notification temporaire</strong><br/> Affiché temporairement pour afficher une notification. Supprimé après un délai d’expiration ou lorsque le problème sous-jacent est traité ou effectué par une tâche. <br/></td>
<td>Les icônes temporaires sont préférées pour les sources de notification pures. N’affichez pas d’icône qui ne fournit pas d’état dynamique utile, pertinent, car il se peut qu’une fonctionnalité doive afficher une notification à l’avenir. <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> Dans cet exemple, l’icône plug-and-Play s’affiche lors de l’affichage d’une notification nouveau matériel détecté.<br/></td>
</tr>
<tr class="odd">
<td><strong>Application à instance unique réduite</strong><br/> Pour réduire l’encombrement de la barre des tâches, une application à instance unique et à exécution longue peut être réduite à une icône de zone de notification à la place. <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> Dans cet exemple de Windows Vista, Outlook et Windows Live Messenger sont des applications à instance unique qui réduisent les icônes de la zone de notification.<br/> Envisagez d’utiliser ce modèle uniquement si tous les éléments suivants s’appliquent : <br/>
<ul>
<li>L’application ne peut avoir qu’une seule instance.</li>
<li>L’application est exécutée pendant une période prolongée.</li>
<li>L’icône affiche État.</li>
<li>L’icône peut être une source de notification.</li>
<li>Cela est facultatif et les utilisateurs doivent s' <a href="glossary.md">abonner</a>.</li>
</ul>
Si toutes ces conditions s’appliquent, la minimisation d’une icône évite d’avoir deux points d’accès quand un seul est nécessaire. <br/> <strong>Remarque :</strong> Ce modèle d’icône n’est plus recommandé pour Windows 7. Utilisez des boutons de la barre des tâches normaux à la place si votre programme a une présence sur le bureau.<br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> Dans cet exemple de Windows 7, un bouton de barre des tâches normal ne prend que peu d’espace, mais bénéficie des fonctionnalités du bouton de la barre des tâches de Windows 7, notamment les listes de raccourcis, les icônes de superposition et les miniatures enrichies.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Fournissez une seule icône de zone de notification par composant.**
-   **Utilisez une icône avec des versions de pixels 16x16, 20x20 et 24x24.** Les versions plus grandes sont utilisées dans les modes d’affichage haute résolution.

### <a name="when-to-show"></a>Quand afficher

-   Pour le modèle de source de notification temporaire :
    -   Windows affiche l’icône lorsque la notification s’affiche.
    -   Supprimer l’icône en fonction de son modèle de [conception de notification](mess-notif.md) :



    | Modèle                                     | Quand supprimer                                         |
    |--------------------------------------|------------------------------------------|
    | Réussite de l’action<br/>            | Lorsque la notification est supprimée.<br/> |
    | Échec de l’action<br/>            | Lorsque le problème est résolu.<br/>     |
    | Événement système non critique<br/> | Lorsque le problème est résolu.<br/>     |
    | Tâche utilisateur facultative<br/>        | Lorsque la tâche est terminée.<br/>            |
    | INFORMATION<br/>                       | Lorsque la notification est supprimée.<br/> |



 

-   **Pour le modèle d’état d’événement temporaire, affichez l’icône pendant que l’événement se produit.**
-   Pour tous les autres modèles, **Affichez l’icône lorsque le programme, la fonctionnalité ou le processus est en cours d’exécution et que l’icône est pertinente** , à moins que l’utilisateur ait effacé son **icône d’affichage dans l’option zone de notification** (pour plus d’informations, consultez [menus contextuels](#context-menus)). La plupart des icônes sont masquées par défaut dans Windows 7, mais elles peuvent être promues par l’utilisateur dans la zone de notification.
-   **N’affiche pas les icônes destinées aux administrateurs pour les utilisateurs standard.** Enregistrez les informations dans le journal des événements Windows.

### <a name="where-to-show"></a>Où afficher

-   **Affichez les fenêtres lancées à partir des icônes de la zone de notification près de la zone de notification.**

![figure d’une fenêtre près de la zone de notification ](images/winenv-notification-image14.png)

Les fenêtres lancées à partir des icônes de la zone de notification sont affichées près de la zone de notification.

### <a name="icons"></a>Icônes

-   **Choisissez l’icône en fonction de son modèle de conception :**

    | Modèle                                                 | Type d’icône                                   |
    |--------------------------------------------------|------------------------------------|
    | État du système et accès<br/>              | Icône de fonctionnalité système<br/>     |
    | État et accès aux tâches en arrière-plan<br/>     | Icône de programme ou de fonctionnalité<br/> |
    | Source de notification temporaire<br/>         | Icône de programme ou de fonctionnalité<br/> |
    | État de l’événement temporaire<br/>                | Icône de programme ou de fonctionnalité<br/> |
    | Application à instance unique réduite<br/> | Icône de programme<br/>            |

    

     

    ![capture d’écran de la zone de notification et des icônes Outlook ](images/winenv-notification-image15.png)

    Dans cet exemple, Outlook utilise une icône de fonctionnalité de messagerie électronique pour une source de notification temporaire et son icône d’application pour l’application réduite.

-   **Choisissez une conception d’icône facilement reconnaissable.** Préférer les icônes avec des contours uniques sur les icônes de forme carrée ou rectangulaire. N’oubliez pas que les conceptions préfèrent simplement des symboles sur des images réalistes. Appliquez également les autres [règles d’icônes de style Aero](vis-icons.md) .
-   **Utilisez des variantes d’icône ou des superpositions pour indiquer l’État ou les changements d’État.** Utilisez les variations d’icône pour afficher les modifications de quantités ou de forces. Pour les autres types d’État, utilisez les superpositions standard suivantes. Utilisez une seule superposition et localisez-la en bas à droite pour assurer la cohérence. 

    | Overlay                                                                                                       | Statut                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![capture d’écran de petite icône d’avertissement ](images/winenv-notification-image16.png)<br/>               | Avertissement<br/>               |
    | ![capture d’écran de l’icône d’erreur de petite taille ](images/winenv-notification-image17.png)<br/>                 | Error<br/>                 |
    | ![capture d’écran de la petite icône désactivée/déconnectée ](images/winenv-notification-image18.png)<br/> | Désactivé/déconnecté<br/> |
    | ![capture d’écran de la petite icône bloquée/hors connexion ](images/winenv-notification-image19.png)<br/>       | Bloqué/hors connexion<br/>       |

    

     

    ![capture d’écran de la zone de notification et de deux icônes ](images/winenv-notification-image20.png)

    Dans cet exemple, les icônes de la batterie et de la connexion affichent des modifications dans les quantités ou les forces.

    ![capture d’écran de la zone de notification et deux superpositions ](images/winenv-notification-image21.png)

    Dans cet exemple, les superpositions sont utilisées pour afficher les États d’erreur et d’avertissement.

-   **Évitez les quantités de couleur rouge, jaune et vert pur dans vos icônes de base.** Pour éviter toute confusion, réservez ces couleurs pour communiquer l’État. Si votre [personnalisation](exper-branding.md) utilise ces couleurs, envisagez d’utiliser des tons muets pour les icônes de votre zone de notification de base.
-   Pour une [escalade progressive](mess-notif.md), **Utilisez les icônes avec une apparence progressivement plus catégorique, car la situation devient plus urgente.**

    ![capture d’écran de la zone de notification et de cinq icônes ](images/winenv-notification-image22.png)

    Dans ces exemples, l’apparence de l’icône de la batterie devient plus catégorique à mesure que l’urgence augmente.

-   **Ne modifiez pas l’État trop fréquemment.** Les icônes de la zone de notification ne doivent pas apparaître bruyantes, instables ou à la demande. L’œil étant sensible aux modifications apportées au champ de vision du périphérique, les changements d’État doivent être subtils.
    -   **Ne modifiez pas l’icône rapidement.** Si l’État sous-jacent change rapidement, l’icône se reflète sur l’état de haut niveau.

        **Incorrect :**

        ![capture d’écran de l’icône de la zone de notification et du modem ](images/winenv-notification-image23.png)

        Dans cet exemple, l’icône de modem affiche des voyants clignotants (comme le fait un modem matériel), mais ces modifications d’État ne sont pas significatives pour les utilisateurs.

    -   **N’utilisez pas d’animations de longue durée pour afficher les activités continues.** Ces animations sont une gêne. La présence d’une icône dans la zone de notification indique suffisamment l’activité continue.
    -   **Les animations légères et subtiles sont acceptables pour montrer la progression des modifications d’État transitives importantes et temporaires.**

        ![capture d’écran de la zone de notification et de l’icône sans fil ](images/winenv-notification-image24.png)

        Dans cet exemple, l’icône sans fil affiche un indicateur d’activité pour indiquer que le travail est en cours.

    -   **Ne pas faire clignoter l’icône.** Cela est trop gênant. Si un événement requiert une attention immédiate, utilisez plutôt une boîte de dialogue. Si l’événement nécessite une attention, utilisez une notification.

-   **Ne désactivez pas les icônes de la zone de notification.** Si l’icône n’est pas actuellement appliquée, supprimez-la. Toutefois, vous pouvez afficher une icône activée avec un chevauchement d’état désactivé si les utilisateurs peuvent activer à partir de l’icône.

    ![capture d’écran de la zone de notification et du curseur de volume ](images/winenv-notification-image25.png)

    Dans cet exemple, les utilisateurs peuvent activer la sortie audio de l’icône.

Pour obtenir des instructions générales et des exemples, consultez [icônes](vis-icons.md).

### <a name="interaction"></a>Interaction

**Remarque :** Les événements Click suivants doivent se produire au niveau de la souris, et non de la souris.

**Pointage**

-   **Affiche une info-bulle ou une info-bulle qui indique ce que représente l’icône.**

    ![capture d’écran de la zone de notification et de l’info-bulle ](images/winenv-notification-image26.png)

    Dans cet exemple, une info-bulle est utilisée pour décrire l’icône au survol.

Pour obtenir des instructions sur le texte de l’info-bulle, consultez la section [texte](#context-menus) de cet article.

**Clic simple sur la gauche**

-   **Affichez tous les utilisateurs les plus susceptibles de voir**:

    -   Fenêtre de menu volant, boîte de dialogue ou programme avec les paramètres les plus utiles et les tâches couramment exécutées. Pour obtenir des instructions de présentation, consultez [lanceurs de zone de notification](#notification-area-flyouts).

        ![capture d’écran de la zone de notification et des lanceurs ](images/winenv-notification-image27.png)

        Dans ces exemples, le bouton gauche affiche des fenêtres contextuelles avec les paramètres les plus utiles.

    -   Un menu volant d’État.

        ![capture d’écran de la zone de notification et du menu volant d’État ](images/winenv-notification-image28.png)

        Dans cet exemple, le bouton gauche affiche le menu volant État.

        -   Élément du panneau de configuration associé.
        -   Menu contextuel.

    Les utilisateurs s’attendent à ce qu’un simple clic s’affichent, de sorte que rien ne fait apparaître une icône de zone de notification qui ne répond pas.

-   **Affichez un menu contextuel uniquement si les autres choix ne s’appliquent pas**, avec la commande par défaut en gras. Dans ce cas, affichez le même menu contextuel qui s’affiche en cliquant avec le bouton droit pour éviter toute confusion.
-   **Préférez l’utilisation d’une fenêtre contextuelle sur une boîte de dialogue** pour une sensation plus légère. Affichez uniquement les paramètres les plus courants et faites en sorte qu’ils prennent effet immédiatement pour une interaction plus simple. Faire disparaître la fenêtre contextuelle si l’utilisateur clique n’importe où en dehors de la fenêtre.
-   **Affichez les petites fenêtres près de l’icône associée.** Toutefois, les grandes fenêtres telles que les éléments du panneau de configuration peuvent être affichées au centre de l’analyse par défaut.

**Double-clic gauche**

-   **Exécutez la commande par défaut dans le menu contextuel.** En général, cette option affiche l’interface utilisateur principale associée à l’icône, par exemple l’élément du panneau de configuration associé, la feuille de propriétés ou la fenêtre du programme.
-   **S’il n’existe pas de commande par défaut, effectuez la même action qu’un simple clic gauche.**

**Cliquez avec le bouton droit sur**

-   **Affichez le menu contextuel** avec la commande par défaut en gras.

### <a name="context-menus"></a>Menu contextuels

-   **Affichez le menu contextuel près de l’icône qui lui est associée**, mais en dehors de la barre des tâches.
-   **Le menu contextuel peut inclure les éléments suivants**, le cas échéant, dans l’ordre indiqué (le texte exact est entre guillemets) :

Commandes principales

Open (par défaut, List First, en gras)

Exécuter

Commandes secondaires

Séparateur de <>

Commande de suspension/reprise d’activation/désactivation (coche)

« Réduit à la zone de notification » (coche)

Accepter les notifications (coche)

« Afficher l’icône dans la zone de notification » (coche)

Séparateur de <>

Relatives

« Quitter »

-   **Supprimez plutôt que de désactiver les éléments de menu contextuel qui ne s’appliquent pas.**
-   Pour les commandes d’ouverture, d’exécution et de suspension/reprise, **Soyez précis sur ce qui est en cours d’ouverture, d’exécution, de suspension et de reprise.**

![Capture d’écran montrant une zone de notification et des commandes.](images/winenv-notification-image29.png)

Dans cet exemple, Windows Defender dispose de commandes d’ouverture et d’exécution spécifiques.

-   **Utilisez suspendre/reprendre l’exécution des tâches en arrière-plan, activer/désactiver pour tout le reste.**
-   **Utilisez des coches pour indiquer l’État.** Répertorier et activer tous les États et placer la coche en regard de l’état actuel. Ne désactivez pas les options ou modifiez les étiquettes d’option pour indiquer l’état actuel.

**Correct :**

![capture d’écran d’une commande avec coche ](images/winenv-notification-image29.png)

**Incorrect :**

![capture d’écran d’une commande sans coche ](images/winenv-notification-image30.png)

Dans l’exemple incorrect, Windows Defender doit utiliser une coche pour indiquer l’état actuel.

-   **Toutes les tâches en arrière-plan doivent avoir une commande de suspension/reprise.** Le choix de la commande doit suspendre temporairement la tâche. Les utilisateurs peuvent souhaiter suspendre temporairement les tâches en arrière-plan pour augmenter les performances du système ou réduire la consommation d’énergie. Les tâches en arrière-plan suspendues sont redémarrées lors de la reprise par l’utilisateur ou lors du redémarrage de Windows.
-   **Autorisez les utilisateurs à s’abonner à des types de notification différents** si votre programme contient des notifications que certains utilisateurs peuvent ne pas vouloir voir. Le modèle de notification [Money](mess-notif.md) oblige les utilisateurs à s’abonner. par conséquent, ces notifications doivent être désactivées par défaut.

![capture d’écran de la zone de notification et des commandes ](images/winenv-notification-image31.png)

Dans cet exemple, Outlook permet aux utilisateurs de choisir les notifications qu’ils reçoivent de l’icône.

-   **La désactivation de l’option « Afficher l’icône dans la zone de notification » supprime l’icône de la zone de notification**, mais n’affecte pas le programme, la fonctionnalité ou le processus sous-jacent. Les utilisateurs peuvent réafficher l’icône à partir de la boîte de dialogue Options du programme. Ne réaffichez pas automatiquement l’icône lorsque Windows est redémarré.
-   **La commande Quitter quitte le programme pour la session Windows en cours et supprime l’icône.** N’avez pas de commande quitter si le programme ne peut pas être arrêté. Le programme est redémarré lorsque Windows est redémarré. Les utilisateurs peuvent quitter définitivement le programme à partir de la boîte de dialogue Options.
-   **N’avez pas de commande à propos de.** Ces informations doivent être communiquées par l’icône, son info-bulle et le menu contextuel. Si les utilisateurs souhaitent plus d’informations, ils peuvent afficher l’interface utilisateur principale.
    -   **Exception :** Vous pouvez fournir une commande à propos de si l’icône est destinée à un programme qui n’a pas de présence sur le bureau.

Pour obtenir des instructions générales sur le menu contextuel et des exemples, consultez [menus](cmd-menus.md).

### <a name="rich-tooltips"></a>Info-bulles riches

-   **Utilisez des info-bulles riches uniquement pour faciliter la compréhension des informations.** N’utilisez pas d’info-bulles riches pour décorer la fonctionnalité. Si vous ne pouvez pas utiliser la richesse pour faciliter la compréhension des informations, utilisez plutôt une info-bulle simple.

    **Incorrect :**

    ![capture d’écran de la zone de notification et de l’info-bulle enrichie ](images/winenv-notification-image32.png)

    **Correct :**

    ![capture d’écran de la zone de notification et de l’info-bulle simple ](images/winenv-notification-image33.png)

    Dans l’exemple incorrect, l’icône du calendrier ne rend pas la date plus facile à comprendre.

-   **Utilisez une présentation concise.** Utilisez un texte concis et une disposition concise avec une icône de pixel 32x32. Les info-bulles les plus gênantes sont risquées, surtout lorsqu’elles sont affichées involontairement.
-   **Ne placez pas de contrôles ou d’éléments qui apparaissent interactifs dans une info-bulle riche.** Les info-bulles ne sont pas interactives et n’apparaissent donc pas interactives. N’utilisez pas de texte bleu ou souligné.

    **Correct :**

    ![capture d’écran de l’info-bulle enrichie avec du texte noir ](images/winenv-notification-image34.png)

    **Incorrect :**

    ![capture d’écran de l’info-bulle enrichie avec du texte en bleu ](images/winenv-notification-image35.png)

    Dans l’exemple incorrect, le mode de gestion de l’alimentation actuel semble être un lien, mais il est impossible de cliquer.

### <a name="notification-area-flyouts"></a>Menus volants de la zone de notification

-   Le cas échéant, présentez les menus volants de la zone de notification avec trois sections :
    -   **Récapitulatif.** Affichez les mêmes informations que celles affichées dans l’info-bulle ou l’info-bulle de l’icône, éventuellement avec plus de détails. Pour des fins de cohérence, utilisez le même texte et les mêmes icônes, et généralement la même disposition (si vous utilisez une info-bulle riche). Contrairement à info-bulles, ces informations sont accessibles lors de l’utilisation de Touch.
    -   **Tâches courantes.** Présentez les tâches les plus couramment exécutées directement dans le menu volant.
    -   **Liens connexes.** Fournissez au plus un de chaque type des liens facultatifs suivants :
        -   Lien vers la tâche la plus fréquemment exécutée dans le panneau de configuration. Indiquez si une tâche fréquemment exécutée ne peut pas être présentée dans la section tâches courantes.
        -   Lien vers l’élément du panneau de configuration associé. Cet élément du panneau de configuration doit permettre aux utilisateurs d’effectuer des tâches qui ne peuvent pas être effectuées dans la section tâches courantes.
        -   Lien vers une rubrique d’aide spécifique appropriée. Suivez les [instructions du lien d’aide](winenv-help.md)standard.

![capture d’écran de la zone de notification et du menu volant ](images/winenv-notification-image36.png)

Cet exemple montre un menu volant de zone de notification à l’aide de la présentation recommandée.

### <a name="options-dialog-box"></a>Options (boîte de dialogue)

-   Les options qui ne sont pas accessibles directement à partir du menu contextuel doivent se trouver dans la boîte de dialogue Options. Cette boîte de dialogue peut être le panneau de configuration de la fonctionnalité.
-   **La boîte de dialogue Options peut inclure les éléments suivants, le** cas échéant (le texte exact est entre guillemets) :
    -   Activer le \[ nom \] de la fonctionnalité (case à cocher)
        -   Si vous désactivez cette option, le programme est quitté de manière permanente. Le programme peut être redémarré à partir de son élément du panneau de configuration. La commande quitter du menu contextuel quitte le programme uniquement pour la session Windows en cours.
    -   « Afficher l’icône dans la zone de notification » (case à cocher)
        -   La suppression de l’icône de la zone de notification n’affecte pas la fonctionnalité sous-jacente.
        -   La sélection de cette option permet à l’utilisateur de restaurer l’icône, ce qui, bien sûr, ne peut pas être effectué à partir de l’icône elle-même.
-   Désactivez les fonctionnalités rarement utilisées, ou potentiellement gênantes ou gênantes. Permettez aux utilisateurs d' [accepter](glossary.md) ces fonctionnalités.

Pour obtenir des instructions générales sur la boîte de dialogue Options et des exemples, consultez [fenêtres de propriétés](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimisation des programmes dans la zone de notification

**Remarque : la minimisation des fenêtres de programme dans la zone de notification n’est plus recommandée pour Windows 7.** Utilisez des boutons de [la barre des tâches](winenv-taskbar.md) normaux à la place. Votre programme peut prendre en charge les deux mécanismes de compatibilité descendante.

-   Pour réduire l’encombrement de la barre des tâches, envisagez de limiter les programmes à la zone de notification uniquement si tous les éléments suivants s’appliquent :
    -   Le programme ne peut avoir qu’une seule instance.
    -   Le programme est exécuté pendant une période prolongée.
    -   L’icône affiche État.
    -   L’icône peut être une source de notification.
    -   Cela est facultatif et les utilisateurs doivent s' [abonner](glossary.md).
-   Utilisez le bouton réduire de la barre de titre de l’application, et non le bouton Fermer.

## <a name="text"></a>Texte

### <a name="infotips"></a>Info-bulles

-   L’info-bulle de l’icône doit avoir l’un des formats suivants (où le nom de la société est facultatif) :
    -   (Nom de la société) Nom de la fonctionnalité, du programme ou de l’appareil
    -   ![capture d’écran de l’info-bulle avec le nom de la société ](images/winenv-notification-image37.png)
    -   (Nom de la société) Nom de la fonctionnalité, du programme ou de l’appareil-Résumé de l’État
    -   ![capture d’écran de l’info-bulle affichant le résumé de l’État ](images/winenv-notification-image38.png)
    -   (Nom de la société) Instruction de l’état du nom de la fonctionnalité, du programme ou de l’appareil.
    -   ![capture d’écran de l’info-bulle affichant l’État ](images/winenv-notification-image39.png)
    -   (Nom de la société) Nom de la fonctionnalité, du programme ou de l’appareil
    -   Liste d’États avec chaque élément sur une ligne distincte
    -   ![capture d’écran de l’info-bulle affichant la liste d’État ](images/winenv-notification-image40.png)

Formulation de l’info-bulle :

-   Concentrez-vous sur les informations les plus utiles. Affiche d’autres informations sur un simple clic gauche.
-   Soyez concis. Utilisez des fragments de phrase ou des instructions simples.
-   N’utilisez pas de ponctuation finale, sauf si Tip est formulées comme une phrase complète.
-   Omettez les mots inutiles. N’incluez pas la version du logiciel ou d’autres informations superflues.

    **Incorrect :**

    ![capture d’écran de l’info-bulle avec des informations inutiles ](images/winenv-notification-image41.png)

    Dans cet exemple, l’info-bulle contient des informations superflues.

-   N’Expliquez pas comment interagir avec l’icône.

    **Incorrect :**

    ![capture d’écran d’une info-bulle avec des instructions de clic droit ](images/winenv-notification-image42.png)

    Dans cet exemple, l’icône connexion réseau sans fil donne des instructions de clic droit.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à la zone de notification :

-   Reportez-vous à la zone de notification comme zone de notification, et non dans la barre d’état système.

Quand vous faites référence à une icône de zone de notification :

-   Reportez-vous à l’icône en utilisant le nom exact donné dans son info-bulle, y compris sa mise en majuscules, suivi de l’icône.
-   Pour obtenir la première référence, reportez-vous également à la zone de notification.
-   Dans la mesure du possible, mettez en forme le texte d’en-tête en gras. Sinon, placez l’en-tête entre guillemets uniquement si nécessaire pour éviter toute confusion.

**Exemple :** Pour vérifier rapidement l’état du réseau, cliquez sur l’icône **réseau** dans la zone de notification.

 


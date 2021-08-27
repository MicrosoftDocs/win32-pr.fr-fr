---
title: Notifications (concepts de base de la conception)
description: Une notification informe les utilisateurs d’événements qui ne sont pas liés à l’activité de l’utilisateur actuel, en affichant brièvement une info-bulle à partir d’une icône dans la zone de notification.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 48b32da195663d42024a9febed5451e2fd3f0840
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471615"
---
# <a name="notifications-design-basics"></a>Notifications (concepts de base de la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une notification informe les utilisateurs d’événements qui ne sont pas liés à l’activité de l’utilisateur actuel, en affichant brièvement une info-bulle à partir d’une icône dans la zone de notification. la notification peut être due à une action de l’utilisateur ou à un événement système significatif, ou peut fournir des informations potentiellement utiles à partir de Microsoft Windows ou d’une application.

Les informations contenues dans une notification sont **utiles et pertinentes, mais jamais critiques.** Par conséquent, les notifications ne nécessitent pas d’action immédiate de l’utilisateur et les utilisateurs peuvent les ignorer librement.

![capture d’écran de l’info-bulle avec « nouvelles mises à jour » dans le titre ](images/mess-notif-image1.png)

Une notification classique.

dans Windows Vista et versions ultérieures, les notifications s’affichent pour une durée fixe de 9 secondes. Les notifications ne s’affichent pas immédiatement lorsque les utilisateurs sont inactifs ou que les économiseurs d’écran sont en cours d’exécution. Windows met automatiquement en file d’attente les notifications à ce moment-là et affiche les notifications mises en file d’attente lorsque l’utilisateur reprend l’activité normale. Par conséquent, vous n’avez rien à faire pour gérer ces circonstances particulières.

**Développeurs :** Vous pouvez déterminer quand l’utilisateur est actif à l’aide de l’API SHQueryUserNotificationState.

**Remarque :** Les instructions relatives à la [zone de notification](winenv-notification.md), à [la barre des tâches](winenv-taskbar.md)et aux [bulles](ctrl-balloons.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les informations sont-elles le résultat immédiat et direct de l’interaction des utilisateurs avec votre application ?** Dans ce cas, affichez ces informations synchrones directement dans votre application à l’aide d’une [boîte de dialogue](win-dialog-box.md), d’une [boîte de message](glossary.md), d’une [bulle](ctrl-balloons.md)ou d’une interface utilisateur [en place](glossary.md) . Les notifications sont destinées uniquement à des informations asynchrones.

![capture d’écran de l’alerte de sécurité Windows ](images/mess-notif-image2.png)

dans cet exemple, la boîte de dialogue exceptions de pare-feu Windows s’affiche comme un résultat direct de l’interaction de l’utilisateur. Une notification ne serait pas appropriée ici.

-   **Les informations s’appliquent-elles uniquement lorsque les utilisateurs utilisent activement votre application ?** Dans ce cas, affichez les informations dans la [barre d’État](ctrl-status-bars.md) de votre application ou dans une autre zone d’État.

![capture d’écran de la barre d’État Outlook ](images/mess-notif-image3.png)

dans cet exemple, Outlook affiche son état de connexion et de synchronisation sur sa barre d’état.

-   **Les informations sont-elles rapidement modifiées, continues et en temps réel ?** Les exemples incluent la progression du traitement, les cotations boursières et les scores sportifs. Si c’est le cas, n’utilisez pas de notifications, car elles ne conviennent pas pour modifier rapidement les informations.
-   **Les informations sont-elles utiles et pertinentes ? Les utilisateurs risquent-ils de modifier leur comportement ou d’éviter tout désagrément en raison de la réception des informations ?** Si ce n’est pas le cas, n’affichez pas les informations ou ne les placez pas dans une fenêtre d’État ou un fichier journal.
-   **Les informations sont-elles critiques ? L’action immédiate est-elle nécessaire ?** Dans ce cas, affichez les informations à l’aide d’une interface qui exige une attention et qui ne peut pas être ignorée facilement, par exemple une boîte de dialogue modale ou une boîte de message. Si le programme n’est pas actif, vous pouvez attirer l’attention sur les informations critiques en [clignotant le bouton de la barre des tâches du programme](winenv-taskbar.md) trois fois et en le laissant mis en surbrillance jusqu’à ce que le programme soit actif.
-   **Les principaux utilisateurs ciblent-ils les professionnels de l’informatique ?** Dans ce cas, utilisez un autre mécanisme de commentaires, comme les entrées de [fichier journal](glossary.md) ou les messages électroniques. Les professionnels de l’informatique préfèrent fortement les fichiers journaux pour les informations non critiques. En outre, les serveurs sont souvent gérés à distance et sont généralement exécutés sans qu’aucun utilisateur ne soit connecté, ce qui rend les notifications inefficaces.

## <a name="design-concepts"></a>Principes de conception

Les notifications efficaces qui favorisent une bonne expérience utilisateur sont les suivantes :

-   **Synchrone.** l’événement n’est pas un résultat immédiat et direct de l’interaction actuelle des utilisateurs avec Microsoft Windows ou votre application.
-   **Adapté.** Il y a un risque raisonnable que les utilisateurs effectuent une tâche ou modifient leur comportement en tant que résultat de la notification.
-   **Nécessaire.** La notification affiche des informations utiles dont les utilisateurs se chargent et ne connaissent pas encore.
-   **Non critique.** Les notifications ne sont pas modales et ne nécessitent pas d’intervention de l’utilisateur, de sorte que les utilisateurs peuvent les ignorer librement.
-   **Exploitables.** Pour les notifications qui suggèrent l’exécution d’une action, cette action est lancée en cliquant sur la notification. Toutefois, l’action peut toujours être reportée.
-   **Présenté de manière appropriée.** La présentation de la notification (durée, fréquence, texte, icône et interactivité) correspond à ses circonstances.
-   **Pas ennuyeux !** Il y a une fine ligne entre l’informant en douceur des utilisateurs d’un événement et l’Pestering.

Malheureusement, il y a trop de notifications non pertinentes, inappropriées et inutiles. prenez en compte ces notifications du Windows XP Hall de dommage :

![capture d’écran de la notification « visite guidée de Windows XP » ](images/mess-notif-image4.png)

![capture d’écran de la notification « inutilisé Icons » ](images/mess-notif-image5.png)

![capture d’écran de la notification « ajouter .NET Passport » ](images/mess-notif-image6.png)

dans ces exemples, Windows XP est soi-disant qui tente d’aider les utilisateurs avec leur configuration initiale. Toutefois, ces notifications s’affichent beaucoup trop souvent et bien une fois qu’elles sont utiles, elles ne sont guère plus que des publications de fonctionnalités non sollicitées.

## <a name="user-flow-must-be-maintained"></a>Le workflow de l’utilisateur doit être conservé

**Idéalement, les utilisateurs immergés dans leur travail ne verront pas vos notifications. Au lieu de cela, ils voient vos notifications uniquement lorsque leur Flow est déjà rompu.**

dans Flow : la psychologie de l’expérience optimale, Mihaly Csikszentmihalyi indique que les utilisateurs entrent un état de Flow lorsqu’ils sont entièrement absorbés dans l’activité pendant laquelle ils perdent leur sens et ont des sentiments de grande satisfaction.

**Les notifications efficaces aident les utilisateurs à conserver leur flow en présentant des informations utiles et pertinentes qui peuvent être facilement ignorées.** Les notifications sont présentées de manière périphérique et à clé basse, et elles ne nécessitent pas d’interaction.

Ne partez pas du principe que si les notifications sont [non modales](glossary.md) , elles ne peuvent pas être une interruption ennuyeux. Les notifications ne demandent pas d’attention aux utilisateurs, mais elles le demandent certainement. Vous pouvez interrompre le workflow des utilisateurs en procédant comme suit :

-   Affichage des notifications qui ne se soucient pas des utilisateurs.
-   Affichage d’une notification trop souvent.
-   Utilisation de plusieurs notifications lorsqu’une seule notification suffit.
-   Utilisation de son lors de l’affichage d’une notification.

dans Windows 7, les utilisateurs disposent d’un contrôle optimal sur les notifications. **Si les utilisateurs détectent que les notifications d’un programme sont trop ennuyeuses, ils peuvent choisir de supprimer toutes les notifications de ce programme.** Assurez-vous que les utilisateurs ne font pas cela à votre programme en présentant des informations utiles et pertinentes et en suivant ces instructions.

## <a name="notifications-must-be-ignorable"></a>Les notifications doivent être ignorables

**Les notifications ne nécessitent pas d’action immédiate de l’utilisateur et peuvent être ignorées librement par les utilisateurs.**

Les développeurs et les concepteurs veulent souvent présenter leurs notifications de manière à ce que les utilisateurs ne puissent pas les ignorer. Cet objectif a entièrement pour effet de découper l’avantage principal des notifications, car cela entraînerait la rupture du passage des utilisateurs. Si les utilisateurs sont gênés par vos notifications ou s’ils sont obligés de les lire, votre conception de notification a échoué.

**Si vous craignez que les utilisateurs ignorent vos notifications, tenez compte des points suivants :**

-   Si vous utilisez des notifications correctement et qu’elles ne nécessitent pas d’action immédiate de l’utilisateur, le fait de faire en sorte que les utilisateurs choisissent de les ignorer est par défaut. Ne modifiez pas cette modification.
-   Si l’événement nécessite une action immédiate de l’utilisateur, utilisez une autre interface utilisateur que les utilisateurs ne peuvent pas ignorer. S’agit-il de l’interface utilisateur appropriée ? pour les alternatives.

## <a name="use-progressive-escalation-where-applicable"></a>Utiliser l’escalade progressive le cas échéant

Si une notification est utilisée pour un événement que les utilisateurs peuvent ignorer en toute sécurité au premier, mais qui doivent être traités par la suite, une autre interface utilisateur doit être utilisée lorsque la situation devient critique. Cette technique est appelée escalade progressive.

par exemple, le système de gestion de l’alimentation Windows indique initialement une batterie faible en modifiant simplement son icône de zone de notification.

![capture d’écran de six icônes montrant l’état de la batterie ](images/mess-notif-image7.png)

dans ces exemples, Windows la gestion de l’alimentation utilise l’icône de la zone de notification pour informer les utilisateurs de la batterie plus faible.

à mesure que la puissance de la batterie diminue, Windows avertit les utilisateurs de la faible puissance de la batterie à l’aide d’une notification.

![capture d’écran de la notification de batterie faible](images/mess-notif-image8.png)

dans cet exemple, Windows la gestion de l’alimentation utilise une notification pour informer les utilisateurs que leur batterie est faible.

Cette notification s’affiche lorsque les utilisateurs disposent toujours de plusieurs options. Les utilisateurs peuvent se connecter, modifier leurs options d’alimentation, englober leur travail et arrêter l’ordinateur, ou ignorer la notification et continuer à travailler. Lorsque l’alimentation de la batterie continue à se décharger, le texte et l’icône de la notification reflètent l’urgence supplémentaire. toutefois, une fois que la batterie est tellement faible que les utilisateurs doivent agir immédiatement, Windows la gestion de l’alimentation notifie les utilisateurs à l’aide d’une boîte de message [modale](glossary.md) .

![capture d’écran d’un avertissement d’alimentation sur batterie gravement faible](images/mess-notif-image9.png)

dans cet exemple, Windows la gestion de l’alimentation utilise une boîte de message modale pour notifier les utilisateurs d’une batterie dangereusement insuffisante.

**Si vous ne faites que trois choses...**

1.  Utilisez les notifications uniquement si vous en avez vraiment besoin. Lorsque vous affichez une notification, vous pouvez potentiellement interrompre les utilisateurs ou même les ennuyeux. Assurez-vous que l’interruption est justifiée.
2.  Utilisez des notifications pour les événements non critiques ou les situations qui ne nécessitent pas d’action immédiate de l’utilisateur. Pour les événements critiques ou les situations qui nécessitent une action immédiate de l’utilisateur, utilisez une autre interface utilisateur (par exemple, une boîte de dialogue modale).
3.  Si vous utilisez des notifications, faites-en une bonne expérience utilisateur. N’essayez pas de forcer les utilisateurs à voir vos notifications. Si les utilisateurs sont tellement plongés dans leur travail qu’ils ne voient pas vos notifications, votre conception est bonne.

## <a name="usage-patterns"></a>Modèles d’usage

Les notifications ont plusieurs modèles d’utilisation :




| | | <strong>Réussite</strong> de l’action<br /> Avertit les utilisateurs lorsqu’une action asynchrone lancée par l’utilisateur se termine correctement. <br /> | <strong>Correctrices</strong><br /><img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br /> dans cet exemple, Windows Update avertit les utilisateurs lorsque leur ordinateur a été correctement mis à jour.<br /><strong>Incorrect :</strong><br /><img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br /> dans cet exemple, Microsoft Outlook avertit les utilisateurs lorsqu’une vérification des fichiers de données est terminée. Que sont les utilisateurs censés faire maintenant ? Et pourquoi avertir les utilisateurs de la réussite de l’opération ?<br /><strong>Afficher quand :</strong> À la fin d’une tâche asynchrone. Informez les utilisateurs des actions réussies uniquement s’ils sont susceptibles d’attendre la fin de l’opération ou après des échecs récents.<br /><strong>Montrez comment :</strong> Utilisez l’option temps réel afin que ces notifications ne soient pas mises en file d’attente lorsque les utilisateurs exécutent une application en plein écran ou n’utilisent pas activement leur ordinateur.<br /><strong>Affichez la fréquence :</strong> Toutes.<br /><strong>Facteur d’ennui :</strong> Faible si la réussite n’est pas attendue en raison de défaillances récentes, la réussite est après une défaillance critique ou très inhabituelle, de sorte que l’utilisateur a besoin de commentaires supplémentaires ou que l’utilisateur attend la fin de son exécution. élevé dans le cas contraire.<br /><strong>Alternatives :</strong> Envoyer des commentaires « à la demande » en affichant une icône (ou en modifiant une icône existante) dans la zone de notification pendant que l’opération est en cours d’exécution ; supprimer l’icône (ou restaurer l’icône précédente) lorsque l’opération est terminée. <br /> | | <strong>Échec</strong> de l’action<br /> Avertit les utilisateurs lorsqu’une action asynchrone initiée par l’utilisateur échoue. <br /> | <strong>Correctrices</strong><br /><img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br /> dans cet exemple, Windows activation avertit les utilisateurs de l’échec.<br /><strong>Incorrect :</strong><br /><img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br /> dans cet exemple, Microsoft Outlook utilisé pour informer les utilisateurs qu’ils ne sont pas susceptibles de s’intéresser.<br /><strong>Afficher quand :</strong> En cas de défaillance d’une tâche asynchrone.<br /><strong>Affichez la fréquence :</strong> Toutes.<br /><strong>Facteur d’ennui :</strong> Faible si utile et pertinent ; élevé si le problème se résoudra immédiatement à lui-même ou à des utilisateurs qui ne se soucient pas.<br /><strong>Alternatives :</strong> Utilisez une boîte de dialogue modale si les utilisateurs doivent résoudre le problème immédiatement. <br /> | | <strong>Événement système non critique</strong><br /> Avertit les utilisateurs d’événements système importants ou de l’État qui peuvent être ignorés en toute sécurité, au moins temporairement. <br /> | <img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br /> dans cet exemple, Windows avertit les utilisateurs d’une batterie faible, mais il reste beaucoup de temps avant qu’ils ne soient en mesure d’agir.<br /><strong>Afficher quand :</strong> Lorsqu’un événement se produit et que l’utilisateur est actif, ou qu’une condition continue à exister. En cas de problème, supprimez immédiatement les notifications actuellement affichées une fois que le problème est résolu. Comme avec les notifications d’action, avertissez les utilisateurs des événements système réussis uniquement si les utilisateurs sont susceptibles d’attendre l’événement ou après des échecs récents.<br /><strong>Affichez la fréquence :</strong> Une fois lorsque l’événement se produit pour la première fois. Si cela est le résultat d’un problème que les utilisateurs doivent résoudre, réaffichez une fois par jour.<br /><strong>Facteur d’ennui :</strong> Faible, tant que la notification n’est pas affichée trop souvent.<br /><strong>Alternatives :</strong> Si les utilisateurs doivent finalement résoudre un problème, utilisez l’escalade progressive en affichant une boîte de dialogue modale lorsque la résolution devient obligatoire. <br /> | | <strong>Tâche utilisateur facultative</strong><br /> Avertit les utilisateurs des tâches asynchrones qu’ils doivent effectuer. Qu’il soit facultatif ou obligatoire, la tâche peut être ajournée en toute sécurité. <br /> | <img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br /> dans cet exemple, Windows Update notifie les utilisateurs d’une nouvelle mise à jour de sécurité.<br /><strong>Afficher quand :</strong> Lorsque la nécessité d’effectuer une tâche est déterminée et que l’utilisateur est actif.<br /><strong>Affichez la fréquence :</strong> Une fois par jour pour un maximum de trois fois.<br /><strong>Facteur d’ennui :</strong> Faible, tant que les utilisateurs considèrent la tâche comme importante et que la notification n’est pas affichée trop souvent.<br /><strong>Alternatives :</strong> Si les utilisateurs doivent finir par exécuter la tâche, utilisez l’escalade progressive en affichant une boîte de dialogue modale lorsque la tâche devient obligatoire. <br /> | | <strong>Money</strong><br /> Avertit les utilisateurs des informations pertinentes susceptibles d’être utiles. Vous pouvez avertir les utilisateurs d’informations marginales de pertinence si elles sont facultatives et que les utilisateurs choisissent. <br /> | <strong>Correctrices</strong><br /><img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br /> Dans cet exemple, les utilisateurs sont avertis lors de la réception d’un nouveau message électronique.<br /><strong>Correct :</strong><br /><img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br /> Dans cet exemple, les utilisateurs sont avertis lorsque les contacts sont en ligne et qu’ils choisissent de recevoir ces informations facultatives.<br /><strong>Incorrect :</strong><br /><img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br /> Dans cet exemple, les informations sont utiles uniquement si l’utilisateur a déjà installé des ports USB à haut débit. Dans le cas contraire, il est probable que l’utilisateur n’ait rien d’autre que le résultat.<br /><strong>Afficher quand :</strong> Lorsque l’événement de déclenchement se produit.<br /><strong>Montrez comment :</strong> Utilisez l’option temps réel afin que ces notifications ne soient pas mises en file d’attente lorsque les utilisateurs exécutent une application en plein écran ou n’utilisent pas activement leur ordinateur.<br /><strong>Affichez la fréquence :</strong> Toutes.<br /><strong>Facteur d’ennui :</strong> Moyen à élevé, en fonction de la perception de l’utilité des utilisateurs et de leur pertinence. Non recommandé s’il existe une faible probabilité d’intérêt pour l’utilisateur.<br /><strong>Alternatives :</strong> Ne pas avertir les utilisateurs. <br /> | | <strong>Publication des fonctionnalités</strong><br /> Avertit les utilisateurs des fonctionnalités système ou d’application récemment installées et inutilisées.<br /> | <strong>N’utilisez pas de notifications pour les publications de fonctionnalités !</strong> Au lieu de cela, utilisez une autre méthode pour rendre la fonctionnalité détectable, par exemple : <br /><ul><li>Concevez la fonctionnalité pour qu’elle soit plus facile à détecter dans les contextes lorsque cela est nécessaire.</li><li>N’effectuez aucune action particulière et permettez aux utilisateurs de découvrir la fonctionnalité de manière autonome.</li></ul><strong>Incorrect :</strong><br /><img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br /> N’utilisez pas de notifications pour les publications de fonctionnalités.<br /> | 




 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Sélectionnez le modèle de notification en fonction de son utilisation.** Pour obtenir une description de chaque modèle d’utilisation, consultez le tableau précédent.
-   **n’utilisez pas de notifications au cours de l’expérience de Windows initiale.** pour améliorer sa première expérience, Windows 7 supprime toutes les notifications affichées au cours des premières heures d’utilisation. Concevez votre programme en supposant que les utilisateurs ne verront pas ces notifications.

### <a name="what-to-notify"></a>Éléments à notifier

-   **Ne pas notifier les opérations réussies, sauf dans les circonstances suivantes :**
    -   **Sécurité.** Les utilisateurs considèrent les opérations de sécurité comme étant de l’importance la plus élevée, par conséquent, informez les utilisateurs de la réussite des opérations de sécurité.
    -   **Échec récent.** Les utilisateurs ne sont pas autorisés à effectuer des opérations réussies en cas d’échec juste avant, avertissant les utilisateurs de la réussite de l’opération.
    -   **Empêchez tout désagrément.** Signaler les opérations réussies lorsque cela peut empêcher les utilisateurs gêner. Par conséquent, avertissez les utilisateurs lorsqu’une opération réussie est exécutée de manière inattendue, par exemple lorsqu’une opération est longue ou terminée plus tôt ou plus tard que prévu.
-   **Dans d’autres circonstances, vous ne devez fournir aucun commentaire pour la réussite ou envoyer des commentaires « à la demande ».** Supposons que les utilisateurs effectuent des opérations réussies pour leur accord. Vous pouvez envoyer des commentaires à la demande en affichant une icône (ou en modifiant une icône existante) dans la zone de notification pendant que l’opération est effectuée et en supprimant l’icône (ou en restaurant l’icône précédente) lorsque l’opération est terminée.
-   Pour le modèle Money, **ne fournissez pas de notification si les utilisateurs peuvent continuer à travailler normalement ou sont peu susceptibles de faire quelque chose de différent en raison de la notification.**

    **Incorrect :**

    ![capture d’écran de notification pour des performances plus rapides ](images/mess-notif-image17.png)

    Dans cet exemple, les informations sont utiles uniquement si l’utilisateur a déjà installé les ports. Dans le cas contraire, il est probable que l’utilisateur n’ait rien d’autre que le résultat.

    -   Exception : **vous pouvez notifier aux utilisateurs des informations de pertinence pouvant être interrogées si elles sont facultatives et que les utilisateurs choisissent.**

        **Correct :**

        ![capture d’écran de la notification du contact connecté ](images/mess-notif-image16.png)

        Dans cet exemple, les utilisateurs sont avertis lorsque les contacts sont en ligne et qu’ils choisissent de recevoir ces informations facultatives.

-   Pour les modèles d’événements et de notifications système non critiques, **Utilisez des notifications complètes pour un seul événement.** Ne pas présenter plusieurs éléments partiels.

    **Incorrect :**

    ![capture d’écran de la notification « détection du nouveau matériel » ](images/mess-notif-image18.png)

    ces exemples affichent uniquement quatre des huit notifications qui ont été affichées par Windows XP quand un utilisateur attache un clavier USB spécifique, chacun présentant des informations incrémentielles.

    **Correct :**

    ![capture d’écran des notifications de l’état d’installation ](images/mess-notif-image19.png)

    Dans cet exemple, l’attachement d’un clavier USB aboutit à deux notifications complètes.

### <a name="when-to-notify"></a>Quand notifier

-   **Afficher une notification en fonction de son modèle de conception :**



| Modèle              | Quand notifier          |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Réussite de l’action<br/>            | À la fin d’une tâche asynchrone. Informez les utilisateurs des actions réussies uniquement s’ils sont susceptibles d’attendre la fin de l’opération ou après des échecs récents.<br/>                                             |
| Échec de l’action<br/>            | En cas de défaillance d’une tâche asynchrone.<br/>                                                                                                                                                                   |
| Événement système non critique<br/> | Lorsqu’un événement se produit et que l’utilisateur est actif, ou que la condition continue à exister. Si cela est le résultat d’un problème, supprimez immédiatement la notification actuellement affichée une fois le problème résolu.<br/> |
| Tâche utilisateur facultative<br/>        | Lorsque la nécessité d’effectuer une tâche est déterminée et que l’utilisateur est actif.<br/>                                                                                                                                   |
| INFORMATION<br/>                       | Lorsque l’événement de déclenchement se produit.<br/>                                                                                                                                                                       |



 

-   Pour le modèle d’échec d’action, **si le problème peut se corriger de lui-même en quelques secondes, Retardez la notification d’échec pendant un laps de temps approprié.** Si le problème se corrige lui-même, signalez rien. Notifier uniquement après un délai suffisant que l’échec est perceptible. Si vous signalez trop tôt, les utilisateurs risquent de ne pas remarquer le problème signalé, mais ils remarqueront la notification inutile.

**Incorrect :**

![capture d’écran d’aucune notification de connexion réseau ](images/mess-notif-image20.png)

Lorsqu’il est immédiatement suivi de :

![capture d’écran de la notification de connexion réussie ](images/mess-notif-image21.png)

dans cet exemple, dans Windows Vista, la notification d’absence de connectivité sans fil est prématurée, car elle est souvent suivie immédiatement d’une notification de bonne connectivité.

-   Pour les modèles d’action Success et Money, **Utilisez l’option en temps réel afin que les notifications obsolètes ne soient pas mises en file d’attente** lorsque les utilisateurs exécutent une application en plein écran ou n’utilisent pas activement leur ordinateur.
-   Pour le modèle d’événement système non critique, **ne créez pas le potentiel des tempêtes de notification en fragmentant les événements liés à des événements connus tels que l’ouverture de session utilisateur.** Au lieu de cela, liez l’événement à un laps de temps après l’événement. Par exemple, vous pouvez rappeler aux utilisateurs d’inscrire votre produit cinq minutes après l’ouverture de session de l’utilisateur.

### <a name="how-long-to-notify"></a>Délai de notification

dans Windows Vista et versions ultérieures, les notifications s’affichent pour une durée fixe de 9 secondes.

### <a name="how-often-to-notify"></a>Fréquence de notification

-   **Le nombre d’affichages d’une notification est basé sur son modèle de conception :**



| Modèle           | Fréquence de notification  |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Réussite de l’action<br/>            | Une seule fois.<br/>                                                                                                            |
| Échec de l’action<br/>            | Une seule fois.<br/>                                                                                                            |
| Événement système non critique<br/> | Une fois lorsque l’événement se produit pour la première fois. Si cela est le résultat d’un problème que les utilisateurs doivent résoudre, réaffichez une fois par jour.<br/> |
| Tâche utilisateur facultative<br/>        | Une fois par jour pour un maximum de trois fois.<br/>                                                                         |
| INFORMATION<br/>                       | Une seule fois.<br/>                                                                                                            |



 

-   **Pour les tâches utilisateur facultatives, ne tentez pas de pester les utilisateurs en soumission en affichant constamment des notifications.** Si la tâche est requise, affichez une boîte de dialogue modale immédiatement au lieu d’utiliser des notifications.

### <a name="notification-escalation"></a>Escalade de notifications

-   **Ne partez pas du principe que les utilisateurs verront vos notifications.** Les utilisateurs ne les voient pas dans les cas suivants :
    -   Ils sont immergés dans leur travail.
    -   Ils ne font pas attention.
    -   Ils sont éloignés de leur ordinateur.
    -   Ils exécutent une application en plein écran.
    -   Son administrateur a désactivé toutes les notifications pour son ordinateur.
-   **Si les utilisateurs doivent finalement entreprendre un certain type d’action, utilisez l’escalade progressive** pour afficher une autre interface utilisateur que les utilisateurs ne peuvent pas ignorer.

### <a name="interaction"></a>Interaction

-   **Rendez les notifications cliquables dans les cas suivants :**
    -   **Les utilisateurs doivent effectuer une action.** Cliquer sur la notification doit afficher une fenêtre dans laquelle les utilisateurs peuvent effectuer l’action. Cette approche est recommandée pour les modèles d’échec d’action et de conception de tâches utilisateur facultatives.
    -   **Les utilisateurs peuvent souhaiter afficher plus d’informations.** Cliquer sur la notification doit afficher une fenêtre dans laquelle les utilisateurs peuvent afficher des informations supplémentaires.
-   **Affiche toujours une fenêtre lorsque les utilisateurs cliquent pour effectuer une action.** Vous n’avez pas besoin d’effectuer une action directement.
-   **En cliquant sur pour afficher plus d’informations, vous devez toujours afficher plus d’informations.** Ne vous contentez pas de reformuler les informations qui se trouvent déjà dans la notification.

### <a name="icons"></a>Icônes

-   **Pour le modèle échec d’action, utilisez l’icône d’erreur standard.**
-   **Pour les modèles d’événements système non critiques, utilisez l’icône d’avertissement standard.**
-   **Pour les autres modèles, utilisez des icônes indiquant les objets qui concernent ou suggèrent le sujet**, tel qu’un bouclier pour la sécurité ou une batterie à la puissance.
-   **Utilisez des icônes basées sur la personnalisation de votre application ou de votre société si vos utilisateurs cibles les reconnaissent et qu’il n’existe pas de meilleure alternative.**
-   Pour une escalade progressive, **envisagez d’utiliser des icônes avec une apparence progressivement plus catégorique à mesure que la situation devient urgente.**
-   **N’utilisez pas l’icône d’informations standard.** Les notifications sont envoyées à des informations sans dire.
-   **Envisagez d’utiliser de grandes icônes (32x32 pixels) dans les cas suivants :**
    -   Les utilisateurs comprendront rapidement l’icône et non le texte.
    -   Les grandes icônes transmettent leur signification plus clairement et efficacement que les icônes de pixels 16x16 standard.
    -   L’icône utilise le [style Aero](vis-icons.md).

![capture d’écran de la notification « messages importants » ](images/mess-notif-image22.png)

Dans cet exemple, les utilisateurs peuvent rapidement comprendre la nature de la notification en un clin d’œil sur la grande icône.

### <a name="notification-queuing"></a>Mise en file d’attente des notifications

**Remarque :** Les notifications sont mises en file d’attente chaque fois qu’elles ne peuvent pas être affichées immédiatement, par exemple lorsqu’une autre notification est affichée, que l’utilisateur exécute une application en plein écran ou que l’utilisateur n’utilise pas activement l’ordinateur. Les notifications en temps réel sont conservées dans la file d’attente pendant seulement 60 secondes.

-   **Pour les modèles d’action Success et Money, utilisez l’option en temps réel** afin que la notification ne soit pas mise en file d’attente pendant longtemps. Ces notifications ont une valeur uniquement lorsqu’elles peuvent être affichées immédiatement.
-   **Supprimer les notifications en file d’attente lorsqu’elles ne sont plus pertinentes.**
-   **Développeurs :** Pour ce faire, vous pouvez définir l' \_ indicateur d’informations NSI dans uFlags et définir szInfo sur une chaîne vide. Cela n’a aucun effet si la notification n’est plus dans la file d’attente.

### <a name="system-integration"></a>Intégration du système

-   Si votre application n’a pas toujours d’icône dans la [zone de notification](winenv-notification.md) lorsqu’elle est en cours d’exécution, **Affichez temporairement une icône au cours de la tâche ou de l’événement asynchrone à l’origine de la notification.**

## <a name="text"></a>Texte

### <a name="title-text"></a>Texte du titre

-   **Utilisez un texte de titre qui résume brièvement les informations les plus importantes dont vous avez besoin pour communiquer avec les utilisateurs dans un langage clair, clair, concis et spécifique.** Les utilisateurs doivent être en mesure de comprendre l’objectif des informations de notification rapidement et avec un minimum d’effort.
-   **Utilisez des fragments de texte ou des phrases entières sans ponctuation finale.**
-   **Utilisez les majuscules comme pour les phrases.**
-   **N’utilisez pas plus de 48 caractères (en anglais) pour prendre en charge la localisation.** Le titre a une longueur maximale de 63 caractères, mais vous devez autoriser une extension de 30% lorsque le texte en anglais est traduit.

### <a name="body-text"></a>Texte du corps

-   **Utilisez le corps de texte qui fournit une description (sans répéter les informations du titre) et, éventuellement, qui donne des détails spécifiques sur la notification et permet également aux utilisateurs de savoir quelle action est disponible.**
-   **Utilisez des phrases complètes avec la ponctuation finale.**
-   **Utilisez les majuscules comme pour les phrases.**
-   **N’utilisez pas plus de 200 caractères (en anglais) pour prendre en charge la localisation.** Le corps du texte a une longueur maximale de 255 caractères, mais vous devez autoriser une expansion de 30% lorsque le texte en anglais est traduit.
-   **Incluez des informations essentielles dans le corps du texte, telles que des noms d’objets spécifiques.** (Exemples : noms d’utilisateurs, noms de fichiers ou URL.) Les utilisateurs ne doivent pas avoir à ouvrir une autre fenêtre pour rechercher ces informations.
-   **Placez des guillemets doubles autour des noms d’objets.**
    -   **Exception :** N’utilisez pas de guillemets dans les cas suivants :
        -   Le nom d’objet utilise toujours la mise en [majuscules de style titre](glossary.md), comme avec les noms d’utilisateur.
        -   Le nom de l’objet est décalé par un signe deux-points (exemple : nom de l’imprimante : mon imprimante).
        -   Le nom de l’objet peut être facilement déterminé à partir du contexte.
-   **Si vous devez tronquer les noms d’objets à une taille maximale fixe pour prendre en charge la localisation, utilisez des points de suspension pour indiquer la troncation.**

    ![capture d’écran du message contenant un nom abrégé ](images/mess-notif-image23.png)

    Dans cet exemple, un nom d’objet est tronqué à l’aide d’un bouton de sélection.

-   **Utilisez la formulation suivante si la notification est exploitable :**
    -   Si les utilisateurs peuvent cliquer sur la notification pour effectuer une action :

        < brève description des informations essentielles>

        <optional details>

        Cliquez sur pour <do something> .

        ![capture d’écran du message : « cliquez pour afficher la progression » ](images/mess-notif-image24.png)

        Dans cet exemple, les utilisateurs peuvent cliquer pour effectuer une action.

    -   Si les utilisateurs peuvent cliquer sur la notification pour afficher plus d’informations :

        < brève description des informations essentielles>

        <optional details>

        Cliquez pour plus d’informations.

        ![capture d’écran du message : cliquez pour plus d’informations ](images/mess-notif-image25.png)

        Dans cet exemple, les utilisateurs peuvent cliquer pour obtenir plus d’informations.

-   **Ne dites pas que l’utilisateur « doit » exécuter une action dans une notification.** Les notifications concernent les informations non critiques que les utilisateurs peuvent ignorer librement. Si les utilisateurs doivent vraiment exécuter une action, n’utilisez pas de notifications.
-   **Si les utilisateurs doivent effectuer une action, rendez l’importance claire.**
-   Pour l’échec d’action et les modèles d’événement système non critiques, **Décrivez les problèmes en langage simple.**

    **Incorrect :**

    ![capture d’écran d’un message long et complexe ](images/mess-notif-image26.png)

    Dans cet exemple, le problème est décrit à l’aide d’une langue trop technique, mais non spécifique.

    **Correct :**

    ![capture d’écran d’un message clair et concis ](images/mess-notif-image27.png)

    Dans cet exemple, le problème est décrit en langage simple.

-   **Décrivez l’événement d’une manière qui est pertinente pour les utilisateurs cibles.** Une notification est pertinente s’il y a un risque raisonnable que les utilisateurs effectuent une tâche ou modifient leur comportement en tant que résultat de la notification. Pour ce faire, vous pouvez souvent décrire les notifications en termes d’objectifs d’utilisateur au lieu de problèmes technologiques.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des notifications :

-   Utilisez le texte exact du titre, y compris sa mise en majuscules.
-   Reportez-vous au composant sous la forme d’une notification, et non d’une bulle ou d’une alerte.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme le texte du titre en gras. Sinon, placez le titre entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : lorsque la notification **mises à jour critiques prêtes à être installées** s’affiche, cliquez sur la notification pour démarrer le processus.

Lorsque vous faites référence à la zone de notification :

-   Reportez-vous à la zone de notification comme zone de notification, et non dans la barre d’état système.

 


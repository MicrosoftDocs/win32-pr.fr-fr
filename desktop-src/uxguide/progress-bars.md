---
title: Barres de progression
description: Avec une barre de progression, les utilisateurs peuvent suivre la progression d’une longue opération. Une barre de progression peut afficher un pourcentage approximatif d’achèvement (arrêt) ou indiquer qu’une opération est en cours (indéterminé).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6762be91d448c883a53c2977d506a0e1d638c26f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468336"
---
# <a name="progress-bars"></a>Barres de progression

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une barre de progression, les utilisateurs peuvent suivre la progression d’une longue opération. Une barre de progression peut afficher un pourcentage approximatif d’achèvement (arrêt) ou indiquer qu’une opération est en cours (indéterminé).

Les études de convivialité ont montré que les utilisateurs connaissent des temps de réponse de plus d’une seconde. Par conséquent, vous devez envisager des opérations qui nécessitent deux secondes ou plus pour être longues et nécessitant un certain type de commentaires sur la progression.

![capture d’écran d’une barre de progression classique ](images/progress-bars-image1.png)

Barre de progression classique.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’opération se termine-t-elle en environ cinq secondes ou moins ?** Si c’est le cas, utilisez un [indicateur d’activité](inter-mouse.md) à la place, car l’affichage d’une barre de progression pour une durée de ce type serait gênant. Si l’opération prend généralement cinq secondes ou moins, mais qu’elle prend parfois plus de temps, commencez avec un pointeur occupé et convertissez-la en barre de progression après cinq secondes.
-   **Une barre de progression indéterminée est-elle utilisée pour attendre que l’utilisateur termine une tâche ?** Dans ce cas, n’utilisez pas de barre de progression. Les barres de progression concernent la progression de l’ordinateur, pas la progression de l’utilisateur.
-   **Une barre de progression indéterminée est-elle associée à une animation ?** Dans ce cas, utilisez simplement l’animation à la place. La barre de progression indéterminée est effectivement une animation générique et n’ajoute aucune valeur à l’animation.
-   **L’opération est-elle une tâche en arrière-plan très longue (plus de deux minutes) pour laquelle les utilisateurs sont plus intéressés par la progression.** Si c’est le cas, utilisez [des notifications](mess-notif.md) à la place. Dans ce cas, les utilisateurs effectuent d’autres tâches en attendant et ne surveillent pas la progression. L’utilisation d’une notification permet aux utilisateurs d’effectuer d’autres tâches sans interruption. L’impression, la sauvegarde, les analyses système et les transferts de données en bloc et les conversions sont des exemples d’opérations de longue durée.
-   **Une fois l’opération terminée, les utilisateurs pourront-ils relire les résultats ?** Dans ce cas, utilisez un curseur à la place. Les opérations d’enregistrement et de lecture vidéo et audio sont des exemples de ces opérations.

    ![capture d’écran du lecteur multimédia et du curseur ](images/progress-bars-image2.png)

    Dans cet exemple, un curseur est utilisé pour indiquer la progression tout en lisant le son. Cela permet aux utilisateurs de relire les résultats ultérieurement.

## <a name="design-concepts"></a>Principes de conception

Au cours d’une opération longue, les utilisateurs ont besoin d’une idée générale de ce que fait l’opération. Ils doivent également connaître les éléments suivants :

-   Qu’une longue opération a démarré.
-   Cette progression est effectuée et la finalisation de l’opération se termine (et n’est donc pas verrouillée).
-   Pourcentage approximatif de l’opération qui a été effectué (et par conséquent le pourcentage restant).
-   S’ils doivent annuler l’opération s’il est inutile de continuer à attendre.
-   S’ils doivent continuer à attendre ou à effectuer une autre opération pendant que l’opération se termine.

**Utilisez les barres de progression de la désachèvement pour les opérations qui requièrent un laps de temps limité,** même si cette durée ne peut pas être prédite avec précision. Les barres de progression indéterminées indiquent que la progression est effectuée, mais ne fournit aucune autre information. Ne choisissez pas une barre de progression indéterminée uniquement en fonction du manque de précision possible uniquement.

Supposons, par exemple, qu’une opération nécessite cinq étapes et que chacune de ces étapes nécessite un laps de temps limité, mais la durée de chaque étape peut varier considérablement. Dans ce cas, utilisez une barre de progression déterminée et affichez la progression lorsque chaque étape se termine proportionnellement à la durée d’exécution de chaque étape. Utilisez une barre de progression indéterminée uniquement si une barre de progression qui se termine empêche les utilisateurs de conclure de manière incorrecte que l’opération a été verrouillée.

**Si vous n’avez qu’une seule chose...**

Veillez à fournir des commentaires sur la progression des opérations de longue durée et à communiquer clairement les informations ci-dessus. Utilisez les barres de progression de la déterminaison chaque fois que possible.

## <a name="usage-patterns"></a>Modèles d’usage

Les barres de progression ont plusieurs modèles d’utilisation :

### <a name="determinate-progress-bars"></a>Désarrêter les barres de progression




| | | <strong>Barres de progression de l’arrêt modal</strong><br /> Indiquez la progression d’une opération en remplissant de gauche à droite et en remplissant complètement une fois l’opération terminée. <br /> | Étant donné que ces commentaires sont <a href="glossary.md">modaux</a>, les utilisateurs ne peuvent pas effectuer d’autres tâches dans la fenêtre (ou son parent si celui-ci est affiché dans une boîte de dialogue modale) jusqu’à ce que l’opération soit terminée. <br /><img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br /> Dans cet exemple, la barre de progression donne des commentaires au cours de la configuration. <br /> | | <strong>Barre de progression des arrêts modaux avec un bouton Annuler ou arrêter</strong><br /> Autoriser les utilisateurs à arrêter l’opération, peut-être parce que l’opération prend trop de temps ou ne justifie pas l’attente.<br /> | <img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br /> Dans cet exemple, les utilisateurs peuvent cliquer sur arrêter pour arrêter l’opération et conserver l’environnement dans son état actuel.<br /> | | <strong>Barre de progression des arrêts modaux avec un bouton Annuler ou arrêter et une animation</strong><br /> Autorisez les utilisateurs à arrêter l’opération et incluez une animation pour aider les utilisateurs à visualiser l’effet d’une opération.<br /> | <img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br /> Dans cet exemple, les utilisateurs peuvent cliquer sur arrêter pour arrêter l’opération et conserver l’environnement dans son état actuel.<br /> | | <strong>Désarrêter les barres de progression de type modal</strong><br /> Indique la progression d’une opération en plusieurs étapes en indiquant la progression de l’étape actuelle dans la première barre de progression et la progression globale dans la deuxième barre.<br /> | Étant donné que la première barre de progression fournit peu d’informations supplémentaires et peut être très gênante, ce modèle n’est pas recommandé. Au lieu de cela, vous devez faire en sorte que toutes les étapes de l’opération partagent une partie de la progression et qu’une seule barre de progression passe à l’achèvement une fois. <br /><img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br /> Dans cet exemple, la première barre de progression affiche la progression de l’étape actuelle et la deuxième barre de progression indique la progression globale.<br /><blockquote>[!Note]<br />Ce modèle est généralement inutile et doit être évité.</blockquote><br /><br /> | | <strong>Barres de progression déterminées non modales</strong><br /> Indiquez la progression d’une opération en remplissant de gauche à droite et en remplissant complètement une fois l’opération terminée.<br /> | Contrairement aux barres de progression modales, les utilisateurs peuvent effectuer d’autres tâches pendant que l’opération est en cours. Ces barres de progression peuvent être affichées en contexte ou sur une barre d’État. <br /><img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br /> dans cet exemple, Windows internet ExplorerWindows internet Explorer affiche la progression du chargement d’une page Web dans la barre d’état. Les utilisateurs peuvent effectuer d’autres tâches pendant le chargement de la page.<br /> | 




 

### <a name="indeterminate-progress-bars"></a>Barres de progression indéterminées



|   Type de barre de progression  | Description             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barres de progression indéterminées modales**<br/> indiquez qu’une opération est en cours en présentant une animation qui continue continuellement à travers la barre de gauche à droite. <br/>   | Utilisé uniquement pour les opérations dont la progression globale ne peut pas être déterminée, donc il n’y a aucune notion d’exhaustivité. les barres de progression de désachèvement sont préférables, car elles indiquent le pourcentage approximatif de l’opération qui a été effectuée, et aident les utilisateurs à déterminer si l’opération doit continuer à attendre. ils sont également moins gênants. <br/> ![capture d’écran de la barre de progression modale](images/progress-bars-image8.png)<br/> dans cet exemple, Windows Update utilise une barre de progression modale modale pour indiquer la progression lors de la recherche de mises à jour.<br/> |
| **Barres de progression indéterminées non modales**<br/> indiquez qu’une opération est en cours en présentant une animation qui continue continuellement à travers la barre de gauche à droite.<br/> | Contrairement aux barres de progression modales, les utilisateurs peuvent effectuer d’autres tâches pendant que le traitement est en cours. Ces barres de progression peuvent être affichées en contexte ou sur une barre d’État. <br/> ![capture d’écran de la barre de progression fine dans la fenêtre Outlook ](images/progress-bars-image9.png)<br/> dans cet exemple, Microsoft Outlook utilise une barre de progression indéterminée non modale lors du remplissage des propriétés de contact. Les utilisateurs peuvent continuer à utiliser la fenêtre des propriétés pendant que ce travail est en cours.<br/>                                                                                                                    |



 

### <a name="meters"></a>Compteurs



|   Type                                                                                       |   Description                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mètres**<br/> Indiquez un pourcentage qui n’est pas lié à la progression. <br/> | Ce modèle n’est pas une barre de progression, mais il est implémenté à l’aide du contrôle de barre de progression. les compteurs ont une apparence distincte pour les différencier des véritables barres de progression. <br/> ![capture d’écran du compteur montrant l’espace disque disponible ](images/progress-bars-image10.png)<br/> Dans cet exemple, le compteur affiche le pourcentage d’espace disque utilisé.<br/> |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Fournissez des commentaires sur la progression de l’exécution d’une opération de longue durée.** Les utilisateurs ne doivent jamais deviner si la progression est effectuée.
-   **Indiquez clairement la progression réelle.** La barre de progression doit avancer si la progression est effectuée. Si la plage des durées d’achèvement attendues est importante, envisagez d’utiliser une échelle non linéaire pour indiquer la progression des longues périodes. Vous ne souhaitez pas que les utilisateurs se terminent que votre programme s’est bloqué quand il ne l’a pas fait.
-   **Indiquez clairement l’absence de progression.** La barre de progression ne doit pas avancer si aucune progression n’est effectuée. Vous ne souhaitez pas que les utilisateurs attendent indéfiniment une opération qui ne se termine pas.
-   **Fournissez des détails de progression utiles.** Fournissez des informations de progression supplémentaires, mais uniquement si les utilisateurs peuvent en faire une autre. Assurez-vous que le texte s’affiche suffisamment longtemps pour permettre aux utilisateurs de le lire.

    ![capture d’écran de la barre de progression montrant la vitesse de transfert ](images/progress-bars-image11.png)

    Dans cet exemple, les utilisateurs peuvent voir la vitesse de transfert. Le taux de transfert faible ici suggère la nécessité d’utiliser une connexion réseau à bande passante élevée.

-   **Ne fournissez pas de détails inutiles.** En général, les utilisateurs ne se soucient pas des détails de l’opération en cours d’exécution. Par exemple, les utilisateurs d’un programme d’installation ne se soucient pas du fichier en cours de copie ou des composants système en cours d’enregistrement, car ils n’ont pas d’attentes sur ces détails. En règle générale, une barre de progression correctement étiquetée fournit uniquement des informations suffisantes. par conséquent, fournissez des informations de progression supplémentaires uniquement si les utilisateurs peuvent en faire une autre. Le fait de fournir des détails qui ne s’intéressent pas aux utilisateurs rend l’expérience utilisateur trop complexe et technique. Si vous avez besoin d’informations plus détaillées pour le débogage, ne l’affichez pas dans les versions release.

    **Correct :**

    ![capture d’écran de la progression de l’installation ](images/progress-bars-image12.png)

    Dans cet exemple, la barre de progression étiquetée est tout ce qui est nécessaire.

    **Correct :**

    ![capture d’écran de la barre de progression montrant la vitesse de transfert ](images/progress-bars-image11.png)

    dans cet exemple, Windows Explorer copie les fichiers sélectionnés par l’utilisateur, de sorte que l’affichage des noms de fichiers en cours de copie est explicite.

    **Incorrect :**

    ![capture d’écran de la progression de l’inscription ](images/progress-bars-image13.png)

    Dans cet exemple, un programme d’installation fournit des détails qui n’ont pas de sens pour l’utilisateur.

-   **Fournissez des animations utiles.** Si c’est bien fait, les animations améliorent l’expérience utilisateur en aidant les utilisateurs à visualiser l’opération. Les bonnes animations ont un impact plus important que le texte seul. par exemple, la barre de progression de la commande Outlook Delete affiche la corbeille pour la destination si les fichiers peuvent être récupérés, mais aucune corbeille si les fichiers ne peuvent pas être récupérés.

    ![capture d’écran de la progression de la suppression ](images/progress-bars-image14.png)

    Dans cet exemple, l’absence d’une corbeille renforce la suppression définitive des fichiers. Ces informations supplémentaires ne sont pas communiquées de manière efficace à l’aide de texte seul.

-   **N’utilisez pas d’animations inutiles.** Les animations peuvent être trompeuses, car elles s’exécutent généralement dans un thread séparé de la tâche réelle et peuvent par conséquent suggérer la progression même si l’opération a été verrouillée. En outre, si l’opération est plus lente que prévu, les utilisateurs partent parfois du principe que l’animation fait partie de la raison. Par conséquent, utilisez uniquement des animations lorsqu’il y a une justification claire ; ne les utilisez pas pour tenter de divertir les utilisateurs.
-   **Place les animations centrées sur la barre de progression.** Placez l’animation au-dessus des étiquettes de la barre de progression, si vous en avez un. S’il y a un bouton Annuler ou arrêter à droite de la barre de progression, incluez le bouton lors de la détermination du centre.
-   **Émettre un effet sonore à l’achèvement d’une opération uniquement si elle est très longue (plus de deux minutes), peu fréquentes et importantes.** Si l’utilisateur est susceptible de quitter une opération importante pendant son traitement, un effet sonore rétablit l’attention de l’utilisateur. L’utilisation d’un effet sonore à l’achèvement dans d’autres circonstances serait gênante.
-   **Ne dérobez pas le focus d’entrée pour afficher une mise à jour ou une fin de progression.** Les utilisateurs basculent souvent vers d’autres programmes en attente et ne veulent pas être interrompus. Les tâches en arrière-plan doivent rester en arrière-plan.
-   **Ne vous inquiétez pas du support technique.** Étant donné que les commentaires fournis par les barres de progression ne sont pas nécessairement précis et qu’ils flottent, les barres de progression ne sont pas un bon moyen de fournir des informations pour le support technique. Par conséquent, si l’opération peut échouer (comme avec un programme d’installation), ne fournissez pas d’informations de progression supplémentaires qui ne sont utiles que pour le support technique. Au lieu de cela, fournissez un autre mécanisme comme un fichier journal pour enregistrer les informations de support technique.

    **Incorrect :**

    ![capture d’écran de la barre de progression montrant le nom du serveur ](images/progress-bars-image15.png)

    Dans cet exemple, la barre de progression présente des détails destinés au support technique.

-   **Ne placez pas le pourcentage terminé ou tout autre texte sur une barre de progression.** Ce texte n’est pas accessible et n’est pas compatible avec l’utilisation de thèmes.

    **Incorrect :**

    ![capture d’écran de la barre de progression avec du texte dans la barre ](images/progress-bars-image16.png)

    Dans cet exemple, le texte de pourcentage sur la barre de progression n’est pas accessible.

-   **Ne combinez pas une barre de progression à un pointeur occupé.** Utilisez l’un ou l’autre, mais pas les deux à la fois.
-   **N’utilisez pas de barres de progression verticales.** Les barres de progression horizontales ont un mappage plus naturel et un meilleur Flow.

### <a name="determinate-progress-bars"></a>Désarrêter les barres de progression

-   **Utilisez les barres de progression de la désachèvement pour les opérations qui requièrent un laps de temps limité,** même si cette durée ne peut pas être prédite avec précision. Les barres de progression indéterminées indiquent que la progression est effectuée, mais ne fournit aucune autre information. Ne choisissez pas une barre de progression indéterminée uniquement en fonction du manque de précision possible uniquement.
-   **Indiquez clairement la phase de progression.** La barre de progression doit être en mesure d’indiquer si l’opération est au début, au milieu ou à la fin d’une opération. Par exemple, les barres de progression qui se déforment immédiatement à 99% de l’achèvement, puis restent là pendant une longue période sont particulièrement informatives et ennuyeux. Dans ce cas, la barre de progression doit être définie initialement sur au plus 33 pour cent pour indiquer que l’opération est toujours en phase de début.
-   **Indiquez clairement la fin de l’opération.** Ne laissez pas une barre de progression aller à 100%, sauf si l’opération est terminée.
-   **Indiquez une estimation du temps restant si vous pouvez le faire correctement.** Les estimations de temps restantes qui sont exactes sont utiles, mais les estimations qui sont en dehors de la marque ou du rebond autour ne sont pas utiles. Vous devrez peut-être effectuer un traitement avant de pouvoir fournir des estimations précises. Dans ce cas, n’affichez pas d’estimations potentiellement inexactes au cours de cette période initiale.
-   **Ne pas redémarrer la progression.** Une barre de progression perd sa valeur si elle redémarre (peut-être parce qu’une étape de l’opération se termine), car les utilisateurs n’ont aucun moyen de savoir à quel moment l’opération se termine. Au lieu de cela, vous devez faire en sorte que toutes les étapes de l’opération partagent une partie de la progression et que la barre de progression passe à l’achèvement une fois.

    **Incorrect :**

    ![capture d’écran de la barre de progression qui a redémarré ](images/progress-bars-image17.png)

    Dans cet exemple, l’opération a été déplacée vers l’étape de copie des fichiers et de réinitialisation de la barre de progression pour cette étape. Désormais, les utilisateurs n’ont aucune idée de la progression ou du temps restant.

-   **Ne pas sauvegarder la progression.** Comme pour un redémarrage, une barre de progression perd sa valeur si elle est sauvegardée. Augmentez toujours la progression de façon monotone. Toutefois, vous pouvez avoir une estimation du temps restant qui augmente (et diminue), car le taux de progression peut varier.

### <a name="indeterminate-progress-bars"></a>Barres de progression indéterminées

-   **Utilisez des barres de progression indéterminées uniquement pour les opérations dont la progression globale ne peut pas être déterminée.** Utilisez des barres de progression indéterminées pour les opérations qui nécessitent une durée illimitée ou qui accèdent à un nombre inconnu d’objets. Utilisez des délais d’attente pour accorder des limites aux opérations basées sur le temps.
-   **Convertit en barre de progression d’arrêt une fois que la progression globale peut être déterminée.** Par exemple, s’il faut beaucoup plus de deux secondes pour déterminer le nombre d’objets, vous pouvez utiliser une barre de progression indéterminée pendant que les objets sont comptés, puis effectuer une conversion en une barre de progression qui se termine.
-   **Ne combinez pas des barres de progression indéterminées avec des estimations de pourcentage d’achèvement ou de temps restant.** Si vous pouvez fournir ces informations, utilisez une barre de progression arrêtée à la place.
-   **Ne combinez pas des barres de progression indéterminées avec des animations.** Une barre de progression indéterminée est effectivement une animation générique. vous devez donc utiliser l’une ou l’autre, mais jamais les deux à la fois.

    **Correct :**

    ![capture d’écran de la progression de la détection du serveur ](images/progress-bars-image18.png)

    Dans cet exemple, seule une animation est utilisée pour montrer qu’une opération est en cours.

### <a name="modeless-progress-bars"></a>Barres de progression non modales

-   **Si les utilisateurs peuvent effectuer des opérations productives pendant que l’opération est en cours, fournissez un feedback non modal.** Vous devrez peut-être désactiver un sous-ensemble de fonctionnalités qui requièrent l’exécution de l’opération.
-   **Si la fenêtre possède une barre d’adresses, affichez la progression non modale dans la barre d’adresses.**

    ![capture d’écran de la barre de progression dans la barre d’adresse ](images/progress-bars-image19.png)

    Dans cet exemple, la progression non modale s’affiche dans la barre d’adresses.

-   Sinon, **si la fenêtre a une barre d’État, affichez la progression non modale dans la barre d’État.** Placez tout texte correspondant à gauche dans la barre d’État.

    ![capture d’écran de la barre de progression dans la barre d’État ](images/progress-bars-image7.png)

    Dans cet exemple, la progression non modale s’affiche dans la barre d’État.

### <a name="modal-progress-bars"></a>Barres de progression modales

-   **Placez les barres de progression modales sur les pages de progression ou les boîtes de dialogue de** [progression](win-dialog-box.md).
-   **Fournissez un bouton de commande pour arrêter l’opération si elle prend plus de quelques secondes ou si elle peut ne pas se terminer.** Étiquette le bouton Annuler si l’annulation rétablit l’état précédent de l’environnement (sans effet secondaire). sinon, étiquetez l’arrêt du bouton pour indiquer qu’il laisse l’opération partiellement terminée intacte. Vous pouvez modifier l’étiquette du bouton Annuler pour arrêter au milieu de l’opération si, à un moment donné, il n’est pas possible de rétablir l’état précédent de l’environnement. Centrez le bouton de commande verticalement avec la barre de progression au lieu d’aligner son sommet.

    **Correct :**

    ![capture d’écran de la progression de l’attente du réseau ](images/progress-bars-image20.png)

    Dans cet exemple, l’arrêt de la connexion réseau n’a aucun effet secondaire, l’annulation est donc utilisée.

    **Correct :**

    ![capture d’écran de la barre de progression montrant l’heure de la copie à gauche ](images/progress-bars-image21.png)

    Dans cet exemple, l’arrêt de la copie laisse les fichiers copiés, donc le bouton de commande s’intitule arrêter.

    **Incorrect :**

    ![capture d’écran de la barre de progression de la recherche et du bouton arrêter ](images/progress-bars-image22.png)

    Dans cet exemple, l’arrêt de la recherche ne laisse aucun effet secondaire, donc le bouton de commande doit être étiqueté annuler.

### <a name="time-remaining"></a>Temps restant

Pour arrêter les barres de progression :

-   **Utilisez les formats d’heure suivants.** Commencez par le premier des formats suivants, où la plus grande unité de temps n’est pas égale à zéro, puis passez au format suivant une fois que la plus grande unité de temps devient zéro.

    **Pour les barres de progression :**

    **Si les informations connexes sont affichées au format deux-points :**

    Temps restant : h heures, m minutes

    Temps restant : m minutes, s secondes

    Temps restant : s secondes

    **Si l’espace à l’écran est à un niveau Premium :**

    h h, m min restant

    m min, s secondes restantes

    s secondes restantes

    **Sinon :**

    h heures, m minutes restantes

    m minutes, s secondes restantes

    s secondes restantes

    **Pour les barres de titre :**

    hh : mm restant

    mm : SS restant

    0 : SS restant

    Ce format compact affiche d’abord les informations les plus importantes afin qu’elles ne soient pas tronquées dans la barre des tâches.

-   **Effectuez des estimations précises, mais n’attribuez pas une précision fausse.** Si la plus grande unité est hours, indiquez les minutes (si significatives) mais pas les secondes.

    **Incorrect :**

    hh heures, mm minutes, SS secondes

-   **Maintenez l’estimation à jour.** Mettre à jour les estimations de temps restant au moins toutes les 5 secondes.
-   **Concentrez-vous sur le temps restant** , car il s’agit des informations que les utilisateurs ont le plus de soin. Indiquez le temps total écoulé uniquement lorsque des scénarios où le temps écoulé est utile (par exemple, lorsque la tâche est susceptible d’être répétée). Si l’estimation du temps restant est associée à une barre de progression, n’avez pas de texte d’achèvement de pourcentage, car ces informations sont transmises par la barre de progression elle-même.
-   **Corriger par programmation.** Utilisez des unités singulières lorsque le nombre est un.

    **Incorrect :**

    1 minute, 1 seconde

-   **Utilisez les majuscules comme pour les phrases.**

### <a name="progress-bar-colors"></a>Couleurs de la barre de progression

-   **Utilisez les barres de progression rouge ou jaune uniquement pour indiquer l’état de progression, et non les résultats finaux d’une tâche.** Une barre de progression rouge ou jaune indique que les utilisateurs doivent prendre des mesures pour terminer la tâche. Si la condition n’est pas récupérable, laissez la barre de progression verte et affichez un message d’erreur.
-   **Activez la barre de progression en rouge lorsqu’il existe une condition récupérable par l’utilisateur qui empêche la poursuite de la progression.** Affichez un message pour expliquer le problème et recommander une solution.
-   **Activez la barre de progression en jaune pour indiquer que l’utilisateur a suspendu la tâche ou qu’il existe une condition qui entrave la progression** , mais que la progression est toujours en cours (par exemple, avec une connectivité réseau médiocre). Si l’utilisateur a été suspendu, remplacez l’étiquette du bouton suspendre par reprendre. Si la progression est entravée, affichez un message pour expliquer le problème et recommander une solution.

### <a name="meters"></a>Compteurs

-   **Utilisez les barres de progression uniquement pour la progression.** Utilisez des compteurs pour indiquer les pourcentages qui ne sont pas liés à la progression.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![Diagramme montrant le dimensionnement et l’espacement de la barre de progression ](images/progress-bars-image23.png)

Dimensionnement et espacement recommandés pour les barres de progression.

-   Utilisez toujours la hauteur de la barre de progression recommandée.
    -   **Exception :** Vous pouvez utiliser une autre hauteur si la fenêtre parente ne prend pas en charge la hauteur recommandée.
-   Utilisez la largeur minimale si vous souhaitez rendre la barre de progression discrète.
-   N’utilisez pas de largeur supérieure à la valeur maximale recommandée. La barre de progression n’a pas besoin de remplir l’espace disponible.
-   Centrer la barre de progression horizontalement si la fenêtre est bien plus large que la largeur maximale recommandée.

## <a name="labels"></a>Étiquettes

### <a name="progress-bar-labels"></a>Étiquettes de la barre de progression

-   **Utilisez une étiquette concise avec un contrôle de texte statique pour indiquer ce que l’opération fait.** Démarrez l’étiquette avec un verbe (par exemple, copie) et terminez par des points de suspension. Cette étiquette peut changer dynamiquement si l’opération comporte plusieurs étapes ou s’il traite plusieurs objets.
-   N’attribuez pas une [clé d’accès](glossary.md) unique, car le contrôle n’est pas interactif.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Si l’opération n’a pas été lancée directement par l’utilisateur, vous pouvez inclure une étiquette supplémentaire pour fournir le contexte et excuser l’interruption. Démarrez cette étiquette supplémentaire avec l’expression, veuillez patienter pendant. Cette étiquette ne doit pas changer au cours de l’opération.

    ![capture d’écran de la barre de progression avec l’étiquette ](images/progress-bars-image24.png)

    Dans cet exemple, l’utilisateur est invité à patienter, car l’utilisateur n’a pas lancé l’opération directement.

-   Placez l’étiquette au-dessus de la barre de progression et alignez l’étiquette sur le bord gauche de la barre de progression.

### <a name="progress-bar-details"></a>Détails de la barre de progression

-   Fournissez des détails dans du texte statique, en faisant précéder les données d’une étiquette se terminant par un signe deux-points. Spécifiez les unités (secondes, kilo-octets, etc.) après le texte des détails.

    **Correct :**

    ![capture d’écran de la barre de progression montrant la vitesse de transfert ](images/progress-bars-image11.png)

    Dans cet exemple, les détails sont correctement étiquetés.

    **Incorrect :**

    ![capture d’écran de la barre de progression sans étiquette appropriée ](images/progress-bars-image25.png)

    Dans cet exemple, les détails ne sont pas étiquetés, ce qui oblige les utilisateurs à déterminer leur signification.

-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Placez les détails sous la barre de progression et alignez l’étiquette sur le bord gauche de la barre de progression.
-   Ne fournissez pas le pourcentage terminé ou restant, car ces informations sont transmises par la barre de progression elle-même.

### <a name="cancel-button"></a>Bouton Annuler

-   Étiquette le bouton Annuler si l’annulation retourne l’environnement à son état précédent (sans effet secondaire); Sinon, étiquetez l’arrêt du bouton pour indiquer qu’il laisse l’opération partiellement terminée intacte.
-   Vous pouvez modifier l’étiquette du bouton Annuler pour arrêter au milieu de l’opération si, à un moment donné, il n’est pas possible de rétablir l’état précédent de l’environnement.

### <a name="progress-dialog-box-titles"></a>Titres de la boîte de dialogue de progression

-   Si la barre de progression s’affiche dans une boîte de dialogue modale, le titre de la boîte de dialogue doit être le nom du programme ou le nom de l’opération. N’utilisez pas ce qui doit être l’étiquette de la barre de progression pour le titre de la boîte de dialogue.

    **Correct :**

    ![capture d’écran du titre de la barre de progression avec le nom de la tâche ](images/progress-bars-image26.png)

    Dans cet exemple, le nom de la tâche est utilisé pour le titre de la boîte de dialogue.

    **Incorrect :**

    ![capture d’écran du titre de boîte de dialogue redondante ](images/progress-bars-image27.png)

    Dans cet exemple, le texte du titre de la boîte de dialogue est un Remode de l’étiquette de la barre de progression. Le nom du programme doit être utilisé à la place.

-   Si la barre de progression s’affiche dans une boîte de dialogue non modale, optimisez le titre à afficher dans la barre des tâches en plaçant d’abord les informations distinctives. Exemple : « 66% terminé ».

 


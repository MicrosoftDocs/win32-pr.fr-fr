---
title: Messages d’erreur (concepts de base de la conception)
description: Un message d’erreur avertit les utilisateurs d’un problème qui s’est déjà produit.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0ceffd3d1fecccd8342cb1e634735653bdba9722
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469016"
---
# <a name="error-messages-design-basics"></a>Messages d’erreur (concepts de base de la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Un message d’erreur avertit les utilisateurs d’un problème qui s’est déjà produit. En revanche, un message d’avertissement avertit les utilisateurs d’une condition susceptible de provoquer un problème à l’avenir. Des messages d’erreur peuvent être présentés à l’aide de boîtes de dialogue modales, de messages sur place, de notifications ou de bulles.

![capture d’écran du message d’erreur : impossible de renommer](images/mess-error-image1.png)

Message d’erreur modal classique.

Les messages d’erreur effectifs informent les utilisateurs qu’un problème s’est produit, expliquent pourquoi il s’est produit et fournissent une solution qui permet aux utilisateurs de résoudre le problème. Les utilisateurs doivent exécuter une action ou modifier leur comportement à la suite d’un message d’erreur.

Des messages d’erreur utiles et bien écrits sont essentiels pour une expérience utilisateur de qualité. Des messages d’erreur mal écrits entraînent une faible satisfaction du produit et constituent une cause de risque pour des coûts de support technique évitables. Des messages d’erreur inutiles rompent le déroulement des utilisateurs.

**Remarque :** Les instructions relatives [aux boîtes de dialogue](win-dialog-box.md), aux messages d' [Avertissement](mess-warn.md), aux [confirmations](mess-confirm.md), aux [icônes standard](vis-std-icons.md), aux [notifications](mess-notif.md)et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

- **L’interface utilisateur présente-t-elle un problème qui s’est déjà produit ?** Si ce n’est pas le cas, le message n’est pas une erreur. Si l’utilisateur est alerté d’une condition susceptible de provoquer un problème à l’avenir, utilisez un message d’avertissement.
- **Le problème peut-il être évité sans entraîner de confusion ?** Dans ce cas, empêchez plutôt le problème. Par exemple, utilisez des contrôles qui sont limités à des valeurs valides au lieu d’utiliser des contrôles non restreints qui peuvent nécessiter des messages d’erreur. De plus, désactivez les contrôles en cas d’erreur, à condition qu’il soit évident que le contrôle est désactivé.
- **Le problème peut-il être corrigé automatiquement ?** Dans ce cas, gérez le problème et supprimez le message d’erreur.
- **Les utilisateurs sont susceptibles d’effectuer une action ou de modifier leur comportement en tant que résultat du message ?** Si ce n’est pas le cas, la condition ne justifie pas l’interruption de l’utilisateur. il est donc préférable de supprimer l’erreur.
- **Le problème est-il lié à l’utilisation active d’autres programmes par les utilisateurs ?** Dans ce cas, envisagez d’illustrer le problème à l’aide d’une [icône de zone de notification](winenv-notification.md).
- **Le problème n’est-il pas lié à l’activité de l’utilisateur actuel, il ne nécessite pas d’action immédiate de l’utilisateur et les utilisateurs peuvent-ils l’ignorer librement ?** Dans ce cas, utilisez une [notification d’échec d’action](mess-notif.md) à la place.
- **Le problème est-il lié à l’état d’une tâche en arrière-plan dans une fenêtre principale ?** Si c’est le cas, envisagez d’illustrer le problème à l’aide des [barres d’État](ctrl-status-bars.md).
- **Les principaux utilisateurs ciblent-ils les professionnels de l’informatique ?** Si c’est le cas, envisagez d’utiliser un autre mécanisme de commentaires, comme des entrées de [fichier journal](glossary.md) ou des alertes par courrier électronique. Les professionnels de l’informatique préfèrent fortement les fichiers journaux pour les informations non critiques.

## <a name="design-concepts"></a>Principes de conception

**Caractéristiques des messages d’erreur médiocres**

Il ne devrait pas être surprenant qu’il y ait de nombreux messages d’erreur gênants, incorrects et mal écrits. Et étant donné que les messages d’erreur sont souvent présentés à l’aide de boîtes de dialogue modales, ils interrompent l’activité actuelle de l’utilisateur et la demande à être confirmée avant de permettre à l’utilisateur de continuer.

Une partie du problème est qu’il existe de nombreuses façons de le faire. Prenons l’exemple des messages d’erreur de dommage :

**Messages d’erreur inutiles**

**Incorrect :**

![capture d’écran du message d’erreur : échec de l’application ](images/mess-error-image2.png)

cet exemple de Windows XP peut être le pire message d’erreur. elle indique qu’un programme n’a pas pu être lancé, car Windows lui-même est en cours d’arrêt. il n’y a rien à faire que l’utilisateur peut faire à ce sujet (l’utilisateur a choisi d’arrêter Windows, après tout). en affichant ce message d’erreur, Windows empêche son arrêt !

**Le problème :** Le message d’erreur lui-même est le problème. Hormis le fait de rejeter le message d’erreur, il n’y a rien à faire pour les utilisateurs.

**Cause principale :** Signalement de tous les cas d’erreur, quels que soient les objectifs ou le point de vue des utilisateurs.

**Alternative recommandée :** Ne signalez pas les erreurs qui ne se soucient pas des utilisateurs.

**Messages d’erreur de « réussite »**

**Incorrect :**

![capture d’écran du message d’erreur : échec de la suppression ](images/mess-error-image3.png)

ce message d’erreur est dû au fait que l’utilisateur a choisi de ne pas redémarrer Windows immédiatement après la suppression du programme. La suppression du programme a été effectuée à partir du point de vue de l’utilisateur.

**Le problème :** Il n’y a aucune erreur du point de vue de l’utilisateur. Hormis le fait de rejeter le message d’erreur, il n’y a rien à faire pour les utilisateurs.

**Cause principale :** La tâche s’est terminée correctement du point de vue de l’utilisateur, mais a échoué à partir du point de vue du programme de désinstallation.

**Alternative recommandée :** Ne signalez pas les erreurs pour les conditions que les utilisateurs considèrent comme acceptables.

**Messages d’erreur complètement inutiles**

**Incorrect :**

![capture d’écran du message d’erreur : erreur inconnue ](images/mess-error-image4.png)

Les utilisateurs apprennent qu’une erreur s’est produite, mais n’ont aucune idée de l’erreur ou de la marche à suivre. Et non, ce n’est pas OK !

**Le problème :** Le message d’erreur ne fournit pas de problème spécifique et il n’y a rien à faire pour les utilisateurs.

**Cause principale :** Probablement, le programme a une mauvaise gestion des erreurs.

**Alternative recommandée :** Concevoir une bonne gestion des erreurs dans le programme.

**Messages d’erreur incompréhensibles**

**Incorrect :**

![capture d’écran du message d’erreur : sauvegarde non terminée ](images/mess-error-image5.png)

Dans cet exemple, la déclaration de problème est claire, mais l’explication supplémentaire est le chicane.

**Le problème :** La solution ou l’instruction à problème est incompréhensible.

**Cause principale :** Explication du problème du point de vue du code à la place de l’utilisateur.

**Alternative recommandée :** Écrire le texte du message d’erreur que vos utilisateurs cibles peuvent facilement comprendre. Fournissez des solutions que les utilisateurs peuvent réellement effectuer. La conception de l’expérience du message d’erreur de votre programme n’a pas de programmeurs qui composent des messages d’erreur à l’endroit.

**Messages d’erreur qui surcommuniquent**

**Incorrect :**

![capture d’écran d’un message extrêmement détaillé ](images/mess-error-image6.png)

Dans cet exemple, le message d’erreur tente apparemment d’expliquer chaque étape de dépannage.

**Le problème :** Trop d’informations.

**Cause principale :** Donner trop de détails ou essayer d’expliquer un processus de dépannage complexe dans un message d’erreur.

**Alternative recommandée :** Évitez les détails inutiles. Évitez également les dépannages. Si vous avez besoin d’un utilitaire de résolution des problèmes, concentrez-vous sur les solutions les plus probables et expliquez le reste en établissant un lien vers la rubrique appropriée dans l’aide.

**Messages d’erreur inutilement difficiles**

**Incorrect :**

![capture d’écran du message : objet introuvable ](images/mess-error-image7.png)

L’impossibilité pour le programme de trouver un objet n’est pas une catastrophe. En supposant qu’il s’agit d’une catastrophe, pourquoi la réponse est-elle correcte ?

**Le problème :** La tonalité du programme est inutilement trop importante ou spectaculaire.

**Cause principale :** Le problème est dû à un bogue qui apparaît catastrophique du point de vue du programme.

**Alternative recommandée :** Choisissez langue avec soin en fonction du point de vue de l’utilisateur.

**Messages d’erreur qui ont pour responsabilité les utilisateurs**

**Incorrect :**

![capture d’écran du message : caractère non conforme ](images/mess-error-image8.png)

Pourquoi faire en sorte que les utilisateurs ressemblent à un criminel ?

**Le problème :** Le message d’erreur est formulées d’une façon qui accuses à l’utilisateur de faire une erreur.

**Cause principale :** Formulation non sensible qui se concentre sur le comportement de l’utilisateur plutôt que sur le problème.

**Alternative recommandée :** Concentrez-vous sur le problème, et non sur l’action de l’utilisateur qui a entraîné le problème, en utilisant la voix passive en fonction des besoins.

**Messages d’erreur idiots**

**Incorrect :**

![capture d’écran du message : erreur dans le rapport d’erreurs ](images/mess-error-image9.png)

Dans cet exemple, l’énoncé du problème est relativement Iron et aucune solution n’est fournie.

**Le problème :** Les instructions de message d’erreur sont idiotes ou non-des abandons.

**Cause principale :** Création de messages d’erreur sans tenir considération de leur contexte.

**Alternative recommandée :** Faites en sorte que vos messages d’erreur soient élaborés et revus par un rédacteur. Tenez compte du contexte et de l’état de l’utilisateur lorsque vous examinez les erreurs.

**Messages d’erreur du programmeur**

**Incorrect :**

![capture d’écran du message : adresse de violation d’accès ](images/mess-error-image10.png)

Dans cet exemple, le message d’erreur indique qu’il existe un bogue dans le programme. Ce message d’erreur a une signification uniquement pour le programmeur.

**Le problème :** Les messages destinés à aider les développeurs du programme à trouver des bogues sont laissés dans la version finale du programme. Ces messages d’erreur n’ont aucune signification ni valeur pour les utilisateurs.

**Cause principale :** Les programmeurs utilisant une interface utilisateur normale pour faire des messages à eux-mêmes.

**Alternative recommandée :** Les développeurs doivent compiler de façon conditionnelle tous les messages de ce type afin qu’ils soient automatiquement supprimés de la version finale d’un produit. Ne perdez pas de temps à essayer d’effectuer des erreurs comme celle qui est compréhensible pour les utilisateurs, car leur seul public est le programmeur.

**Messages d’erreur mal présentés**

**Incorrect :**

![capture d’écran du message : défaillance inattendue ](images/mess-error-image11.png)

Cet exemple présente de nombreuses erreurs de présentation courantes.

**Le problème :** Obtention de tous les détails erronés dans la présentation du message d’erreur.

**Cause principale :** Vous ne connaissez pas et n’appliquez pas les instructions relatives aux messages d’erreur. N’utilise pas les rédacteurs et les éditeurs pour créer et consulter les messages d’erreur.

La nature de la gestion des erreurs est telle que la plupart de ces erreurs sont très faciles à effectuer. Il est inquiétant de constater que la plupart des messages d’erreur peuvent être nomines pour le hall de dommage.

**Caractéristiques des messages d’erreur corrects**

Contrairement aux exemples incorrects précédents, les messages d’erreur corrects ont :

- **Un problème.** Indique qu’un problème s’est produit.
- **Une cause.** Explique pourquoi le problème s’est produit.
- **Une solution.** Fournit une solution qui permet aux utilisateurs de résoudre le problème.

En outre, les messages d’erreur corrects sont présentés de la façon suivante :

- **Nécessaire.** Le message présente un problème auquel les utilisateurs se soucient.
- **Exploitables.** Les utilisateurs doivent exécuter une action ou modifier leur comportement en tant que résultat du message.
- **Centrée sur l’utilisateur.** Le message décrit le problème en termes d’actions ou d’objectifs de l’utilisateur cible, et non pas en termes d’insatisfaction du code.
- **Brève.** Le message est aussi bref que possible, mais pas plus petit.
- **Effacé.** Le message utilise un langage simple afin que les utilisateurs cibles puissent facilement comprendre le problème et la solution.
- **Plus.** Le message décrit le problème à l’aide d’une langue spécifique, en attribuant des noms spécifiques, des emplacements et des valeurs des objets concernés.
- **Courtois.** Les utilisateurs ne doivent pas être mis en cause ou être stupides.
- **Rares.** Affiché rarement. Les messages d’erreur fréquemment affichés sont un signe de mauvaise conception.

En concevant votre expérience de gestion des erreurs de façon à ce que vous disposiez de ces caractéristiques, vous pouvez conserver les messages d’erreur de votre programme en dehors de la salle de dommage des messages d’erreur.

**Éviter les messages d’erreur inutiles**

Souvent, le meilleur message d’erreur n’est pas un message d’erreur. De nombreuses erreurs peuvent être évitées par une meilleure conception, et il existe souvent de meilleures alternatives aux messages d’erreur. Il est généralement préférable d’éviter une erreur plutôt que d’en signaler une.

Les messages d’erreur les plus évidents à éviter sont ceux qui ne sont pas exploitables. Si les utilisateurs sont susceptibles de faire disparaître le message sans effectuer ou modifier quoi que ce soit, omettez le message d’erreur.

Certains messages d’erreur peuvent être éliminés, car ils ne sont pas des problèmes du point de vue de l’utilisateur. Supposons, par exemple, que l’utilisateur a tenté de supprimer un fichier qui est déjà en cours de suppression. Bien qu’il s’agisse d’un cas inattendu du point de vue du code, les utilisateurs ne considèrent pas cette erreur comme le résultat souhaité.

**Incorrect :**

![capture d’écran du message : impossible de supprimer le fichier ](images/mess-error-image12.png)

Ce message d’erreur doit être éliminé, car l’action a été correctement effectuée du point de vue de l’utilisateur.

Pour un autre exemple, supposons que l’utilisateur annule explicitement une tâche. Pour le point de vue de l’utilisateur, la condition suivante n’est pas une erreur.

**Incorrect :**

![capture d’écran du message : impossible de terminer la sauvegarde ](images/mess-error-image13.png)

Ce message d’erreur doit également être éliminé, car l’action a été correctement effectuée du point de vue de l’utilisateur.

Parfois, les messages d’erreur peuvent être éliminés en se concentrant sur les objectifs des utilisateurs au lieu de la technologie. Dans ce cas, reconsidérez ce qu’est vraiment une erreur. Le problème est-il lié aux objectifs de l’utilisateur ou à la capacité de votre programme à les satisfaire ? Si l’action de l’utilisateur a un sens dans le monde réel, elle doit également être pertinente dans le logiciel.

Supposons, par exemple, qu’un utilisateur tente de trouver un produit à l’aide de la recherche dans un programme de commerce électronique, mais que la requête de recherche littérale n’a pas de correspondance et que le produit souhaité ne soit plus stocké. Techniquement, il s’agit d’une erreur, mais au lieu de fournir un message d’erreur, le programme peut :

- Continuez à rechercher les produits qui correspondent le mieux à la requête.
- Si la recherche comporte des erreurs évidentes, recommandez automatiquement une requête corrigée.
- Gérer automatiquement les problèmes courants tels que les fautes d’orthographe, les orthographes alternatives et les cas de pluralisation et de casse des verbes.
- Indiquez le moment où le produit sera en stock.

Tant que la demande de l’utilisateur est raisonnable, un programme de commerce électronique bien conçu devrait retourner des résultats raisonnables sans erreurs.

Vous pouvez également éviter les messages d’erreur en empêchant les problèmes en premier lieu. Vous pouvez éviter les erreurs en procédant comme suit :

- **Utilisation de contrôles limités.** Utilisez des contrôles qui sont limités à des valeurs valides. Les contrôles tels que les listes, les curseurs, les cases à cocher, les cases d’option et les sélecteurs de date et d’heure sont limités aux valeurs valides, alors que les zones de texte ne sont souvent pas et peuvent nécessiter des messages d’erreur. Toutefois, vous pouvez contraindre les zones de texte à accepter uniquement certains caractères et accepter un nombre maximal de caractères.
- **Utilisation des interactions avec restriction.** Pour les opérations de glisser-déplacer, autoriser les utilisateurs à supprimer uniquement les cibles valides.
- **Utilisation des contrôles désactivés et des éléments de menu.** Désactivez les contrôles et les éléments de menu lorsque les utilisateurs peuvent facilement déduire la raison pour laquelle le contrôle ou l’élément de menu est désactivé.
- **Fournir les bonnes valeurs par défaut.** Les utilisateurs sont moins susceptibles d’effectuer des erreurs d’entrée s’ils peuvent accepter les valeurs par défaut. Même si les utilisateurs décident de modifier la valeur, la valeur par défaut permet aux utilisateurs de connaître le format d’entrée attendu.
- **Faire fonctionner simplement des choses.** Les utilisateurs sont moins susceptibles de commettre des erreurs si les tâches sont inutiles ou exécutées automatiquement pour eux. Ou si les utilisateurs font de petites erreurs, mais que leur intention est claire, le problème est résolu automatiquement. Par exemple, vous pouvez corriger automatiquement les problèmes de mise en forme mineurs.

**Fournir les messages d’erreur nécessaires**

Il est parfois nécessaire de fournir un message d’erreur. Les utilisateurs font des erreurs, les réseaux et les périphériques cessent de fonctionner, les objets sont introuvables ou modifiés, les tâches ne peuvent pas être effectuées et les programmes présentent des bogues. Dans l’idéal, ces problèmes se produisent moins souvent, par exemple, nous pouvons concevoir nos logiciels pour empêcher de nombreux types d’erreurs utilisateur, mais il n’est pas réaliste d’éviter tous ces problèmes. Et lorsque l’un de ces problèmes se produit, un message d’erreur utile permet aux utilisateurs de revenir rapidement à leurs pieds.

L’une des convictions courantes est que les messages d’erreur sont les pires expériences utilisateur et doivent être évités à tout prix, mais il est plus précis de dire que la confusion des utilisateurs est la pire expérience et doit être évitée à tous les coûts. Parfois, ce coût est un message d’erreur utile.

Envisagez les contrôles désactivés. La plupart du temps, il est évident qu’un contrôle est désactivé, donc la désactivation du contrôle est un excellent moyen d’éviter un message d’erreur. Toutefois, que se passe-t-il si la raison pour laquelle un contrôle est désactivé n’est pas évidente ? L’utilisateur ne peut pas continuer et il n’y a pas de commentaire pour déterminer le problème. L’utilisateur est maintenant bloqué et doit déduire le problème ou obtenir un support technique. Dans ce cas, il est préférable de laisser le contrôle activé et de fournir un message d’erreur utile à la place.

**Incorrect :**

![capture d’écran du message : où enregistrer la sauvegarde ? ](images/mess-error-image14.png)

Pourquoi le bouton suivant est-il désactivé ici ? Mieux pour la garder activée et éviter toute confusion utilisateur en donnant un message d’erreur utile.

Si vous ne savez pas si vous devez fournir un message d’erreur, commencez par composer le message d’erreur que vous pouvez fournir. Si les utilisateurs sont susceptibles d’effectuer une action ou de modifier leur comportement en conséquence, fournissez le message d’erreur. En revanche, si les utilisateurs sont susceptibles de faire disparaître le message sans effectuer ou modifier quoi que ce soit, omettez le message d’erreur.

**Conception pour une bonne gestion des erreurs**

Bien que la création d’un bon texte de message d’erreur puisse être difficile, il est parfois impossible de recourir à un bon support de gestion des erreurs du programme. Considérez ce message d’erreur :

**Incorrect :**

![capture d’écran du message : erreur inconnue ](images/mess-error-image15.png)

Il y a de fortes chances, le problème est vraiment inconnu, car la prise en charge de la gestion des erreurs du programme est absente.

Bien qu’il soit possible qu’il s’agisse d’un message d’erreur très mal écrit, il reflète probablement l’absence de bonne gestion des erreurs par le code sous-jacent, aucune information spécifique n’est connue sur le problème.

Afin de créer des messages d’erreur spécifiques, exploitables et centrés sur l’utilisateur, le code de gestion des erreurs de votre programme doit fournir des informations d’erreur spécifiques et de haut niveau :

- Chaque problème doit être associé à un code d’erreur unique.
- Si un problème a plusieurs causes, le programme doit déterminer la cause spécifique dans la mesure du possible.
- Si le problème a des paramètres, les paramètres doivent être conservés.
- Les problèmes de bas niveau doivent être traités à un niveau suffisamment élevé afin que le message d’erreur puisse être présenté à partir du point de vue de l’utilisateur.

De bons messages d’erreur ne sont pas seulement un problème d’interface utilisateur, mais il s’agit d’un problème de conception logicielle. Une bonne expérience de message d’erreur ne peut pas être réutilisée ultérieurement.

**Résolution des problèmes (et comment l’éviter)**

La résolution des problèmes se produit lorsqu’un problème avec plusieurs causes différentes est signalé par un message d’erreur unique.

**Incorrect :**

![diagramme d’un message indiquant trois causes ](images/mess-error-image16.png)

**Correct :**

![diagramme de trois messages indiquant une cause](images/mess-error-image17.png)

Résolution des résultats lorsque plusieurs problèmes sont signalés avec un seul message d’erreur.

Dans l’exemple suivant, un élément n’a pas pu être déplacé, car il a déjà été déplacé ou supprimé, ou l’accès a été refusé. Si le programme peut facilement déterminer la cause du problème, pourquoi imposer-vous la charge de l’utilisateur pour déterminer la cause spécifique ?

**Incorrect :**

![capture d’écran d’un message indiquant deux causes ](images/mess-error-image18.png)

Eh bien, qu’est-ce que c’est ? L’utilisateur doit maintenant résoudre les problèmes.

Le programme peut déterminer si l’accès a été refusé. ce problème doit donc être signalé avec un message d’erreur spécifique.

**Correct :**

![capture d’écran du message indiquant une cause ](images/mess-error-image19.png)

En raison d’une cause spécifique, aucune résolution des problèmes n’est requise.

Utilisez des messages avec plusieurs causes uniquement lorsque la cause spécifique ne peut pas être déterminée. Dans cet exemple, il serait difficile pour le programme de déterminer si l’élément a été déplacé ou supprimé. par conséquent, un seul message d’erreur avec plusieurs causes peut être utilisé ici. Toutefois, il est peu probable que les utilisateurs se soucient si, par exemple, ils n’ont pas pu déplacer un fichier supprimé. Pour ces causes, le message d’erreur n’est même pas nécessaire.

**Gestion des erreurs inconnues**

Dans certains cas, vous ne connaissez pas réellement le problème, la cause ou la solution. S’il est déconseillé de supprimer l’erreur, il est préférable d’être au début du manque d’informations que de présenter des problèmes, des causes ou des solutions qui peuvent ne pas être correctes.

Par exemple, si votre programme a une exception non gérée, le message d’erreur suivant est approprié :

![capture d’écran du message : une erreur inconnue s’est produite ](images/mess-error-image20.png)

Si vous ne pouvez pas supprimer une erreur inconnue, il est préférable d’être au début du manque d’informations.

En revanche, vous pouvez fournir des informations spécifiques et exploitables si elles sont susceptibles d’être utiles la plupart du temps.

![capture d’écran montrant un message Office Communicator’serveur non disponible'. ](images/mess-error-image21.png)

Ce message d’erreur est approprié pour une erreur inconnue si la connectivité réseau est généralement le problème.

**Déterminer le type de message approprié**

Certains problèmes peuvent être présentés sous la forme d’une erreur, d’un avertissement ou d’informations, en fonction de l’importance et de la formulation. par exemple, supposons qu’une page Web ne peut pas charger un contrôle de ActiveX non signé basé sur la configuration actuelle de Windows Internet Explorer :

- **Erreurs.** « cette page ne peut pas charger un contrôle de ActiveX non signé ». (Formulées en tant que problème existant.)
- **Tres.** « cette page peut ne pas se comporter comme prévu, car Windows Internet Explorer n’est pas configuré pour charger les contrôles de ActiveX non signés ». ou «autoriser cette page à installer un contrôle de ActiveX non signé ? Cette opération à partir de sources non approuvées peut endommager votre ordinateur.» (Les deux formulées comme des conditions qui peuvent entraîner des problèmes futurs.)
- **Informations.** « vous avez configuré Windows Internet Explorer pour bloquer les contrôles de ActiveX non signés ». (Formulées en tant que déclaration de faits.)

**Pour déterminer le type de message approprié, concentrez-vous sur l’aspect le plus important du problème que les utilisateurs doivent connaître ou agir.** En règle générale, si un problème empêche l’utilisateur de continuer, vous devez le présenter comme une erreur. Si l’utilisateur peut continuer, présentez-le en tant qu’avertissement. Élaborez l' [instruction principale](text-ui.md) ou un autre texte correspondant en fonction de ce Focus, puis choisissez une icône ([standard](vis-std-icons.md) ou autre) qui correspond au texte. Le texte d’instruction principal et les icônes doivent toujours correspondre.

**Présentation des messages d’erreur**

la plupart des messages d’erreur dans Windows programmes sont présentés à l’aide de boîtes de dialogue modales (comme dans la plupart des exemples de cet article), mais il existe d’autres options :

- Sur place
- Bulles
- Notifications
- Icônes de la zone de notification
- Barres d'état
- Fichiers journaux (pour les erreurs destinées aux professionnels de l’informatique)

Le fait de placer des messages d’erreur dans des boîtes de dialogue modales présente l’avantage de demander l’attention immédiate de l’utilisateur et l’accusé de réception. Toutefois, il s’agit également de leur inconvénient principal si cette attention n’est pas nécessaire.

![capture d’écran du message : arrêter ce que vous effectuez ](images/mess-error-image22.png)

Avez-vous vraiment besoin d’interrompre les utilisateurs pour qu’ils puissent cliquer sur le bouton Fermer ? Si ce n’est pas le cas, envisagez d’utiliser une boîte de dialogue modale.

Les boîtes de dialogue modales sont un bon choix lorsque l’utilisateur doit accuser réception du problème immédiatement avant de continuer, mais souvent un mauvais choix. En règle générale, il est préférable d’utiliser la présentation poids le plus clair qui fait le travail.

**Éviter la surcommunication**

En règle générale, [les utilisateurs ne lisent pas](vis-layout.md). Plus le texte est grand, plus le texte est difficile à analyser et plus les utilisateurs sont susceptibles de lire le texte. Par conséquent, il est important de réduire le texte à ses fondamentaux, et d’utiliser la divulgation progressive et les liens d’aide quand cela est nécessaire pour fournir des informations supplémentaires.

Il existe de nombreux exemples extrêmes, mais examinons un peu plus en exemple. L’exemple suivant présente la plupart des attributs d’un bon message d’erreur, mais son texte n’est pas concis et nécessite une motivation pour la lecture.

**Incorrect :**

![capture d’écran du message détaillé ](images/mess-error-image23.png)

Cet exemple est un bon message d’erreur, mais il surcommunique.

Qu’est-ce que tout ce texte est vraiment dit ? Un peu comme ceci :

**Correct :**

![capture d’écran du message : enregistreur de CD non détecté ](images/mess-error-image24.png)

Ce message d’erreur a essentiellement les mêmes informations, mais il est beaucoup plus concis.

En utilisant l’aide pour fournir les détails, ce message d’erreur a un [style pyramidal inversé](text-ui.md) de présentation.

Pour obtenir plus d’instructions et des exemples sur la surcommunication, consultez texte de l' [interface utilisateur](text-ui.md).

**Si vous ne faites que huit choses**

1. Concevez votre programme pour la gestion des erreurs.
2. Ne fournissez pas de messages d’erreur inutiles.
3. Évitez les confusions utilisateur en donnant les messages d’erreur nécessaires.
4. Assurez-vous que le message d’erreur indique un problème, une cause et une solution.
5. Assurez-vous que le message d’erreur est pertinent, actionnable, concis, clair, spécifique, courtois et rare.
6. Concevez les messages d’erreur du point de vue de l’utilisateur, et non le point de vue du programme.
7. Éviter d’impliquer l’utilisateur lors de la résolution des problèmes utilisez un autre message d’erreur pour chaque cause détectable.
8. Utilisez la méthode de présentation poids le plus clair qui effectue le travail.

**Modèles d’usage**

Les messages d’erreur ont plusieurs modèles d’utilisation :


| | | <strong>Problèmes système</strong><br /> Le système d’exploitation, le périphérique matériel, le réseau ou le programme a échoué ou n’est pas dans l’État requis pour effectuer une tâche. <br /> | De nombreux problèmes système peuvent être résolus par l’utilisateur : <br /><ul><li>Les problèmes de périphérique peuvent être résolus en mettant l’appareil sous tension, en reconnectant l’appareil et en insérant des médias.</li><li>Les problèmes réseau peuvent être résolus en vérifiant la connexion au réseau physique et en exécutant le <strong>diagnostic et la réparation du réseau</strong>.</li><li>Vous pouvez résoudre les problèmes liés aux programmes en modifiant les options du programme ou en redémarrant le programme.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> Dans cet exemple, le programme ne peut pas trouver d’appareil photo pour effectuer une tâche utilisateur.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> Dans cet exemple, une fonctionnalité requise pour effectuer une tâche doit être activée.<br /> | | <strong>Problèmes liés aux fichiers</strong><br /> Un fichier ou un dossier requis pour une tâche initiée par l’utilisateur est introuvable, est déjà utilisé ou n’a pas le format attendu. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> Dans cet exemple, le fichier ou le dossier ne peut pas être supprimé car il n’a pas été trouvé.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> Dans cet exemple, le programme ne prend pas en charge le format de fichier donné.<br /> | | <strong>Problèmes de sécurité</strong><br /> L’utilisateur n’a pas l’autorisation d’accéder à une ressource, ou un privilège suffisant pour effectuer une tâche initiée par l’utilisateur. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> Dans cet exemple, l’utilisateur n’a pas l’autorisation d’accéder à une ressource.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> Dans cet exemple, l’utilisateur n’a pas le privilège d’effectuer une tâche.<br /> | | <strong>Problèmes de tâche</strong><br /> Un problème spécifique est survenu lors de l’exécution d’une tâche initiée par l’utilisateur (autre qu’un système, fichier introuvable, format de fichier ou problème de sécurité). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> Dans cet exemple, les données du presse-papiers ne peuvent pas être collées dans Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> Dans cet exemple, l’utilisateur ne peut pas installer une mise à niveau logicielle.<br /> | | <strong>Problèmes d’entrée d’utilisateur</strong><br /> L’utilisateur a entré une valeur incorrecte ou incohérente avec d’autres entrées utilisateur. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> Dans cet exemple, l’utilisateur a entré une valeur d’heure incorrecte.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> Dans cet exemple, l’entrée utilisateur n’est pas au bon format.<br /> | 


## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

- **Utilisez les boîtes de dialogue de tâches chaque fois que nécessaire** pour obtenir une apparence et une disposition cohérentes. les boîtes de dialogue de tâches requièrent Windows Vista ou version ultérieure. elles ne conviennent donc pas aux versions antérieures de Windows. Si vous devez utiliser une boîte de message, séparez l’instruction principale de l’instruction supplémentaire par deux sauts de ligne.

### <a name="user-input-errors"></a>Erreurs d’entrée utilisateur

- **Dans la mesure du possible, évitez ou réduisez les erreurs d’entrée utilisateur en :**
  - Utilisation de contrôles qui sont limités à des valeurs valides.
  - La désactivation des contrôles et des éléments de menu en cas de clic entraînerait une erreur, à condition qu’il soit évident que le contrôle ou l’élément de menu est désactivé.
  - Fournir les bonnes valeurs par défaut.

**Incorrect :**

![capture d’écran de la zone de texte avec l’étiquette de volume de l’intervenant ](images/mess-error-image35.png)

Dans cet exemple, une zone de texte sans contrainte est utilisée pour l’entrée contrainte. Utilisez plutôt un curseur.

- **Utilisez la gestion des erreurs non modale (erreurs ou bulles sur place) pour les problèmes d’entrée d’utilisateur contextuel.**
- **Utilisez des bulles pour les problèmes d’entrée d’utilisateur non critiques détectés dans une zone de texte ou immédiatement après qu’une zone de texte perd le focus.** Les [bulles](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) ne nécessitent pas d’espace d’écran disponible ou la disposition dynamique requise pour afficher des messages sur place. Affichez une seule bulle à la fois. Étant donné que le problème n’est pas critique, aucune icône d’erreur n’est nécessaire. Les bulles disparaissent quand l’utilisateur clique dessus, lorsque le problème est résolu ou après un délai d’attente.

![capture d’écran du message : caractère incorrect ](images/mess-error-image36.png)

Dans cet exemple, une bulle indique un problème d’entrée tout en restant dans le contrôle.

- **Utilisez des erreurs sur place pour la détection des erreurs différées,** généralement des erreurs trouvées en cliquant sur un bouton de validation. (N’utilisez pas d' [Erreurs sur place](glossary.md) pour les paramètres qui sont validés immédiatement.) Il peut y avoir plusieurs erreurs sur place à la fois. Utilisez du texte normal et une icône d’erreur de 16x16 pixels, en les plaçant directement en regard du problème, dans la mesure du possible. Les erreurs sur place ne sont pas supprimées, sauf si l’utilisateur est validé et qu’aucune autre erreur n’est détectée.

![capture d’écran du message : adresse de messagerie incorrecte ](images/mess-error-image37.png)

Dans cet exemple, une erreur sur place est utilisée pour une erreur trouvée en cliquant sur le bouton valider.

- **Utilisez la gestion des erreurs modale (boîtes de dialogue de tâches ou boîtes de message) pour tous les autres problèmes,** y compris les erreurs qui impliquent plusieurs contrôles ou sont des erreurs non contextuelles ou non contextuelles trouvées par un clic sur un bouton de validation.
- **Lorsqu’un problème d’entrée d’utilisateur est signalé, définissez le focus d’entrée sur le premier contrôle avec les données incorrectes.** Faites défiler le contrôle vers l’affichage si nécessaire. Si le contrôle est une zone de texte, sélectionnez tout le contenu. Il doit toujours être évident à quoi le message d’erreur fait référence.
- **Ne désactivez pas l’entrée incorrecte.** Au lieu de cela, laissez-le à l’utilisateur pour qu’il puisse voir et corriger le problème sans recommencer.
  - **Exception :** Effacez les zones de texte mot de passe et code confidentiel incorrectes, car les utilisateurs ne peuvent pas corriger efficacement l’entrée masquée.

### <a name="troubleshooting"></a>Dépannage

- **Évitez de créer des problèmes de dépannage.** Ne vous fiez pas à un seul message d’erreur pour signaler un problème avec plusieurs causes détectables différentes.
- **Utilisez un autre message d’erreur (généralement une autre instruction supplémentaire) pour chaque cause détectable.** Par exemple, si un fichier ne peut pas être ouvert pour plusieurs raisons, fournissez une instruction supplémentaire distincte pour chaque raison.
- **Utilisez un message avec plusieurs causes uniquement lorsque la cause spécifique ne peut pas être déterminée.** Dans ce cas, présentez les solutions pour pouvoir résoudre le problème. Cela permet aux utilisateurs de résoudre plus efficacement le problème.

### <a name="icons"></a>Icônes

- **Les boîtes de dialogue des messages d’erreur modaux n’ont pas d’icônes de barre de titre.** Les icônes de barre de titre sont utilisées comme une distinction visuelle entre les fenêtres principales et les fenêtres secondaires.
- **Utilisez une icône d’erreur.** Exceptions :
  - Si l’erreur est un problème d’entrée utilisateur affiché à l’aide d’une boîte de dialogue modale ou d’une bulle, n’utilisez pas d’icône. Cela se fait en ce qui concerne le ton encourageant de Windows. Toutefois, les messages d’erreur sur place doivent utiliser une petite icône d’erreur (16x16 pixels) pour les identifier clairement en tant que messages d’erreur.

     ![capture d’écran du format postal du message incorrect](images/mess-error-image38.png)

     ![capture d’écran du message nom de l’ordinateur trop longue](images/mess-error-image39.png)

     Dans ces exemples, les problèmes d’entrée d’utilisateur n’ont pas besoin d’icônes d’erreur.

     ![capture d’écran du format de numéro de téléphone du message incorrect](images/mess-error-image40.png)

     Dans cet exemple, un message d’erreur sur place a besoin d’une petite icône d’erreur pour l’identifier clairement en tant que message d’erreur.

- Si le problème concerne une fonctionnalité qui a une icône (et non un problème d’entrée d’utilisateur), vous pouvez utiliser l’icône de fonctionnalité avec une superposition d’erreur. Si vous procédez ainsi, utilisez également le nom de la fonctionnalité comme objet de l’erreur.

    ![capture d’écran message le lecteur multimédia ne peut pas lire le fichier ](images/mess-error-image41.png)

    Dans cet exemple, l’icône de fonctionnalité a une superposition d’erreur et la fonctionnalité est l’objet de l’erreur.

- **N’utilisez pas les icônes d’avertissement pour les erreurs.** Cela est souvent fait pour rendre la présentation moins grave. Les erreurs ne sont pas des avertissements.

    **Incorrect :**

    ![capture d’écran de la commutation rapide de message non activée ](images/mess-error-image42.png)

    Dans cet exemple, une icône d’avertissement est utilisée de manière incorrecte pour que l’erreur semble moins grave.

Pour obtenir des instructions et des exemples supplémentaires, consultez [icônes standard](vis-std-icons.md).

### <a name="progressive-disclosure"></a>Affichage progressif

- **Utilisez le bouton afficher/masquer les détails de la divulgation progressive pour masquer les informations avancées ou détaillées dans un message d’erreur.** Cela simplifie le message d’erreur pour une utilisation classique. Ne masquez pas les informations nécessaires, car les utilisateurs ne le trouvent peut-être pas.

![capture d’écran du message : ActiveSync ne peut pas ouvrir de session ](images/mess-error-image43.png)

Dans cet exemple, le bouton de divulgation progressive aide les utilisateurs à accéder à plus de détails s’ils le souhaitent, ou à simplifier l’interface utilisateur si ce n’est pas le cas.

- **N’utilisez pas afficher/masquer les détails à moins qu’il y ait vraiment plus de détails.** Ne restatez pas uniquement les informations existantes dans un format plus détaillé.
- **N’utilisez pas afficher/masquer les détails pour afficher les informations d’aide.** Utilisez à la place des liens d’aide.

Pour obtenir des instructions sur l’étiquetage, consultez [contrôles de divulgation progressif](ctrl-progressive-disclosure-controls.md).

**Ne plus afficher ce message**

- **Si un message d’erreur a besoin de cette option, réexaminez l’erreur et sa fréquence.** S’il possède toutes les caractéristiques d’une bonne erreur (pertinente, actionnable et rare), il ne devrait pas être logique pour les utilisateurs de le supprimer.

Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).

### <a name="default-values"></a>Valeurs par défaut

- **Sélectionnez le niveau de réponse le plus sûr, le moins destructif ou le plus sécurisé par défaut.** Si la sécurité n’est pas un facteur, sélectionnez la commande la plus probable ou la plus pratique.

### <a name="help"></a>Aide

- **Concevez des messages d’erreur pour éviter d’avoir besoin d’aide.** Normalement, les utilisateurs ne doivent pas avoir à lire le texte externe pour comprendre et résoudre le problème, à moins que la solution ne nécessite plusieurs étapes.
- **Assurez-vous que le contenu de l’aide est pertinent et utile.** Il ne doit pas s’agir d’un reformatage détaillé du message d’erreur. il doit contenir des informations utiles qui n’entrent pas dans le cadre du message d’erreur, notamment des moyens d’éviter le problème à l’avenir. Ne fournissez pas de lien d’aide juste parce que vous pouvez.
- **Utilisez des liens d’aide spécifiques, concis et pertinents pour accéder au contenu de l’aide.** N’utilisez pas de boutons de commande ou de divulgation progressive à cet effet.
- **Pour les messages d’erreur que vous ne pouvez pas rendre spécifiques et exploitables, envisagez de fournir des liens vers le contenu de l’aide en ligne.** En procédant ainsi, vous pouvez fournir aux utilisateurs des informations supplémentaires que vous pouvez mettre à jour une fois le programme publié.

Pour plus d’instructions, consultez [l’aide](winenv-help.md)de.

### <a name="error-codes"></a>Codes d’erreur

- **Pour les messages d’erreur que vous ne pouvez pas rendre spécifiques et exploitables ou qui tirent parti de l’aide, pensez à fournir également des codes d’erreur.** Les utilisateurs utilisent souvent ces codes d’erreur pour rechercher des informations supplémentaires sur Internet.
- **Fournissez toujours un texte de description du problème et de la solution.** Ne dépendez pas uniquement du code d’erreur à cet effet.

**Incorrect :**

![capture d’écran du message : impossible d’ouvrir le fichier ](images/mess-error-image44.png)

Dans cet exemple, un code d’erreur est utilisé comme substitut d’un texte de solution.

- **Attribuez un code d’erreur unique pour chaque cause.** Cela permet d’éviter la résolution des problèmes.
- **Choisissez des codes d’erreur pouvant faire l’objet de recherches facilement sur Internet.** Si vous utilisez des codes 32 bits, utilisez une représentation hexadécimale avec un « 0x » et des caractères majuscules de début.

**Correct :**

1234

0xC0001234

**Incorrect :**

-1

-67113524

- **Utilisez afficher/masquer les détails pour afficher les codes d’erreur.** Expression comme code d’erreur : <error code> .

![capture d’écran du message : le programme n’a pas été initialisé ](images/mess-error-image45.png)

Dans cet exemple, un code d’erreur est utilisé pour compléter un message d’erreur qui peut bénéficier d’informations supplémentaires.

### <a name="sound"></a>Son

- **Ne pas accompagner les messages d’erreur avec un effet sonore ou un bip.** Cela est transférerez et inutile.
  - **Exception :** Jouez l’effet de son arrêt critique si le problème est critique pour le fonctionnement de l’ordinateur, et si l’utilisateur doit prendre des mesures immédiates pour éviter des conséquences graves.

## <a name="text"></a>Texte

**Général**

- **Supprimez le texte redondant.** Recherchez-en les titres, les instructions principales, les instructions supplémentaires, les liens de commande et les boutons de validation. En règle générale, laissez le texte intégral dans les instructions et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
- **Utilisez les explications centrées sur l’utilisateur.** Décrivez le problème en termes d’actions ou d’objectifs de l’utilisateur, et non en termes d’insatisfaction des logiciels. Utilisez la langue que les utilisateurs cibles comprennent et utilisent. Évitez le jargon technique.

**Incorrect :**

![capture d’écran du message : entrée-appel synchrone ](images/mess-error-image46.png)

**Correct :**

![capture d’écran du message : occupée recevant un appel ](images/mess-error-image47.png)

Dans ces exemples, la version appropriée parle de la langue de l’utilisateur, alors que la version incorrecte est trop technique.

- **N’utilisez pas les mots suivants :**
  - Erreur, échec (utilisez à la place le problème)
  - Échec de (utilisation impossible à la place)
  - Non conforme, non valide, mauvais (utilisez incorrect à la place)
  - Abandonner, arrêter, terminer (utilisez plutôt Stop)
  - Catastrophique, fatale (utilisation grave à la place)

Ces termes sont inutiles et contraires au ton encourageant de Windows. Lorsqu’il est [utilisé correctement](vis-std-icons.md), l’icône d’erreur indique qu’il y a un problème.

**Incorrect :**

![capture d’écran du message : échec catastrophique ! ](images/mess-error-image48.png)

**Correct :**

![capture d’écran du message : la sauvegarde doit être fermée à la fois ](images/mess-error-image49.png)

Dans l’exemple incorrect, les termes « catastrophique » et « Failure » ne sont pas nécessaires.

- N’utilisez pas de formulation qui est responsable de l’utilisateur ou qui implique une erreur de l’utilisateur. Évitez d’utiliser vous et votre dans la formulation. Alors que la voix active est généralement préférée, utilisez la voix passive lorsque l’utilisateur est l’objet et peut-être être responsable de l’erreur si la voix active a été utilisée.

**Incorrect :**

![capture d’écran du message que vous avez entrée incorrecte ](images/mess-error-image50.png)

**Correct :**

![capture d’écran du message : mot de passe incorrect ](images/mess-error-image51.png)

L’exemple incorrect est responsable de l’utilisateur à l’aide de la voix active.

- **Être spécifiques.** Évitez les formulations vagues, telles que l’erreur de syntaxe et l’opération illégale. Fournissez des noms, des emplacements et des valeurs spécifiques des objets concernés.

**Incorrect :**

Fichier introuvable.

Le disque est saturé.

Valeur hors limites.

Le caractère n’est pas valide.

Appareil non disponible.

Ces problèmes seraient beaucoup plus faciles à résoudre avec des noms, des emplacements et des valeurs spécifiques.

- **N’autorisez pas des problèmes, des causes ou des solutions susceptibles d’être spécifiques.** Ne fournissez pas de problème, de cause ou de solution, sauf s’il est probable qu’il soit correct. Par exemple, il est préférable de dire qu’une erreur inconnue s’est produite qu’un problème susceptible d’être inexact.
- **Évitez le mot « Merci »,** sauf dans les situations où l’utilisateur est invité à faire un peu de confort (comme en attente) ou si le logiciel est responsable de la situation.

**Correct :**

veuillez patienter pendant que Windows copie les fichiers sur votre ordinateur.

- **Utilisez le mot « désolée » uniquement dans les messages d’erreur qui entraînent des problèmes graves pour l’utilisateur** (par exemple, une perte de données ou une incapacité à utiliser l’ordinateur). Ne vous inquiétez pas si le problème s’est produit au cours du fonctionnement normal du programme (par exemple, si l’utilisateur doit attendre la détection d’une connexion réseau).

**Correct :**

Nous sommes désolés, mais Fabrikam Backup a détecté un problème irrécupérable et a été arrêté pour protéger les fichiers sur votre ordinateur.

- **Reportez-vous aux produits à l’aide de leurs noms courts.** N’utilisez pas les noms de produits complets ou les symboles de marque. N’incluez pas le nom de la société, sauf si les utilisateurs associent le nom de la société au produit. N’incluez pas de numéros de version de programme.

**Incorrect :**

![capture d’écran montrant un message d’Microsoft Office Outlook « impossible d’ouvrir cet élément ». ](images/mess-error-image52.png)

**Correct :**

![capture d’écran du message : impossible d’ouvrir cet élément ](images/mess-error-image53.png)

Dans l’exemple incorrect, les noms de produits complets et les symboles de marque sont utilisés.

- **Utilisez des guillemets doubles autour des noms d’objets.** Cela rend le texte plus facile à analyser et évite les instructions potentiellement gênantes.
  - **Exception :** Les chemins d’accès complets aux fichiers, les URL et les noms de domaine n’ont pas besoin d’être entre guillemets doubles.

**Correct :**

![capture d’écran du message : « ma maison » n’est pas disponible ](images/mess-error-image54.png)

Dans cet exemple, le message d’erreur serait confus si le nom de l’objet ne se trouvait pas entre guillemets.

- **Évitez de démarrer des phrases avec des noms d’objets.** Cela est souvent difficile à analyser.
- **N’utilisez pas de points d’exclamation ou de mots avec des majuscules.** Les points d’exclamation et les lettres majuscules vous informent que vous craignez l’utilisateur.

Pour obtenir des instructions et des exemples supplémentaires, consultez [style et tonal](text-style-tone.md).

**Titres**

- **Utilisez le titre pour identifier la commande ou la fonctionnalité à l’origine de l’erreur.** Exceptions :
  - Si une erreur est affichée par de nombreuses commandes différentes, envisagez d’utiliser le nom du programme à la place.
  - Si ce titre est redondant ou confus avec l’instruction principale, utilisez le nom du programme à la place.
- **N’utilisez pas le titre pour expliquer ou résumer le problème** qui est l’objectif de l’instruction principale.

**Incorrect :**

![Capture d’écran montrant un message « Impossible de renommer le nouveau dossier ». ](images/mess-error-image55.png)

Dans cet exemple, le titre est incorrectement utilisé pour expliquer le problème.

- Utilisez la mise en majuscules de style titre, sans ponctuation finale.

**Instructions principales**

- **Utilisez l’instruction principale pour décrire le problème en clair, en clair et dans un langage spécifique.**
- **N’utilisez qu’une seule phrase complète.** Réduisez l’instruction principale aux informations essentielles. Vous pouvez faire en sorte que l’objet soit implicite s’il s’agit de votre programme ou de l’utilisateur. Incluez la raison du problème si vous pouvez le faire de façon concise. Si vous devez apporter des explications supplémentaires, utilisez une instruction supplémentaire.

**Incorrect :**

![capture d’écran du message : impossible d’installer la mise à niveau ](images/mess-error-image56.png)

Dans cet exemple, le message d’erreur entier est placé dans l’instruction principale, ce qui le rend difficile à lire.

- **Être spécifique s’il y a des objets impliqués, donnez-leur des noms.**
- **Évitez de placer des chemins d’accès complets et des URL dans l’instruction principale.** Au lieu de cela, utilisez un nom abrégé (tel que le nom de fichier) et le nom complet (par exemple, le chemin d’accès du fichier) dans l’instruction supplémentaire. Toutefois, vous pouvez placer un seul chemin d’accès de fichier complet ou une seule URL dans l’instruction principale si le message d’erreur n’a pas besoin d’une instruction supplémentaire.

![capture d’écran du message : impossible de supprimer le fichier Fabrikam ](images/mess-error-image57.png)

Dans cet exemple, seul le nom de fichier se trouve dans l’instruction principale. Le chemin d’accès complet se trouve dans l’instruction supplémentaire.

- **Ne fournissez pas le chemin d’accès complet et l’URL du fichier s’il est évident du contexte.**

![capture d’écran du message : impossible de renommer le nouveau dossier ](images/mess-error-image58.png)

dans cet exemple, l’utilisateur renomme un fichier à partir de Windows Explorer. Dans ce cas, le chemin d’accès complet du fichier n’est pas nécessaire, car il est évident du contexte.

- Utilisez-les à chaque fois que cela est possible.
- Utilisez les majuscules comme pour les phrases.
- N’incluez pas de périodes finales si l’instruction est une instruction. Si l’instruction est une question, incluez un point d’interrogation final.

**Modèles d’instructions principaux**

Bien qu’il n’existe pas de règles strictes pour les formulations, essayez d’utiliser les modèles d’instruction principaux suivants dans la mesure du possible :

- [nom de l’objet facultatif] ne peut pas [effectuer l’action]
- [nom de l’objet facultatif] ne peut pas [effectuer l’action], car [raison]
- [nom de l’objet facultatif] ne peut pas [effectuer d’action] en « [nom de l’objet] »
- [nom d’objet facultatif] ne peut pas [effectuer d’action] en « [nom de l’objet] », car [raison]
- Il n’y a pas assez de [ressource] pour [exécuter l’action]
- [Nom d’objet] n’a pas de [nom d’objet] requis pour [Purpose]
- [Appareil ou paramètre] est désactivé afin que les [résultats indésirables]
- [Appareil ou paramètre] n’est pas [disponible \| \| \| activé activé]
- « [nom de l’objet] » n’est pas disponible actuellement
- Le nom d’utilisateur ou le mot de passe est incorrect
- Vous n’avez pas l’autorisation d’accéder à « [nom de l’objet] »
- Vous n’avez pas de privilège pour [exécuter action]
- [nom du programme] a rencontré un problème grave et doit se fermer immédiatement

Bien sûr, apportez les modifications nécessaires pour que l’instruction principale soit correcte par programmation et conforme aux instructions principales de l’instruction.

**Instructions supplémentaires**

- Utilisez l’instruction supplémentaire pour :
  - Donnez des détails supplémentaires sur le problème.
  - Expliquez la cause du problème.
  - Répertoriez les étapes que l’utilisateur peut entreprendre pour résoudre le problème.
  - Fournissez des mesures pour éviter que le problème ne se reproduise.
- **Dans la mesure du possible, proposez une solution pratique et utile pour que les utilisateurs puissent résoudre le problème.** Toutefois, assurez-vous que la solution proposée est susceptible de résoudre le problème. Ne gaspillez pas le temps des utilisateurs en suggérant des solutions possibles, mais improbables.

**Incorrect :**

![capture d’écran du message : mémoire insuffisante ](images/mess-error-image59.png)

Dans cet exemple, si le problème et sa solution recommandée sont possibles, ils sont très peu probables.

- **Si le problème est une valeur incorrecte que l’utilisateur a entrée, utilisez l’instruction supplémentaire pour expliquer les valeurs correctes.** Les utilisateurs ne doivent pas avoir à déterminer ces informations à partir d’une autre source.
- **Ne fournissez pas de solution si elle peut être déduite de façon triviale de l’instruction de problème.**

![capture d’écran du message : valeur d’heure incorrecte ](images/mess-error-image33.png)

Dans cet exemple, aucune instruction supplémentaire n’est nécessaire ; la solution peut être déduite de façon triviale de l’instruction de problème.

- **Si la solution comporte plusieurs étapes, présentez les étapes dans l’ordre dans lequel elles doivent être terminées.** Toutefois, évitez les solutions à plusieurs étapes, car les utilisateurs ont des difficultés à mémoriser plus de deux ou trois étapes simples. Si des étapes supplémentaires sont requises, reportez-vous à la rubrique d’aide appropriée.
- **Conservez les instructions supplémentaires de manière concise.** Fournissez uniquement ce que les utilisateurs doivent savoir. Omettez les détails inutiles. L’objectif est d’un maximum de trois phrases de longueur modérée.
- **Pour éviter des erreurs pendant que les utilisateurs effectuent des instructions, placez les résultats avant l’action.**

**Correct :**

pour redémarrer Windows, cliquez sur OK.

**Incorrect :**

Cliquez sur OK pour redémarrer Windows.

Dans l’exemple incorrect, il est plus probable que les utilisateurs cliquent sur OK par accident.

- **Il est déconseillé de contacter un administrateur, sauf si cela fait partie des solutions les plus probables au problème.** Réservez ces solutions pour les problèmes qui ne peuvent être résolus que par un administrateur.

**Incorrect :**

![capture d’écran du message : serveur non disponible ](images/mess-error-image60.png)

Dans cet exemple, le problème est probablement lié à la connexion réseau de l’utilisateur. il n’est donc pas utile de contacter un administrateur.

- **Ne vous recommandez pas de contacter le support technique.** L’option permettant de contacter le support technique pour résoudre un problème est toujours disponible et n’a pas besoin d’être promue par le biais de messages d’erreur. Au lieu de cela, concentrez-vous sur l’écriture de messages d’erreur utiles afin que les utilisateurs puissent résoudre les problèmes sans contacter le support technique.

**Incorrect :**

![Capture d’écran montrant un message « Impossible d’ouvrir cet élément ». ](images/mess-error-image61.png)

Dans cet exemple, le message d’erreur recommande de contacter le support technique de manière incorrecte.

- Utilisez des phrases complètes, des majuscules de style phrase et des signes de ponctuation de fin.

**Boutons de validation**

- Si le message d’erreur fournit des boutons de commande ou des liens de commande qui résolvent le problème, suivez leurs instructions respectives dans les [boîtes de dialogue](win-dialog-box.md).
- Si le programme doit s’arrêter à la suite de l’erreur, fournissez un bouton quitter le programme. Pour éviter toute confusion, n’utilisez pas close à cet effet.
- Dans le cas contraire, fournissez un bouton Fermer. N’utilisez pas OK pour les messages d’erreur, car cette formulation implique que les problèmes sont OK.
  - **Exception :** Utilisez OK si votre mécanisme de rapport d’erreurs contient des étiquettes fixes (comme avec l’API MessageBox).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence aux erreurs :

- Reportez-vous aux erreurs par l’instruction principale. Si l’instruction principale est longue ou détaillée, résumez-la.
- Si nécessaire, vous pouvez faire référence à une boîte de dialogue de message d’erreur sous la forme d’un message. Reportez-vous à un message d’erreur uniquement en programmation et dans une documentation technique.
- Dans la mesure du possible, mettez en forme le texte en gras. Sinon, placez le texte entre guillemets uniquement si nécessaire pour éviter toute confusion.

**Exemple :** Si vous recevez un CD **-** ROM, insérez un nouveau CD dans le lecteur, puis réessayez.

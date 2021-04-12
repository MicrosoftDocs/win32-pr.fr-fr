---
title: Bulles
description: Une info-bulle est une petite fenêtre contextuelle qui informe les utilisateurs d’un problème non critique ou d’une condition spéciale dans un contrôle.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321401"
---
# <a name="balloons"></a>Bulles

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une info-bulle est une petite fenêtre contextuelle qui informe les utilisateurs d’un problème non critique ou d’une condition spéciale dans un contrôle.

![Capture d’écran montrant une info-bulle indiquant que la touche VERR. MAJ est activée.](images/ctrl-balloons-image1.png)

Info-bulle classique.

Les bulles ont une icône, un titre et un corps de texte, qui sont tous facultatifs. Contrairement aux info-bulles et aux info-bulles, les bulles ont également une fin qui identifie leur source. En règle générale, la source est un contrôle, si tel est le cas, appelée « [contrôle propriétaire](glossary.md)».

Alors que les ballons informent les utilisateurs de problèmes non critiques, ils n’empêchent pas les problèmes même si le contrôle propriétaire le peut. Tout problème non géré doit être géré par l’interface utilisateur (IU) du propriétaire lorsque les utilisateurs essaient de valider l’action.

Les bulles sont généralement utilisées avec des zones de texte ou des contrôles qui utilisent des zones de texte pour modifier les valeurs, telles que les zones de liste modifiable, les affichages de liste et les arborescences. Les autres types de contrôles sont suffisamment bien limités et n’ont pas besoin de bulles de commentaires supplémentaires. En outre, en cas de problème avec d’autres types de contrôles, il implique souvent une incohérence entre plusieurs contrôles, une situation pour laquelle les bulles ne sont pas adaptées. Seuls les contrôles de saisie de texte sont à la fois sans contrainte et une source commune d' [Erreurs de point unique](glossary.md).

Une notification est un type spécifique de bulle affichée par une icône de [zone de notification](winenv-notification.md) .

**Remarque :** Les instructions relatives aux [notifications](mess-notif.md), aux [info-bulles et aux info-bulles](ctrl-tooltips-and-infotips.md)et aux [messages d’erreur](mess-error.md) sont présentées dans des articles distincts.

**Est-ce le contrôle approprié ?**

Pour vous décider, posez-vous les questions suivantes :

-   **Les informations décrivent-elles un problème ou une condition spéciale ?** Si ce n’est pas le cas, utilisez un autre contrôle. N’utilisez pas de bulles pour afficher des informations supplémentaires sur un contrôle ; envisagez plutôt d’utiliser du [texte statique](glossary.md), des[info-bulles](glossary.md), une [Divulgation progressive](glossary.md)ou des invites.
-   **Le problème ou la condition spéciale peuvent-ils être détectés immédiatement** en entrée ou lorsque le contrôle propriétaire perd le focus d’entrée ? Dans le cas contraire, utilisez un message d’erreur affiché dans une [boîte de dialogue de tâche](glossary.md) ou une boîte de [message](glossary.md).
-   **Pour résoudre les problèmes, le problème est-il critique ?** Dans ce cas, utilisez un message d’erreur affiché dans une boîte de dialogue de tâche ou une boîte de message. Ces messages d’erreur nécessitent une interaction (ce qui convient aux erreurs critiques), contrairement aux bulles.
-   **Pour les conditions spéciales, est-ce que la condition valide est probablement inattendue ?** Si c’est le cas, les bulles sont appropriées. Pour les conditions non valides, il est préférable de les éviter en premier lieu. Pour les conditions probables, il n’est pas nécessaire de faire quoi que ce soit.
-   **Le problème ou la condition spéciale peuvent-ils être exprimés de façon concise ?** Si ce n’est pas le cas, utilisez un autre contrôle. Les bulles ne peuvent pas avoir d’explications détaillées ou fournir des informations supplémentaires.
-   **Les informations décrivent-elles le contrôle actuellement pointé ?** Dans ce cas, utilisez une info-bulle à la place, à moins que les utilisateurs aient besoin d’interagir avec le message.
-   **Les informations relatives à l’activité actuelle de l’utilisateur sont-elles les mêmes ?** Si ce n’est pas le cas, envisagez plutôt d’utiliser une [notification](mess-notif.md) ou une [boîte de dialogue](win-dialog-box.md) . Les utilisateurs peuvent ignorer les bulles en dehors de l’activité en cours et, par défaut, les bulles expirent après 10 secondes.
-   **Les informations proviennent-elles d’une source unique et spécifique ?** Si un problème ou une condition a plusieurs sources ou aucune source spécifique, utilisez plutôt un [message sur place](glossary.md) ou une boîte de dialogue.

**Incorrect :** ![ capture d’écran d’une bulle : ouverture de session infructueuse](images/ctrl-balloons-image2.png)

Dans cet exemple, le problème peut être lié au nom d’utilisateur ou au mot de passe, mais le fait de signaler le problème avec une bulle suggère visuellement que seul le mot de passe est le problème. Par conséquent, les commentaires de la saisie d’un nom d’utilisateur incorrect sont trompeurs.

Les bulles sont une alternative à info-bulles, aux boîtes de dialogue et aux messages sur place. Contrairement aux info-bulles et info-bulles :

-   Les bulles peuvent être affichées indépendamment de l’emplacement du pointeur actuel, de sorte qu’elles ont une fin qui indique leur source.
-   Les bulles comportent un titre, un corps de texte et une icône.
-   Les bulles peuvent être interactives, alors qu’il est impossible de cliquer sur une info-bulle.

Contrairement aux boîtes de dialogue modales :

-   Les bulles ne volent pas le focus d’entrée ou nécessitent une interaction.
-   Les bulles identifient une source unique et spécifique. Les boîtes de dialogue modales peuvent avoir plusieurs sources, ou aucune source spécifique.

Contrairement aux messages sur place :

-   Les bulles sont plus visibles.
-   Les bulles ne nécessitent pas d’espace d’écran disponible ou la disposition dynamique requise pour afficher des messages sur place.
-   Les bulles se suppriment automatiquement après un délai d’expiration.

**Modèles d’usage**

Les bulles ont les modèles d’utilisation suivants :



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problème d’entrée** Un problème d’entrée utilisateur non critique provenant d’un seul contrôle propriétaire, généralement une zone de texte. <br/>                                               | l’utilisation de bulles pour les messages d’erreur ne vole pas le focus d’entrée, mais reste très visible si le contrôle propriétaire a le focus d’entrée. pour corriger le problème, l’utilisateur devra peut-être modifier ou entrer à nouveau l’entrée ; Toutefois, si le contrôle propriétaire ignore une entrée incorrecte, il se peut que l’utilisateur n’ait pas à apporter de modifications. étant donné que le problème n’est pas critique, aucune [icône d’erreur](vis-std-icons.md) n’est nécessaire. <br/> ![Capture d’écran montrant une bulle indiquant un caractère incorrect.](images/ctrl-balloons-image3.png)<br/> Bulle utilisée pour signaler un problème d’entrée d’utilisateur non critique.<br/>                                                                                                  |
| **Condition spéciale** Le contrôle propriétaire est dans un État qui affecte l’entrée. Cet État est probablement involontaire et l’utilisateur peut ne pas se rendre compte qu’une entrée est affectée. <br/> | Utilisez des bulles pour empêcher la frustration en avertissant les utilisateurs de conditions spéciales dès qu’elles se produisent (par exemple, en dépassant la taille maximale d’entrée ou en définissant le verrouillage des majuscules sur par erreur). Il est important de fournir ces commentaires sans voler le focus d’entrée ou forcer l’interaction, car ces conditions peuvent être intentionnelles. ces bulles sont particulièrement importantes pour les zones de mot de passe et pin, où les utilisateurs travaillent avec un minimum de commentaires. ces bulles ont une [icône d’avertissement](vis-std-icons.md). <br/> ![Capture d’écran montrant les bulles indiquant que Verr. MAJ est activé et qu’un caractère incorrect est entré.](images/ctrl-balloons-image4.png)<br/> Bulle utilisée pour signaler une condition spéciale.<br/> |



 

**Instructions**

**Quand afficher**

-   **Affichez l’info-bulle dès que le problème ou la condition spéciale est détecté, même s’il est répété, sans délai notable.**
    -   Pour les problèmes impliquant des caractères individuels ou la taille d’entrée maximale, affichez la bulle immédiatement à l’entrée.
    -   Pour les problèmes impliquant la valeur d’entrée (y compris la nécessité d’une valeur non vide), affichez l’info-bulle lorsque le contrôle propriétaire perd le focus d’entrée. Dans le cas contraire, l’affichage des bulles pendant que les utilisateurs entrent des entrées potentiellement valides peut être gênant et ennuyeux.
-   **Affichez une seule bulle à la fois.** L’affichage de plusieurs ballons peut être écrasant. Si un seul événement entraîne plusieurs problèmes, présentez tous les problèmes en même temps ou signalez uniquement le problème le plus important.

**Incorrect :** ![ capture d’écran de deux bulles pointant vers une zone](images/ctrl-balloons-image5.png)

Dans cet exemple, deux problèmes sont présentés de manière incorrecte en même temps.

**Durée d’affichage**

-   **Supprimer une bulle lorsque :**
    -   Le problème est résolu ou la condition spéciale est supprimée.
    -   L’utilisateur entre des données valides (pour les problèmes d’entrée).
    -   La bulle expire. Par défaut, les bulles se suppriment après 10 secondes, bien que les utilisateurs puissent les modifier en modifiant le \_ paramètre système SPI MESSAGEDURATION.
-   **Supprimez le délai d’expiration si les utilisateurs ne peuvent pas continuer tant que le problème n’est pas résolu. Développeurs :** dans Win32, vous pouvez définir l’heure d’affichage à l’aide du \_ message atténuation SETDELAYTIME.

**Comment afficher**

-   **Affichez les bulles sous leur contrôle propriétaire.** Cela permet aux utilisateurs d’afficher le contexte, y compris le contrôle propriétaire et son étiquette. Microsoft Windows ajuste automatiquement les positions des bulles pour qu’elles soient entièrement affichées. Le comportement par défaut consiste à afficher une info-bulle au-dessus de son contrôle de propriétaire, comme terminé avec les notifications.

**Correct :** ![ capture d’écran d’une bulle affichée sous son contrôle](images/ctrl-balloons-image6.png)

**Incorrect :** ![ capture d’écran d’une bulle affichée au-dessus de son contrôle](images/ctrl-balloons-image7.png)

Dans l’exemple incorrect, la bulle est correctement affichée au-dessus de son contrôle propriétaire.

**Zones de texte mot de passe et code confidentiel**

-   **Utilisez une bulle pour indiquer que Verr. MAJ est activé**, en utilisant le texte de l’exemple suivant :

![capture d’écran d’une bulle indiquant que le verrouillage des majuscules est activé](images/ctrl-balloons-image8.png)

Dans cet exemple, une bulle indique que la touche VERR. MAJ est activée dans une zone de texte PIN.

-   **Utilisez une bulle pour indiquer quand les utilisateurs essaient de dépasser la taille d’entrée maximale.** L’atteinte de la taille d’entrée maximale est bien moins évidente dans les zones de texte mot de passe et code confidentiel que les zones de texte ordinaires.

![capture d’écran d’une bulle indiquant les limites du code PIN](images/ctrl-balloons-image9.png)

Dans cet exemple, une bulle indique que l’utilisateur tente de dépasser la taille d’entrée maximale.

-   **Utilisez une bulle pour indiquer à quel moment les utilisateurs saisissent des caractères incorrects.** Toutefois, il est préférable de ne pas avoir de telles restrictions, car elles réduisent la sécurité du mot de passe ou du code PIN. Pour empêcher la divulgation d’informations, l’info-bulle doit mentionner uniquement des faits documentés sur les codes confidentiels ou les mots de passe valides.

![capture d’écran d’une bulle indiquant une entrée incorrecte](images/ctrl-balloons-image10.png)

Dans cet exemple, une bulle indique que le code PIN requiert des nombres.

**Autres zones de texte**

-   **Envisagez d’utiliser une bulle pour indiquer à quel moment les utilisateurs essaient de dépasser la taille d’entrée maximale pour les zones de texte courtes critiques destinées aux utilisateurs débutants.** Les noms d’utilisateur et les noms de compte sont des exemples. Les zones de texte signalent un bip lorsque les utilisateurs tentent de dépasser le nombre maximal d’entrées, mais les utilisateurs débutants peuvent ne pas comprendre la signification du signal sonore.

![capture d’écran d’une bulle indiquant des limites de caractères](images/ctrl-balloons-image11.png)

Dans cet exemple, une bulle indique que l’utilisateur a tenté de dépasser la taille d’entrée maximale.

**Interaction**

-   **Quand les utilisateurs cliquent sur une info-bulle, il suffit de faire disparaître l’info-bulle sans afficher d’autre interface utilisateur ni avoir d’autre effet secondaire.** Contrairement aux notifications, les bulles ne doivent pas avoir de boutons de fermeture.

**Icônes**

-   Choisissez l’icône en fonction du modèle d’utilisation :



    |  Modèle |  Icône                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problème d’entrée | Pas d'icône. L’absence d’une [icône d’erreur](vis-std-icons.md) ici est cohérente avec les directives de [tonalité Windows](text-style-tone.md) . |
    | Condition spéciale | [Icône d’avertissement](vis-std-icons.md)standard de 16x16 pixels.                                                                                  |

**Accessibilité**

Lorsqu’elles sont utilisées correctement, les bulles améliorent l’accessibilité. Pour que les bulles soient accessibles :

-   Affiche uniquement les bulles relatives à l’activité actuelle de l’utilisateur.
-   Laissez le texte de la bulle concis. Cela rend le texte de la bulle plus facile à lire pour les utilisateurs ayant une acuité visuelle réduite et minimise l’interruption lorsqu’ils sont lus par les lecteurs d’écran.
-   Réaffichez la bulle chaque fois que le problème ou la condition se répète.

**Text**

**Texte du titre**

-   **Utilisez un texte de titre qui résume brièvement le problème d’entrée ou la condition spéciale dans un langage clair, clair, concis et spécifique.** Les utilisateurs doivent être en mesure de comprendre l’objectif de la bulle rapidement et avec un minimum d’effort.
-   **Utilisez des fragments de texte ou des phrases entières sans ponctuation finale.**
-   **Utilisez les majuscules comme pour les phrases.** Pour plus d’informations, consultez le [Glossaire](./glossary.md).
-   **N’utilisez pas plus de 48 caractères (en anglais) pour prendre en charge la localisation.** Le titre a une longueur maximale de 63 caractères et doit pouvoir être étendu d’au moins 30% pour prendre en charge la localisation.

**Texte du corps**

-   **Utilisez la première phrase du corps du texte pour indiquer le problème ou la condition d’une façon qui est clairement pertinente pour l’utilisateur.** Ne répétez pas les informations dans le titre. Omettez This s’il n’y a rien à ajouter.
-   **Utilisez la deuxième phrase pour indiquer ce que l’utilisateur peut faire pour résoudre le problème ou rétablir l’État.** Conformément aux règles de [style et de tonalité](./text-style-tone.md) , il n’est pas nécessaire d’utiliser le mot dans cette déclaration. Placez deux sauts de ligne entre la première et la deuxième phrase.

![capture d’écran d’une bulle avec le titre et le corps de texte](images/ctrl-balloons-image12.png)

Cet exemple montre la disposition du texte de la bulle standard.

-   **Expliquez comment résoudre le problème ou rétablir l’État même si cette explication est évidente,** mais omettez la redondance entre l’instruction du problème et sa résolution. **Exceptions :**
    -   Omettez la résolution si elle ne peut pas être exprimée de façon concise ou sans redondance significative.
    -   Omettez la résolution s’il n’y a rien à faire pour l’utilisateur, par exemple quand des caractères incorrects sont ignorés.
-   **Utilisez des phrases complètes avec la ponctuation finale.**
-   **Utilisez les majuscules comme pour les phrases.**
-   **N’utilisez pas plus de 200 caractères (en anglais) pour prendre en charge la localisation.** Le corps du texte a une longueur maximale de 255 caractères et doit pouvoir être étendu d’au moins 30% pour prendre en charge la localisation.

**Documentation**

Lorsque vous faites référence aux bulles :

-   Utilisez le texte exact du titre, y compris sa mise en majuscules.
-   Reportez-vous au composant sous la forme d’une bulle, et non d’une notification ou d’une alerte.
-   Dans la mesure du possible, mettez en forme le texte du titre en gras. Sinon, placez le titre entre guillemets uniquement si nécessaire pour éviter toute confusion.


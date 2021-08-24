---
description: à compter de la version 1,0 du kit de développement logiciel (SDK) de Microsoft Windows XP Tablet pc Edition, le panneau de saisie Tablet pc au niveau du système fournit un mécanisme universel permettant d’effectuer des entrées de texte sur la plateforme Windows, bien qu’il n’offre pas d’accès par programme. L’objet PenInputPanel du kit de développement logiciel Tablet PC version 1,5 intègre les outils d’entrée de texte dans les applications.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: À propos du panneau de saisie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844409"
---
# <a name="about-the-input-panel"></a>À propos du panneau de saisie

\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel). Pour plus d’informations, consultez [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]

à compter de la version 1,0 du kit de développement logiciel (SDK) de Microsoft Windows XP Tablet pc Edition, le panneau de saisie Tablet pc au niveau du système fournit un mécanisme universel permettant d’effectuer des entrées de texte sur la plateforme Windows, bien qu’il n’offre pas d’accès par programme. L’objet [**PenInputPanel**](peninputpanel-class.md) du kit de développement logiciel Tablet PC version 1,5 intègre les outils d’entrée de texte dans les applications.

Le graphique suivant montre le panneau de saisie du stylet affiché sur l’exemple d’exemple de [formulaire de déclaration automatique](auto-claims-form-sample.md) .

![panneau de saisie du stylet affiché sur l’exemple de formulaire de déclaration automatique](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

L’objet [**PenInputPanel**](peninputpanel-class.md) est pratique pour les développeurs d’applications. Il n’est pas nécessaire de remplacer des contrôles sur des formulaires existants. Vous pouvez simplement attacher des objets **PenInputPanel** à des contrôles existants qui reçoivent des entrées de texte, et ils peuvent commencer à recevoir des données de l’objet **PenInputPanel** .

L’objet [**PenInputPanel**](peninputpanel-class.md) adopte les paramètres du panneau de saisie pour les propriétés suivantes :

-   Layout
-   Épaisseur de l’encre
-   Délai de reconnaissance
-   Taille de boîte, mode d’envoi et autres paramètres spécifiques à l’entrée boxed d’Extrême-Orient

L’objet [**PenInputPanel**](peninputpanel-class.md) ne fournit pas l’accès à l’encre sous-jacente. Pour récupérer l’encre, utilisez le contrôle [InkPicture](inkpicture-control-reference.md) .

L’objet [**PenInputPanel**](peninputpanel-class.md) fournit une interface utilisateur (IU) sur place qui est facilement détectable par les utilisateurs finaux de vos applications. Elle est automatiquement activée lorsque l’utilisateur appuie sur une fenêtre avec un objet **PenInputPanel** à l’aide du stylet. Le panneau de saisie du stylet s’affiche automatiquement lorsque le système détecte un événement CursorButtonUp pour la fenêtre à laquelle l’objet **PenInputPanel** est attaché. L’activation automatique peut être désactivée en affectant la **valeur false** à la propriété [**affichage**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) automatique.

Le panneau de saisie du stylet n’apparaît pas automatiquement sur les événements de souris. Les événements de stylet sont convertis en événements de souris lors de l’utilisation des services Terminal Server. L’objet [**PenInputPanel**](peninputpanel-class.md) ne fonctionne pas sur une connexion aux services Terminal Server.

## <a name="pen-input-panel-input-modes"></a>Modes d’entrée du panneau de saisie du stylet

L’objet [**PenInputPanel**](peninputpanel-class.md) permet d’utiliser les fonctionnalités du clavier ou l’écriture manuscrite, avec des pavés supplémentaires pour faciliter l’entrée. L’interface utilisateur du panneau de saisie du stylet comprend les éléments suivants :

-   Bloc d’écriture
-   Writing pad pour les langues d’Extrême-Orient
-   Pavés de QuickKeys
-   Clavier sur place

La disponibilité du bloc d’écriture par rapport au bloc d’écriture pour les langues d’Asie orientale dépend des paramètres régionaux par défaut de l’utilisateur dans le système d’exploitation.

### <a name="writing-pad"></a>Bloc d’écriture

Le pavé d’écriture ressemble à l’interface utilisateur du panneau de saisie.

Le pavé d’écriture collecte l’écriture manuscrite à partir de l’utilisateur final. L’interface utilisateur de base comprend une ligne d’écriture unique sur laquelle l’utilisateur peut écrire du texte avec un stylet numérique. Lorsque l’utilisateur termine l’écriture et appuie sur le bouton envoyer ou attend qu’un délai d’attente se produise, l’écriture manuscrite est envoyée au module de reconnaissance.

L’encre est reconnue après qu’un laps de temps spécifié s’est écoulé depuis l’heure à laquelle le dernier trait d’encre a été collecté. Lorsque le délai d’attente se produit, l’entrée manuscrite est supprimée de l’aire de collection et la reconnaissance se produit. Le texte reconnu est ensuite inséré dans le contrôle auquel l’objet [**PenInputPanel**](peninputpanel-class.md) est attaché.

### <a name="east-asian-multibox-pad"></a>Pad Multibox asiatique

La version d’Extrême-Orient du panneau de saisie du stylet affiche une interface multibox pour la saisie des caractères asiatiques. Il fournit des alternatives et est semblable à l’interface utilisateur du panneau de saisie. Les utilisateurs peuvent corriger les caractères mal reconnus en appuyant sur une zone d’écriture et en sélectionnant le caractère approprié dans une liste de remplacements dans la barre en haut du panneau de saisie du stylet. Des boutons de filtre sont disponibles pour affiner la liste des variantes de reconnaissance aux types de caractères spécifiés, tels que les symboles.

Les versions coréenne et japonaise du bloc d’écriture ont une clé de conversion en plus des mini-clés rapides qui sont communes à toutes les apparences de langage.

Pour obtenir des caractères latins dans le pavé d’écriture pour les langues d’Extrême-Orient, définissez la propriété [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) pour augmenter la précision de la reconnaissance des caractères latins. Définissez le membre **digit** de l’objet [**Factoid**](factoid-constants.md) pour les caractères numériques ou le membre **OneChar** de l’objet **Factoid** pour les caractères alphabétiques et numériques.

### <a name="quickkeys-keypads"></a>Pavés de QuickKeys

Le panneau de saisie du stylet fournit deux petits pavés pour entrer les symboles et les nombres.

### <a name="in-place-keyboard"></a>Clavier sur place

Le panneau de saisie du stylet fournit un mode clavier pour les situations où la reconnaissance de l’écriture manuscrite n’est pas suffisante. Par exemple, lors de l’entrée d’un mot de passe ou d’un numéro de référence, les utilisateurs sont susceptibles d’avoir plus de succès en utilisant le clavier du panneau de saisie du stylet que le pavé d’écriture. Cela est dû au fait que les mots de passe et les numéros de référence sont peu susceptibles de se trouver dans le dictionnaire de reconnaissance du bloc d’écriture.

## <a name="recognizer-support"></a>Prise en charge du module de reconnaissance

l’objet [**PenInputPanel**](peninputpanel-class.md) prend en charge les détecteurs d’expédition pour Windows XP édition Tablet pc version 1,0 et le kit de développement logiciel (SDK) tablet pc version 1,5.

## <a name="automatic-positioning"></a>Positionnement automatique

Par défaut, le panneau de saisie du stylet est automatiquement positionné par rapport au contrôle auquel il est attaché. Il ne chevauche pas le contrôle à moins qu’il n’y ait pas suffisamment d’écran pour le panneau de saisie du stylet et le contrôle, ou à moins que le développeur définisse explicitement la position du panneau de saisie du stylet.

Fonctions de positionnement automatique uniquement lorsque le développeur n’a pas défini explicitement la position à l’aide de la méthode [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) . Pour remplacer le positionnement automatique, modifiez les valeurs des propriétés [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) et [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) dans un gestionnaire d’événements [**PanelMoving**](peninputpanel-panelmoving.md) .

La position du panneau de saisie du stylet est restreinte par les bords de l’écran. Aucun bord du panneau de saisie du stylet ne peut être plus proche de 0,25 centimètres de n’importe quelle bordure de l’écran.

Par défaut, le haut du panneau de saisie du stylet apparaît en bas du contrôle auquel il est attaché et est séparé du contrôle par la valeur de la propriété [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) . S’il n’y a pas suffisamment d’espace sous le contrôle, le bas du panneau de saisie du stylet apparaît en haut du contrôle auquel il est attaché et est séparé du contrôle par la valeur de la propriété **VerticalOffset** . S’il n’y a toujours pas assez de place, comme dans le cas d’un contrôle d’édition plein écran, le panneau de saisie du stylet chevauche le contrôle.

Le panneau de saisie du stylet du bord gauche apparaît sur le bord gauche du contrôle auquel il est attaché et est séparé du contrôle par la valeur de la propriété [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) , sauf si elle est délimitée par l’écran. Si la position souhaitée place le panneau de saisie du stylet au-delà des limites d’écran disponibles, le panneau de saisie du stylet prend la position horizontale la plus proche possible.

### <a name="forced-overlap"></a>Chevauchement forcé

Il est parfois nécessaire que le panneau de saisie du stylet chevauche le contrôle attaché, comme dans le cas d’un contrôle d’édition en plein écran. Dans ce cas, le positionnement automatique du panneau de saisie du stylet est déterminé à l’aide des règles suivantes :

-   Lorsque le point d’insertion se trouve dans la moitié supérieure du contrôle attaché, la position verticale du panneau de saisie du stylet se trouve au bas de l’écran, éventuellement placé sur la partie inférieure du contrôle.
-   Lorsque le point d’insertion se trouve dans la moitié inférieure du contrôle attaché, la position verticale du panneau de saisie du stylet se trouve en haut de l’écran, éventuellement placé sur la moitié supérieure du contrôle.

### <a name="windowless-controls"></a>Contrôles sans fenêtre

Dans le cas où un objet [**PenInputPanel**](peninputpanel-class.md) est attaché à un contrôle sans fenêtre, le panneau de saisie du stylet est positionné par rapport au parent du contrôle sans fenêtre. Définissez les propriétés [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) et [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) dans un gestionnaire d’événements [**PanelMoving**](peninputpanel-panelmoving.md) ou utilisez la méthode [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) pour positionner manuellement le panneau de saisie du stylet.

 

 

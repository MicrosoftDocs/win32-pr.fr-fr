---
title: Contrôler Spy v 2.0
description: Control Spy est un outil qui aide les développeurs à comprendre les contrôles communs sur la manière d’appliquer des styles à eux et comment ils répondent aux messages et aux notifications.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032024"
---
# <a name="control-spy-v20"></a>Contrôler Spy v 2.0

Control Spy est un outil qui aide les développeurs à comprendre les contrôles courants : comment leur appliquer des styles et comment ils répondent aux messages et aux notifications. À l’aide de Control Spy, vous pouvez voir immédiatement comment différents styles affectent le comportement et l’apparence de chaque contrôle, ainsi que la façon dont vous pouvez modifier l’état de chaque contrôle en envoyant des messages.

Deux versions de Control Spy sont disponibles, une pour [Comctl32.dll version 5. x](common-control-versions.md) et une pour Comctl32.dll version 6,0 et versions ultérieures. ControlSpyV6.exe a un manifeste d’application intégré, afin qu’il utilise les contrôles les plus récents. ControlSpyV5.exe n’a pas ce manifeste. par conséquent, il s’agit par défaut de l’ancienne version.

Cette rubrique contient les sections suivantes.

-   [Vue d’ensemble](#overview)
-   [Styles](#styles)
-   [Messages](#messages)
-   [Taille/couleur](#sizecolor)
-   [Où se procurer l’espionnage de contrôle](#where-to-get-control-spy)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Le contrôle Spy héberge un contrôle commun sélectionné au centre de sa fenêtre d’application. Vous pouvez modifier le contrôle affiché en sélectionnant différents contrôles dans la zone de liste située à gauche de la fenêtre. Les messages ou notifications reçus par le contrôle sont affichés dans la partie droite de la fenêtre à mesure qu’ils arrivent. Vous pouvez activer ou désactiver cette fonctionnalité à l’aide des cases à cocher **messages reçus** et **notifications reçues** .

L’illustration suivante montre l’application Control Spy.

![fenêtre Espion de contrôle](images/controlspy-main.png)

En bas de la fenêtre, plusieurs onglets présentent davantage de fonctionnalités.

## <a name="styles"></a>Styles

L’onglet **styles** vous permet de modifier le style de fenêtre actuel du contrôle. Sélectionnez ou désélectionnez les styles répertoriés, puis cliquez sur le bouton **appliquer** pour modifier le style du contrôle affiché. Vous pouvez également utiliser le bouton **recréer** pour créer un nouveau contrôle avec les styles sélectionnés. Le bouton **Réinitialiser** retournera le contrôle aux styles par défaut.

Les boutons **copier le style** et **copier** le style sous l’onglet copient les constantes de style sélectionnées dans le presse-papiers sous la forme d’une liste délimitée par des bits ou ( \| ). Vous pouvez coller cette liste directement dans votre appel à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour fournir un contrôle dans votre application avec le même style.

L’illustration suivante montre l’onglet **styles** pour un contrôle bouton.

![onglet de contrôle des styles Spy](images/controlspy-styles.png)

## <a name="messages"></a>Messages

L’onglet **messages** vous permet d’envoyer presque n’importe quel message à un contrôle. Après avoir sélectionné un message dans la zone de liste, vous pouvez entrer des données qui sont envoyées en tant que paramètres *wParam* et *lParam* de l’appel à [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Une fois que vous avez cliqué sur **Envoyer**, le message est envoyé au contrôle et tous les résultats s’affichent dans la zone de texte en bas de l’onglet.

L’illustration suivante montre l’onglet messages lorsqu’un message particulier est sélectionné.

![onglet de contrôle des messages Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a>Taille/couleur

L’onglet **taille/couleur** peut être utilisé pour modifier la taille du contrôle ainsi que la couleur de son arrière-plan.

## <a name="where-to-get-control-spy"></a>Où se procurer l’espionnage de contrôle

Vous pouvez télécharger [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) à partir de MSDN. Les deux versions sont contenues dans le téléchargement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Contrôles Windows](window-controls.md)
</dt> <dt>

[Activation des styles visuels](cookbook-overview.md)
</dt> </dl>

 

 
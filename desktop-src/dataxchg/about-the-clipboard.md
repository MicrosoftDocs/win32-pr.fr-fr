---
title: À propos du presse-papiers
description: Cette section décrit le presse-papiers.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- presse-papiers, à propos de
- presse-papiers, formats
- presse-papiers, commandes
- presse-papiers, fenêtres
- presse-papiers, numéros de séquence
- presse-papiers, visionneuses
- presse-papiers, fenêtres de visionneuse
- presse-papiers, formats d’affichage
- presse-papiers, formats d’affichage du propriétaire
- afficher les formats du presse-papiers
- propriétaire afficher les formats du presse-papiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe22a16886c62824775b5f2d8174e2a8e244b9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915692"
---
# <a name="about-the-clipboard"></a>À propos du presse-papiers

Le *presse-papiers* est un ensemble de fonctions et de messages qui permettent aux applications de transférer des données. Étant donné que toutes les applications ont accès au Presse-papiers, les données peuvent être facilement transférées entre les applications ou au sein d’une application.

Le presse-papiers est piloté par l’utilisateur. Une fenêtre doit transférer les données vers ou à partir du presse-papiers uniquement en réponse à une commande de l’utilisateur. Une fenêtre ne doit pas utiliser le presse-papiers pour transférer des données sans la connaissance de l’utilisateur.

Un objet mémoire sur le presse-papiers peut être dans n’importe quel format de données, appelé format presse-papiers. Chaque format est identifié par une valeur entière non signée. Pour les formats de presse-papiers standard (prédéfinis), cette valeur est une constante définie dans winuser. h ; pour les formats de presse-papiers inscrits, il s’agit de la valeur de retour de la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) .

À l’exception de l’inscription des formats de presse-papiers, les fenêtres individuelles effectuent la plupart des opérations de presse En règle générale, une procédure de fenêtre transfère les informations vers ou depuis le presse-papiers en réponse au message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .

Cette section aborde les points suivants :

-   [Commandes du presse-papiers](#clipboard-commands)
-   [Numéro de séquence du presse-papiers](#clipboard-sequence-number)
-   [Visionneuses de presse-papiers](#clipboard-viewers)
    -   [Presse-papiers Windows](#clipboard-viewer-windows)
    -   [Formats d’affichage](#display-formats)
    -   [Format d’affichage du propriétaire](#owner-display-format)
-   [Rubriques connexes](#related-topics)

## <a name="clipboard-commands"></a>Commandes du presse-papiers

Un utilisateur effectue généralement des opérations de presse-papiers en choisissant des commandes dans le menu **Edition** d’une application. Vous trouverez ci-dessous une brève description des commandes standard du presse-papiers.



|  Commande        |  Description                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Couper**    | Place une copie de la sélection actuelle dans le presse-papiers et supprime la sélection du document. Le contenu précédent du presse-papiers est détruit.                                                          |
| **Copier**   | Place une copie de la sélection actuelle dans le presse-papiers. Le document reste inchangé. Le contenu précédent du presse-papiers est détruit.                                                                      |
| **Coller**  | Remplace la sélection actuelle par le contenu du presse-papiers. Le contenu du presse-papiers n’est pas modifié.                                                                                                    |
| **Supprimer** | Supprime la sélection actuelle du document. Le contenu du presse-papiers n’est pas modifié. Cette commande n’implique pas le presse-papiers, mais elle doit apparaître avec les commandes du presse-papiers dans le menu **Edition** . |



 

## <a name="clipboard-sequence-number"></a>Numéro de séquence du presse-papiers

Le presse-papiers de chaque station Windows est associé à un numéro de séquence du presse-papiers. Ce nombre est incrémenté chaque fois que le contenu du presse-papiers change. Pour obtenir le numéro de séquence du presse-papiers, appelez la fonction [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .

## <a name="clipboard-viewers"></a>Visionneuses de presse-papiers

Une visionneuse du presse-papiers est une fenêtre qui affiche le contenu actuel du presse-papiers. La fenêtre de la visionneuse du presse-papiers est un outil pratique pour l’utilisateur et n’affecte pas les fonctions de transaction de données du presse-papiers.

En règle générale, une fenêtre de la visionneuse du presse-papiers peut afficher au moins les trois formats les plus courants : **CF \_ Text**, **CF \_ bitmap** et **CF \_ MetaFilePict**. Si une fenêtre ne rend pas les données disponibles dans l’un de ces trois formats, elle doit fournir des données dans un format d’affichage ou utiliser le format d’affichage du propriétaire.

Une *chaîne de visionneuse du presse-papiers* est le lien entre deux entités ou plus afin qu’elles soient dépendantes les unes des autres pour l’opération. Cette interdépendance (chaîne) permet à toutes les applications de visionneuse du presse-papiers en cours d’exécution de recevoir les messages envoyés au Presse-papiers actuel.

Les rubriques suivantes sont présentées dans cette section.

-   [Presse-papiers Windows](#clipboard-viewer-windows)
-   [Formats d’affichage](#display-formats)
-   [Format d’affichage du propriétaire](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Presse-papiers Windows

Une fenêtre s’ajoute à la chaîne de la visionneuse du presse-papiers en appelant la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . La valeur de retour est le handle de la fenêtre suivante dans la chaîne. Pour récupérer le handle de la première fenêtre de la chaîne, appelez la fonction [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) .

Chaque fenêtre de la visionneuse du presse-papiers doit suivre la fenêtre suivante dans la chaîne du presse-papiers. Lorsque le contenu du presse-papiers change, le système envoie un message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) à la première fenêtre de la chaîne. Après la mise à jour de son affichage, chaque fenêtre de la visionneuse du presse-papiers doit passer ce message à la fenêtre suivante dans la chaîne.

Avant de fermer, une fenêtre de la visionneuse du presse-papiers doit se supprimer de la chaîne du presse-papiers en appelant la fonction [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . Le système envoie ensuite un message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) à la première fenêtre de la chaîne.

Pour plus d’informations sur le traitement des messages [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) et [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) , consultez [création d’une fenêtre de la visionneuse du presse-papiers](using-the-clipboard.md).

### <a name="display-formats"></a>Formats d'affichage

Un format d’affichage est un format de presse-papiers utilisé pour afficher des informations dans une fenêtre de la visionneuse du presse-papiers. Un propriétaire de presse-papiers qui utilise un format de presse-papiers privé ou inscrit, et aucun des formats standard les plus courants, doit fournir des données dans un format d’affichage pour l’affichage dans une fenêtre de la visionneuse du presse-papiers. Les formats d’affichage sont uniquement destinés à l’affichage et ne doivent pas être collés dans un document.

Les quatre formats d’affichage sont **: \_ CF DSPBITMAP**, **CF \_ DSPMETAFILEPICT**, **CF \_ DSPTEXT** et **CF \_ DSPENHMETAFILE**. Ces formats d’affichage sont rendus de la même façon que les formats standard, qui sont : **CF \_ bitmap**, **CF \_ Text**, **CF \_ MetaFilePict** et **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Format d’affichage du propriétaire

Pour un propriétaire de presse-papiers qui n’utilise aucun des formats de presse-papiers standard courants, une alternative à la fourniture d’un format d’affichage consiste à utiliser le format de presse-papiers (**CF \_ OWNERDISPLAY**) owner-Display.

En utilisant le format d’affichage propriétaire, un propriétaire de presse-papiers peut éviter la surcharge liée au rendu des données dans un format supplémentaire en contrôlant directement la peinture de la fenêtre de la visionneuse du presse-papiers. La fenêtre de la visionneuse du presse-papiers envoie des messages au propriétaire du presse-papiers chaque fois qu’une partie de la fenêtre doit être redessinée ou que la fenêtre est défilée ou redimensionnée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats de presse-papiers standard](standard-clipboard-formats.md)
</dt> </dl>

 

 
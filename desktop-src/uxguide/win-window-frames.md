---
title: Frames de fenêtre
description: La plupart des programmes doivent utiliser des frames de fenêtre standard. Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre. Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dee701f7aad12e348a89034010de1f44134e9d3e
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812253"
---
# <a name="window-frames"></a>Frames de fenêtre

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La plupart des programmes doivent utiliser des frames de fenêtre standard. Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre. Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente.

Avec un frame de fenêtre, les utilisateurs peuvent manipuler une fenêtre et afficher le titre et l’icône pour identifier son contenu.

![capture d’écran d’un cadre de fenêtre autour de la fenêtre du bloc-notes ](images/win-window-frames-image1.png)

Frame de fenêtre classique.

**Remarque :** Les instructions relatives à la gestion et à la [personnalisation](exper-branding.md) des [fenêtres](win-window-mgt.md) sont présentées dans des articles distincts.

## <a name="design-concepts"></a>Principes de conception

### <a name="glass-window-frames"></a>Frames de fenêtres en verre

les cadres de fenêtres en verre sont un tout nouvel aspect de Microsoft Windows esthétiques, qui visent à être à la fois attrayante et légère. Ces frames translucides offrent aux fenêtres une apparence ouverte, moins intrusive, permettant aux utilisateurs de se concentrer sur le contenu et les fonctionnalités plutôt que sur l’interface qui les entoure.

![capture d’écran d’un cadre de transparence autour de la calculatrice ](images/win-window-frames-image2.png)

Frames de fenêtres en verre.

Vous pouvez utiliser la transparence de manière stratégique dans les petites zones d’une fenêtre qui touchent le cadre de la fenêtre. Ces régions semblent faire partie du cadre de la fenêtre, même si techniquement elles font partie de la zone cliente de la fenêtre.

![capture d’écran de la fenêtre avec bord translucide ](images/win-window-frames-image3.png)

Dans cet exemple, la transparence est utilisée dans la zone cliente pour qu’elle ressemble à une partie du cadre.

### <a name="hidden-frames"></a>Frames masqués

Parfois, le meilleur frame de fenêtre n’est pas du tout. C’est souvent le cas pour la [fenêtre principale](glossary.md) d’applications [plein écran](glossary.md) immersives qui ne sont pas utilisées conjointement avec d’autres programmes, tels que des lecteurs multimédias, des jeux et des applications kiosque.

Les visionneuses de contenu bénéficient souvent d’une option permettant d’afficher le contenu en mode plein écran. exemples : Windows Internet Explorer, Galerie de photos Windows Live, Windows Movie Maker HD, Microsoft PowerPoint et Microsoft Word.

![capture d’écran du lecteur multimédia en mode plein écran ](images/win-window-frames-image4.png)

dans cet exemple, Lecteur Windows Media pouvez afficher son contenu en mode plein écran.

### <a name="custom-frames"></a>Frames personnalisés

la plupart des applications Windows doivent utiliser les frames de fenêtre standard. Toutefois, pour les applications isolées, plein écran et autonomes comme les jeux et les applications kiosque, il peut être approprié d’utiliser des frames personnalisés pour toutes les fenêtres qui ne sont pas affichées en mode plein écran. La motivation d’utiliser des frames personnalisés doit être d’offrir une expérience globale unique, pas seulement pour la [personnalisation](exper-branding.md).

![illustration du puzzle image brouillé et du cadre ](images/win-window-frames-image5.png)

Les trames personnalisées sont appropriées pour les applications immersives, plein écran et autonomes, telles que les jeux.

## <a name="guidelines"></a>Consignes

### <a name="window-frames"></a>Frames de fenêtre

-   Utilisez des frames de fenêtre standard.
    -   **Exception :** Pour fournir aux applications autonomes plein écran, une sensation unique :
        -   Envisagez de masquer le cadre de fenêtre de la [fenêtre principale](glossary.md).
        -   Envisagez d’utiliser des frames personnalisés pour la [fenêtre secondaire](glossary.md).
        -   Si un frame personnalisé est approprié, choisissez une conception légère et n’attire pas trop l’attention sur elle-même.

            **Incorrect :**

            ![capture d’écran du cadre gênant ](images/win-window-frames-image6.png)

            Dans cet exemple, le frame personnalisé s’attire trop bien sur lui-même.
-   N’ajoutez pas de contrôles à un frame de fenêtre. Placez plutôt les contrôles dans la fenêtre.

    **Incorrect :**

    ![capture d’écran du contrôle dans le frame de fenêtre ](images/win-window-frames-image7.png)

    **Correct :**

    ![capture d’écran du contrôle dans la zone cliente ](images/win-window-frames-image8.png)

    Dans l’exemple correct, le contrôle se trouve dans la zone cliente et non dans le cadre de la fenêtre.

### <a name="full-screen-mode"></a>Mode plein écran

-   Pour les programmes qui ont un mode plein écran facultatif, pour activer le mode plein écran :
    -   Utilisez une commande modale plein écran dans la barre de menus ou la barre d’outils. Lorsque l’utilisateur clique sur la commande, affichez la commande dans son état sélectionné.

        ![capture d’écran de la fenêtre avec l’élément de menu plein écran ](images/win-window-frames-image9.png)

        Cet exemple montre la commande plein écran avec sa touche de raccourci standard.

-   Utilisez F11 pour la touche de raccourci plein écran.
-   S’il y a une barre d’outils et que le mode plein écran est couramment utilisé, vous avez également un bouton de barre d’outils graphique avec une info-bulle en plein écran.

    ![capture d’écran des boutons plein écran et rétablir ](images/win-window-frames-image10.png)

    Exemples de boutons de la barre d’outils plein écran.

-   Pour revenir en arrière en mode plein écran :
    -   Utilisez une commande modale plein écran dans la barre de menus ou la barre d’outils. Lorsque l’utilisateur clique sur la commande, affichez la commande dans son état d’effacement.
    -   Utilisez F11 pour la touche de raccourci plein écran. Si ce n’est déjà fait, la touche Échap peut également être utilisée à cet effet.

### <a name="glass"></a>Glass

les frames de fenêtre Standard utilisent le verre automatiquement dans Windows, mais vous pouvez également utiliser la transparence dans les régions qui touchent le cadre de la fenêtre.

-   **Envisagez d’utiliser la transparence de manière stratégique dans les petites régions qui touchent le cadre de la fenêtre sans texte.** Cela peut donner à un programme un aspect plus simple, plus clair et plus cohérent en faisant en sorte que la région apparaisse comme faisant partie du cadre.
-   ![capture d’écran de la fenêtre avec bord translucide ](images/win-window-frames-image3.png)
-   Dans cet exemple, la transparence porte l’attention de l’utilisateur sur le contenu au lieu des contrôles.
-   **N’utilisez pas de verre dans les situations où un arrière-plan de fenêtre ordinaire serait plus attrayant ou plus facile à utiliser.**

**Correct :**

![capture d’écran de la fenêtre avec quatre graphiques et étiquette ](images/win-window-frames-image11.png)

Dans cet exemple, la transparence est utilisée pour attribuer une apparence légère à la fenêtre ALT + TAB. La vitre fonctionne pour cette fenêtre, car elle se compose de graphiques et d’une seule étiquette de texte fort.

**Incorrect :**

![capture d’écran de la fenêtre avec douze graphiques ](images/win-window-frames-image12.png)

Dans cet exemple incorrect, l’utilisation de la vitre est gênante. Un arrière-plan de fenêtre ordinaire est un meilleur choix.

 

 

---
title: À propos des barres de défilement
description: Une fenêtre peut afficher un objet de données, tel qu’un document ou un bitmap, qui est plus grand que la zone cliente de la fenêtre.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d410e98ea1fe722d6dc1c4869010df30f99bddb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031884"
---
# <a name="about-scroll-bars"></a>À propos des barres de défilement

Une fenêtre peut afficher un objet de données, tel qu’un document ou un bitmap, qui est plus grand que la zone cliente de la fenêtre. Lorsqu’il est fourni avec une barre de défilement, l’utilisateur peut faire défiler un objet de données dans la zone cliente pour afficher les parties de l’objet qui s’étendent au-delà des bordures de la fenêtre.

Les barres de défilement doivent être incluses dans toute fenêtre pour laquelle le contenu de la zone cliente s’étend au-delà des limites de la fenêtre. L’orientation d’une barre de défilement détermine la direction dans laquelle le défilement se produit lorsque l’utilisateur exécute la barre de défilement. Une barre de défilement horizontale permet à l’utilisateur de faire défiler le contenu d’une fenêtre vers la gauche ou vers la droite. Une barre de défilement verticale permet à l’utilisateur de faire défiler le contenu vers le haut ou vers le haut.

Les rubriques suivantes sont présentées dans cette section.

-   [Parties d’une barre de défilement](#parts-of-a-scroll-bar)
-   [Barres de défilement standard et contrôles de barre de défilement](#standard-scroll-bars-and-scroll-bar-controls)
-   [Position de la case de défilement et plage de défilement](#scroll-box-position-and-scrolling-range)
-   [Visibilité de la barre de défilement](#scroll-bar-visibility)
-   [Requêtes de barre de défilement](#scroll-bar-requests)
-   [Interface clavier pour une barre de défilement](#keyboard-interface-for-a-scroll-bar)
-   [Défilement de la zone client](#scrolling-the-client-area)
-   [Couleurs et métriques de la barre de défilement](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Parties d’une barre de défilement

Une barre de défilement se compose d’un arbre ombré avec un bouton fléché à chaque extrémité et d’une *case de défilement* (parfois appelée curseur de défilement) entre les boutons fléchés. Une barre de défilement représente la longueur ou la largeur globale d’un objet de données dans la zone cliente d’une fenêtre. la case de défilement représente la partie de l’objet qui est visible dans la zone cliente. La position de la case de défilement change chaque fois que l’utilisateur fait défiler un objet de données pour en afficher une partie différente. Le système ajuste également la taille de la case de défilement d’une barre de défilement de sorte qu’elle indique la partie de l’objet de données entière qui est actuellement visible dans la fenêtre. Si la plus grande partie de l’objet est visible, la case de défilement occupe la plus grande partie de l’arbre de la barre de défilement. De même, si seule une petite partie de l’objet est visible, la case de défilement occupe une petite partie de l’arbre de la barre de défilement.

L’utilisateur fait défiler le contenu d’une fenêtre en cliquant sur l’un des boutons de direction, en cliquant sur la zone de l’arbre de la barre de défilement ombrée ou en faisant glisser la case de défilement. Quand l’utilisateur clique sur un bouton fléché, l’application fait défiler le contenu d’une unité (généralement une ligne ou une colonne). Lorsque l’utilisateur clique sur les zones ombrées, l’application fait défiler le contenu d’une fenêtre à l’autre. La quantité de défilement qui se produit lorsque l’utilisateur fait glisser la case de défilement dépend de la distance pendant laquelle l’utilisateur fait glisser la case de défilement et sur la plage de défilement de la barre de défilement. Pour plus d’informations sur la plage de défilement, consultez [position de la case de défilement et plage de défilement](#scroll-box-position-and-scrolling-range).

La capture d’écran suivante montre un contrôle RichEdit avec des barres de défilement verticales et horizontales, telles qu’elles peuvent apparaître dans Windows Vista. La barre de défilement verticale est actuellement « chaude », car le pointeur de la souris se trouve au-dessus de celle-ci au moment où la capture d’écran a été effectuée.

![capture d’écran d’un contrôle RichEdit avec des barres de défilement](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barres de défilement standard et contrôles de barre de défilement

Une barre de défilement est incluse dans une fenêtre comme une barre de défilement standard ou comme un contrôle de barre de défilement. Une barre de défilement standard est située dans la zone non cliente d’une fenêtre. Il est créé avec la fenêtre et s’affiche lorsque la fenêtre est affichée. Le seul but d’une barre de défilement standard est de permettre à l’utilisateur de générer des requêtes de défilement pour afficher l’ensemble du contenu de la zone cliente. Vous pouvez inclure une barre de défilement standard dans une fenêtre en spécifiant [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles), ou les deux styles lorsque vous créez la fenêtre. Le style **WS \_ HSCROLL** crée une barre de défilement horizontale positionnée en bas de la zone cliente. Le style **WS \_ VSCROLL** crée une barre de défilement verticale positionnée à droite de la zone cliente. Les \_ valeurs de métrique du système SM CXHSCROLL et SM \_ CYHSCROLL définissent la largeur et la hauteur d’une barre de défilement horizontale standard. Les \_ valeurs SM CXVSCROLL et SM \_ CYVSCROLL définissent la largeur et la hauteur d’une barre de défilement verticale standard. Une barre de défilement standard fait partie de la fenêtre qui lui est associée et n’a donc pas de handle de fenêtre propre.

Un contrôle de barre de défilement est une fenêtre de contrôle qui appartient à la classe de fenêtre SCROLLBAR. Un contrôle de barre de défilement apparaît et fonctionne comme une barre de défilement standard, mais il s’agit d’une fenêtre distincte. Dans une fenêtre distincte, un contrôle de barre de défilement prend le focus d’entrée directe. Contrairement à une barre de défilement standard, un contrôle de barre de défilement a également une interface clavier intégrée.

Vous pouvez utiliser autant de contrôles de barre de défilement que nécessaire dans une seule fenêtre. Lorsque vous créez un contrôle de barre de défilement, vous devez spécifier la taille et la position de la barre de défilement. Toutefois, si une fenêtre de contrôle de barre de défilement peut être redimensionnée, les ajustements apportés à la taille de la barre de défilement doivent être effectués à chaque fois que la taille de la fenêtre change.

L’avantage de l’utilisation d’une barre de défilement standard est que le système crée la barre de défilement et définit automatiquement sa taille et sa position. Toutefois, les barres de défilement standard sont parfois trop restrictives. Par exemple, supposons que vous souhaitiez diviser une zone client en quadrants et utiliser un ensemble distinct de barres de défilement pour contrôler le contenu de chaque quadrant. Vous ne pouvez pas utiliser les barres de défilement standard, car vous ne pouvez créer qu’un seul jeu de barres de défilement pour une fenêtre particulière. Utilisez à la place des contrôles de barre de défilement, car vous pouvez en ajouter autant que vous le souhaitez dans une fenêtre.

Les applications peuvent fournir des contrôles de barre de défilement à d’autres fins que de faire défiler le contenu d’une fenêtre. Par exemple, une application d’économiseur d’écran peut fournir une barre de défilement pour définir la vitesse à laquelle les graphiques sont déplacés sur l’écran.

Un contrôle de barre de défilement peut avoir un certain nombre de styles servant à contrôler l’orientation et la position de la barre de défilement. Vous spécifiez les styles souhaités quand vous appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle de barre de défilement. Certains styles créent un contrôle de barre de défilement qui utilise une largeur ou une hauteur par défaut. Toutefois, vous devez toujours spécifier les coordonnées x et y et les autres dimensions de la barre de défilement.

Pour obtenir un tableau des styles de contrôle de barre de défilement, consultez [styles de contrôle de barre de défilement](scroll-bar-control-styles.md).

> [!Note]  
> Pour utiliser des styles visuels avec des barres de défilement, une application doit inclure un manifeste et doit appeler [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) au début du programme. Pour plus d’informations sur les styles visuels, consultez [styles visuels](themes-overview.md). Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="scroll-box-position-and-scrolling-range"></a>Position de la case de défilement et plage de défilement

La position de la case de défilement est représentée sous la forme d’un entier. Il est relatif à l’extrémité gauche ou supérieure de la barre de défilement, selon que la barre de défilement est horizontale ou verticale. La position doit être comprise entre les valeurs minimale et maximale de la plage de défilement. Par exemple, dans une barre de défilement avec une plage comprise entre 0 et 100, la position 50 est en milieu et les autres positions sont distribuées de manière égale le long de la barre de défilement. La plage initiale dépend de la barre de défilement. Les barres de défilement standard ont une plage initiale comprise entre 0 et 100 ; les contrôles de barre de défilement ont une plage vide (les valeurs minimale et maximale sont égales à zéro), sauf si vous fournissez une plage explicite lors de la création du contrôle. Vous pouvez modifier la plage à tout moment. Vous pouvez utiliser la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) pour définir les valeurs de plage, et la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) pour récupérer les valeurs de plage actuelles.

En général, une application ajuste la plage de défilement à des entiers pratiques, ce qui facilite la conversion de la position de la case de défilement en valeur correspondant à l’objet de données à faire défiler. Par exemple, si une application doit afficher 260 lignes d’un fichier texte dans une fenêtre qui ne peut afficher que 16 lignes à la fois, la plage de la barre de défilement verticale peut être définie sur 1 à 244. Si la case de défilement est à la position 1, la première ligne se trouve en haut de la fenêtre. Si la case de défilement est à la position 244, la dernière ligne (ligne 260) se trouve au bas de la fenêtre. Si une application tente de spécifier une valeur de position inférieure à la valeur minimale ou supérieure à la valeur maximale, la valeur de la plage de défilement minimale ou maximale est utilisée à la place.

Vous pouvez définir une taille de page pour une barre de défilement. La *taille* de la page représente le nombre d’unités de données pouvant être contenues dans la zone cliente de la fenêtre propriétaire en fonction de sa taille actuelle. Par exemple, si la zone cliente peut contenir 16 lignes de texte, une application définit la taille de la page à 16. Le système utilise la taille de la page, ainsi que la plage de défilement et la longueur de l’arbre de la barre de défilement, pour définir la taille de la case de défilement. Chaque fois qu’une fenêtre contenant une barre de défilement est redimensionnée, une application doit appeler la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) pour définir la taille de la page. Une application peut récupérer la taille de page actuelle en appelant la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) d’envoi.

Pour établir une relation utile entre la plage de la barre de défilement et l’objet de données, une application doit ajuster la plage chaque fois que la taille de l’objet de données change.

Lorsque l’utilisateur déplace la case de défilement dans une barre de défilement, la barre de défilement signale la position de la case de défilement comme un entier dans la plage de défilement. Si la position est la valeur minimale, la case de défilement se trouve en haut d’une barre de défilement verticale ou à l’extrémité gauche d’une barre de défilement horizontale. Si la position est la valeur maximale, la case de défilement se trouve en bas d’une barre de défilement verticale ou à l’extrémité droite d’une barre de défilement horizontale.

La valeur maximale qu’une barre de défilement peut rapporter (c’est-à-dire la position maximale de défilement) dépend de la taille de la page. Si la barre de défilement a une taille de page supérieure à un, la position de défilement maximale est inférieure à la valeur de plage maximale. Vous pouvez utiliser la formule suivante pour calculer la position de défilement maximale :


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Une application doit déplacer la case de défilement dans une barre de défilement. Bien que l’utilisateur fasse une demande de défilement dans une barre de défilement, la barre de défilement ne met pas automatiquement à jour la position de la case de défilement. Au lieu de cela, elle transmet la requête à la fenêtre parente, qui doit faire défiler les données et mettre à jour la position de la case de défilement. Une application utilise la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) pour mettre à jour la position de la case de défilement ; dans le cas contraire, elle utilise la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Comme il contrôle le mouvement de la case de défilement, l’application peut déplacer la case de défilement dans des incréments qui conviennent le mieux aux données faisant l’objet d’un défilement.

## <a name="scroll-bar-visibility"></a>Visibilité de la barre de défilement

Le système masque et désactive une barre de défilement standard lorsque des valeurs minimales et maximales égales sont spécifiées. Le système masque et désactive également une barre de défilement standard si vous spécifiez une taille de page qui comprend la totalité de la plage de défilement de la barre de défilement. Il s’agit de la façon de masquer temporairement une barre de défilement lorsqu’elle n’est pas nécessaire pour le contenu de la zone cliente. Il n’est pas nécessaire de faire défiler les demandes de défilement dans la barre de défilement lorsqu’elle est masquée. Le système active la barre de défilement et l’affiche à nouveau lorsque vous définissez les valeurs minimale et maximale sur des valeurs inégales ou lorsque la taille de la page n’inclut pas l’intégralité de la plage de défilement. La fonction [**ShowScrollBar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) peut également être utilisée pour masquer ou afficher une barre de défilement. Elle n’affecte pas la plage de la barre de défilement, la taille de la page ou la position de la case de défilement.

La fonction [**EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) peut être utilisée pour désactiver l’une ou les deux flèches d’une barre de défilement. Une application affiche des flèches désactivées en grisé et ne répond pas aux entrées d’utilisateur.

## <a name="scroll-bar-requests"></a>Requêtes de barre de défilement

L’utilisateur effectue des requêtes de défilement en cliquant sur différentes parties d’une barre de défilement. Le système envoie la requête à la fenêtre spécifiée sous la forme d’un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) . Une barre de défilement horizontale envoie le message **WM \_ HSCROLL** ; une barre de défilement verticale envoie le message **WM \_ VSCROLL** . Chaque message comprend un code de demande qui correspond à l’action de l’utilisateur, au handle vers la barre de défilement (contrôles de barre de défilement uniquement) et, dans certains cas, à la position de la case de défilement.

Le diagramme suivant montre le code de requête que l’utilisateur génère lorsqu’il clique sur différentes parties d’une barre de défilement.

![Diagramme montrant les codes de demande associés à chaque région sur deux barres de défilement](images/csscr-02.png)

Les \_ valeurs SB spécifient l’action effectuée par l’utilisateur. Une application examine les codes qui accompagnent les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) , puis effectue l’opération de défilement appropriée. Dans le tableau suivant, l’action de l’utilisateur est spécifiée pour chaque valeur, suivie de la réponse de l’application. Dans chaque cas, une unité est définie par l’application en fonction des données. Par exemple, l’unité typique de défilement vertical du texte est une ligne de texte.



| Requête           | Action                                                                               | response                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_gamme SB        | L’utilisateur clique sur la flèche de défilement supérieure.                                                | Décrémente la position de la case de défilement ; fait défiler vers le haut des données d’une unité.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | L’utilisateur clique sur la flèche de défilement inférieure.                                             | Incrémente la position de la case de défilement ; fait défiler vers le bas des données d’une unité.                                                                                                                                                                                                                                           |
| \_LINELEFT SB      | L’utilisateur clique sur la flèche de défilement vers la gauche.                                               | Décrémente la position de la case de défilement ; fait défiler vers l’extrémité gauche des données d’une unité.                                                                                                                                                                                                                                         |
| \_LINERIGHT SB     | L’utilisateur clique sur la flèche de défilement vers la droite.                                              | Incrémente la position de la case de défilement ; fait défiler vers la fin des données d’une unité.                                                                                                                                                                                                                                        |
| SB \_ PG PRÉC        | L’utilisateur clique sur l’axe de la barre de défilement au-dessus de la case de défilement.                           | Décrémente la position de la case de défilement en fonction du nombre d’unités de données dans la fenêtre ; fait défiler vers le haut des données en utilisant le même nombre d’unités.                                                                                                                                                                                    |
| SB \_ PG.      | L’utilisateur clique sur l’arbre de la barre de défilement sous la case de défilement.                           | Incrémente la position de la case de défilement en fonction du nombre d’unités de données dans la fenêtre ; fait défiler vers le bas des données en utilisant le même nombre d’unités.                                                                                                                                                                                 |
| \_PAGELEFT SB      | L’utilisateur clique sur l’arbre de la barre de défilement à gauche de la case de défilement.                  | Décrémente la position de la case de défilement en fonction du nombre d’unités de données dans la fenêtre ; fait défiler vers l’extrémité gauche des données en utilisant le même nombre d’unités.                                                                                                                                                                               |
| \_ÉPINGLÉE SB     | L’utilisateur clique sur l’arbre de la barre de défilement à droite de la case de défilement.                 | Incrémente la position de la case de défilement en fonction du nombre d’unités de données dans la fenêtre ; fait défiler vers la fin des données d’un même nombre d’unités.                                                                                                                                                                              |
| \_THUMBPOSITION SB | L’utilisateur relâche la case de défilement après l’avoir glissée.                                  | Définit la case de défilement à la position spécifiée dans le message ; fait défiler les données du même nombre d’unités que la case de défilement a été déplacée.                                                                                                                                                                                             |
| \_THUMBTRACK SB    | L’utilisateur fait glisser la case de défilement.                                                       | Définit la case de défilement à la position spécifiée dans le message et fait défiler les données du même nombre d’unités que la case de défilement a été déplacée pour les applications qui dessinent des données rapidement. Les applications qui ne peuvent pas dessiner rapidement des données doivent attendre le \_ Code de demande SB THUMBPOSITION avant de déplacer la case de défilement et de faire défiler les données. |
| \_ENDSCROLL SB     | L’utilisateur relâche la souris après l’avoir appuyée sur une flèche ou dans l’arbre de la barre de défilement. | Aucune réponse n’est nécessaire.                                                                                                                                                                                                                                                                                                           |



 

Une barre de défilement génère \_ du code de demande SB THUMBPOSITION et SB \_ THUMBTRACK lorsque l’utilisateur clique sur la case de défilement et la fait glisser. Une application doit être programmée pour traiter le \_ Code de demande SB THUMBTRACK ou SB \_ THUMBPOSITION.

Le \_ Code de demande SB THUMBPOSITION se produit lorsque l’utilisateur relâche le bouton de la souris après avoir cliqué sur la case de défilement. Une application qui traite ce message effectue l’opération de défilement après que l’utilisateur a déplacé la case de défilement vers la position souhaitée et relâché le bouton de la souris.

Le \_ Code de demande SB THUMBTRACK se produit lorsque l’utilisateur fait glisser la case de défilement. Si une application traite \_ des codes de demande SB THUMBTRACK, elle peut faire défiler le contenu d’une fenêtre lorsque l’utilisateur fait glisser la case de défilement. Toutefois, une barre de défilement peut générer un grand nombre \_ de codes de requête SB THUMBTRACK sur une période brève, de sorte qu’une application ne doit traiter ces codes de requête que si elle peut rapidement redessiner le contenu de la fenêtre.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interface clavier pour une barre de défilement

Un contrôle de barre de défilement fournit une interface clavier intégrée qui permet à l’utilisateur d’émettre des requêtes de défilement à l’aide du clavier. pas de barre de défilement standard. Lorsqu’un contrôle de barre de défilement a le focus clavier, il envoie les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) à sa fenêtre parente quand l’utilisateur appuie sur les touches de direction. Le code de la requête est envoyé avec chaque message correspondant à la touche de direction sur laquelle l’utilisateur a appuyé. Voici les touches de direction et leurs codes de demande correspondants.



| Touche de direction | Code de la requête                  |
|-----------|-------------------------------|
| INACTIF      | SB \_ LINEDOWN ou SB \_ LINERIGHT |
| FIN       | \_bord inférieur SB                    |
| Origine      | haut de la SB \_                       |
| LEFT      | \_Gamme SB ou SB \_ LINELEFT    |
| PG suiv      | SB \_ PG. épinglée ou SB \_ |
| PRÉCÉDENTE      | SB \_ PG. PAGELEFT ou SB \_    |
| RIGHT     | SB \_ LINEDOWN ou SB \_ LINERIGHT |
| UP        | \_Gamme SB ou SB \_ LINELEFT    |



 

 

> [!Note]  
> L’interface clavier d’un contrôle de barre de défilement envoie les \_ codes de demande SB Top et SB \_ Bottom. Le \_ Code de demande SB Top indique que l’utilisateur a atteint la valeur supérieure de la plage de défilement. Une application fait défiler le contenu de la fenêtre vers le bas afin que le haut de l’objet de données soit visible. Le \_ Code de requête du bas SB indique que l’utilisateur a atteint la valeur inférieure de la plage de défilement. Si une application traite le \_ Code de demande SB Bottom, elle fait défiler le contenu de la fenêtre vers le haut afin que le bas de l’objet de données soit visible.

 

Si vous souhaitez une interface clavier pour une barre de défilement standard, vous pouvez en créer une vous-même en traitant le message [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut dans votre procédure de fenêtre, puis en effectuant l’action de défilement appropriée en fonction du code de la touche virtuelle qui accompagne le message. Pour plus d’informations sur la création d’une interface clavier pour une barre de défilement, consultez [création d’une interface clavier pour une barre de défilement standard](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Défilement de la zone client

La façon la plus simple de faire défiler le contenu d’une zone client consiste à l’effacer, puis à le redessiner. Il s’agit de la méthode qu’une application est susceptible d’utiliser avec les \_ codes de demande SB PageUp, SB \_ PageDown et SB \_ Top, qui nécessitent généralement un contenu entièrement nouveau.

Pour certains codes de demande, tels que SB \_ LineUp et SB \_ LINEDOWN, tout le contenu n’a pas besoin d’être effacé, car certains restent visibles une fois le défilement effectué. La fonction [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) conserve une partie du contenu de la zone client, déplace la partie conservée d’une quantité spécifiée, puis prépare le reste de la zone cliente pour la peinture de nouvelles informations. **ScrollWindowEx** utilise la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) pour déplacer une partie spécifique de l’objet de données vers un nouvel emplacement dans la zone cliente. Toute partie non couverte de la zone client (tout ce qui n’est pas préservé) est invalidée, effacée et peinte lorsque le message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) suivant se produit.

La fonction [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) peut être utilisée pour exclure une partie de la zone cliente de l’opération de défilement. Cela permet de conserver les éléments avec des positions fixes, telles que les fenêtres enfants, de se déplacer dans la zone cliente. Il invalide automatiquement la partie de la zone cliente qui doit recevoir les nouvelles informations, de sorte que l’application n’a pas à calculer ses propres régions de découpage. Pour plus d’informations sur le découpage, consultez [découpage](/windows/desktop/gdi/clipping).

En général, une application fait défiler le contenu d’une fenêtre dans la direction opposée à celle indiquée par la barre de défilement. Par exemple, quand l’utilisateur clique sur l’arbre de la barre de défilement dans la zone située sous la case de défilement, une application fait défiler l’objet dans la fenêtre vers le haut pour révéler une partie de l’objet qui se trouve sous la partie visible.

Vous pouvez également faire défiler une zone rectangulaire à l’aide de la fonction [**ScrollDC**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) .

## <a name="scroll-bar-colors-and-metrics"></a>Couleurs et métriques de la barre de défilement

La valeur de couleur définie par le système, ScrollBar de couleur \_ , contrôle la couleur dans un arbre de barre de défilement. Utilisez la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) pour déterminer la couleur de l’arbre de la barre de défilement et la fonction [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) pour définir la couleur de l’arbre de la barre de défilement. Notez, toutefois, que ce changement de couleur affecte toutes les barres de défilement dans le système.

Vous pouvez récupérer les dimensions des bitmaps que le système utilise dans les barres de défilement standard en appelant la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Voici les valeurs de métriques système associées aux barres de défilement.



| Métrique du système | Description                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| \_CXHSCROLL SM | Largeur de la bitmap de direction sur la barre de défilement horizontale                                                                             |
| \_CXHTHUMB SM  | Largeur de la case de défilement sur la barre de défilement horizontale. Cette valeur récupère la largeur d’une barre de défilement dont la taille de page est égale à zéro.    |
| \_CXVSCROLL SM | Largeur de la bitmap de direction sur la barre de défilement verticale                                                                               |
| \_CYHSCROLL SM | Hauteur de la bitmap de direction sur la barre de défilement horizontale                                                                            |
| \_CYVSCROLL SM | Hauteur de la bitmap de direction sur la barre de défilement verticale                                                                              |
| \_CYVTHUMB SM  | Hauteur de la case de défilement sur la barre de défilement verticale. Cette valeur récupère la hauteur d’une barre de défilement dont la taille de page est égale à zéro. |



 

 

 
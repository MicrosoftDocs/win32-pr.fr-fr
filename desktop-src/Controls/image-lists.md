---
title: À propos des listes d’images
description: Une liste d’images est une collection d’images de même taille, dont chacune peut être référencée par son index.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f059e89b04d16088fff1d937bd29cb23a427d4c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316530"
---
# <a name="about-image-lists"></a>À propos des listes d’images

Une liste d’images est une collection d’images de même taille, dont chacune peut être référencée par son index. Les listes d’images permettent de gérer efficacement de grands ensembles d’icônes ou de bitmaps. Toutes les images d’une liste d’images sont contenues dans un seul bitmap de grande largeur dans le format de l’appareil à l’écran. Une liste d’images peut également inclure une bitmap monochrome qui contient des masques utilisés pour dessiner des images en toute transparence (style d’icône).

L’API Microsoft Win32 fournit des fonctions de liste d’images et des macros qui vous permettent de créer et de détruire des listes d’images, d’ajouter et de supprimer des images, de remplacer et de fusionner des images, de dessiner des images et de faire glisser des images. Pour utiliser les fonctions de liste d’images, incluez le fichier d’en-tête de contrôle commun dans vos fichiers de code source et liez-le à la bibliothèque d’exportation de contrôle commune. En outre, avant d’appeler une fonction de liste d’images, utilisez la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) pour vous assurer que la dll de contrôles communs est chargée.

Les rubriques suivantes sont présentées dans cette section :

-   [Types](#types)
-   [Création et destruction de listes d’images](#creating-and-destroying-image-lists)
-   [Ajout et suppression d’images](#adding-and-removing-images)
-   [Remplacement et fusion d’images](#replacing-and-merging-images)
-   [Dessiner des images](#drawing-images)
-   [Faire glisser des images](#dragging-images)
-   [Informations sur l’image](#image-information)
-   [Superpositions d’images](#image-overlays)
-   [Icônes d’anticrénelage 32 bits](#32-bit-antialiased-icons)

## <a name="types"></a>Types

Il existe deux types de listes d’images : non masqué et masqué. Une liste d’images non masquées se compose d’une image bitmap de couleur qui contient une ou plusieurs images. Une liste d’images masquées est constituée de deux bitmaps de taille égale. La première est une image bitmap de couleur qui contient les images, tandis que la seconde est une image bitmap monochrome qui contient une série de masques, un pour chaque image de la première bitmap.

Lorsqu’une image non masquée est dessinée, elle est simplement copiée dans le contexte de périphérique cible ; autrement dit, il est dessiné sur la couleur d’arrière-plan existante du contexte de périphérique. Quand une image masquée est dessinée, les bits de l’image sont combinés avec les bits du masque, ce qui produit généralement des zones transparentes dans la bitmap où la couleur d’arrière-plan du contexte de périphérique cible s’affiche. Vous pouvez spécifier plusieurs styles de dessin quand vous dessinez une image masquée. Par exemple, vous pouvez spécifier que l’image soit pour indiquer un objet sélectionné.

## <a name="creating-and-destroying-image-lists"></a>Création et destruction de listes d’images

Pour créer une liste d’images, appelez la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . Les paramètres incluent le type de liste d’images à créer, les dimensions de chaque image et le nombre d’images que vous avez l’intention d’ajouter à la liste. Pour une liste d’images non masquées, la fonction crée une seule bitmap suffisamment grande pour contenir le nombre spécifié d’images des dimensions données. Ensuite, il crée un contexte de périphérique compatible avec l’écran et y sélectionne la bitmap. Pour une liste d’images masquées, la fonction crée deux bitmaps et deux contextes de périphérique compatibles avec l’écran. Il sélectionne l’image bitmap dans un contexte de périphérique et le bitmap de masque dans l’autre. La DLL du contrôle commun contient le code exécutable pour les fonctions de la liste d’images.

Dans [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), vous spécifiez le nombre initial d’images qui figureront dans une liste d’images, ainsi que le nombre d’images par lesquelles la liste peut croître. Par conséquent, si vous essayez d’ajouter d’autres images que celles initialement spécifiées, la liste d’images augmente automatiquement pour s’adapter aux nouvelles images.

Si [**la \_ création de ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) s’effectue correctement, elle retourne un handle vers le type HIMAGELIST. Vous utilisez ce handle dans d’autres fonctions de liste d’images pour accéder à la liste d’images et gérer les images. Vous pouvez ajouter et supprimer des images, copier des images d’une liste d’images vers une autre, et fusionner des images de deux listes d’images différentes. Lorsque vous n’avez plus besoin d’une liste d’images, vous pouvez la détruire en spécifiant son handle dans un appel à la fonction de [**\_ destruction ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) .

## <a name="adding-and-removing-images"></a>Ajout et suppression d’images

Vous pouvez ajouter des images bitmap, des icônes ou des curseurs à une liste d’images. Vous ajoutez des images bitmap en spécifiant les descripteurs à deux bitmaps dans un appel à la fonction [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) . La première bitmap contient une ou plusieurs images à ajouter à la bitmap de l’image, et la deuxième bitmap contient les masques à ajouter à la bitmap du masque. Pour les listes d’images non masquées, le deuxième descripteur de bitmap est ignoré ; elle peut avoir la valeur **null**.

La [**fonction \_ AddMasked ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) ajoute également des images bitmap à une liste d’images masquées. Cette fonction est similaire à [**l' \_ Ajout ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), sauf que vous ne spécifiez pas d’image bitmap de masque. Au lieu de cela, vous spécifiez une couleur que le système associe à la bitmap de l’image pour générer automatiquement les masques. Chaque pixel de la couleur spécifiée dans la bitmap d’image est remplacé par le noir et le bit correspondant dans le masque est défini sur 1. Par conséquent, tout pixel de l’image qui correspond à la couleur spécifiée est transparent lorsque l’image est dessinée.

La [**macro \_ addicon ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) ajoute une icône ou un curseur à une liste d’images. Si la liste d’images est masquée, **ImageList \_ addicon** ajoute le masque fourni avec l’icône ou le curseur à la bitmap de masque. Si la liste d’images n’est pas masquée, le masque de l’icône ou du curseur n’est pas utilisé lors du dessin de l’image.

Vous pouvez créer une icône basée sur une image et un masque dans une liste d’images à l’aide de la fonction [**\_ GetIcon ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) . La fonction retourne le handle vers la nouvelle icône.

[**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)et [**ImageList \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) affectent un index à chaque image quand elle est ajoutée à une liste d’images. Les index sont de base zéro ; autrement dit, la première image de la liste a un index égal à zéro, la suivante a un index d’un, et ainsi de suite. Après l’ajout d’une seule image, les fonctions retournent l’index de l’image. Quand plusieurs images sont ajoutées à la fois, les fonctions retournent l’index de la première image.

La fonction [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) supprime une image d’une liste d’images.

## <a name="replacing-and-merging-images"></a>Remplacement et fusion d’images

Les fonctions [**ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) et [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) remplacent une image dans une liste d’images par une nouvelle image. **ImageList \_ Replace** remplace une image par une image bitmap et un masque, tandis que **ImageList \_ ReplaceIcon** remplace une image par une icône ou un curseur.

La fonction de [**\_ fusion ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) fusionne deux images, en stockant la nouvelle image dans une nouvelle liste d’images. La nouvelle image est créée en dessinant la deuxième image de manière transparente sur la première. Le masque de la nouvelle image résulte de l’exécution d’une opération **or** logique sur les bits des masques pour les deux images existantes.

## <a name="drawing-images"></a>Dessiner des images

Pour dessiner une image, vous utilisez la fonction [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . Vous spécifiez le handle d’une liste d’images, l’index de l’image à dessiner, le handle vers le contexte de périphérique de destination, un emplacement dans le contexte de périphérique et un ou plusieurs styles de dessin.

Lorsque vous spécifiez le style **\_ transparent icher** , [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) utilise un processus en deux étapes pour dessiner une image masquée. Tout d’abord, elle effectue une opération **and** logique sur les bits de l’image et les bits du masque. Il effectue ensuite une opération **Xor** logique sur les résultats de la première opération et les bits d’arrière-plan du contexte de périphérique de destination. Ce processus crée des zones transparentes dans l'image résultante ; autrement dit, chaque bit blanc dans le masque rend le bit correspondant dans l'image résultante transparent.

Avant de dessiner une image masquée sur un arrière-plan de couleur unie, vous devez utiliser la fonction [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) pour définir la couleur d’arrière-plan de la liste d’images sur la même couleur que la destination. La définition de la couleur élimine la nécessité de créer des zones transparentes dans l’image et permet à [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) de simplement copier l’image dans le contexte de périphérique de destination, ce qui entraîne une augmentation significative des performances. Pour dessiner l’image, spécifiez le style **\_ normal icher** dans un appel à **ImageList \_ Draw** ou **ImageList \_ DrawEx**.

Vous pouvez définir la couleur d’arrière-plan d’une liste d’images masquées à tout moment pour qu’elle soit correctement dessinée sur un arrière-plan Uni. Si la couleur d’arrière-plan est définie sur CLR \_ None, les images sont dessinées de manière transparente par défaut. Pour récupérer la couleur d’arrière-plan d’une liste d’images, utilisez la fonction [**ImageList \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) .

Les styles **icher \_ BLEND25** et **icher \_ BLEND50** dithernt l’image avec la couleur de surbrillance du système. Ces styles sont utiles si vous utilisez une image masquée pour représenter un objet que l'utilisateur peut sélectionner. Par exemple, vous pouvez utiliser le style **icher \_ BLEND50** pour dessiner l’image lorsque l’utilisateur la sélectionne.

Une image non masquée est copiée dans le contexte de périphérique de destination à l’aide de l’opération SRCCOPY raster. Les couleurs dans l'image s'affichent de la même façon indépendamment de la couleur d'arrière-plan du contexte de périphérique. Les styles de dessin spécifiés dans [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) n’ont pas d’effet sur l’apparence d’une image non masquée.

## <a name="dragging-images"></a>Faire glisser des images

L’API Win32 comprend des fonctions permettant de faire glisser une image à l’écran. Les fonctions Glisser-déplacer déplacent une image en douceur, en couleurs, sans aucun clignotement du curseur. Les images masquées et démasquées peuvent être glissées.

La [**fonction \_ BeginDrag ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) commence une opération glisser. Les paramètres incluent le handle de la liste d’images, l’index de l’image à faire glisser et l’emplacement de la zone réactive dans l’image. La zone réactive est un seul pixel que les fonctions de glissement identifient comme l'emplacement exact de l'image à l'écran. Généralement, une application définit la zone réactive afin qu'elle coïncide avec la zone réactive du curseur de la souris. La [**fonction \_ DragMove ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) déplace l’image vers un nouvel emplacement.

La [**fonction \_ DragEnter DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) définit la position initiale de l’image de glissement dans une fenêtre et dessine l’image à la position. Les paramètres incluent le handle vers la fenêtre dans laquelle dessiner l’image et les coordonnées de la position initiale dans la fenêtre. Les coordonnées sont exprimées par rapport au coin supérieur gauche de la fenêtre, pas de la zone cliente. Il en va de même pour toutes les fonctions de glissement d’images qui prennent des coordonnées en tant que paramètres. Cela signifie que vous devez compenser les largeurs des éléments de la fenêtre, tels que la bordure, la barre de titre et la barre de menus, lorsque vous spécifiez les coordonnées. Si vous spécifiez un handle de fenêtre **null** lors de l’appel à **ImageList \_ DragEnter**, les fonctions de glissement dessinent l’image dans le contexte de périphérique associé à la fenêtre du bureau, et les coordonnées sont relatives au coin supérieur gauche de l’écran.

La [**fonction \_ SetDragCursorImage ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) crée une image de glissement en combinant l’image donnée (généralement une image de curseur de la souris) avec l’image de glissement actuelle. Étant donné que les fonctions de glissement utilisent la nouvelle image pendant une opération de glissement, vous devez utiliser la fonction [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) pour masquer le curseur de la souris réel après avoir appelé **ImageList \_ SetDragCursorImage**. Sinon, le système peut sembler être composé de deux curseurs de souris pour la durée de l'opération Glisser-déplacer.

Quand une application appelle [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag), le système crée une liste d’images interne temporaire, puis copie l’image de glissement spécifiée dans la liste interne. Vous pouvez récupérer le descripteur de la liste d’images de glissement temporaire à l’aide de la fonction [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) . La fonction récupère également l'emplacement actuel de glissement et le décalage de l'image glissée par rapport à la position de glissement.

## <a name="image-information"></a>Informations sur l’image

Il existe un certain nombre de fonctions qui récupèrent des informations à partir d’une liste d’images. La [**fonction \_ GetImageInfo ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) remplit une structure [**IMAGEINFO**](/windows/desktop/api) avec des informations sur une image unique, y compris les handles des bitmaps d’image et de masque, le nombre de plans de couleur et de bits par pixel et le rectangle englobant de l’image dans la bitmap de l’image. Vous pouvez utiliser ces informations pour manipuler directement les bitmaps de l’image. La [**fonction \_ GetImageCount ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) récupère le nombre d’images dans une liste d’images.

## <a name="image-overlays"></a>Superpositions d’images

Chaque liste d’images comprend une liste d’index à utiliser comme superpositions. Une superposition est une image qui est dessinée de façon transparente sur une autre image. Toute image qui figure actuellement dans la liste d’images peut être utilisée en tant que superposition. Vous pouvez spécifier jusqu’à quatre superpositions par liste d’images. Cette limite a été étendue à 15 dans la version 4,71.

Vous ajoutez l’index d’une image à la liste des superpositions à l’aide de la fonction [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , en spécifiant le descripteur de la liste d’images, l’index de l’image existante et l’index de superposition souhaité. Cela indique en effet à la liste d’images que « l’image à l’index *x* peut être utilisée comme superposition et que je veux faire référence à la superposition en tant qu’index de superposition *y*. » Les index de superposition sont basés sur un et non sur zéro, car un index de superposition de zéro signifie qu’aucun chevauchement n’est utilisé.

Vous spécifiez une superposition lors du dessin d’une image avec la fonction [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . La superposition est spécifiée en effectuant une opération **or** logique entre les indicateurs de dessin souhaités et le résultat de la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . La macro **INDEXTOOVERLAYMASK** prend l’index de superposition et le met en forme pour l’inclure avec les indicateurs de ces fonctions. Cette opération dessine l’image avec la superposition spécifiée. L’exemple suivant montre comment une superposition est ajoutée et spécifiée lors du dessin de l’image.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



L’image 1 est alors dessinée, puis superposée à l’image 0. Comme 3 est l’index de superposition que vous avez spécifié dans l’appel [**\_ SetOverlayImage ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , 3 est placé dans la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) .

## <a name="32-bit-antialiased-icons"></a>Icônes d’anticrénelage 32 bits

L’anticrénelage est une technique d’adoucissement ou de flou des bords nets. Cela donne aux images une apparence plus naturelle. Les listes d’images dans Windows Vista et Windows 7 prennent en charge l’utilisation des bitmaps et des icônes antialias 32 bits. Les valeurs de couleur utilisent 24 bits et 8 bits sont utilisés comme canal alpha sur les icônes. Pour créer une liste d’images pouvant gérer une image 32 bits par pixel (BPP), appelez la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , en passant un indicateur ILC \_ COLOR32.

Pour créer correctement des icônes 32 bits, vous devez créer plusieurs images pour chaque icône, comme indiqué dans l’illustration suivante.

![Illustration montrant trois tailles d’icônes pour chacune des trois profondeurs de couleurs](images/theme2.png)

-   Les trois premières images sont en mode 16 couleurs pour une utilisation en mode sans échec.
-   Les trois icônes suivantes sont utilisées en mode 256 couleurs.
-   Les trois dernières icônes ont le canal alpha et peuvent être utilisées uniquement dans les systèmes d’exploitation qui exécutent une couleur 24 bits ou supérieure.
-   L’ordre des images dans le format des icônes importe peu. Si l’ordre est incorrect, les versions antérieures de Windows fonctionnent mal lors de l’extraction des icônes. L’extraction incorrecte des icônes peut entraîner une altération de la mémoire et un rendu incorrect.
-   Les versions précédentes de Windows contenait une limite de ressources de 10 icônes.

> [!Note]  
> Vous pouvez utiliser des outils tiers pour générer des fichiers d’icône et des bitmaps qui contiennent un canal alpha. Si vous utilisez [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) pour charger une image bitmap 32 BPP qui contient alpha, vous devez spécifier l' \_ indicateur CREATEDIBSECTION LR.

 

 

 
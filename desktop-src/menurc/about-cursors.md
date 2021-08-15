---
title: À propos des curseurs
description: Cette rubrique décrit les curseurs standard.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- ressources, curseurs
- curseurs, à propos de
- curseurs, standard
- curseurs standard
- SetSystemCursor fonction)
- curseurs, personnalisés
- curseurs personnalisés
- curseurs, zones réactives
- curseurs, création
- création de curseurs
- curseurs, emplacement
- curseurs, apparence
- destruction de curseurs
- duplication de curseurs
- curseur de classe
- affinage des curseurs
- curseurs, destruction
- curseurs, duplication
- curseurs, classe
- curseurs, affinage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735379"
---
# <a name="about-cursors"></a>À propos des curseurs

Windows fournit un ensemble de curseurs standard qui sont disponibles pour n’importe quelle application à utiliser à tout moment. Les fichiers d’en-tête du kit de développement logiciel (SDK) contiennent des identificateurs pour les curseurs standard : les identificateurs commencent par le préfixe **IDC \_** .

Chaque curseur standard possède une image par défaut correspondante qui lui est associée. L’utilisateur ou une application peut remplacer l’image par défaut associée à n’importe quel curseur standard à tout moment. Une application remplace une image par défaut à l’aide de la fonction [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) . l’illustration suivante montre plusieurs curseurs standard de Windows Vista :

![curseurs standard, y compris main, signe plus à quatre flèches, flèche avec point d’interrogation, cercle, plume](images/cursorsstandard.png)

Une application peut utiliser la fonction [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) pour récupérer l’image actuelle d’un curseur et peut dessiner le curseur à l’aide de la fonction [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Pour dessiner l’image par défaut d’un curseur standard, spécifiez l’indicateur **di \_ compat** dans l’appel à **DrawIconEx**. Si vous ne spécifiez pas l’indicateur de **\_ compatibilité di** , **DrawIconEx** dessine le curseur standard à l’aide de l’image spécifiée par l’utilisateur.

Les curseurs personnalisés sont conçus pour être utilisés dans une application spécifique et peuvent être toute conception définie par le développeur. L’illustration suivante montre plusieurs curseurs personnalisés.

![curseurs personnalisés, y compris main, Banana, tambour, montre en main, métronome](images/cursorscustom.png)

Les curseurs peuvent être de type monochrome ou couleur, et être statiques ou animés. Le type de curseur utilisé sur un système informatique particulier dépend de l’affichage du système. Les anciens affichages tels que VGA ne prennent pas en charge les curseurs de couleur ou animés. Les nouveaux affichages, dont les pilotes d’affichage utilisent le moteur DIB (Device-Independent Bitmap), les prennent en charge.

Les curseurs et les icônes sont similaires et peuvent être utilisés indifféremment dans de nombreuses situations. La seule différence réside dans le fait qu’une image spécifiée comme curseur doit être au format pris en charge par l’affichage. Par exemple, un curseur doit être monochrome pour un affichage VGA.

Cette vue d’ensemble fournit des informations sur les rubriques suivantes :

-   [Zone réactive](#the-hot-spot)
-   [La souris et le curseur](#the-mouse-and-the-cursor)
-   [Création de curseur](#cursor-creation)
-   [Emplacement et apparence du curseur](#cursor-location-and-appearance)
-   [Limiter le curseur](#cursor-confinement)
-   [Destruction de curseur](#cursor-destruction)
-   [Duplication de curseur](#cursor-duplication)
-   [Curseur de la classe de fenêtre](#the-window-class-cursor)

## <a name="the-hot-spot"></a>Zone réactive

Dans le curseur, un pixel appelé « *spot* » marque l’emplacement exact de l’écran qui est affecté par un événement de souris, par exemple en cliquant sur un bouton de la souris. En règle générale, la zone réactive est le point focal du curseur. Le système effectue le suivi de ce point et le reconnaît comme position du curseur. Par exemple, les zones réactives typiques sont le pixel à l’extrémité d’un curseur en forme de flèche et le pixel au milieu d’un curseur en forme de croix. Les images suivantes montrent deux curseurs d’un programme de dessin, dans lesquels les zones réactives sont associées à la pointe du pinceau et la Croix de la peinture peut.

![zones réactives sur deux curseurs](images/cursorhotspot.png)

Quand un événement d’entrée de la souris se produit, le pilote de la souris convertit l’événement en un message de souris approprié qui comprend les coordonnées de la zone réactive. Le système envoie le message de la souris à la fenêtre qui contient la zone réactive ou à la fenêtre qui capture l’entrée de la souris. Pour plus d’informations, consultez [entrée de la souris](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>La souris et le curseur

Le système reflète le mouvement de la souris en déplaçant le curseur sur l’écran en conséquence. Lorsque le curseur se déplace sur différentes parties de fenêtres ou dans différentes fenêtres, le système (ou une application) modifie l’apparence du curseur. Par exemple, lorsque le curseur traverse un lien hypertexte, le système modifie le curseur d’une flèche en une main.

![curseur standard passant à une main quand vous êtes au-dessus d’un lien hypertexte](images/cursorchangingstate.png)

Si le système n’a pas de souris, le système affiche et déplace le curseur uniquement lorsque l’utilisateur choisit certaines commandes système, telles que celles utilisées pour dimensionner ou déplacer une fenêtre. Pour permettre à l’utilisateur d’afficher et de déplacer le curseur quand une souris n’est pas disponible, une application peut utiliser les fonctions de curseur pour simuler le mouvement de la souris. À partir de cette fonctionnalité de simulation, l’utilisateur peut utiliser les touches de direction pour déplacer le curseur.

## <a name="cursor-creation"></a>Création de curseur

Étant donné que les curseurs standard sont prédéfinis, il n’est pas nécessaire de les créer. Pour utiliser un curseur standard, une application récupère un handle de curseur à l’aide de la fonction [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *handle de curseur* est une valeur unique du type **HCURSOR** qui identifie un curseur standard ou personnalisé.

Pour créer un curseur personnalisé pour une application, vous utilisez généralement une application graphique et incluez le curseur en tant que ressource dans le fichier de définition de ressources de l’application. Au moment de l’exécution, appelez [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) pour récupérer le handle de curseur. Les ressources de curseur contiennent des données pour plusieurs périphériques d’affichage différents. La fonction **LoadCursor** sélectionne automatiquement les données les plus appropriées pour le périphérique d’affichage actuel. Pour charger un curseur directement à partir d’un. CUR ou. Fichier ANI, utilisez la fonction [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) .

Vous pouvez également créer un curseur personnalisé au moment de l’exécution à l’aide de la fonction [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , qui crée un curseur basé sur le contenu d’une structure [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La fonction [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) remplit cette structure avec des coordonnées de zone réactive et des informations relatives au masque et à la couleur associés.

Les applications doivent implémenter des curseurs personnalisés en tant que ressources et utiliser [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) au lieu de créer le curseur au moment de l’exécution. L’utilisation des ressources de curseur évite la dépendance des appareils, simplifie la localisation et permet aux applications de partager des conceptions de curseurs.

La fonction [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permet à une application de créer des icônes et des curseurs basés sur les données de ressources. **CreateIconFromResourceEx** crée un curseur basé sur les données de ressources binaires à partir d’autres fichiers exécutables (.exe) ou dll. Elle doit être précédée d’appels à la fonction [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) , ainsi que de plusieurs fonctions de ressources. **LookupIconIdFromDirectoryEx** identifie les données de curseur les plus appropriées pour le périphérique d’affichage actuel. Pour plus d’informations sur les fonctions de ressource, consultez [ressources](resources.md).

## <a name="cursor-location-and-appearance"></a>Emplacement et apparence du curseur

Le système affiche automatiquement un curseur pour la souris et met à jour sa position à l’écran. Vous pouvez obtenir les coordonnées de l’écran actuel du curseur et déplacer le curseur vers n’importe quel emplacement de l’écran à l’aide des fonctions [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) et [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) , respectivement.

Vous pouvez également récupérer le handle du curseur en cours à l’aide de la fonction [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) , et vous pouvez définir le curseur à l’aide de la fonction [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) . Une fois que vous avez appelé **SetCursor**, l’apparence du curseur n’est pas modifiée tant que la souris n’est pas déplacée, le curseur est explicitement défini sur un autre curseur ou une commande système est exécutée.

Lorsque l’utilisateur déplace la souris, le système redessine le curseur au nouvel emplacement. Le système redessine automatiquement la conception de curseur associée à la fenêtre vers laquelle le curseur pointe.

Vous pouvez masquer et réafficher le curseur, sans modifier la conception du curseur, à l’aide de la fonction [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) . Cette fonction utilise un compteur interne pour déterminer quand masquer ou afficher le curseur. Une tentative d’affichage du curseur incrémente le compteur ; une tentative de masquage du curseur décrémente le compteur. Le curseur est visible uniquement si ce compteur est supérieur ou égal à zéro.

La fonction [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) obtient les informations suivantes pour le curseur global : indique si le curseur est masqué ou affiché, le handle du curseur et les coordonnées du curseur.

## <a name="cursor-confinement"></a>Limiter le curseur

Vous pouvez limiter le curseur à une zone rectangulaire sur l’écran à l’aide de la fonction [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) . Cela est utile lorsque l’utilisateur doit répondre à un certain événement dans la zone confinée du rectangle. Par exemple, vous pouvez utiliser **ClipCursor** pour limiter le curseur à une boîte de dialogue modale, ce qui empêche l’utilisateur d’interagir avec d’autres fenêtres jusqu’à la fermeture de la boîte de dialogue.

La fonction [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) récupère les coordonnées d’écran de la zone rectangulaire dans laquelle le curseur est provisoirement confiné. Lorsqu’il est nécessaire de limiter le curseur, vous pouvez également utiliser cette fonction pour enregistrer les coordonnées de la zone d’origine dans laquelle le curseur peut se déplacer. Ensuite, vous pouvez restaurer le curseur dans la zone d’origine lorsque la nouvelle confineion n’est plus nécessaire.

## <a name="cursor-destruction"></a>Destruction de curseur

Vous pouvez détruire le handle de curseur et libérer la mémoire du curseur utilisé en appelant la fonction [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) . Toutefois, cette fonction n’a aucun effet sur un curseur partagé. Un curseur partagé est valide tant que le module à partir duquel il a été chargé reste en mémoire. Les fonctions suivantes obtiennent un curseur partagé :

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (si vous utilisez l' **indicateur \_ partagé LR** )
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (si vous utilisez l’indicateur **LR \_ COPYRETURNORG** et que *hImage* est un curseur partagé)

Lorsque vous n’avez plus besoin d’un curseur que vous avez créé à l’aide de la fonction [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , vous devez détruire le curseur. La fonction [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) détruit le handle de curseur et libère la mémoire utilisée par le curseur. Utilisez cette fonction uniquement sur les curseurs créés avec **CreateIconIndirect**.

## <a name="cursor-duplication"></a>Duplication de curseur

La fonction [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copie un handle de curseur. Cela permet au code de l’application ou de la DLL de récupérer le descripteur d’un curseur détenu par un autre module. Ensuite, si l’autre module est libéré, le module qui a copié le curseur peut toujours utiliser la conception de curseur.

Pour plus d’informations sur l’ajout, la suppression ou le remplacement de ressources de curseur dans des fichiers exécutables, consultez [ressources](resources.md).

## <a name="the-window-class-cursor"></a>Curseur de la classe de fenêtre

Lorsque vous inscrivez une classe de fenêtre à l’aide de la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) , vous pouvez lui assigner un curseur par défaut, appelé *curseur de classe*. Une fois que l’application a inscrit la classe de fenêtre, chaque fenêtre de cette classe possède le curseur de classe spécifié.

Pour remplacer le curseur de la classe, traitez le message [**WM \_ SETCURSOR**](wm-setcursor.md) . Vous pouvez également remplacer un curseur de classe à l’aide de la fonction [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Cette fonction modifie les paramètres de fenêtre par défaut pour toutes les fenêtres d’une classe spécifiée. Pour plus d’informations, consultez [Class Cursor](/windows/desktop/winmsg/about-window-classes).

 

 
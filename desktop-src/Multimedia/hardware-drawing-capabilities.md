---
title: Fonctionnalités de dessin matériel
description: Fonctionnalités de dessin matériel
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- Gestionnaire de compression vidéo (VCM), dessin
- VCM (gestionnaire de compression vidéo), dessin
- ICGetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029311"
---
# <a name="hardware-drawing-capabilities"></a>Fonctionnalités de dessin matériel

Certains convertisseurs peuvent dessiner directement sur du matériel vidéo au fur et à mesure qu’ils décompressent des images vidéo. Ces convertisseurs retournent l' \_ indicateur de dessin VIDCF en réponse à la fonction [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Lorsque vous utilisez ce type de convertisseur, votre application n’a pas à gérer les données décompressées. Elle permet au convertisseur de conserver les données décompressées pour le dessin.

Si votre application utilise un convertisseur avec des fonctionnalités de dessin, elle doit gérer les tâches suivantes :

-   Sélectionnez un convertisseur.
-   Spécifiez des formats d’image.
-   Initialisez le convertisseur.
-   Dessinez les données.
-   Paramètres de dessin de contrôle.

## <a name="renderer-selection"></a>Sélection du convertisseur

La macro [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) ouvre un convertisseur qui peut dessiner des images avec le format spécifié. Elle retourne un handle d’un convertisseur si elle réussit, ou zéro dans le cas contraire. Cette macro utilise la fonction [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) pour ouvrir le convertisseur.

## <a name="specifying-image-formats"></a>Spécification des formats d’image

Étant donné que votre application n’a pas besoin de dessiner les données décompressées, elle n’a pas besoin d’un format de sortie spécifique. Toutefois, il doit s’assurer que le convertisseur peut dessiner à l’aide du format d’entrée à l’aide du message de [**\_ \_ requête ICM de dessin**](icm-draw-query.md) (ou de la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) ). Ce message ne peut pas déterminer si un convertisseur peut dessiner une image bitmap. Si votre application doit déterminer si le convertisseur peut dessiner la bitmap, utilisez ce message avec la fonction [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) .

Votre application peut avoir un convertisseur suggérant un format d’entrée à l’aide de la fonction [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) . Cette fonction est utilisée lorsqu’un convertisseur sépare les fonctionnalités de dessin des fonctionnalités de décompression. La plupart des applications qui utilisent les fonctions de dessin n’ont pas besoin de déterminer le format de sortie.

## <a name="renderer-initialization"></a>Initialisation du convertisseur

La fonction [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) Initialise un convertisseur et lui indique la destination du dessin. Cette fonction peut également effectuer les tâches suivantes :

-   Déterminez si le convertisseur prend en charge un format d’entrée spécifique.
-   Spécifie si l’opération de dessin occupe une fenêtre ou la totalité de l’écran.
-   Spécifiez la partie de l’image à afficher à l’aide du rectangle source.
-   Définissez la vitesse de lecture de la séquence d’images.

Certains convertisseurs encadrent les données compressées pour fonctionner plus efficacement. Votre application peut envoyer le [**message \_ GETBUFFERSWANTED ICM**](icm-getbufferswanted.md) (ou utiliser la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) ) pour déterminer le nombre de mémoires tampons demandées par le convertisseur. Votre application doit précharger ces mémoires tampons et les envoyer au convertisseur avant le dessin.

## <a name="drawing-the-data"></a>Dessin des données

Vous pouvez utiliser la fonction [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) pour décompresser les données pour le dessin. Toutefois, le convertisseur ne commence pas à dessiner des données tant que votre application n’a pas envoyé le message de [**\_ \_ début de dessin ICM**](icm-draw-start.md) (ou utilise la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) ). Lorsque votre application appelle cette fonction, le convertisseur commence à dessiner les frames à la vitesse spécifiée par le paramètre *dwRate* divisée par le paramètre *dwScale* ; ces paramètres ont été fournis lorsque l’application a initialisé le convertisseur à l’aide de la fonction [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) . Le dessin continue jusqu’à ce que votre application envoie le message d' [**\_ \_ arrêt du dessin ICM**](icm-draw-stop.md) (ou utilise la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) ).

> [!Note]  
> Si un convertisseur met en mémoire tampon les données avant le dessin, votre application ne doit pas utiliser la macro **ICDrawStart** tant qu’elle n’a pas envoyé le nombre de frames renvoyés par le convertisseur pour la macro **ICGetBuffersWanted** .

 

Le paramètre *lTime* de [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) spécifie l’heure de dessin d’une image. Le convertisseur divise cet entier par l’échelle de temps spécifiée avec [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) pour obtenir l’heure réelle. Les heures pour les fonctions **ICDraw** sont relatives à **ICDrawStart**. **ICDrawStart** définit l’horloge sur zéro. Par exemple, si votre application spécifie 1000 pour l’échelle de temps et 75 pour *lTime*, le convertisseur dessine le frame 75 millisecondes dans la séquence.

## <a name="controlling-drawing-parameters"></a>Contrôle des paramètres de dessin

Vous pouvez surveiller l’horloge d’un convertisseur en envoyant le message de l’affichage [**ICM de \_ dessin \_**](icm-draw-gettime.md) (ou en utilisant la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) ) et vous pouvez définir l’horloge d’un convertisseur qui peut dessiner des données en envoyant le message [**ICM \_ Draw \_ setTime**](icm-draw-settime.md) (ou en utilisant la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) ).

Pour modifier la position actuelle lors du dessin d’un convertisseur, votre application peut envoyer le message de [**\_ \_ fenêtre de dessin ICM**](icm-draw-window.md) (ou utiliser la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) ) pour repositionner la fenêtre. Les applications utilisent généralement ce message à chaque modification de la fenêtre.

Si la fenêtre de lecture reçoit un message de génération de palette, votre application doit envoyer le message ICM de réalisation (ou utiliser la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) ) pour que le convertisseur réalise à nouveau la palette pour la lecture. [**\_ \_**](icm-draw-realize.md) Les applications peuvent modifier la palette en envoyant le message [**\_ \_ CHANGEPALETTE de dessin ICM**](icm-draw-changepalette.md) (ou en utilisant la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) ) et obtenir la palette actuelle en envoyant le message d' [**obtention de \_ \_ \_ palette ICM**](icm-draw-get-palette.md) .

Certains convertisseurs doivent être spécifiquement demandés pour afficher les frames qui leur sont passés. L’envoi du message [**\_ \_ RENDERBUFFER de dessin ICM**](icm-draw-renderbuffer.md) (ou l’utilisation de la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) ) entraîne la création du frame par ces convertisseurs.

 

 





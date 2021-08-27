---
description: l’interface GDI (graphics device interface) de Microsoft Windows permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois dans l’affichage vidéo et l’imprimante.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bbdd515379c5c3d1f2c17ff0b991141b3a40a8cb42594be95e391da6dabb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092539"
---
# <a name="windows-gdi"></a>Windows GDI

## <a name="purpose"></a>Objectif

l’interface GDI (graphics device interface) de Microsoft Windows permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois dans l’affichage vidéo et l’imprimante. les applications basées sur des Windows n’accèdent pas directement au matériel graphique. Au lieu de cela, GDI interagit avec les pilotes de périphérique pour le compte des applications.

## <a name="where-applicable"></a>Le cas échéant

GDI peut être utilisé dans toutes les applications basées sur Windows.

## <a name="developer-audience"></a>Développeurs concernés

Cette API est conçue pour être utilisée par les programmeurs C/C++. vous devez vous familiariser avec la Windows [architecture pilotée](../learnwin32/window-messages.md) par les messages.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.

## <a name="in-this-section"></a>Dans cette section

-   [Images bitmap](bitmaps.md)
-   [Pinceaux](brushes.md)
-   [Découpage](clipping.md)
-   [Couleurs](colors.md)
-   [Espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md)
-   [Contextes de périphérique](device-contexts.md)
-   [Formes remplies](filled-shapes.md)
-   [Polices et texte](fonts-and-text.md)
-   [Lignes et courbes](lines-and-curves.md)
-   [Métafichiers](metafiles.md)
-   [Moniteurs multiples](multiple-display-monitors.md)
-   [Peinture et dessin](painting-and-drawing.md)
-   [Chemins d’accès](paths.md)
-   [Stylets](pens.md)
-   [Spouleur d’impression et d’impression](/previous-versions//dd162860(v=vs.85))
-   [Rectangles](rectangles.md)
-   [Régions](regions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectX](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[GDI+](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[Technologie](../opengl/opengl.md)
</dt> <dt>

[Windows Acquisition d’images](../wia/-wia-startpage.md)
</dt> </dl>

 

 

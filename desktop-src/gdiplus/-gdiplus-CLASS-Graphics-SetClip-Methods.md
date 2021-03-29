---
description: Cette rubrique répertorie les méthodes SetClip de la classe Graphics. Pour obtenir la liste complète des méthodes de la classe Graphics, consultez Graphics.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Graphics. SetClip, méthodes
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 488d617dfb53343fc728fff722c0c0bc1db57335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202463"
---
# <a name="graphicssetclip-methods"></a>Graphics. SetClip, méthodes

Cette rubrique répertorie les méthodes SetClip de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Pour obtenir la liste complète des méthodes de la classe **Graphics** , consultez [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip (HRGN, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | La méthode [**Graphics :: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sur une région qui est la combinaison de lui-même et d’une région GDI.<br/>                                                                                                                                                                                                          |
| [**SetClip (Rect&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | La méthode [**Graphics :: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) en une région qui est la combinaison de lui-même et d’un rectangle.<br/>                                                                                                                                                                                          |
| [**SetClip (RectF&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | La méthode [**Graphics :: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) en une région qui est la combinaison de lui-même et d’un rectangle.<br/>                                                                                                                                                                                         |
| [**SetClip (Region \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | La méthode [**Graphics :: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) en une région qui est la combinaison de lui-même et de la région spécifiée par un objet [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) .<br/>                                                                                                                                      |
| [**SetClip (Graphics \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | La méthode [**Graphics :: SetClip**](/previous-versions//ms535823(v=vs.85)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) en une région qui est la combinaison de elle-même et de la zone de découpage d’un autre objet **Graphics** .<br/>                                                                                                                                                                       |
| [**SetClip (GraphicsPath \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | La méthode [**Graphics :: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) met à jour la zone de découpage de cet objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sur une région qui est la combinaison de lui-même et de la région spécifiée par un tracé graphique. Si une figure dans le chemin d’accès n’est pas fermée, cette méthode traite la figure non fermée comme si elle était fermée par une ligne droite qui relie les points de départ et de fin de la figure.<br/> |



 

 

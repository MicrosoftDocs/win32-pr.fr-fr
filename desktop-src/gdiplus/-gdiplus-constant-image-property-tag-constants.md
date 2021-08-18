---
description: Plusieurs formats de fichier image vous permettent de stocker des métadonnées avec une image.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de balise de propriété d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509caf20659628909d225bb2dc34a4dbaa27047c08e361b28e9777141f213751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696417"
---
# <a name="image-property-tag-constants"></a>Constantes de balise de propriété d’image

Plusieurs formats de fichier image vous permettent de stocker des métadonnées avec une image. Les métadonnées sont des informations sur une image, par exemple le titre, la largeur, le modèle d’appareil photo et l’artiste. Windows GDI+ fournit un moyen uniforme de stocker et de récupérer des métadonnées à partir de fichiers image au format TIFF (tagged image file Format), JPEG, PNG (Portable Network graphics) et EXIF (exchangeable image file).

dans GDI+, un élément de métadonnées est appelé un *élément de propriété*, et un élément de propriété individuel est identifié par une constante numérique appelée *balise de propriété*. Vous pouvez stocker et récupérer des métadonnées en appelant les méthodes [**image :: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) et [**image :: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , et vous n’avez pas à vous soucier des détails de la façon dont un format de fichier particulier stocke ces métadonnées.

Les rubriques suivantes répertorient et décrivent les éléments de propriété pris en charge par GDI+. Les descriptions sont brèves et générales afin qu’elles s’appliquent à un large éventail de formats de fichiers. Pour obtenir une description détaillée de la façon dont un élément de propriété est utilisé dans un format de fichier particulier, consultez la spécification de ce format de fichier. Pour obtenir des liens vers plusieurs spécifications de format de fichier, consultez [spécifications de format de fichier image](-gdiplus-constant-image-file-format-specifications.md). Pour plus d’informations sur les métadonnées, consultez [lecture et écriture de métadonnées](-gdiplus-reading-and-writing-metadata-use.md) et [**constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Balises de propriété dans l’ordre numérique](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Balises de propriété par ordre alphabétique](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descriptions des éléments de propriété](-gdiplus-constant-property-item-descriptions.md)

 

 




---
description: Plusieurs formats de fichier image vous permettent de stocker des métadonnées avec une image.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de balise de propriété d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972915"
---
# <a name="image-property-tag-constants"></a>Constantes de balise de propriété d’image

Plusieurs formats de fichier image vous permettent de stocker des métadonnées avec une image. Les métadonnées sont des informations sur une image, par exemple le titre, la largeur, le modèle d’appareil photo et l’artiste. Windows GDI+ offre un moyen uniforme de stocker et de récupérer des métadonnées à partir de fichiers image au format TIFF (Tagged Image File Format), JPEG, PNG (Portable Network Graphics) et EXIF (Exchangeable Image File).

Dans GDI+, un élément de métadonnées est appelé *élément de propriété*, et un élément de propriété individuel est identifié par une constante numérique appelée *balise de propriété*. Vous pouvez stocker et récupérer des métadonnées en appelant les méthodes [**image :: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) et [**image :: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , et vous n’avez pas à vous soucier des détails de la façon dont un format de fichier particulier stocke ces métadonnées.

Les rubriques suivantes répertorient et décrivent les éléments de propriété pris en charge par GDI+. Les descriptions sont brèves et générales afin qu’elles s’appliquent à un large éventail de formats de fichiers. Pour obtenir une description détaillée de la façon dont un élément de propriété est utilisé dans un format de fichier particulier, consultez la spécification de ce format de fichier. Pour obtenir des liens vers plusieurs spécifications de format de fichier, consultez [spécifications de format de fichier image](-gdiplus-constant-image-file-format-specifications.md). Pour plus d’informations sur les métadonnées, consultez [lecture et écriture de métadonnées](-gdiplus-reading-and-writing-metadata-use.md) et [**constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Balises de propriété dans l’ordre numérique](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Balises de propriété par ordre alphabétique](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descriptions des éléments de propriété](-gdiplus-constant-property-item-descriptions.md)

 

 




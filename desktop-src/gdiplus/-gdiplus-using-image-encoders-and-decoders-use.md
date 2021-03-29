---
description: Windows GDI+ fournit la classe image et la classe Bitmap pour le stockage des images en mémoire et la manipulation d’images en mémoire.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Utilisation d’encodeurs et de décodeurs d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112935"
---
# <a name="using-image-encoders-and-decoders"></a>Utilisation d’encodeurs et de décodeurs d’images

Windows GDI+ fournit la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et la classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) pour le stockage des images en mémoire et la manipulation d’images en mémoire. GDI+ écrit des images dans des fichiers sur disque à l’aide d’encodeurs d’images et charge des images à partir de fichiers disque à l’aide de décodeurs d’image. Un encodeur convertit les données d’un objet **image** ou **bitmap** en un format de fichier de disque désigné. Un décodeur convertit les données d’un fichier de disque au format requis par les objets **image** et **bitmap** . GDI+ contient des encodeurs et des décodeurs intégrés qui prennent en charge les types de fichiers suivants :

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ possède également des décodeurs intégrés qui prennent en charge les types de fichiers suivants :

-   WMF
-   EMF
-   ICON

Les rubriques suivantes décrivent plus en détail les encodeurs et les décodeurs :

-   [Liste des encodeurs installés](-gdiplus-listing-installed-encoders-use.md)
-   [Liste des décodeurs installés](-gdiplus-listing-installed-decoders-use.md)
-   [Récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Détermination des paramètres pris en charge par un encodeur](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Conversion d’une image BMP en image PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Définition du niveau de compression JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformation d’une image JPEG sans perte d’informations](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Création et enregistrement d’une image multiframe](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copie de frames individuels à partir d’une image Multiple-Frame](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 




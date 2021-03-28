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
# <a name="image-property-tag-constants"></a><span data-ttu-id="5b530-103">Constantes de balise de propriété d’image</span><span class="sxs-lookup"><span data-stu-id="5b530-103">Image Property Tag Constants</span></span>

<span data-ttu-id="5b530-104">Plusieurs formats de fichier image vous permettent de stocker des métadonnées avec une image.</span><span class="sxs-lookup"><span data-stu-id="5b530-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="5b530-105">Les métadonnées sont des informations sur une image, par exemple le titre, la largeur, le modèle d’appareil photo et l’artiste.</span><span class="sxs-lookup"><span data-stu-id="5b530-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="5b530-106">Windows GDI+ offre un moyen uniforme de stocker et de récupérer des métadonnées à partir de fichiers image au format TIFF (Tagged Image File Format), JPEG, PNG (Portable Network Graphics) et EXIF (Exchangeable Image File).</span><span class="sxs-lookup"><span data-stu-id="5b530-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="5b530-107">Dans GDI+, un élément de métadonnées est appelé *élément de propriété*, et un élément de propriété individuel est identifié par une constante numérique appelée *balise de propriété*.</span><span class="sxs-lookup"><span data-stu-id="5b530-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="5b530-108">Vous pouvez stocker et récupérer des métadonnées en appelant les méthodes [**image :: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) et [**image :: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , et vous n’avez pas à vous soucier des détails de la façon dont un format de fichier particulier stocke ces métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5b530-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="5b530-109">Les rubriques suivantes répertorient et décrivent les éléments de propriété pris en charge par GDI+.</span><span class="sxs-lookup"><span data-stu-id="5b530-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="5b530-110">Les descriptions sont brèves et générales afin qu’elles s’appliquent à un large éventail de formats de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5b530-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="5b530-111">Pour obtenir une description détaillée de la façon dont un élément de propriété est utilisé dans un format de fichier particulier, consultez la spécification de ce format de fichier.</span><span class="sxs-lookup"><span data-stu-id="5b530-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="5b530-112">Pour obtenir des liens vers plusieurs spécifications de format de fichier, consultez [spécifications de format de fichier image](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="5b530-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="5b530-113">Pour plus d’informations sur les métadonnées, consultez [lecture et écriture de métadonnées](-gdiplus-reading-and-writing-metadata-use.md) et [**constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5b530-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="5b530-114">Balises de propriété dans l’ordre numérique</span><span class="sxs-lookup"><span data-stu-id="5b530-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="5b530-115">Balises de propriété par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="5b530-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="5b530-116">Descriptions des éléments de propriété</span><span class="sxs-lookup"><span data-stu-id="5b530-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 




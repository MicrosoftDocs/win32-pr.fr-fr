---
description: Autres objets sources
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Autres objets sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747052"
---
# <a name="other-source-objects"></a><span data-ttu-id="d5793-103">Autres objets sources</span><span class="sxs-lookup"><span data-stu-id="d5793-103">Other Source Objects</span></span>

<span data-ttu-id="d5793-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="d5793-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d5793-105">En plus des sources audio et vidéo, les [services de modification DirectShow](directshow-editing-services.md) (des) prennent en charge les objets sources suivants.</span><span class="sxs-lookup"><span data-stu-id="d5793-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="d5793-106">**Images fixes**</span><span class="sxs-lookup"><span data-stu-id="d5793-106">**Still Images**</span></span>

<span data-ttu-id="d5793-107">DES prend en charge les formats de fichier suivants pour les images fixes :</span><span class="sxs-lookup"><span data-stu-id="d5793-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="d5793-108">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="d5793-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="d5793-109">GIF (format d’échange Graphics)</span><span class="sxs-lookup"><span data-stu-id="d5793-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="d5793-110">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="d5793-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="d5793-111">Carte graphique Targa ou Truevision (. TGA) : mode 2 (RGB non compressé) en format 16 bits, 24,-bit ou 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d5793-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="d5793-112">Ces fichiers peuvent être utilisés comme images fixes ou pour créer des animations.</span><span class="sxs-lookup"><span data-stu-id="d5793-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="d5793-113">Pour les fichiers bitmap, JPEG et Targa, si vous utilisez le fichier comme image continue, appelez la méthode [**IAMTimelineSrc :: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) pour définir la fréquence d’images sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d5793-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="d5793-114">**Séquences DIB**</span><span class="sxs-lookup"><span data-stu-id="d5793-114">**DIB Sequences**</span></span>

<span data-ttu-id="d5793-115">Étant donné une série de fichiers bitmap, JPEG ou Targa, le moteur de rendu peut construire une séquence DIB.</span><span class="sxs-lookup"><span data-stu-id="d5793-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="d5793-116">Pour créer une séquence DIB, donnez des noms séquentiels aux fichiers, par exemple Image001.bmp, Image002.bmp, Image003.bmp, etc.</span><span class="sxs-lookup"><span data-stu-id="d5793-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="d5793-117">Utilisez le premier fichier de la séquence comme source.</span><span class="sxs-lookup"><span data-stu-id="d5793-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="d5793-118">Définissez la fréquence d’images de la séquence en appelant [**IAMTimelineSrc :: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span><span class="sxs-lookup"><span data-stu-id="d5793-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="d5793-119">Le moteur de rendu parcourt les images de la séquence à la fréquence d’images spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d5793-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="d5793-120">Si la séquence est trop petite pour remplir la durée, en fonction de la fréquence d’images, le reste de la durée est un noir fixe.</span><span class="sxs-lookup"><span data-stu-id="d5793-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="d5793-121">Aucune erreur ne se produit pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="d5793-121">No error occurs during rendering.</span></span>

<span data-ttu-id="d5793-122">**Sources GIF**</span><span class="sxs-lookup"><span data-stu-id="d5793-122">**GIF Sources**</span></span>

<span data-ttu-id="d5793-123">DES prend en charge les sources GIF, y compris les gif animés et transparents, à l’aide de la spécification GIF89a.</span><span class="sxs-lookup"><span data-stu-id="d5793-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="d5793-124">Avec une image GIF animée, contrairement aux autres types de fichiers, vous n’avez pas besoin de définir la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="d5793-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="d5793-125">Le fichier GIF spécifie le délai entre chaque image de l’animation.</span><span class="sxs-lookup"><span data-stu-id="d5793-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="d5793-126">Pour prendre en charge les images GIF transparentes, DES convertit des zones transparentes dans l’image en RVB triple RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d5793-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="d5793-127">Vous pouvez ensuite utiliser la [transition de clé](key-transition.md) vers la touche sur RVB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d5793-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="d5793-128">DES convertit également les régions noires qui se trouvent dans la plage RVB (de 0 à 7, de 0 à 7, de 0 à 7) à la valeur RVB (8, 8, 8), à l’exception de l’index de transparence, si cette plage est comprise dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="d5793-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="d5793-129">Cette conversion n’est pas détectable à l’oeil.</span><span class="sxs-lookup"><span data-stu-id="d5793-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="d5793-130">**Source de couleur vidéo**</span><span class="sxs-lookup"><span data-stu-id="d5793-130">**Video Color Source**</span></span>

<span data-ttu-id="d5793-131">L’objet [source de couleur vidéo](video-color-source.md) crée une image vidéo continue d’une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="d5793-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="d5793-132">Une utilisation pour cet objet consiste à en faire une couche dans une transition.</span><span class="sxs-lookup"><span data-stu-id="d5793-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="d5793-133">Par exemple, utilisez-le dans une vidéo en fondu ou en fondu.</span><span class="sxs-lookup"><span data-stu-id="d5793-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="d5793-134">**Filtres de source personnalisés**</span><span class="sxs-lookup"><span data-stu-id="d5793-134">**Custom Source Filters**</span></span>

<span data-ttu-id="d5793-135">DES peut utiliser un filtre source DirectShow comme source de chronologie, si le filtre remplit les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5793-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="d5793-136">Il prend en charge la recherche</span><span class="sxs-lookup"><span data-stu-id="d5793-136">It supports seeking</span></span>
-   <span data-ttu-id="d5793-137">Il produit un format pris en charge par.</span><span class="sxs-lookup"><span data-stu-id="d5793-137">It produces a format that DES supports.</span></span> <span data-ttu-id="d5793-138">Le format peut être compressé tant que le système de l’utilisateur dispose d’un filtre DirectShow capable de le décoder.</span><span class="sxs-lookup"><span data-stu-id="d5793-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="d5793-139">Pour utiliser une source personnalisée, spécifiez le CLSID du filtre en tant que GUID de sous-objet de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="d5793-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="d5793-140">Pour plus d’informations, consultez sous- [objets](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="d5793-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="d5793-141">Pour prendre en charge les propriétés personnalisées, implémentez-les en tant que propriétés « put » **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="d5793-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="d5793-142">Seules les propriétés statiques sont prises en charge sur les objets sources ; les propriétés dynamiques ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d5793-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5793-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5793-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5793-144">Utilisation des sources</span><span class="sxs-lookup"><span data-stu-id="d5793-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 




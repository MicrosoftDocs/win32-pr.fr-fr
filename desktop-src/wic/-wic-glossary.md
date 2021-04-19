---
description: Définit les termes utilisés dans WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossaire du composant de création d’images Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522084"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="90d75-103">Glossaire du composant de création d’images Windows</span><span class="sxs-lookup"><span data-stu-id="90d75-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="90d75-104">B</span><span class="sxs-lookup"><span data-stu-id="90d75-104">B</span></span>

<dl> <dt>

<span data-ttu-id="90d75-105">**profondeur de bit**</span><span class="sxs-lookup"><span data-stu-id="90d75-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-106">Nombre de valeurs de couleur qui peuvent être affectées à un seul pixel dans une image.</span><span class="sxs-lookup"><span data-stu-id="90d75-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="90d75-107">La profondeur des couleurs peut être comprise entre 1 bit (noir et blanc) et 32 bits (plus de 16,7 millions couleurs).</span><span class="sxs-lookup"><span data-stu-id="90d75-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="90d75-108">Voir aussi : profondeur de couleur</span><span class="sxs-lookup"><span data-stu-id="90d75-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="90d75-109">**bits par pixel (BPP)**</span><span class="sxs-lookup"><span data-stu-id="90d75-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-110">Nombre de bits représentant la valeur de couleur de chaque pixel dans une image numérisée.</span><span class="sxs-lookup"><span data-stu-id="90d75-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="90d75-111">Voir aussi : BPP</span><span class="sxs-lookup"><span data-stu-id="90d75-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="90d75-112">C</span><span class="sxs-lookup"><span data-stu-id="90d75-112">C</span></span>

<dl> <dt>

<span data-ttu-id="90d75-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="90d75-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-114">Objet IWICBitmapClipper.</span><span class="sxs-lookup"><span data-stu-id="90d75-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-115">**Codec**</span><span class="sxs-lookup"><span data-stu-id="90d75-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-116">Filtre qui compresse (encode) ou décompresse (décode) un flux de données.</span><span class="sxs-lookup"><span data-stu-id="90d75-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-117">**contexte de couleur**</span><span class="sxs-lookup"><span data-stu-id="90d75-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-118">Abstraction d’un profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="90d75-118">An abstraction for a color profile.</span></span> <span data-ttu-id="90d75-119">Le profil peut être chargé à partir d’un fichier (par ex. « sRGB Color Space Profile. ICM ») ou à partir d’une mémoire tampon obtenue en lisant.</span><span class="sxs-lookup"><span data-stu-id="90d75-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="90d75-120">Les informations de contexte de couleur sont définies par l’interface IWICColorContext pour WIC et sont récupérées avec la méthode GetColorContext.</span><span class="sxs-lookup"><span data-stu-id="90d75-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-121">**transformation de couleur**</span><span class="sxs-lookup"><span data-stu-id="90d75-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-122">Mappage des couleurs du contexte de couleur source au contexte de couleur de destination dans un format de pixel de sortie donné.</span><span class="sxs-lookup"><span data-stu-id="90d75-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-123">**Modèle de couleurs CYMK**</span><span class="sxs-lookup"><span data-stu-id="90d75-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-124">Espace colorimétrique multidimensionnel constitué des intensités cyan, magenta, jaune et noir qui composent une couleur donnée.</span><span class="sxs-lookup"><span data-stu-id="90d75-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="90d75-125">D</span><span class="sxs-lookup"><span data-stu-id="90d75-125">D</span></span>

<dl> <dt>

<span data-ttu-id="90d75-126">**décodeur**</span><span class="sxs-lookup"><span data-stu-id="90d75-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-127">Voir le terme : codec</span><span class="sxs-lookup"><span data-stu-id="90d75-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="90d75-128">E</span><span class="sxs-lookup"><span data-stu-id="90d75-128">E</span></span>

<dl> <dt>

<span data-ttu-id="90d75-129">**codeur**</span><span class="sxs-lookup"><span data-stu-id="90d75-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-130">Voir le terme : codec</span><span class="sxs-lookup"><span data-stu-id="90d75-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="90d75-131">L</span><span class="sxs-lookup"><span data-stu-id="90d75-131">L</span></span>

<dl> <dt>

<span data-ttu-id="90d75-132">**perte**</span><span class="sxs-lookup"><span data-stu-id="90d75-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-133">Type de compression qui garantit que les données d’origine peuvent être récupérées exactement, sans perte de qualité d’image.</span><span class="sxs-lookup"><span data-stu-id="90d75-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-134">**pertes**</span><span class="sxs-lookup"><span data-stu-id="90d75-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-135">Processus de compression des données dans laquelle les informations jugées inutiles sont supprimées et ne peuvent pas être récupérées lors de la décompression.</span><span class="sxs-lookup"><span data-stu-id="90d75-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="90d75-136">Généralement utilisé avec les données audio et visuelles dans lesquelles une légère dégradation de la qualité est acceptable.</span><span class="sxs-lookup"><span data-stu-id="90d75-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="90d75-137">M</span><span class="sxs-lookup"><span data-stu-id="90d75-137">M</span></span>

<dl> <dt>

<span data-ttu-id="90d75-138">**cloisonnement multithread (MTA)**</span><span class="sxs-lookup"><span data-stu-id="90d75-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-139">Forme de multithread prise en charge par le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="90d75-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="90d75-140">Dans un modèle à cloisonnement multithread, tous les threads du processus qui ont été initialisés en tant que threads libres résident dans un seul cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="90d75-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="90d75-141">N</span><span class="sxs-lookup"><span data-stu-id="90d75-141">N</span></span>

<dl> <dt>

<span data-ttu-id="90d75-142">**format de pixel natif**</span><span class="sxs-lookup"><span data-stu-id="90d75-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-143">L’un des formats de pixel fournis par WIC, où la disposition de la mémoire de chaque pixel dans une image bitmap est décrite.</span><span class="sxs-lookup"><span data-stu-id="90d75-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="90d75-144">P</span><span class="sxs-lookup"><span data-stu-id="90d75-144">P</span></span>

<dl> <dt>

<span data-ttu-id="90d75-145">**palette**</span><span class="sxs-lookup"><span data-stu-id="90d75-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-146">Ensemble de couleurs utilisé par un objet ou une application.</span><span class="sxs-lookup"><span data-stu-id="90d75-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-147">**stratégie de métadonnées de photos**</span><span class="sxs-lookup"><span data-stu-id="90d75-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-148">Stratégie Windows pour la lecture, l’écriture et la suppression des métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="90d75-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-149">**format de pixel**</span><span class="sxs-lookup"><span data-stu-id="90d75-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-150">Taille et disposition des composants de couleur de pixel en mémoire.</span><span class="sxs-lookup"><span data-stu-id="90d75-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="90d75-151">Elle est spécifiée par le nombre total de bits utilisés par pixel et par le nombre de bits utilisés pour stocker les composants rouge, vert, bleu et alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="90d75-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="90d75-152">Par exemple, le format de pixel RGB24 utilise 24 bits pour stocker une couleur de pixel, avec huit bits chacun pour le rouge, le vert et le bleu.</span><span class="sxs-lookup"><span data-stu-id="90d75-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="90d75-153">Le format de pixel ARGB32 utilise 32 bits, avec 24 bits d’informations de couleur et 8 bits d’informations de canal alpha.</span><span class="sxs-lookup"><span data-stu-id="90d75-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="90d75-154">**décodage progressif**</span><span class="sxs-lookup"><span data-stu-id="90d75-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-155">Processus de décodage d’images qui ont été encodées avec des informations sur les différents niveaux de décodage.</span><span class="sxs-lookup"><span data-stu-id="90d75-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="90d75-156">S</span><span class="sxs-lookup"><span data-stu-id="90d75-156">S</span></span>

<dl> <dt>

<span data-ttu-id="90d75-157">**train**</span><span class="sxs-lookup"><span data-stu-id="90d75-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-158">Fait référence à une interface COM IStream qui peut être utilisée pour lire ou écrire des données séquentiellement dans des fichiers, de la mémoire ou des emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="90d75-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="90d75-159">T</span><span class="sxs-lookup"><span data-stu-id="90d75-159">T</span></span>

<dl> <dt>

<span data-ttu-id="90d75-160">**courbe tonale**</span><span class="sxs-lookup"><span data-stu-id="90d75-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-161">Graphique utilisé dans la photographie numérique qui affiche la plage tonale de l’image.</span><span class="sxs-lookup"><span data-stu-id="90d75-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="90d75-162">W</span><span class="sxs-lookup"><span data-stu-id="90d75-162">W</span></span>

<dl> <dt>

<span data-ttu-id="90d75-163">**Composant Imagerie Windows (WIC)**</span><span class="sxs-lookup"><span data-stu-id="90d75-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="90d75-164">Plateforme extensible qui fournit une API de bas niveau pour les images numériques.</span><span class="sxs-lookup"><span data-stu-id="90d75-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 




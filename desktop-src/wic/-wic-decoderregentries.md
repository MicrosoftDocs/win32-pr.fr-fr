---
description: Decoder-Specific les entrées de Registre
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific les entrées de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535677"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="5bce8-103">Decoder-Specific les entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="5bce8-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="5bce8-104">Outre les entrées de Registre requises pour tous les encodeurs et décodeurs, les entrées de Registre suivantes sont requises spécifiquement pour les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="5bce8-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="5bce8-105">Ces entrées inscrivent votre décodeur sous la catégorie des décodeurs WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="5bce8-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="5bce8-106">Le premier GUID dans ces entrées est l’identificateur de catégorie (CATID) pour [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="5bce8-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="5bce8-107">Comme indiqué dans la section [découverte et arbitrage](-wic-howwicworks.md) du fonctionnement du composant Windows Imaging, le mécanisme qui permet à un décodeur approprié pour une image spécifique d’être découvert au moment de l’exécution est basé sur la mise en correspondance d’un modèle d’identification incorporé dans le fichier image avec un modèle spécifié dans l’entrée de Registre du décodeur.</span><span class="sxs-lookup"><span data-stu-id="5bce8-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="5bce8-108">Pour activer la découverte des décodeurs au moment de l’exécution, vous devez inscrire le modèle d’identification unique pour votre format d’image comme suit.</span><span class="sxs-lookup"><span data-stu-id="5bce8-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="5bce8-109">Toutes ces entrées de Registre sont requises, à l’exception de l’entrée **EndOfStream** , qui est facultative, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5bce8-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="5bce8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bce8-110">Value</span></span>       | <span data-ttu-id="5bce8-111">Description</span><span class="sxs-lookup"><span data-stu-id="5bce8-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bce8-112">Position</span><span class="sxs-lookup"><span data-stu-id="5bce8-112">Position</span></span>    | <span data-ttu-id="5bce8-113">Offset dans le fichier où se trouve le modèle.</span><span class="sxs-lookup"><span data-stu-id="5bce8-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5bce8-114">Longueur</span><span class="sxs-lookup"><span data-stu-id="5bce8-114">Length</span></span>      | <span data-ttu-id="5bce8-115">Longueur du modèle.</span><span class="sxs-lookup"><span data-stu-id="5bce8-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5bce8-116">Modèle</span><span class="sxs-lookup"><span data-stu-id="5bce8-116">Pattern</span></span>     | <span data-ttu-id="5bce8-117">Bits réels qui composent le modèle.</span><span class="sxs-lookup"><span data-stu-id="5bce8-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="5bce8-118">Il s’agit des bits qui sont mis en correspondance avec le modèle d’identification dans un fichier image pendant la découverte.</span><span class="sxs-lookup"><span data-stu-id="5bce8-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="5bce8-119">Mask</span><span class="sxs-lookup"><span data-stu-id="5bce8-119">Mask</span></span>        | <span data-ttu-id="5bce8-120">Autorise les valeurs de caractères génériques dans les modèles.</span><span class="sxs-lookup"><span data-stu-id="5bce8-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="5bce8-121">Le masque est appliqué en effectuant une opération AND logique sur le modèle et le masque.</span><span class="sxs-lookup"><span data-stu-id="5bce8-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="5bce8-122">Tout bit du modèle qui correspond à un bit dans le masque avec une valeur de 0 est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5bce8-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="5bce8-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="5bce8-123">EndOfStream</span></span> | <span data-ttu-id="5bce8-124">Le décalage du modèle d’identification doit être calculé à partir de la fin du flux, et non au début.</span><span class="sxs-lookup"><span data-stu-id="5bce8-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="5bce8-125">Certains formats d’image placent le modèle d’identification à la fin ou près de la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="5bce8-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="5bce8-126">Étant donné que la valeur par défaut consiste à effectuer une recherche à partir du début, à moins que votre modèle ne soit près de la fin du fichier, vous pouvez omettre cette entrée.</span><span class="sxs-lookup"><span data-stu-id="5bce8-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="5bce8-127">Un codec peut prendre en charge plusieurs modèles d’identification.</span><span class="sxs-lookup"><span data-stu-id="5bce8-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="5bce8-128">Dans ce cas, vous devez répéter toutes les clés sous les **\_ classes HKEY \_ \\ CLSID racine CLSID \\ {Decoder CLSID} \\** et utiliser la clé numérique (0 dans l’exemple) pour faire la distinction entre les différents modèles.</span><span class="sxs-lookup"><span data-stu-id="5bce8-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="5bce8-129">Vous devez inclure chacune des quatre valeurs sous la clé pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="5bce8-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="5bce8-130">Inscription d’un format de conteneur avec des lecteurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="5bce8-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="5bce8-131">Si vous créez un nouveau format de conteneur pour votre codec, vous devez également créer des entrées de Registre pour prendre en charge la découverte des lecteurs de métadonnées pour les blocs de métadonnées dans vos images, tout comme vous l’avez fait pour les enregistreurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5bce8-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="5bce8-132">Les entrées suivantes doivent être créées sous l’identificateur de classe (CLSID) du lecteur de métadonnées pour chaque format de métadonnées que votre format de conteneur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5bce8-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="5bce8-133">(Notez que, si votre codec utilise un conteneur TIFF (Tagged Image File Format), ces informations se trouvent déjà dans le registre.)</span><span class="sxs-lookup"><span data-stu-id="5bce8-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="5bce8-134">Étant donné que les entrées pour les lecteurs de métadonnées sont également utilisées pour la découverte, elles sont très similaires aux entrées pour les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="5bce8-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="5bce8-135">Ces entrées sont utilisées par la fabrique de composants pour rechercher les lecteurs de métadonnées pris en charge par votre conteneur et pour sélectionner l’application appropriée, lorsque votre implémentation de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) demande un lecteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5bce8-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="5bce8-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bce8-136">Value</span></span>      | <span data-ttu-id="5bce8-137">Description</span><span class="sxs-lookup"><span data-stu-id="5bce8-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bce8-138">Position</span><span class="sxs-lookup"><span data-stu-id="5bce8-138">Position</span></span>   | <span data-ttu-id="5bce8-139">Offset dans le conteneur du bloc de métadonnées dans lequel l’en-tête de métadonnées est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5bce8-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="5bce8-140">Pour les blocs de métadonnées de niveau supérieur, il s’agit du décalage dans le flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="5bce8-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="5bce8-141">Pour les blocs de métadonnées imbriqués dans d’autres blocs de métadonnées, il s’agit du décalage par rapport au bloc de métadonnées conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bce8-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="5bce8-142">Modèle</span><span class="sxs-lookup"><span data-stu-id="5bce8-142">Pattern</span></span>    | <span data-ttu-id="5bce8-143">Bits réels qui composent le modèle.</span><span class="sxs-lookup"><span data-stu-id="5bce8-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="5bce8-144">Il s’agit des bits qui sont mis en correspondance avec le modèle d’identification dans un fichier image pendant la découverte.</span><span class="sxs-lookup"><span data-stu-id="5bce8-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="5bce8-145">Mask</span><span class="sxs-lookup"><span data-stu-id="5bce8-145">Mask</span></span>       | <span data-ttu-id="5bce8-146">L’en-tête de métadonnées est généralement défini par le gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5bce8-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="5bce8-147">Vous devez utiliser l’en-tête de métadonnées standard pour chaque lecteur, sauf si, pour une raison quelconque, le modèle doit avoir un format différent dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bce8-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="5bce8-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="5bce8-148">DataOffset</span></span> | <span data-ttu-id="5bce8-149">Offset à partir du début de l’en-tête de métadonnées au niveau duquel les données réelles commencent.</span><span class="sxs-lookup"><span data-stu-id="5bce8-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="5bce8-150">Dans les cas où les métadonnées ne sont pas situées à un décalage spécifique par rapport à l’en-tête, cette entrée peut être omise.</span><span class="sxs-lookup"><span data-stu-id="5bce8-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5bce8-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5bce8-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5bce8-152">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5bce8-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5bce8-153">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="5bce8-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="5bce8-154">Intégration à la Galerie de photos Windows et à l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="5bce8-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="5bce8-155">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5bce8-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5bce8-156">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="5bce8-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




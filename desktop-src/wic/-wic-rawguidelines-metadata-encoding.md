---
description: Encodage
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Encodage (composant Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536794"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="efa8d-103">Encodage (composant Windows Imaging)</span><span class="sxs-lookup"><span data-stu-id="efa8d-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="efa8d-104">L’auteur de l’encodeur doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="efa8d-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="efa8d-105">Implémentez des interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="efa8d-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="efa8d-106">Implémentez [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur l’encodeur de trame.</span><span class="sxs-lookup"><span data-stu-id="efa8d-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="efa8d-107">Si le codec prend en charge les métadonnées au niveau du conteneur, cette interface doit être implémentée sur l’encodeur au niveau du conteneur, ainsi que sur l’encodeur de trame.</span><span class="sxs-lookup"><span data-stu-id="efa8d-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="efa8d-108">Si le format de conteneur contient implicitement des blocs de métadonnées obligatoires, instanciez un générateur de métadonnées pour chaque bloc de ce type.</span><span class="sxs-lookup"><span data-stu-id="efa8d-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="efa8d-109">Par exemple, le format TIFF requiert un appareil d’interface (IFD) pour chaque trame, de sorte que l’enregistreur IFD doit toujours être exposé.</span><span class="sxs-lookup"><span data-stu-id="efa8d-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="efa8d-110">Implémentez la prise en charge de la gestion de la collection des enregistreurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="efa8d-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="efa8d-111">Le writer de bloc gère les exigences de commande ou les restrictions de conteneur sur les types de blocs de métadonnées qui peuvent être encodés.</span><span class="sxs-lookup"><span data-stu-id="efa8d-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="efa8d-112">Le writer de bloc doit vérifier que tous les nouveaux enregistreurs de métadonnées peuvent être incorporés dans le format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="efa8d-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="efa8d-113">Lors de l’encodage du flux d’image, appelez [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) pour sérialiser le contenu de chaque générateur de métadonnées dans le flux.</span><span class="sxs-lookup"><span data-stu-id="efa8d-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="efa8d-114">Si le bloc de métadonnées contient des métadonnées « critiques », l’encodeur doit définir les éléments de métadonnées critiques avant de demander au writer de métadonnées de sérialiser le contenu.</span><span class="sxs-lookup"><span data-stu-id="efa8d-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="efa8d-115">Vérifiez la présence de gestionnaires de métadonnées inconnus pour vous assurer que les blocs de métadonnées redondants ne sont pas présents.</span><span class="sxs-lookup"><span data-stu-id="efa8d-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="efa8d-116">Cela est important car, tout en préservant les métadonnées dans un scénario de décodage ou de codage, les blocs inconnus peuvent être un doublon de blocs de métadonnées obligatoires.</span><span class="sxs-lookup"><span data-stu-id="efa8d-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa8d-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="efa8d-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="efa8d-118">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="efa8d-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="efa8d-119">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="efa8d-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="efa8d-120">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="efa8d-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="efa8d-121">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="efa8d-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




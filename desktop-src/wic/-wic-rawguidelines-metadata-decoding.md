---
description: Décodage
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Décodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867318"
---
# <a name="decoding"></a><span data-ttu-id="db887-103">Décodage</span><span class="sxs-lookup"><span data-stu-id="db887-103">Decoding</span></span>

<span data-ttu-id="db887-104">Pour prendre en charge correctement les métadonnées, les auteurs des décodeurs doivent effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="db887-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="db887-105">Implémentez des interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="db887-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="db887-106">Implémentez [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sur le décodeur de trame.</span><span class="sxs-lookup"><span data-stu-id="db887-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="db887-107">Si le codec prend en charge les métadonnées au niveau du conteneur, cette interface doit être implémentée sur le décodeur au niveau du conteneur, ainsi que sur le décodeur de trame.</span><span class="sxs-lookup"><span data-stu-id="db887-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="db887-108">Lors du décodage du flux d’image, appelez [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) pour instancier un lecteur de métadonnées pour chaque bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="db887-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="db887-109">(Tous les nouveaux lecteurs de métadonnées implémentés par le codec doivent être inscrits auprès de WIC.)</span><span class="sxs-lookup"><span data-stu-id="db887-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="db887-110">Le décodeur ne doit pas créer ses propres lecteurs de métadonnées, mais plutôt utiliser le WIC pour les créer en fonction des blocs de métadonnées dans le flux.</span><span class="sxs-lookup"><span data-stu-id="db887-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="db887-111">Le décodeur doit le faire sur tous les blocs qu’il trouve, même s’ils ne sont pas connus de façon native du code, car les lecteurs de métadonnées futurs peuvent être installés sur le système et comprendre comment gérer ces blocs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="db887-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="db887-112">S’il n’existe aucun gestionnaire de métadonnées pour un bloc, instanciez le lecteur de métadonnées inconnu à l’aide des options de création de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="db887-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="db887-113">Exposez la collection de lecteurs de métadonnées via l’interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="db887-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db887-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db887-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="db887-115">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="db887-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="db887-116">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="db887-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="db887-117">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="db887-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="db887-118">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="db887-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




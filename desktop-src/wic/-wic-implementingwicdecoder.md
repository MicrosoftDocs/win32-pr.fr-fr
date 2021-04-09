---
description: 'En savoir plus sur : implémentation d’un décodeur WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implémentation d’un décodeur WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866762"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="03e89-103">Implémentation d’un décodeur WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="03e89-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="03e89-104">L’implémentation d’un décodeur WIC (Windows Imaging Component) requiert l’écriture de deux classes.</span><span class="sxs-lookup"><span data-stu-id="03e89-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="03e89-105">Les interfaces sur ces classes correspondent directement aux responsabilités de décodeur décrites dans la section [décodage](-wic-howwicworks.md) du [fonctionnement du composant de création d’images Windows](-wic-howwicworks.md).</span><span class="sxs-lookup"><span data-stu-id="03e89-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="03e89-106">L’une des classes fournit des services au niveau du conteneur et implémente l’interface [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) .</span><span class="sxs-lookup"><span data-stu-id="03e89-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="03e89-107">Si votre format d’image prend en charge les métadonnées au niveau du conteneur, vous devez également implémenter l’interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) sur cette classe.</span><span class="sxs-lookup"><span data-stu-id="03e89-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="03e89-108">Il est recommandé de prendre en charge l’interface [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sur le décodeur et l’encodeur afin de prendre en charge une meilleure expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03e89-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="03e89-109">L’autre classe que vous allez implémenter fournit des services au niveau de la trame et effectue le décodage réel des bits d’image pour chaque frame dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="03e89-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="03e89-110">Cette classe implémente l’interface [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) et l’interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) .</span><span class="sxs-lookup"><span data-stu-id="03e89-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="03e89-111">Si vous écrivez un décodeur pour un format brut, vous implémentez également l’interface [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) sur cette classe.</span><span class="sxs-lookup"><span data-stu-id="03e89-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="03e89-112">Outre les interfaces requises, il est vivement recommandé d’implémenter l’interface [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) sur cette classe pour bénéficier des meilleures performances possibles pour votre format d’image.</span><span class="sxs-lookup"><span data-stu-id="03e89-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="03e89-113">L’un des objets fournis par WIC est le [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="03e89-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="03e89-114">Vous utilisez fréquemment l’interface [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) sur cet objet pour créer différents composants.</span><span class="sxs-lookup"><span data-stu-id="03e89-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="03e89-115">Étant donné qu’il est fréquemment utilisé, vous devez conserver une référence à celui-ci en tant que propriété de membre sur vos classes de décodeur et d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="03e89-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="03e89-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03e89-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03e89-117">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="03e89-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03e89-118">Fonctionnement du composant de création d’images Windows</span><span class="sxs-lookup"><span data-stu-id="03e89-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="03e89-119">Interfaces de décodeur</span><span class="sxs-lookup"><span data-stu-id="03e89-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="03e89-120">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="03e89-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="03e89-121">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="03e89-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="03e89-122">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="03e89-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="03e89-123">Vue d’ensemble de l’encodage</span><span class="sxs-lookup"><span data-stu-id="03e89-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 




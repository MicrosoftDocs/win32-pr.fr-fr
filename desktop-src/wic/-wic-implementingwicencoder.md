---
description: Implémentation d’un encodeur WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implémentation d’un encodeur WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203806"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="97f25-103">Implémentation d’un encodeur WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="97f25-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="97f25-104">Introduction</span><span class="sxs-lookup"><span data-stu-id="97f25-104">Introduction</span></span>

<span data-ttu-id="97f25-105">L’implémentation d’un encodeur WIC (Windows Imaging Component) requiert l’écriture de deux classes, comme c’est également le cas pour l’implémentation d’un décodeur WIC.</span><span class="sxs-lookup"><span data-stu-id="97f25-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="97f25-106">Les interfaces sur ces classes correspondent directement aux responsabilités d’encodeur décrites dans la section [encodage](-wic-howwicworks.md) du fonctionnement du composant de création d’images Windows.</span><span class="sxs-lookup"><span data-stu-id="97f25-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="97f25-107">L’une des classes fournit des services au niveau du conteneur et gère la sérialisation des trames d’image individuelles dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="97f25-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="97f25-108">Cette classe implémente l’interface [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="97f25-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="97f25-109">Si votre format d’image prend en charge les métadonnées au niveau du conteneur, vous devez également implémenter l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur cette classe.</span><span class="sxs-lookup"><span data-stu-id="97f25-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="97f25-110">L’autre classe fournit des services au niveau de la trame et effectue l’encodage réel des bits d’image pour chaque frame dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="97f25-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="97f25-111">Il itère également au sein des blocs de métadonnées pour chaque frame et demande les enregistreurs de métadonnées appropriés pour sérialiser les blocs.</span><span class="sxs-lookup"><span data-stu-id="97f25-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="97f25-112">Cette classe implémente l’interface **IWICBitmapFrameEncode** et l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) .</span><span class="sxs-lookup"><span data-stu-id="97f25-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="97f25-113">Cette classe doit avoir un membre IStream que la classe de niveau conteneur initialise lors de l’instanciation, dans laquelle la méthode **Commit** sérialise les données de frame.</span><span class="sxs-lookup"><span data-stu-id="97f25-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="97f25-114">Dans certains cas, tels que les formats bruts, l’auteur du codec peut ne pas souhaiter que les applications soient en mesure d’encoder ou de recoder au format brut, car l’objectif d’un fichier brut est de contenir les données de capteur exactement telles qu’elles proviennent de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="97f25-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="97f25-115">Dans les cas où l’auteur du codec ne souhaite pas activer l’encodage, il est toujours nécessaire d’implémenter un encodeur rudimentaire uniquement pour permettre l’ajout de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="97f25-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="97f25-116">Dans ce cas, l’encodeur a uniquement besoin de prendre en charge les méthodes nécessaires pour écrire des métadonnées et peut copier les bits d’image non touchés du décodeur.</span><span class="sxs-lookup"><span data-stu-id="97f25-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97f25-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97f25-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="97f25-118">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="97f25-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97f25-119">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="97f25-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="97f25-120">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="97f25-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97f25-121">Implémentation de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="97f25-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="97f25-122">Interfaces d’encodeur</span><span class="sxs-lookup"><span data-stu-id="97f25-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="97f25-123">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="97f25-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="97f25-124">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="97f25-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




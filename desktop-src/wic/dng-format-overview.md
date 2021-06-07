---
description: Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Vue d’ensemble du format DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444930"
---
# <a name="dng-format-overview"></a><span data-ttu-id="27328-103">Vue d’ensemble du format DNG</span><span class="sxs-lookup"><span data-stu-id="27328-103">DNG Format Overview</span></span>

<span data-ttu-id="27328-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="27328-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27328-105">Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="27328-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="27328-106">Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="27328-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="27328-107">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="27328-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="27328-108">Décodage</span><span class="sxs-lookup"><span data-stu-id="27328-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="27328-109">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="27328-109">Codec Identity</span></span>

<span data-ttu-id="27328-110">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="27328-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="27328-111">Composant</span><span class="sxs-lookup"><span data-stu-id="27328-111">Component</span></span>          |  <span data-ttu-id="27328-112">Description</span><span class="sxs-lookup"><span data-stu-id="27328-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="27328-113">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="27328-113">Formal Name(s)</span></span>         | <span data-ttu-id="27328-114">Négatif numérique (DNG)</span><span class="sxs-lookup"><span data-stu-id="27328-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="27328-115">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="27328-115">File Name Extension(s)</span></span> | <span data-ttu-id="27328-116">.dng</span><span class="sxs-lookup"><span data-stu-id="27328-116">.dng</span></span>                                                 |
| <span data-ttu-id="27328-117">Type (s) MIME</span><span class="sxs-lookup"><span data-stu-id="27328-117">MIME type(s)</span></span>           | <span data-ttu-id="27328-118">image/DNG</span><span class="sxs-lookup"><span data-stu-id="27328-118">image/DNG</span></span>                                            |
| <span data-ttu-id="27328-119">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="27328-119">Specification Support</span></span>  | <span data-ttu-id="27328-120">Version de spécification Digital Negative (DNG) 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="27328-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="27328-121">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec DNG natifs.</span><span class="sxs-lookup"><span data-stu-id="27328-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="27328-122">Composant</span><span class="sxs-lookup"><span data-stu-id="27328-122">Component</span></span>        | <span data-ttu-id="27328-123">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="27328-123">Friendly Name</span></span>             | <span data-ttu-id="27328-124">GUID</span><span class="sxs-lookup"><span data-stu-id="27328-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="27328-125">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="27328-125">Container Format</span></span> | <span data-ttu-id="27328-126">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="27328-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="27328-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="27328-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="27328-128">Décodeur</span><span class="sxs-lookup"><span data-stu-id="27328-128">Decoder</span></span>          | <span data-ttu-id="27328-129">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="27328-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="27328-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="27328-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="27328-131">Décodage</span><span class="sxs-lookup"><span data-stu-id="27328-131">Decoding</span></span>

<span data-ttu-id="27328-132">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="27328-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="27328-133">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="27328-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="27328-134">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="27328-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="27328-135">Le décodeur ne prend pas en charge le décodage des données de capteur brutes et ne prend en charge que les fichiers avec une représentation d’image non brute incorporée dans un IFD avec NewSubFileType égal à 1.</span><span class="sxs-lookup"><span data-stu-id="27328-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 




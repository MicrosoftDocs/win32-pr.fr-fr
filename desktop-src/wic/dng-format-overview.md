---
description: Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Vue d’ensemble du format DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319302"
---
# <a name="dng-format-overview"></a><span data-ttu-id="8d7aa-103">Vue d’ensemble du format DNG</span><span class="sxs-lookup"><span data-stu-id="8d7aa-103">DNG Format Overview</span></span>

<span data-ttu-id="8d7aa-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8d7aa-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8d7aa-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8d7aa-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8d7aa-106">Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="8d7aa-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="8d7aa-107">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="8d7aa-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="8d7aa-108">Décodage</span><span class="sxs-lookup"><span data-stu-id="8d7aa-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="8d7aa-109">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="8d7aa-109">Codec Identity</span></span>

<span data-ttu-id="8d7aa-110">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="8d7aa-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8d7aa-111">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="8d7aa-111">Formal Name(s)</span></span>         | <span data-ttu-id="8d7aa-112">Négatif numérique (DNG)</span><span class="sxs-lookup"><span data-stu-id="8d7aa-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="8d7aa-113">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="8d7aa-113">File Name Extension(s)</span></span> | <span data-ttu-id="8d7aa-114">.dng</span><span class="sxs-lookup"><span data-stu-id="8d7aa-114">.dng</span></span>                                                 |
| <span data-ttu-id="8d7aa-115">Type (s) MIME</span><span class="sxs-lookup"><span data-stu-id="8d7aa-115">MIME type(s)</span></span>           | <span data-ttu-id="8d7aa-116">image/DNG</span><span class="sxs-lookup"><span data-stu-id="8d7aa-116">image/DNG</span></span>                                            |
| <span data-ttu-id="8d7aa-117">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="8d7aa-117">Specification Support</span></span>  | <span data-ttu-id="8d7aa-118">Version de spécification Digital Negative (DNG) 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="8d7aa-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="8d7aa-119">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec DNG natifs.</span><span class="sxs-lookup"><span data-stu-id="8d7aa-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="8d7aa-120">Composant</span><span class="sxs-lookup"><span data-stu-id="8d7aa-120">Component</span></span>        | <span data-ttu-id="8d7aa-121">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="8d7aa-121">Friendly Name</span></span>             | <span data-ttu-id="8d7aa-122">GUID</span><span class="sxs-lookup"><span data-stu-id="8d7aa-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="8d7aa-123">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="8d7aa-123">Container Format</span></span> | <span data-ttu-id="8d7aa-124">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="8d7aa-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="8d7aa-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="8d7aa-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="8d7aa-126">Décodeur</span><span class="sxs-lookup"><span data-stu-id="8d7aa-126">Decoder</span></span>          | <span data-ttu-id="8d7aa-127">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="8d7aa-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="8d7aa-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="8d7aa-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="8d7aa-129">Décodage</span><span class="sxs-lookup"><span data-stu-id="8d7aa-129">Decoding</span></span>

<span data-ttu-id="8d7aa-130">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="8d7aa-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8d7aa-131">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="8d7aa-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8d7aa-132">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8d7aa-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="8d7aa-133">Le décodeur ne prend pas en charge le décodage des données de capteur brutes et ne prend en charge que les fichiers avec une représentation d’image non brute incorporée dans un IFD avec NewSubFileType égal à 1.</span><span class="sxs-lookup"><span data-stu-id="8d7aa-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 




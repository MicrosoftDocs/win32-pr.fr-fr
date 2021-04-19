---
description: Cette rubrique fournit des informations sur le codec ICO natif disponible via WIC (Windows Imaging Component).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Vue d’ensemble du format ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524453"
---
# <a name="ico-format-overview"></a><span data-ttu-id="bf234-103">Vue d’ensemble du format ICO</span><span class="sxs-lookup"><span data-stu-id="bf234-103">ICO Format Overview</span></span>

<span data-ttu-id="bf234-104">Cette rubrique fournit des informations sur le codec ICO natif disponible via WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="bf234-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="bf234-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="bf234-105">Codec Identity</span></span>

<span data-ttu-id="bf234-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="bf234-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="bf234-107">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="bf234-107">Formal Name(s)</span></span>         | <span data-ttu-id="bf234-108">Format d’icône (ICO)</span><span class="sxs-lookup"><span data-stu-id="bf234-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="bf234-109">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="bf234-109">File Name Extension(s)</span></span> | <span data-ttu-id="bf234-110">ICO</span><span class="sxs-lookup"><span data-stu-id="bf234-110">ico</span></span>               |
| <span data-ttu-id="bf234-111">type MIME</span><span class="sxs-lookup"><span data-stu-id="bf234-111">MIME type</span></span>              | <span data-ttu-id="bf234-112">image/ico</span><span class="sxs-lookup"><span data-stu-id="bf234-112">image/ico</span></span>         |
| <span data-ttu-id="bf234-113">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="bf234-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="bf234-114">Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec ICO natifs.</span><span class="sxs-lookup"><span data-stu-id="bf234-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="bf234-115">Composant</span><span class="sxs-lookup"><span data-stu-id="bf234-115">Component</span></span>        | <span data-ttu-id="bf234-116">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="bf234-116">Friendly Name</span></span>            | <span data-ttu-id="bf234-117">GUID</span><span class="sxs-lookup"><span data-stu-id="bf234-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="bf234-118">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="bf234-118">Container Format</span></span> | <span data-ttu-id="bf234-119">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="bf234-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="bf234-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="bf234-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="bf234-121">Décodeur</span><span class="sxs-lookup"><span data-stu-id="bf234-121">Decoder</span></span>          | <span data-ttu-id="bf234-122">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="bf234-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="bf234-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="bf234-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="bf234-124">Encodeur</span><span class="sxs-lookup"><span data-stu-id="bf234-124">Encoder</span></span>          | <span data-ttu-id="bf234-125">NON DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="bf234-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="bf234-126">NON DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="bf234-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="bf234-127">Encodage</span><span class="sxs-lookup"><span data-stu-id="bf234-127">Encoding</span></span>

<span data-ttu-id="bf234-128">WIC ne fournit pas d’encodeur d’image ICO natif.</span><span class="sxs-lookup"><span data-stu-id="bf234-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="bf234-129">Décodage</span><span class="sxs-lookup"><span data-stu-id="bf234-129">Decoding</span></span>

<span data-ttu-id="bf234-130">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="bf234-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bf234-131">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="bf234-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="bf234-132">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="bf234-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



